---
name: map-bylaws-changes
description: Build and maintain a bylaws Change Map that traces every material rule in an organization's current bylaws to its treatment in a proposed rewrite. Use when refactoring bylaws or similar governing documents and reviewers need to see where each old rule went and why, without comparing documents line by line.
license: AGPL-3.0-only
---

# Map Bylaws Changes
## Purpose
Use this workflow to build and maintain a Change Map for a bylaws rewrite. The Change Map is a human-facing traceability artifact: it should let a reviewer see where each material rule in the current bylaws went and why, without reconstructing the rewrite from comments or comparing documents line by line.

## Inputs
- **Initial Translation:** the semantic account of the current bylaws. It restates them in plain language, one rule per numbered item in a decimal hierarchy, with reviewers' questions as bracketed notes. Verify it against the original bylaws before mapping from it.
- **Proposed draft:** the rewritten bylaws, and any rule modules, that serve as the destination and as the source of the generic authority and decision model.
- **[Organizational design principles](../org-design-principles.md):** the judgment guide for the refactor. Cite a principle only when it genuinely explains the choice.
- **[Kernel and rule modules](../README.md#kernel-and-rule-modules):** the kit's layered model that the dispositions point into: law and Articles, the bylaws kernel, board rule modules and delegations, and operational practice.
- **Higher sources:** applicable law, the Articles of Incorporation, or source records, when a legal or source-of-truth question matters.

The example [Initial Translation](examples/initial-translation.md) and [Change Map](examples/change-map.md) show an abridged, genericized pair from a real refactor.

## Mapping protocol
For each material old rule, capture:

1. Old section or rule
2. Disposition
3. Destination in the new draft, a rule module, operational practice, a higher-level source, or none
4. Plain-language rationale
5. Relevant organizational design principles, if they genuinely explain the choice
6. Any legal or source-of-truth question that remains

## Disposition questions
Before assigning a disposition, ask these questions in order:

1. What function is this old rule trying to perform?
2. Does the organization actually need that function governed?
3. Is it already controlled by a higher authority?
4. If the organization needs a rule, what is the least-powerful appropriate layer?
5. Can it use the generic authority, matter and decision machinery rather than a bespoke procedure?
6. Which organizational design principles genuinely explain the disposition?
7. Is there a legal uncertainty that prevents a final decision?

## Disposition categories
- **Carried:** preserved in substance.
- **Simplified:** the same core rule remains, with unnecessary or brittle machinery reduced.
- **Consolidated:** multiple old provisions become one canonical rule.
- **Moved to rule module:** the rule remains part of the organization's enforceable governance but does not live in the bylaws kernel.
- **Moved to operational practice:** the function remains necessary, but an authorized person or team can handle it without a board-level rule.
- **Cited upward:** no rule is needed because a higher authority already controls the point; cite or link the controlling source when context helps.
- **Removed as spent:** transitional or historical language no longer has ongoing effect.
- **Intentionally removed:** a current rule is rejected or replaced for a stated governance reason.
- **Legally unresolved:** treatment depends on law, the operative Articles, or counsel review.
- **New rule:** no predecessor; the new architecture needs a rule that did not exist in the old bylaws.

A disposition may carry a qualifier when the plain category would mislead, such as "Consolidated, with changes" or "Intentionally removed in part".

## Rules for the mapper
Do not let the Change Map generate the architecture. Design the broad governance kernel and authority model separately; the map is a coverage and accountability mechanism. When several architectures are under discussion, assess them against the same requirements without presuming a winner.

Do not silently drop a material old rule. Every material provision must have a disposition, even if several provisions consolidate into one destination.

Do not force every sentence into a separate row if several sentences are one functional rule. Preserve the real unit of meaning.

Do not invent legal conclusions. Flag unresolved legal questions, and cite the governing source when a legal conclusion is used.

Do not use design principles as automatic deletion rules. A principle may explain a choice, but it does not substitute for accounting for the source rule.

When the mapping process exposes a structural problem that cannot be resolved clause by clause, route it back to the governance-design discussion rather than hiding it in a disposition.

## Human-facing output
Keep the Change Map focused on old rule → disposition → destination → why. Keep agent instructions, working checklists and procedural mechanics in this skill rather than in the Change Map.

## Completeness check
Before treating a mapping pass as complete, verify that:

- every material old rule has a disposition
- every intentional removal has a rationale
- every consolidated or moved rule names its destination
- every cited-upward item identifies the controlling source
- every unresolved legal issue is visible
- important new rules are marked as having no predecessor
