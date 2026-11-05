# Bylaws Refactor Kit
An agent skill and working materials for rewriting an organization's bylaws without losing track of what the old ones said. The kit came out of a real refactor of a federated nonprofit's bylaws; its examples are genericized from that work.

The method separates three jobs:

1. **Translate.** Restate the current bylaws in plain language, one rule per numbered item, with reviewers' questions as bracketed notes. This Initial Translation becomes the agreed account of what the old rules actually say.
2. **Design.** Work out the new governance kernel and authority model on its own terms, guided by the [organizational design principles](map-bylaws-changes/references/org-design-principles.md).
3. **Map.** Build a Change Map that gives every material old rule a disposition (carried, consolidated, moved, cited upward, removed, and so on), a destination and a reason, so reviewers can check that nothing was silently dropped.

## Contents
- [`map-bylaws-changes/SKILL.md`](map-bylaws-changes/SKILL.md): the Change Map procedure, with its disposition questions, categories and completeness check.
- [`map-bylaws-changes/references/org-design-principles.md`](map-bylaws-changes/references/org-design-principles.md): nineteen working heuristics for judging governance choices.
- [`map-bylaws-changes/examples/initial-translation.md`](map-bylaws-changes/examples/initial-translation.md): an abridged example Initial Translation.
- [`map-bylaws-changes/examples/change-map.md`](map-bylaws-changes/examples/change-map.md): the matching part of its Change Map.

## Using the skill
`map-bylaws-changes/` is a standard agent skill folder. To make it available to an agent, link it into that agent's skills directory, for example for Claude Code:

```bash
ln -s "$PWD/map-bylaws-changes" ~/.claude/skills/map-bylaws-changes
```

Or point the agent at `map-bylaws-changes/SKILL.md` directly. Give it the Initial Translation, the proposed draft and any higher sources such as the Articles of Incorporation or applicable law.

The skill does not make legal conclusions. It flags unresolved legal questions for counsel.
