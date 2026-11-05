---
layout: default
title: Editions — Standard vs Studio
nav_order: 16
description: "One codebase, two listings. Standard ($79) is the setup, resolver, journal, locks and push-check core. Studio ($149) adds the Team Lock Board, push-gate reports, check history and team policy."
---

# Editions — Standard vs Studio
{: .no_toc }

1. TOC
{:toc}

## One codebase, two listings

MergeGuard ships as **one codebase** with two listings. Studio is the same package with the `MERGEGUARD_STUDIO` feature set enabled — there is no separate Studio project or second install. What differs is which feature set your licence turns on.

## Standard ($79)

- **MergeGuard Home** — one Editor window (Repo Health, Conflict Resolver, Scene Locks, Push Check, Merge Drill, Settings) with one-click setup and verification
- **One-click repo setup** — Force Text, visible meta files, the UnityYAMLMerge driver, `.gitattributes` / `.gitignore` blocks, Git LFS tracking when available (reported honestly when not)
- **Scene & prefab conflict resolver** — conflicts as GameObjects, property-level before/after, Keep Mine / Take Theirs per property, component, or GameObject; unpresentable content left untouched
- **Resolution journal + one-action undo**
- **Scene checkout declarations + lock warnings** — advisory only, shared through your team's own commits
- **Pre-push merge-risk check** — named findings, verdict in words
- **Merge Drill** sample scene
- Documentation set: quick-start, full reference, "what v1 is not"
- **34 automated EditMode tests (NUnit)** on Unity 6 and on 2022.3 LTS

## Studio ($149) adds

- **Team Lock Board** — every scene and prefab declaration across your team's local branches, with stale and duplicate declarations flagged
- **Push-Gate Reports** — any push check exported as a self-contained HTML report plus a Markdown summary, suitable for a pull request
- **Check history** — every push check your team ran, kept in-window (verdict, timestamp, branch pair)
- **Team policy defaults** — a shared `MergeGuardData/policy.json` sets posture, thresholds, staleness window and journal retention for every seat
- **37 automated EditMode tests (NUnit)** on Unity 6

## The verified record, exactly

Standard: 34/34 EditMode tests green on **Unity 6** and 34/34 on **Unity 2022.3 LTS**. Studio: 37/37 on **Unity 6**. A Studio test count on 2022.3 is **not** part of the verified record and is not claimed here. Verification ran on the Windows Editor; macOS Editor results are not part of the record — see [What v1 Is Not]({{ site.baseurl }}/docs/what-v1-is-not/).
