# From Physics to AI — how to add an entry

1. Copy a template from this folder into `_physics2ai/`, named `YYYY-MM-DD-slug.md`.
2. Fill in the front matter:
   - `section`: one of `journal`, `notes`, `papers`, `minimal-model`, `internship`, `physics-x-ai`
     (defined in `_data/physics2ai.yml`)
   - `permalink`: `/physics-to-ai/<slug>/`
   - `draft: true` hides the entry from the lists while you are still writing it.
3. Math: use `$$...$$` for both inline and display formulas (kramdown → MathJax).
4. Optional roadmap (e.g. for a project): add to the entry's front matter
   ```yaml
   roadmap:
     - stage: "v0: baseline"
       stage_zh: "v0：基线"
       status: doing        # done | doing | todo
   ```
   It is shown under the entry on the landing pages.

The landing pages (/physics-to-ai/, /zh/physics-to-ai/) and the homepage
"latest entries" list update automatically.
