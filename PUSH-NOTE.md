# PUSH NOTE — MergeGuard-DOC (built 2026-11-05, local only, NOT pushed)

## What this folder is

The complete, push-ready source tree for MergeGuard's documentation site, built to the Decnet house "-DOC" pattern (structure/config mirrored from AgentProof-DOC / SteamDeck-DOC / ShipSheet-DOC):

- Just the Docs Jekyll site via `remote_theme` (no `theme:` gem key, no `just-the-docs` gem in the Gemfile — the pairing that fixed the two known GitHub Pages errors: "The just-the-docs theme could not be found" and "The github-pages gem can't satisfy your Gemfile's dependencies").
- 21 content pages: Home + Getting Started + Installation + Quick Start + The Home Window + One-Click Setup + The Conflict Resolver + Resolution Journal & Undo + Scene Locks & Declarations + Push Check + The Merge Drill + Team Lock Board (Studio) + Push-Gate Reports & Check History (Studio) + Team Policy (Studio) + Settings + Editions — Standard vs Studio + What v1 Is Not + FAQ + Troubleshooting + Changelog + Support.
- **No media in this tree, by design.** MergeGuard's Editor capture session is still blocked (GUI startup wedge — the project must be opened once by hand in BOSS's live session; staged runners at `C:\MarkBridge\mg-capture\` fire immediately after). Documentation never ships invented imagery: screenshots join `assets/` only after real captures exist, and the pages are written so they do not depend on any image.
- Content sourced ONLY from the verified record: the prep listing copy (`../../mergeguard-prep/LISTING-COPY.md` — every capability line is one of its SPEC-13 allowed claims) and the re-grounded build evidence in `../work/SESSION-NOTES.md` (Standard 34/34 on Unity 6, Studio 37/37 on Unity 6, Standard 34/34 on 2022.3 — XML records in `C:\MarkBridge`). Nothing that needs a screenshot or a GUI session is claimed. Studio is documented as the `MERGEGUARD_STUDIO` feature set on the same codebase — there is no separate Studio project. **macOS is not presented as verified anywhere** (verification ran on the Windows Editor); a Studio test count on 2022.3 is likewise not claimed.
- No product Asset Store URL exists yet (drafts only: Standard 1546210, Studio 1546212), so Home/Installation link the Decnet Games publisher page (118262) — swap in the product URL after the listing goes live, as with the other -DOC trees.

## Exact repo to create

- **Name:** `MergeGuard-DOC`
- **Owner:** `DecNet-Games` (GitHub org account)
- **Visibility:** public (required for GitHub Pages on this setup)
- **Live URL once Pages is on:** https://decnet-games.github.io/MergeGuard-DOC/ (matches the `baseurl: "/MergeGuard-DOC"` already set in `_config.yml`)

## Push route (do this from the laptop, per the standing no-card-spam rule)

Bulk pushes go via laptop git over SSH — never the GitHub connector.

1. BOSS creates the empty repo `DecNet-Games/MergeGuard-DOC` on GitHub (no README, no .gitignore — this tree carries its own).
2. Copy this folder's contents to the laptop clone location, then: `git init` (if needed) → `git add .` → `git commit` → the final `git push` is BOSS's own ~10-second action at his terminal (laptop git credentials only work interactively — known constraint).
3. On GitHub: repo **Settings → Pages → Build and deployment → Source: GitHub Actions** (the standard github-pages workflow), or "Deploy from a branch" → `main` / root if Actions is unavailable. The other -DOC repos run on the same org setup — mirror whichever source they use.
4. After the first successful build, verify:
   - the live URL loads with the Just the Docs theme (no theme error),
   - nav order: Home, Getting Started, Installation, Quick Start, The Home Window, One-Click Setup, The Conflict Resolver, Resolution Journal & Undo, Scene Locks & Declarations, Push Check, The Merge Drill, Team Lock Board (Studio), Push-Gate Reports & Check History (Studio), Team Policy (Studio), Settings, Editions — Standard vs Studio, What v1 Is Not, FAQ, Troubleshooting, Changelog, Support.
5. Only after the site is live: apply the house-format description (`../DESCRIPTION-HOUSE.md`) to the portal drafts 1546210 / 1546212 — its link line carries `DOCUMENTATION → https://decnet-games.github.io/MergeGuard-DOC/` (dead-link rule: never publish the link before the site resolves). The drafts currently carry the plain text from `../../mergeguard-prep/LISTING-COPY.md`; the house file replaces it at that point.

## What remains

- Repo creation + push + Pages enable: BOSS-side steps above (by design — this build stopped at a complete local tree, per instructions).
- Media: after the capture session unblocks (BOSS hand-opens the project once), real frames land in `../raw/` and can be added under `assets/images/` with a small content update — not required for the site to be complete or correct.
- Nothing in the tree itself: content, config and Gemfile are complete and internally verified (page count, front matter, nav order checked against disk).
