---
layout: default
title: Settings
nav_order: 15
description: "MergeGuard's own configuration in the Home window's Settings section — and, in Studio, which values come from the team policy file."
---

# Settings
{: .no_toc }

Settings is the sixth section of [MergeGuard Home]({{ site.baseurl }}/docs/home-window/) — the product's own configuration lives there, in the same window as everything else.

## Policy-sourced values (Studio)

In Studio, some values can be set team-wide by the shared `MergeGuardData/policy.json` — push-check posture, size threshold, staleness window, and journal retention. When a value on this screen comes from team policy, the window shows that it does and names the file. See [Team Policy (Studio)]({{ site.baseurl }}/docs/team-policy/).

## What is not a setting

MergeGuard has no account, no server, and no network behaviour to configure: it never contacts GitHub, GitLab, or any other host, and it never fetches on its own. There is nothing in Settings that changes those limits — they are the product's boundaries, listed in full in [What v1 Is Not]({{ site.baseurl }}/docs/what-v1-is-not/).
