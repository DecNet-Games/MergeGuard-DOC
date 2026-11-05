---
layout: default
title: The Home Window
nav_order: 5
description: "One window, six sections: Repo Health, Conflict Resolver, Scene Locks, Push Check, Merge Drill, Settings. No orphaned feature windows."
---

# The Home Window
{: .no_toc }

**Tools → Decnet Games → MergeGuard** opens MergeGuard Home — the single window everything lives in. The **Conflict Resolver** and **Run Push Check** menu items are shortcuts into this window; there are no orphaned feature windows.

## The six sections

- **Repo Health** — the setup report, and the diagnostic log of every Git command MergeGuard has run. If a finding ever surprises you, this is where the exact command behind it is recorded.
- **Conflict Resolver** — scene and prefab conflicts presented as GameObjects, with the resolution journal behind every decision. See [The Conflict Resolver]({{ site.baseurl }}/docs/conflict-resolver/).
- **Scene Locks** — your declarations and your team's, with warnings when two declarations cover the same asset. In Studio this section is the [Team Lock Board]({{ site.baseurl }}/docs/team-lock-board/). See [Scene Locks & Declarations]({{ site.baseurl }}/docs/scene-locks/).
- **Push Check** — the pre-push merge-risk check and its verdict. In Studio, checks can be exported from here as [push-gate reports]({{ site.baseurl }}/docs/push-gate-reports/) and every check is kept in the check history. See [Push Check]({{ site.baseurl }}/docs/push-check/).
- **Merge Drill** — the shipped sample: a real two-branch Git scene conflict created on your own machine by the product's own driver. See [The Merge Drill]({{ site.baseurl }}/docs/merge-drill/).
- **Settings** — MergeGuard's own configuration. In Studio, values that come from the shared team policy file are shown as policy-sourced and the file is named. See [Settings]({{ site.baseurl }}/docs/settings/) and [Team Policy (Studio)]({{ site.baseurl }}/docs/team-policy/).
