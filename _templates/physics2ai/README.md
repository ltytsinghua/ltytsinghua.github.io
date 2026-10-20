# From Physics to AI — how to add an entry

1. Copy a template from this folder into `_physics2ai/`, named `YYYY-MM-DD-slug.md`.
2. Fill in the front matter:
   - `section`: one of `journal`, `notes`, `papers`, `projects`, `internship`, `physics-x-ai`
     (defined in `_data/physics2ai.yml`)
   - `permalink`: `/physics-to-ai/<slug>/`
   - `draft: true` hides the entry from the lists while you are still writing it.
3. Math: use `$$...$$` for both inline and display formulas (kramdown → MathJax).
4. Update roadmap progress in `_data/physics2ai.yml` (`status: done | doing | todo`).

The landing pages (/physics-to-ai/, /zh/physics-to-ai/) and the homepage
"latest entries" list update automatically.
