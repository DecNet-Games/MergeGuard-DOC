---
layout: default
title: The Conflict Resolver
nav_order: 7
description: "Conflicts presented as GameObjects with components and property-level before/after values — Keep Mine / Take Theirs per property, per component, or per GameObject."
---

# The Conflict Resolver
{: .no_toc }

1. TOC
{:toc}

## Objects, not YAML

When Git reports a conflict in a scene or prefab, MergeGuard reads the **base**, **yours**, and **theirs** versions and presents the conflict as the GameObjects inside it — with their components and property-level before/after values. You never open the YAML to decide.

## Classifications

Every change is classified against the base version:

- changed only in yours
- changed only in theirs
- changed in both
- added
- deleted
- changed in one and deleted in the other

## Your choices

Decide **per property**, **per component**, or **per GameObject** — **Keep Mine** or **Take Theirs**. Nothing is ever auto-decided and no side is ever silently discarded: a file can be written only when every true decision has your choice.

Every choice is written to the [resolution journal]({{ site.baseurl }}/docs/resolution-journal-undo/) **before** the merged file is written — the journal is the record that makes the resolution undoable and auditable.

## "Cannot present — left untouched"

Content the parser cannot present is shown as **"Cannot present — left untouched"** and is left exactly as it was. MergeGuard never drops content it cannot show you. This is a hard rule of the resolver, not a fallback message.

## Scope

The object-level resolver covers **scenes and prefabs** in v1. Other serialized files get the correct `.gitattributes` treatment from setup and are merged by the wired UnityYAMLMerge driver, but are not opened in the resolver. Code conflicts are your text tool's job and are listed as context only. See [What v1 Is Not]({{ site.baseurl }}/docs/what-v1-is-not/).
