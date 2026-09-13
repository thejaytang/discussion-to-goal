# Maintenance

Read `README.md`, `PROJECT_STATE.md`, and then the files relevant to the change.

- `SKILL.md` is the canonical runtime instruction. `agents/openai.yaml` is discovery metadata.
- Keep `README.md` and `README.zh-CN.md` aligned, including their language links, installation steps, examples, and capability limits.
- Preserve draft-only behavior, existing authorization, full-scope acceptance, and truthful Goal status reporting.
- Use `references/design-rationale.md` for maintained rationale and `project-support/` for scoped validation evidence.
- Do not include private conversations, personal filesystem paths, credentials, or private project metrics in examples or commits.
- Test behavioral changes with realistic, side-effect-free scenarios. Structural checks do not establish real Goal integration.
- Publishing authority comes from the current user request. Do not infer it from this file.

Before a release, validate skill frontmatter and UI metadata, inspect local documentation and asset links, review both rendered README languages, inspect the exact archive file list, and check the committed files for accidental private data. Confirm the remote commit and visibility before reporting publication.
