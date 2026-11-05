---
layout: default
title: Troubleshooting
nav_order: 19
description: "The findings MergeGuard reports about itself: LFS missing, stale local refs, setup drift, 'Cannot present — left untouched', and declarations that have not travelled yet."
---

# Troubleshooting
{: .no_toc }

MergeGuard's own failure modes are reported as findings, in the window, with the file named — starting with these.

## "Git LFS is not installed"

Setup completed without LFS and said so. Nothing is broken: install Git LFS with your usual tooling, then re-run [setup]({{ site.baseurl }}/docs/one-click-setup/) so tracking for Unity binary classes is written. Until then, the push check flags large binaries not tracked by LFS.

## The push check says my view of the other branch is old

The check runs from your **local refs only**, and MergeGuard does not fetch on its own. The report names the staleness and gives you the exact `git fetch` command to run in your own terminal. Run it, then run the check again — in Studio, both runs are kept in the [check history]({{ site.baseurl }}/docs/push-gate-reports/).

## A "setup drift" finding

The repo no longer matches what setup established — a merge driver missing, a `.gitattributes` block removed, meta files turned off. Re-run setup: it audits first, shows the plan, and backs up before writing. **Undo Setup Changes** restores the pre-setup state if you change your mind.

## "Cannot present — left untouched" in the resolver

The parser could not present that content as objects, so it was left exactly as it was — never dropped, never guessed at. Resolve the presentable decisions in MergeGuard; the untouched remainder keeps the file honest, and the journal records what was and was not decided.

## A teammate's declaration is not visible yet

Declarations travel through your team's **own commits** — a declaration appears once the commit carrying it has reached your machine. There is no server sync to wait for and no live presence to check; if it is not visible, the commit has not arrived yet. See [Scene Locks & Declarations]({{ site.baseurl }}/docs/scene-locks/).

## Repo Health looks wrong

Repo Health shows the setup report and the **diagnostic log of every Git command MergeGuard has run**. Start there: the exact command behind any behaviour is recorded, which makes a support report (see [Support]({{ site.baseurl }}/docs/support/)) answerable instead of speculative.
