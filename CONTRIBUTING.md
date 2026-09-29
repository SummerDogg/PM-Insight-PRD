# Contributing

Contributions to Product Insight & PRD should improve product research or requirements-writing support while keeping the package focused on those tasks.

## Guidelines

- Keep changes focused and describe the user problem they solve.
- Skills live in `pm-insight-prd/skills/{skill-name}/SKILL.md` and require `name` and `description` frontmatter. The skill name must match its directory.
- Workflow command files live in `pm-insight-prd/commands/{command-name}.md` and require `description` and `argument-hint` frontmatter.
- Update both READMEs and the marketplace manifest when adding, removing, or renaming skills or commands.
- Preserve the MIT license and its copyright notice.
- Before submitting a change, run `python3 validate_plugins.py` and `python3 -m unittest discover -s tests`.
