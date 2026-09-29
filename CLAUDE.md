# CLAUDE.md

Guidance for AI agents working on **产品洞察与 PRD / Product Insight & PRD** (`pm-insight-prd`).

## Scope

The single plugin contains 9 skills and 4 workflows for product research and PRD writing:

- PRD drafting and review
- User personas, segments, segmentation, and journey mapping
- Market sizing, competitor analysis, and feedback sentiment analysis

Do not add marketing campaign planning, growth strategy, or full go-to-market planning to this package unless the product scope is changed deliberately.

## Structure and naming

- `.claude-plugin/marketplace.json` lists the single plugin `pm-insight-prd`.
- `pm-insight-prd/.claude-plugin/plugin.json` must use the same plugin name as its directory.
- Skills are in `pm-insight-prd/skills/{skill-name}/SKILL.md`; their frontmatter `name` must match the folder.
- Workflow files are in `pm-insight-prd/commands/{command-name}.md`.
- Command references use the `/pm-insight-prd:{command-name}` namespace.
- `README.md` is the detailed Chinese and English guide; the plugin README is its concise index.

## Content standards

- Prefer user-provided research and data; distinguish evidence, estimates, assumptions, and open questions.
- Ask focused questions when missing context materially changes the PRD or research result.
- Keep PRDs clear, scoped, measurable, and useful to design and engineering partners.
- Preserve the current 8-section PRD template across `create-prd`, `write-prd`, and the README.
- Keep personal author and promotional references out of package documentation. Preserve the legal copyright notice in `LICENSE`.

## Validation

After structural changes, run:

```bash
python3 validate_plugins.py
python3 -m unittest discover -s tests
```

Update manifests, both READMEs, and consistency counts whenever skills or commands change.
