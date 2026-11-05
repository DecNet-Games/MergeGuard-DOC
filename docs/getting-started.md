---
layout: default
title: Getting Started
nav_order: 2
description: "From the Asset Store download to your first resolved conflict: install MergeGuard, run the one-click setup, and run the Merge Drill."
---

# Getting Started
{: .no_toc }

MergeGuard works in one Editor window and one loop: **set up** the repo once, **declare** what you are editing, **resolve** conflicts as objects when they happen, and **check** before you push. This section takes you from the Asset Store download to your first resolved conflict.

## The path

1. [Install]({{ site.baseurl }}/docs/installation/) the package from the Unity Asset Store.
2. Follow the [Quick Start]({{ site.baseurl }}/docs/quick-start/): open MergeGuard Home, run the one-click setup, and run the Merge Drill.
3. Learn the one window in [The Home Window]({{ site.baseurl }}/docs/home-window/).

## What MergeGuard needs from you

- A Unity project under **Git** — MergeGuard works with your own Git installation. It is not a git client and never contacts a host; see [What v1 Is Not]({{ site.baseurl }}/docs/what-v1-is-not/).
- Unity **2022.3 LTS** or **Unity 6**.
- Optionally, **Git LFS**. Setup uses it for Unity binary classes when it is available — and reports honestly when it is not.

## The honest frame, up front

MergeGuard makes Git safe for Unity files; it does not replace your git tool. Declarations ("I am editing this scene") are advisory warnings that travel through your team's own commits — there is no MergeGuard server and no live presence, and MergeGuard cannot stop anyone from editing a scene. What it does is make sure the team can see who is editing what, present conflicts as objects instead of YAML, journal every resolution choice, and answer "will this merge hurt?" before you push.
