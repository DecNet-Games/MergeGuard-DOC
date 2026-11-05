---
layout: default
title: Scene Locks & Declarations
nav_order: 9
description: "Declare 'I am editing this scene', see who else has declared it, and get warned before two people change the same file — advisory only, shared through your team's own commits."
---

# Scene Locks & Declarations
{: .no_toc }

## Declare before you edit

From the home window, declare **"I am editing this scene"**. Declarations travel through your team's own commits — there is no MergeGuard server and no live presence.

## The warnings

MergeGuard warns when:

- a scene you are about to edit is **declared by someone else**,
- a scene you declared has **changed on another branch**,
- **two declarations exist** for the same asset.

## The limit, stated wherever declarations are shown

Declarations are **warnings** shared through your team's commits. MergeGuard cannot stop anyone from editing a scene — it makes sure the team can see who is editing what, before two people change the same file. The window states this limit wherever declarations are shown; it is never dressed up as enforcement.

## Studio: the Team Lock Board

Studio extends this section into the [Team Lock Board]({{ site.baseurl }}/docs/team-lock-board/): every scene and prefab declaration across your team's local branches, with stale and duplicate declarations flagged.
