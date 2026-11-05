---
layout: default
title: Push-Gate Reports & Check History (Studio)
nav_order: 13
description: "Studio: any push check exported as a self-contained HTML report plus a Markdown summary for a pull request — and a history of every check your team ran."
---

# Push-Gate Reports & Check History
{: .no_toc }

**Studio features.** Both build on the Standard [Push Check]({{ site.baseurl }}/docs/push-check/).

## Push-Gate Reports

Any push check can be exported as:

- a **self-contained HTML report**, and
- a **Markdown summary**,

each carrying the verdict, every finding, and a **data-freshness line** — how current the local refs behind the check were. The pair is suitable for attaching to a pull request, so a reviewer sees the merge-risk state the pusher saw, not a screenshot of it.

## Check History

Every push check your team ran is kept in-window: **verdict, timestamp, branch pair**. History is how a team answers "did anyone check before that merge?" after the fact — from the record, not from memory.
