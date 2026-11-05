# Agent Instructions
This repository owns organization-neutral materials for refactoring bylaws with agents: the `map-bylaws-changes` skill, its design references and genericized examples. Work on a real organization's bylaws belongs in that organization's own records; bring back only what generalizes.

## Workflow source
This repository adopts [Project Workflows](project-workflows/README.md) at `project-workflows/` as unchanged shared source, pinned by the parent gitlink to an exact detached revision. Read [docs/workflow.toml](docs/workflow.toml) first; its `project.root = ".."` resolves to this repository's root. Keep the package unchanged; this project's settings and records stay outside it.

Use [run-project-spike](project-workflows/run-project-spike/SKILL.md) for scoped work with paired reasoning and task records, [capture-for-later](project-workflows/capture-for-later/SKILL.md) for parked subjects, [commit-work](project-workflows/commit-work/SKILL.md) for commits, [setup-project-workflows](project-workflows/setup-project-workflows/SKILL.md) for setup and onboarding, and [update-project-workflows](project-workflows/update-project-workflows/SKILL.md) to move the pin. Prefer these pinned procedures over globally installed copies. [TODO.md](TODO.md) indexes active work; spike pairs live in `docs/active-spikes/`. Create scratch, archive and policy folders only when they have content.

No agent-policy system is adopted here. Rules for this repository are the ones in this file.

## Writing the kit
- Skills live at the repository root as `<skill-name>/SKILL.md`, named verb-first. Frontmatter uses only the standard keys: `name`, `description`, `license`, `allowed-tools`, `compatibility` and `metadata`. Descriptions contain no angle brackets.
- Supporting material for a skill lives inside its folder (`references/`, `examples/`) so the folder works on its own when linked into an agent client.
- Keep content organization-neutral and in plain language. Examples use a fictional organization: no real organization names, people, brand details or private records. Statute and section references in examples are illustrative.
- The kit explains governance design; it does not give legal advice. Flag legal questions for counsel rather than resolving them.

## Contribution coordination
Coordination is local: no forge, hosted issues or automation are selected. Use [coordinate-project-contribution](project-workflows/coordinate-project-contribution/SKILL.md) when work involves another person, and keep one spike per agent thread.

## Git and privacy
Agents may make scoped local commits by explicit pathspec after checking ignores. Never force-add, rewrite history unprompted, add co-author trailers or push. Commit workflow changes in the child repository first, then record its exact gitlink here. Treat this as a public repository: never commit credentials, private organization details or personal machine paths.

## Markdown style
Keep each prose paragraph or comment paragraph on one line and let editors wrap it. Avoid reflow-only edits. Put no blank line between a heading and its content. Preserve meaningful line breaks and explicit formatter requirements.
