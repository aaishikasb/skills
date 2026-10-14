# Project context

Standalone agent skills for developer relations, education, edge AI, hardware, robotics, and cross-domain project review. Deliverables live in `skills/<name>/SKILL.md`; metadata and references stay inside that skill's folder. There is no application build or runtime dependency manifest.

Use Node.js 22.20+ with npm for the skills CLI. Check local discovery with `npx skills add . --list`. For an installation check, run `npx skills add /absolute/path/to/this/repository --skill <name>` from a disposable project. Publishing and remote discovery are separate from local installation.

Keep each skill independently installable, with MIT frontmatter, a `LICENSE.txt` matching the root license, and relative links to bundled references. Preserve automatic discovery and the user's requested scope; a review does not authorize device actuation, flashing, or publication.

When adding or renaming a skill, update the [README catalog](README.md) and [skills.sh grouping](skills.sh.json). Check metadata, local links, and a realistic request before shipping changes; distinguish source inspection from execution or physical verification.

Keep the repository lean: installable skills and concise usage documentation. Keep experiment outputs, benchmark archives, and evaluation infrastructure out of the repository.
