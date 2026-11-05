---
layout: default
title: Installation
nav_order: 3
description: "Install MergeGuard from the Unity Asset Store and run the one-click setup. MergeGuard is sold exclusively through the Unity Asset Store."
---

# Installation
{: .no_toc }

## Asset Store only
{: .no_toc .text-delta }

MergeGuard is sold and delivered **exclusively through the Unity Asset Store** (publisher: Decnet Games). There is no other download channel, no licence server, and no account to create — if a copy of MergeGuard came from anywhere else, it did not come from us.

## Install

1. Purchase MergeGuard (Standard or Studio — same package codebase; Studio enables the `MERGEGUARD_STUDIO` feature set) on the Unity Asset Store.
2. In Unity, open **Window → Package Manager**, select **My Assets**, download and import MergeGuard into your project.
3. Open the window from **Tools → Decnet Games → MergeGuard**. Everything MergeGuard does lives in that one home window — see [The Home Window]({{ site.baseurl }}/docs/home-window/).
4. Run the [one-click setup]({{ site.baseurl }}/docs/one-click-setup/) once per repo. Setup audits first and shows the plan file by file before writing anything.

## Requirements

- Unity **2022.3 LTS** or **Unity 6**.
- A project under **Git**, with your own Git installation — MergeGuard runs your Git; it does not bundle one and never contacts GitHub, GitLab, or any other host.
- **Git LFS** is used when available for Unity binary classes. If LFS is not installed, setup completes without it and says so plainly — it never claims LFS is configured when the probe failed.
- Editor-only tooling: MergeGuard adds nothing to your build.

## Verified state

Automated verification for v1.0.0 ran on the **Windows Editor**: 34/34 EditMode tests green on Unity 6 and on Unity 2022.3 LTS (Standard), 37/37 on Unity 6 (Studio). macOS Editor results are not part of the verified record — see [What v1 Is Not]({{ site.baseurl }}/docs/what-v1-is-not/).
