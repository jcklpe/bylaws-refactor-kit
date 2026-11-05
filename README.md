# Bylaws Refactor Kit
An agent skill and working materials for rewriting an organization's bylaws without losing track of what the old ones said. The kit came out of a real refactor of a federated nonprofit's bylaws; its examples are genericized from that work.

The method separates three jobs:

1. **Translate.** Restate the current bylaws in plain language, one rule per numbered item, with reviewers' questions as bracketed notes. This Initial Translation becomes the agreed account of what the old rules actually say.
2. **Design.** Work out the new governance structure on its own terms: a small bylaws kernel with board rule modules, recorded delegations and operational practice below it, guided by the [organizational design principles](map-bylaws-changes/references/org-design-principles.md).
3. **Map.** Build a Change Map that gives every material old rule a disposition (carried, consolidated, moved, cited upward, removed, and so on), a destination and a reason, so reviewers can check that nothing was silently dropped.

## Contents
- [`map-bylaws-changes/SKILL.md`](map-bylaws-changes/SKILL.md): the Change Map procedure, with its disposition questions, categories and completeness check.
- [`map-bylaws-changes/references/governance-kernel-and-rule-modules.md`](map-bylaws-changes/references/governance-kernel-and-rule-modules.md): the layered model of law and Articles, bylaws kernel, rule modules and operational practice, and how to decide where a rule belongs.
- [`map-bylaws-changes/references/org-design-principles.md`](map-bylaws-changes/references/org-design-principles.md): nineteen working heuristics for judging governance choices.
- [`map-bylaws-changes/examples/initial-translation.md`](map-bylaws-changes/examples/initial-translation.md): an abridged example Initial Translation.
- [`map-bylaws-changes/examples/change-map.md`](map-bylaws-changes/examples/change-map.md): the matching part of its Change Map.
- `project-workflows/`: the pinned [Project Workflows](https://github.com/jcklpe/project-workflows) package used to run work on this repository, configured by [`docs/workflow.toml`](docs/workflow.toml).

## Using the skill
`map-bylaws-changes/` is a standard agent skill folder. To make it available to an agent, link it into that agent's skills directory, for example for Claude Code:

```bash
ln -s "$PWD/map-bylaws-changes" ~/.claude/skills/map-bylaws-changes
```

Or point the agent at `map-bylaws-changes/SKILL.md` directly. Give it the Initial Translation, the proposed draft and any higher sources such as the Articles of Incorporation or applicable law.

The skill does not make legal conclusions. It flags unresolved legal questions for counsel.

## Working on the kit
Clone with the submodule:

```bash
git clone --recurse-submodules <repository-url>
```

In an existing checkout without it, restore the pinned revision:

```bash
git submodule update --init
```

[AGENTS.md](AGENTS.md) holds the rules for agents working here, and [TODO.md](TODO.md) indexes active work. To get an agent oriented, paste this prompt:

```text
Read this repository's README and AGENTS. Help me get its declared Project Workflows source ready in my checkout, then read project-workflows/setup-project-workflows/SKILL.md and follow "Onboard a collaborator". Preserve the pinned submodule revision, the configuration in docs/workflow.toml and other contributors' work. Start with direct file-based skill use and explain any optional client discovery setup. Finish by showing me how to start coordinate-project-contribution here.
```

To start a piece of work, paste this one; it will ask you to describe it:

```text
Read project-workflows/coordinate-project-contribution/SKILL.md and ask me to describe the contribution I want to make, then help me start it. Read AGENTS.md, TODO.md and the relevant records, and follow the humans' existing direction. Use run-project-spike for your own scoped work and commit-work for commits.
```

## License
[AGPL-3.0-only](LICENSE).
