---
layout: default
title: Push Check
nav_order: 10
description: "The pre-push merge-risk check: run against your branch's upstream from local refs only, every finding named with its file, and a verdict in words."
---

# Push Check
{: .no_toc }

1. TOC
{:toc}

## Know before you push

One click runs the pre-push check against your branch's upstream — **from your local refs only**. MergeGuard does not fetch on its own; if your local copy of the other branch is old, the report says so and gives you the exact `git fetch` command to run in your own terminal.

## What it looks for

- The same **scene or prefab changed on both branches** — with GameObject touch counts per side.
- Unity files changed on their side that you have **open and dirty**.
- **Large binaries not tracked by LFS**.
- **Conflict markers committed** in outgoing files.
- **Missing `.meta` pairs**.
- **Setup drift** — the repo no longer matching what [setup]({{ site.baseurl }}/docs/one-click-setup/) established.

Each finding is named with its file.

## The verdict

The verdict is one of three, as words:

- **Safe to push**
- **Review before pushing**
- **High merge risk**

## Studio: reports and history

In Studio, any push check can be exported as a [push-gate report]({{ site.baseurl }}/docs/push-gate-reports/) — a self-contained HTML report plus a Markdown summary, suitable for attaching to a pull request — and every check your team ran is kept in the **check history** (verdict, timestamp, branch pair). Push-check posture is one of the values a shared [team policy]({{ site.baseurl }}/docs/team-policy/) can set.
