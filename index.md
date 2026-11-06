---
layout: home
title: Home
nav_order: 1
description: "MergeGuard resolves Unity scene and prefab merge conflicts by choosing objects — never by editing YAML by hand — with one-click Git setup, lock warnings and a pre-push risk check."
permalink: /
---

# MergeGuard
{: .fs-9 }

Scene and prefab conflicts you resolve by **choosing objects** — never by editing YAML by hand.
{: .fs-6 .fw-300 }

[Get started]({{ site.baseurl }}/docs/getting-started/){: .btn .btn-primary .fs-5 .mb-4 .mb-md-0 .mr-2 }
[Buy on the Unity Asset Store](https://assetstore.unity.com/publishers/118262){: .btn .fs-5 .mb-4 .mb-md-0 }

![MergeGuard — scene and prefab conflicts resolved by choosing objects, not editing YAML]({{ site.baseurl }}/assets/images/cover-2400x1600.png)

---

## The moment every Unity team meets

Every Unity team that uses Git meets the same moment: two people edited the same scene on two branches, the merge stops, and the conflict sits inside a `.unity` file as thousands of lines of YAML. The usual way out is a text editor and hope. MergeGuard is the layer built for that moment — and for the moments before it.

- **One-click setup** wires your project for Git correctly — Force Text, visible meta files, the UnityYAMLMerge merge driver, `.gitattributes`, and Git LFS for your binary files — auditing first, backing up everything it touches, with an undo for the setup itself.
- **Object-level conflict resolution** — when a conflict happens anyway, MergeGuard reads the base, yours, and theirs versions and presents the conflict as the GameObjects inside it, with property-level before/after values. You choose per property, per component, or per GameObject: **Keep Mine** or **Take Theirs**.
- **A journal and one-action undo** — every choice is recorded before the merged file is written, and a completed resolution restores to its exact conflicted state from the journal.
- **Lock warnings** — declare "I am editing this scene" and see who else has declared the same scene, before two people change the same file.
- **A pre-push risk check** — same scene changed on both branches, files you have open and dirty, large binaries not tracked by LFS, committed conflict markers, missing `.meta` pairs, setup drift — each finding named with its file, and a verdict of **Safe to push**, **Review before pushing**, or **High merge risk**.

![The Conflict Resolver: DrillScene in conflict, presented as GameObjects with property-level before, mine and theirs values]({{ site.baseurl }}/assets/images/showcase-01-2400x1600.png)

## See it work in ten minutes

The **Merge Drill** ships in the package. Run setup, then start the drill: MergeGuard's driver uses your own Git to build a real, local two-branch conflict in the DrillScene — the same turret moved differently on both sides, its light re-coloured on theirs, a spawner added on theirs. Open the Conflict Resolver and you see two turrets, not YAML. Keep your position, take their light settings, accept the spawner, write the merged file, and watch the scene open clean. Then undo the whole resolution in one click — the conflict comes back, exactly as it was — resolve it again, and run the Push Check: **Safe to push**. That sequence is the demo, the onboarding, and the product. See [The Merge Drill]({{ site.baseurl }}/docs/merge-drill/).

![The Merge Drill loop: conflict, decisions, merged file written, undo, resolved again]({{ site.baseurl }}/assets/images/mergeguard-resolve-undo.gif)

<video controls width="100%" src="{{ site.baseurl }}/assets/video/mergeguard-demo.mp4"></video>

![Decisions made in the Resolver — every choice recorded in the resolution journal before the merged file is written]({{ site.baseurl }}/assets/images/showcase-02-2400x1600.png)

## Two editions, one codebase

**Standard** is the setup, resolver, journal, locks and push-check core. **Studio** adds the Team Lock Board, push-gate reports and check history, and team policy defaults. Studio is the same codebase with the `MERGEGUARD_STUDIO` feature set enabled — there is no separate Studio product to install. See [Editions]({{ site.baseurl }}/docs/editions/).

![Studio: the Team Lock Board — every scene declaration across the team's local branches, with lock warnings]({{ site.baseurl }}/assets/images/showcase-03-2400x1600.png)

> Automated verification for v1.0.0: **34/34** EditMode tests green on Unity 6 and on Unity 2022.3 LTS (Standard), **37/37** on Unity 6 (Studio), run on the Windows Editor. macOS Editor results are **not** part of the verified record — see [What v1 Is Not]({{ site.baseurl }}/docs/what-v1-is-not/).
