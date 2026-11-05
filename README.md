# Bylaws Refactor Kit
An agent skill and working materials for rewriting an organization's bylaws without losing track of what the old ones said. The kit came out of a real refactor of a federated nonprofit's bylaws; its examples are genericized from that work.

The method separates three jobs:

1. **Translate.** Restate the current bylaws in plain language, one rule per numbered item, with reviewers' questions as bracketed notes. This Initial Translation becomes the agreed account of what the old rules actually say.
2. **Design.** Work out the new governance structure on its own terms, using the [kernel and rule modules](#kernel-and-rule-modules) model below and the [organizational design principles](org-design-principles.md).
3. **Map.** Build a Change Map that gives every material old rule a disposition (carried, consolidated, moved, cited upward, removed, and so on), a destination and a reason, so reviewers can check that nothing was silently dropped.

## Kernel and rule modules
The kit's structural model for a bylaws rewrite. The bylaws become a small **kernel**, the rules for making rules and exercising authority. Everything else moves to a lower layer whose authority comes from the kernel and is recorded. The Change Map then shows which layer each old rule went to.

This is a design model, not legal advice. Whether a given arrangement works under a particular state's law, and under the organization's actual Articles, is a question for counsel.

### The layers
From highest to lowest:

1. **Law and the Articles of Incorporation.** Higher sources the organization cannot override. Cite them; don't copy them (principle 8).
2. **The bylaws kernel.** The minimum code that fully bootstraps the organization: who the constitutional actors are (for example the members or a member body, and the board), their reserved powers, where delegated authority comes from and what limits it, the authority to create subordinate rules, and how the kernel itself is amended.
3. **Rule modules and recorded delegations.** Serious, enforceable governance rules below the kernel, adopted by the board under authority the kernel grants. They work like standing rules: financial controls and signing limits, membership administration, additional officer duties, conduct and safety administration. Recorded delegations give named people or teams clear operating scopes.
4. **Operational policy and practice.** Ordinary procedures and day-to-day policy, set by the people and teams who hold recorded authority within their scope, without recurring board approval.

Below all of these is ordinary freedom: things that need no rule at all (principle 1).

### Why a kernel
The kernel resembles H. L. A. Hart's distinction between primary rules, which regulate conduct, and secondary rules, which establish how rules are recognized, changed and applied. The bylaws are the secondary layer that makes the rest of the system valid and legible.

Keeping that layer small puts stability where it matters and lets everything else change at the cost it deserves. A fiscal-year date or a signing limit should not need a bylaw amendment, and a change to who can elect the board should not be possible by board resolution alone. It also applies several of the [design principles](org-design-principles.md): define a rule once (7), keep governance surface area low (10), follow subsidiarity (12) and use the least power necessary (13).

### The kernel is hard to change on purpose
The board cannot normally amend the kernel by itself. Amendments normally need the concurrence of both the board and the members. Proposal authority can be broader than approval authority: either side may propose a change that still needs both to take effect.

Where law creates an exception to the amendment path, such as letting members change board size or director selection without board concurrence, treat it as an exception inside the one kernel. Don't create a separate "protected kernel" document for it.

### Who governs whom
In a membership organization or federation, a workable separation is:

- members govern themselves
- the member body governs the board at a high level
- the board governs the organization
- the board delegates operational authority downward

The member body's reserved powers make sense when they constitute, constrain or hold the board accountable rather than duplicate it. Examples: electing and removing directors, setting board size, admitting and removing members, approving the annual budget as a high-level resource constraint, and concurring on bylaw changes. The member body can be a continuously existing body that acts asynchronously, not only an annual meeting, so its powers don't lapse when an event slips (principle 15).

Rule modules are a board power in this model. The member body changes the constitutional settlement through the bylaws; it does not need a parallel module system unless a real need emerges.

### Deciding where a rule belongs
1. If law or the Articles require a provision to be in the Articles or bylaws, put it there.
2. Put the organization's allocation of governing authority, rights and decision procedures in the kernel. That is a deliberate design choice, not a claim that the law uses the same taxonomy.
3. A rule module must exercise an identified existing board power: assigning work, selecting an operating procedure, or imposing a control within that power. It cannot give itself independent power over the member body or the board, override the bylaws, or change the process for its own adoption.
4. Adopt each module by a recorded board resolution that states its scope and who implements it.
5. When moving a rule out of the current bylaws, amend the bylaws to remove it before relying on the board's ability to change its replacement module. Relabeling bylaw text as a module does not do that work.

Anything that passes none of these tests is operational practice, or needs no rule at all.

### The legal line
Many state nonprofit statutes define "bylaws" broadly, as the code or codes of rules adopted to regulate or manage the corporation, whatever they are called. Calling something a module therefore does not change its legal status. What distinguishes the layers is **authority and amendment path**: a separately named document adopted as bylaws is still bylaws, while a board resolution adopted under delegated authority is a different layer.

Look for express statutory authority for board resolutions, such as provisions that let the board assign additional officer duties, define committee authority, or add conflict-of-interest requirements. Those give modules a concrete legal basis. Where the line remains uncertain, mark the item "Legally unresolved" in the Change Map and route it to counsel.

### Keeping modules healthy
- Keep each module a separate document linked from the bylaws, and name the kernel authority it implements.
- Avoid module-to-module dependencies, so one can change without breaking another.
- Label draft modules as proposed board resolutions until they are adopted, and keep the adoption record with each.

### What stays out of the stack
Mission and values statements can remain organizational or expressive documents without constitutional force. Values can guide judgment; they should not silently create powers. A rule such as "a member may be removed for acting inconsistently with the organization's values" doesn't remove judgment; it relocates it into an argument about what an abstract value means. If a value truly needs governance force, write its concrete consequence into the kernel.

### How the layers show up in the Change Map
The dispositions map onto the layers: "Carried" and "Consolidated" usually stay in the kernel; "Moved to rule module" and "Moved to operational practice" name the lower layer; "Cited upward" points to law or the Articles; "Intentionally removed" means no layer needs the rule. A draft kernel skeleton that names the likely lower-layer destination for each article makes a move visible rather than letting it read as a deletion.

## Contents
- [`map-bylaws-changes/SKILL.md`](map-bylaws-changes/SKILL.md): the Change Map procedure, with its disposition questions, categories and completeness check.
- [`org-design-principles.md`](org-design-principles.md): nineteen working heuristics for judging governance choices.
- [`map-bylaws-changes/examples/initial-translation.md`](map-bylaws-changes/examples/initial-translation.md): an abridged example Initial Translation.
- [`map-bylaws-changes/examples/change-map.md`](map-bylaws-changes/examples/change-map.md): the matching part of its Change Map.
- `project-workflows/`: the pinned [Project Workflows](https://github.com/jcklpe/project-workflows) package used to run work on this repository, configured by [`docs/workflow.toml`](docs/workflow.toml).

## Using the skill
`map-bylaws-changes/` is a standard agent skill folder. To make it available to an agent, link it into that agent's skills directory, for example for Claude Code:

```bash
ln -s "$PWD/map-bylaws-changes" ~/.claude/skills/map-bylaws-changes
```

The skill reads this README and the design principles through `../` links, so link it from a kit checkout rather than copying the folder on its own. Or point the agent at `map-bylaws-changes/SKILL.md` directly. Give it the Initial Translation, the proposed draft and any higher sources such as the Articles of Incorporation or applicable law.

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
