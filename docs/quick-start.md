---
layout: default
title: Quick Start
nav_order: 4
description: "The ten-minute path: run setup, then let the Merge Drill build a real two-branch scene conflict on your own machine — resolve it, undo it, resolve it again."
---

# Quick Start
{: .no_toc }

1. TOC
{:toc}

## 1. Open MergeGuard Home

**Tools → Decnet Games → MergeGuard** opens the one window everything lives in: Repo Health, Conflict Resolver, Scene Locks, Push Check, Merge Drill, Settings.

## 2. Run the one-click setup

Setup audits your repo first and shows the plan file by file before writing anything on the first run. It sets Force Text serialization and visible meta files, registers the UnityYAMLMerge merge driver in the repo's local config, writes marker-delimited `.gitattributes` and `.gitignore` blocks, and sets up Git LFS tracking for Unity binary classes when LFS is available. Every file it touches is backed up first, and **Undo Setup Changes** restores the pre-setup state. Full detail: [One-Click Setup]({{ site.baseurl }}/docs/one-click-setup/).

## 3. Run the Merge Drill

The drill is the onboarding path. MergeGuard's driver uses your own Git to build a real, local two-branch conflict in the DrillScene:

- the same turret, moved differently on both sides,
- its light re-coloured on theirs,
- a spawner added on theirs.

## 4. Resolve it as objects

Open the Conflict Resolver. You see two turrets, not YAML: each GameObject with its components and property-level before/after values, classified against the base version. Keep your position, take their light settings, accept the spawner — per property, per component, or per GameObject. Every choice is written to the resolution journal before the merged file is, and the scene opens clean. Full detail: [The Conflict Resolver]({{ site.baseurl }}/docs/conflict-resolver/).

## 5. Undo it — then resolve it again

Undo the whole resolution in one action: the file returns to its exact conflicted state, so you can resolve again or use another tool. Resolve it a second time. Full detail: [Resolution Journal & Undo]({{ site.baseurl }}/docs/resolution-journal-undo/).

## 6. Run the Push Check

One click checks your branch against its upstream, from your local refs only, and returns a verdict in words: **Safe to push**, **Review before pushing**, or **High merge risk** — with every finding named with its file. After the drill, the verdict is: Safe to push. Full detail: [Push Check]({{ site.baseurl }}/docs/push-check/).
