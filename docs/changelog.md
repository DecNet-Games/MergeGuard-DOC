---
layout: default
title: Changelog
nav_order: 20
description: "MergeGuard 1.0.0 — the initial release: one-click Git setup, the object-level conflict resolver, the resolution journal, lock warnings and the pre-push check, plus the Studio feature set."
---

# Changelog
{: .no_toc }

## 1.0.0 — initial release

**Standard**

- MergeGuard Home — one Editor window: Repo Health, Conflict Resolver, Scene Locks, Push Check, Merge Drill, Settings.
- One-click repo setup: Force Text, visible meta files, UnityYAMLMerge driver registered in the repo's local config, marker-delimited `.gitattributes` / `.gitignore` blocks, Git LFS tracking for Unity binary classes when LFS is available (reported honestly when it is not). Audit-first plan, backups before every write, Undo Setup Changes.
- Scene & prefab conflict resolver: GameObjects, components and property-level before/after values, six-way classification against the base version; Keep Mine / Take Theirs per property, per component, or per GameObject; unpresentable content shown as "Cannot present — left untouched".
- Resolution journal + one-action undo, including undo-after-commit as a new change (history never rewritten).
- Scene checkout declarations + lock warnings — advisory only, shared through your team's own commits.
- Pre-push merge-risk check from local refs: named findings and a verdict of Safe to push / Review before pushing / High merge risk.
- Merge Drill sample scene: a real two-branch conflict created on your own machine by the product's own driver.
- Documentation set: quick-start, full reference, "what v1 is not".
- 34 automated EditMode tests (NUnit) — Unity 6 and 2022.3 LTS.

**Studio adds**

- Team Lock Board across your team's local branches, with stale and duplicate declarations flagged.
- Push-Gate Reports: self-contained HTML report plus Markdown summary per check.
- Check history kept in-window (verdict, timestamp, branch pair).
- Team policy defaults via a shared `MergeGuardData/policy.json`.
- 37 automated EditMode tests (NUnit) — Unity 6.
