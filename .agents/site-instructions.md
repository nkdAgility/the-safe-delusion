# Site-specific instructions — the-safe-delusion

Hugo site serving one artefact: the community guide *Information for decision-makers considering the SAFe framework*, curated by Luca Minudel and Yves Hanoulle, CC BY-SA 4.0.

The job is **the wrapper pages around that guide**. Nothing else.

## Boundaries

- **Do not touch `site/content/safe-decision-makers/**`.** Published, audited item — the guide markdown, its PDF, `_index.md`, `history/`, `translations/`. Read it, never write it. Do not alter how its pages render.
- **Do not override the HugoGuides module** (`github.com/nkdAgility/HugoGuides/module`, `site/go.mod`). No new files under `site/layouts/` that shadow a module template. Pages render with module layouts; custom markup goes inline in the page — goldmark has `unsafe: true` (`site/hugo.yaml`).
- **Do not touch the build.** No CI, deployment config, routing config, `hugo*.yaml` or `go.mod`.
- No suggestions outside the wrapper pages.

Write surface: `site/content/` outside `safe-decision-makers/`, `site/layouts/index.html` (existing file, edit in place — confirm with a human first), `site/i18n/en.yaml`, `site/static/`.

## Premise

The premise the wrapper works from:

> SAFe is **bought** for psychological cover, not results (Sutherland). It is **sold** as a system of the wrong class for the problem (Thurlow). The failures it produces are then **blamed on the people** running it (Deming). And the one person who could stop it **never sees the evidence** (Weiss).

Four failure points, four jobs:

1. **Name the category error, not the practices** *(Thurlow)* — the wrong class of system for this kind of work, not a list of bad practices. This is why symptoms are framed as the design working, never as decline. "It has become theatre" concedes it once worked; it always was.
2. **Absolve the person, indict the system** *(Deming)* — 94% belongs to the system. Drive out fear. And "by what method?": criticism without method is complaint, so the exits carry as much weight as the symptoms.
3. **Replace the cover being removed** *(Sutherland)* — SAFe is bought for defensibility. Strip that and offer nothing in its place and the reader stays put, because you have made their position more dangerous, not less.
4. **Reach the buyer, in the buyer's units** *(Weiss)* — time to market, cost of delay, talent attrition, market share. Never methodology. Peer to peer, never pleading.

**These four are invisible.** None of them appear in the guide, so citing them on a page would mean the wrapper is introducing evidence its source does not contain. They shape structure, ordering, framing and voice, and are named nowhere.

## What the pages are for

The guide is the source of truth. The pages are the cliff notes and the way in.

Test for any page: *if the guide changed, would this need rewriting?* If yes it is duplication — don't build it. The pages say **what the evidence adds up to** and point at it. They never restate the findings. Pull counts, names and anchors from the guide page rather than typing them.

Write for the reader who is mid-adoption and quietly failing, and believes it is their own fault. Second, the exec who hasn't signed yet. The already-convinced practitioner is a distribution channel, not an audience.

Lead with **recognition, not conclusions**. Symptoms drawn from the case studies — PI planning as theatre, rising spillover, year-long time-to-market, dependencies accommodated rather than removed, everyone certified and nothing faster — then the turn: *this is not your implementation, it is the pattern across ten organisations, three of which SAFe showcased as successes.* The conclusions are the payoff, not the hook.

Keep the guide's civility. It concedes SAFe's adoption is growing, credits its useful elements, and thanks SAFe coaches. The domain name already signals polemic; the copy earns that back rather than spending more of it.

Unaudited site editorial must never be mistaken for the audited document. Show the guide's edition stamp, never a freshness claim.

## Current state

`site/layouts/index.html` is the home template. Three blocks are hand-written HTML copying guide prose — the executive summary (lines 77–96), observed trends (99–119) and the message to SAFe coaches (176–194). That is where the pages have forked from the guide.

The same file already derives correctly elsewhere: the "At a Glance" card (45–67) reads `.Params.guide_comparison` from the guide section, and the contributors card (157–171) uses the module's `functions/get-contributors.html` against `site/data/contributions/safe-decision-makers.yml`. Copy that pattern.

`site/layouts/old.index.html` is a leftover and is not in use.

**Open question for a human:** the guide is CC BY-SA 4.0, so wrapper pages summarising it are derivative works. Licence footer site-wide, or per-page on the derived ones?

