---
layout: default
title: The Merge Drill
nav_order: 11
description: "A real two-branch Git scene conflict created on your own machine by the product's own driver — resolved, undone, and resolved again as the onboarding path."
---

# The Merge Drill
{: .no_toc }

## A real conflict, made locally

The Merge Drill ships in the package. Run setup, then start the drill: MergeGuard's driver uses **your own Git** to build a real, local two-branch conflict in the **DrillScene** — the same turret moved differently on both sides, its light re-coloured on theirs, a spawner added on theirs.

Nothing about the drill is simulated or pre-baked: the conflict is created on your machine, by the product's own driver, in your repo.

## The sequence

1. **Open the Conflict Resolver** — you see two turrets, not YAML.
2. **Resolve** — keep your position, take their light settings, accept the spawner. Every choice lands in the resolution journal before the merged file is written.
3. **Watch the scene open clean.**
4. **Undo the whole resolution in one click** — the conflict comes back, exactly as it was.
5. **Resolve it again.**
6. **Run the Push Check** — the verdict is **Safe to push**.

That sequence is the demo, the onboarding, and the product: it exercises [setup]({{ site.baseurl }}/docs/one-click-setup/), the [resolver]({{ site.baseurl }}/docs/conflict-resolver/), the [journal and undo]({{ site.baseurl }}/docs/resolution-journal-undo/), and the [push check]({{ site.baseurl }}/docs/push-check/) end to end, on a conflict that cannot hurt any real work.
