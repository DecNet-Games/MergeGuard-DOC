---
layout: default
title: Resolution Journal & Undo
nav_order: 8
description: "Every decision recorded before the merged file is written — and a completed resolution restores to its exact conflicted state in one action."
---

# Resolution Journal & Undo
{: .no_toc }

## The journal comes first

Every decision you make in the [Conflict Resolver]({{ site.baseurl }}/docs/conflict-resolver/) is recorded in the resolution journal **before** the merged file is written. The journal is the product's memory of a resolution: what was in conflict, what you chose, per property, per component, per GameObject.

In Studio, journal retention is one of the values a shared [team policy]({{ site.baseurl }}/docs/team-policy/) can set for every seat.

## One-action undo

Every completed resolution can be undone as **one action**, restoring the file to its exact conflicted state so you can resolve again or use another tool. Undo that proves nothing was lost: the conflict comes back exactly as it was.

## Undo after a commit

If the file has since been committed, undo is offered as restoring the pre-resolution version **as a new change** — history is never rewritten. MergeGuard never rewrites history, in undo or anywhere else.
