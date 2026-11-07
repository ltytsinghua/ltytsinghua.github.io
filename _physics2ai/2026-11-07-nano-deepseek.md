---
title: "nano-deepseek: Retracing DeepSeek's Technical Route on Symbolic Integration"
title_zh: "nano-deepseek：在符号积分任务上复现 DeepSeek 的技术路线"
excerpt: "Project overview and roadmap: a small decoder-only model on symbolic integration, adding DeepSeek's techniques version by version, from a LLaMA-style baseline to MoE, MTP, and GRPO."
excerpt_zh: "项目介绍和路线图：在符号积分这个小任务上，从 LLaMA 风格的基线模型出发，按 DeepSeek 技术报告逐版本加入 MLA、MoE、MTP、GRPO 等技术。"
collection: physics2ai
section: minimal-model
permalink: /physics-to-ai/nano-deepseek/
date: 2026-11-07
lang: zh
locale: zh-CN
roadmap:
  - stage: "Data and vocabulary"
    stage_zh: "数据与词表"
    status: done
  - stage: "v0: LLaMA-style baseline (RMSNorm, RoPE, SwiGLU)"
    stage_zh: "v0：LLaMA 风格基线（RMSNorm、RoPE、SwiGLU）"
    status: doing
  - stage: "v1 ≈ DeepSeek-V2: MLA, DeepSeekMoE"
    stage_zh: "v1 ≈ DeepSeek-V2：MLA、DeepSeekMoE"
    status: todo
  - stage: "v2 ≈ DeepSeek-V3: auxiliary-loss-free load balancing, MTP"
    stage_zh: "v2 ≈ DeepSeek-V3：无辅助损失负载均衡、MTP"
    status: todo
  - stage: "v3 ≈ DeepSeek-R1: GRPO, R1-Zero / R1 training, distillation"
    stage_zh: "v3 ≈ DeepSeek-R1：GRPO、R1-Zero / R1 多阶段训练、蒸馏"
    status: todo
  - stage: "v4 ≈ DeepSeek-V4: mHC, Muon, on-policy distillation"
    stage_zh: "v4 ≈ DeepSeek-V4：mHC、Muon、On-Policy Distillation"
    status: todo
tags:
  - minimal-model
  - deepseek
  - llm
---

> 状态：框架搭建中，v0 基线进行中。代码暂未公开。

## 1. 这个项目要做什么

DeepSeek 的技术报告里，每一项技术单独看都不难懂，但它们为什么这样组合、各自带来多少收益，只读论文很难有体感。

所以我想用物理里“最小模型”的思路来学：**找一个能在笔记本上跑通的小任务，把 DeepSeek 从 V2、V3、R1 到 V4 的技术路线完整走一遍。** 从数据、分词、模型、预训练，一直做到强化学习和蒸馏。每个版本按一份技术报告加入新技术，并和上一版做对照实验；每一步配一份中文笔记。

算力只有一台笔记本加一台 CPU 服务器，所以模型规模控制在几千万参数以内。

## 2. 为什么选符号积分

任务是**符号积分**：给出 $$f(x)$$，让模型生成原函数 $$F(x)$$。选它有三个原因：

1. **答案能自动验证。** 对模型给出的 $$F$$ 求导，看是否等于 $$f$$ 就行。这样 R1 那套“可验证奖励的强化学习”在这里能真正做出来，而不只是跑个形式。
2. **规模小。** 数据可以无限生成，词表只有几十个 token，几千万参数的模型就能学会，个人电脑训得动。
3. **有现成结果可以对照。** Lample & Charton 的 *Deep Learning for Symbolic Mathematics*（ICLR 2020）用 seq2seq Transformer 做过同一个任务，数据集也是公开的。

## 3. 版本路线

每个版本对应 DeepSeek 的一份技术报告。版本内的每项技术都能单独开关，用来做消融；所有版本在同一份测试集上评测。

| 版本 | 新加入的技术 | 对应论文 | 状态 |
|---|---|---|---|
| **v0** 基线 | LLaMA 风格 decoder-only Transformer（RMSNorm、RoPE、SwiGLU） | LLaMA | 进行中 |
| **v1** ≈ V2 | MLA 多头潜在注意力、DeepSeekMoE | DeepSeek-V2 | 计划中 |
| **v2** ≈ V3 | 无辅助损失的负载均衡、多 token 预测（MTP） | DeepSeek-V3 | 计划中 |
| **v3** ≈ R1 | GRPO、R1-Zero / R1 多阶段训练、蒸馏 | DeepSeekMath、DeepSeek-R1 | 计划中 |
| **v4** ≈ V4 | mHC、Muon 优化器、On-Policy Distillation | DeepSeek-V4 | 计划中 |

可以预见，小规模下有些技术不会有收益：MLA 主要是为了省推理显存，MoE 的优势也要规模够大才明显。这些对照结果无论好坏我都会如实记录。在什么条件下一项技术没用，本身也是一个结论。

## 4. 目前进度

**已完成：数据与词表。**

- 数据用 Lample & Charton 公开的积分数据集（`prim_fwd`）。
- 表达式写成前缀（波兰）表示，例如 $$\int -\tan x\,dx = \ln\cos x$$ 对应 `mul INT- 1 tan x` → `ln cos x`。每个运算符的参数个数固定，所以不需要括号。
- 词表沿用原文的定义和顺序，再追加 3 个 decoder-only 需要的特殊 token，共 89 个。
- 题目和答案拼成一条序列 `<bos> f <sep> F <eos>`，训练时只对 `<sep>` 之后的部分算 loss。全部样本以 1 字节一个 token 存成二进制文件，训练时用 memmap 按需读取。

**进行中：v0 基线。** 在读 LLaMA 相对原始 Transformer 的改动（RMSNorm、RoPE、SwiGLU），接下来实现模型、训练，并在测试集上评测，作为后面所有版本的对照基准。

## 5. 后续

每完成一个版本，我会在这个栏目写一篇笔记，记录原理、实现中的坑和对照实验结果，并把链接汇总到这里。
