---
layout: default
title: What v1 Is Not
nav_order: 17
description: "MergeGuard v1's explicit boundaries: not a git client, no enforcement behind declarations, resolver scope of scenes and prefabs, Git only, and what was not verified."
---

# What v1 Is Not
{: .no_toc }

This page is the honest list. Everything MergeGuard v1 does is documented in these pages; everything here is what it deliberately does not do.

## Not a git client

MergeGuard has **no commit composer, no branch graph, no history browser**, and **no clone, fetch, pull, or push buttons**. Keep using the git tool you already use; MergeGuard makes it safe for Unity files. It never fetches on its own — when your local refs are stale, the push-check report says so and gives you the exact `git fetch` command to run yourself.

## Declarations are not enforcement

Scene declarations are **advisory warnings** that travel through your team's commits. There is **no MergeGuard server and no live presence**. MergeGuard cannot stop anyone from editing a scene — "lock" in this product means the team can see who is editing what before two people change the same file, never a hard lock.

## Nothing is auto-merged

The resolver never auto-decides a conflict and never silently discards a side. A file is written only when every true decision has your choice, and content the parser cannot present is left untouched. MergeGuard also never rewrites history.

## Resolver scope

The object-level resolver covers **scenes and prefabs** in v1. Other serialized files get the correct `.gitattributes` treatment from setup and are merged by the wired UnityYAMLMerge driver, but are not opened in the resolver. **Code conflicts** are your text tool's job.

## Git only

**Git only in v1**: no Plastic SCM, Perforce, Unity Version Control, or SVN. MergeGuard never contacts GitHub, GitLab, or any other host — it works with your own Git installation, with no account and no server; nothing leaves your machine.

## Platform and verification limits

Editor-only tooling: MergeGuard adds nothing to your build. **No Linux Editor support in v1.** The automated verification record for v1.0.0 is the **Windows Editor** — Standard 34/34 EditMode tests on Unity 6 and on 2022.3 LTS, Studio 37/37 on Unity 6. A Studio test count on 2022.3 is not part of that record, and **macOS Editor results are not part of the verified record** — macOS is not presented as verified anywhere in this documentation.
