---
layout: default
title: One-Click Setup
nav_order: 6
description: "Setup wires a Unity project for Git correctly: audit first, plan shown file by file, backups before every write, and an undo for the setup itself."
---

# One-Click Setup
{: .no_toc }

1. TOC
{:toc}

## What setup changes

One click wires your Unity project for Git correctly:

- **Force Text** serialization and **visible meta files** in the project settings.
- The **UnityYAMLMerge** merge driver registered in the repo's local config, so Git routes Unity file merges through Unity's own merge tool.
- Marker-delimited **`.gitattributes`** and **`.gitignore`** blocks — MergeGuard owns only the block between its markers, not your whole files.
- **Git LFS tracking** for Unity binary classes, when LFS is available.

## Audit first, backups always

Setup audits first and shows the plan file by file before writing on the first run. Every file it touches is backed up first. **Undo Setup Changes** restores the pre-setup state — setup itself is reversible, like everything else MergeGuard writes.

## The LFS honesty rule

If Git LFS is not installed, setup completes without it and says so plainly. MergeGuard never claims LFS is configured when the probe failed — and the Push Check will later flag large binaries that are not tracked by LFS, so the gap stays visible instead of silent. See [Push Check]({{ site.baseurl }}/docs/push-check/).

## Setup drift

The pre-push check watches for **setup drift** — a repo whose current state no longer matches what setup established (a missing merge driver, a removed `.gitattributes` block, meta files turned off). Drift is reported as a named finding with its file, so it can be fixed before it turns into a conflict nobody can read.
