---
layout: default
title: Team Policy (Studio)
nav_order: 14
description: "Studio: a shared MergeGuardData/policy.json sets push-check posture, size threshold, staleness window, and journal retention for every seat."
---

# Team Policy
{: .no_toc }

**Studio feature.**

## One file, every seat

A shared `MergeGuardData/policy.json` sets team defaults for every seat:

- **push-check posture**,
- **size threshold** (the large-binary line the push check applies),
- **staleness window** (how old a local ref or declaration may be before it is flagged),
- **journal retention**.

Leads set the posture once; every seat inherits it through the shared file.

## Shown, not silent

The window shows when a value comes from team policy and **names the file**. A setting that arrived from `MergeGuardData/policy.json` is never presented as if it were a local choice — where a value came from is part of what the window tells you.
