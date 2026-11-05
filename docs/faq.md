---
layout: default
title: FAQ
nav_order: 18
description: "Short answers: git clients, auto-merge, lock enforcement, LFS, fetching, resolver scope, test counts, and where your data lives."
---

# FAQ
{: .no_toc }

1. TOC
{:toc}

## Does MergeGuard replace my git client?

No. It has no commit composer, branch graph, history browser, and no clone, fetch, pull, or push buttons. Keep using the git tool you already use — MergeGuard wires it correctly for Unity files and covers the moments it leaves you alone with YAML.

## Does it ever merge automatically?

No. Nothing is ever auto-decided and no side is ever silently discarded: a file can be written only when every true decision has your choice, and every choice is journaled before the merged file is written.

## Do scene locks stop a teammate from editing?

No — and the product says so wherever declarations are shown. Declarations are advisory warnings that travel through your team's own commits. There is no server and no live presence; the point is that the team can see who is editing what before two people change the same file.

## What if Git LFS is not installed?

Setup completes without LFS and says so plainly — it never claims LFS is configured when the probe failed. The push check will flag large binaries not tracked by LFS, so the gap stays visible.

## Does MergeGuard fetch or contact my host?

No. The push check runs from your local refs only, MergeGuard never fetches on its own, and it never contacts GitHub, GitLab, or any other host. When your local copy of the other branch is old, the report says so and gives you the exact `git fetch` command to run in your own terminal.

## Which files does the resolver open?

Scenes and prefabs in v1. Other serialized files are merged by the wired UnityYAMLMerge driver with the correct `.gitattributes` treatment from setup, but are not opened in the resolver. Code conflicts stay with your text tool.

## What happens to content the resolver cannot present?

It is shown as "Cannot present — left untouched" and left exactly as it was. Content is never dropped because the parser could not show it.

## Can I undo a resolution after committing it?

Yes — as a new change. If the file has since been committed, undo restores the pre-resolution version as a new change; history is never rewritten.

## How is MergeGuard tested?

Automated EditMode suites (NUnit): Standard 34/34 green on Unity 6 and 34/34 on Unity 2022.3 LTS; Studio 37/37 on Unity 6 — run on the Windows Editor. A Studio count on 2022.3 is not part of the verified record, and neither is macOS — see [What v1 Is Not]({{ site.baseurl }}/docs/what-v1-is-not/).

## Where does my data live?

On your machine and in your repo. Declarations and (in Studio) the team policy file travel through your own commits. MergeGuard has no account, no server, and nothing leaves your machine.
