# Wrapper page plan

Working plan for the pages around the guide. Constraints and premise live in `CLAUDE.md`; this is what gets built.

Nothing here exists yet. Every factual claim listed as content comes from the guide and links back to it — the pages assert nothing the guide does not.

---

## `/` — home (rebuild of `site/layouts/index.html`)

**Job:** make one person feel recognised in ten seconds.

**Lenses:** Thurlow supplies the content, Deming the turn, Sutherland the ordering, Weiss the voice.

**Structure, in order:**

1. **Symptoms.** Five or six lines, each framed as the design operating correctly:
   - PI Planning is theatre — the real coordination happens elsewhere
   - Spillover rises every quarter: large batches doing what large batches do
   - A year from idea to customer: a quarterly freeze doing exactly what it specifies
   - Dependencies accommodated rather than removed, because that is the method
   - Everyone certified, nothing faster — training was never the constraint
2. **The turn.** *"It isn't failing. This is what it does."* Then the system-not-you line.
3. **Message to SAFe coaches**, lifted high. Currently the last card on the page.
4. **Payoff:** the guide's three conclusions and the scale of the evidence.
5. **Way in:** read the guide / the brief.

**Sources:** symptoms map to Volvo (PI planning for show, program board low value), Beijer (rising spillover, falling trust), Peaksys (year-long time to market, WIP, quarterly freeze), Poppendieck and Peaksys (dependencies), Capital One (100% trained and certified, then 1,100 roles cut). Conclusions and counts pulled from the guide page, not typed.

**Must not:** open with conclusions; use "has become" or any decline framing; blame anyone; use Agile vocabulary in the symptom list.

---

## `/getting-out/`

**Job:** absolve, then supply a method and the cover to use it.

**Lenses:** Deming's "by what method?" is the spine. Sutherland owns the section on defensibility. Named "getting out" rather than "already doing SAFe" because the job is exit, not remediation.

**Structure:**

1. **The symptoms in detail**, each deep-linked to the organisation that reported it.
2. **Why it is not your implementation** — the guide's conclusion that no verifiable case shows lasting benefit, and that pre-Agile shortcomings are amplified.
3. **What others did** — equal weight to the section above. Beijer left in June 2021 and improvements followed; Peaksys stopped; a Volvo department of 11 teams and 100+ people dropped it and worked more fluidly without it.
4. **How to present stopping as competence.** What you say to a board that approved the budget. Those three are the proof it can be told as a success story rather than a reversal.
5. **Where to go next** — the guide's Appendix 2 (original sources of the ideas SAFe assimilated) and Appendix 3 (alternatives).

**Must not:** offer remediation advice; imply a better implementation exists; restate the case studies rather than pointing at them.

---

## `/brief/`

**Job:** reach the economic buyer. The only page that does.

**Lenses:** pure Weiss. Strategically the most important page, because the practitioner reads the site and the person who can stop the programme never will.

**Structure:** one page, business consequences first, no Agile vocabulary anywhere.

- ANZ — home loan approvals among the slowest in Australia, substantial share of a $2 trillion mortgage market lost, share price down 17%
- Capital One — 1,100 Agile roles eliminated in January 2023, six years after the SAFe case study was published
- Peaksys — around a year from prioritisation to activation
- Volvo — two and a half years of transformation; a department later dropped it
- FitBit — abandoned SAFe; still listed as a success story
- USAF — strongly discouraged, and will not be used in any form

Closing claim in the guide's own evidential form: **in every case permitting independent verification, no evidence of lasting benefit.**

**Constraint:** this page gets forwarded and read detached from the site, in a room with no context. No assertion that is not either taken from the guide or explicitly marked as the site's framing. Every claim carries its link. The page self-identifies on its own face.

**Must not:** mention Scrum, Agile values, empiricism, velocity, or any framework comparison.

---

## `/objections/`

**Job:** arm the reader for the meeting. Every objection answered is cover restored.

**Lenses:** Sutherland — this is the defensibility engine.

**The five, in order:**

1. **"It's a stepping stone."** Chris Matts challenges this directly. First because it is the main defence of *never valuable*.
2. **"We just need to implement it properly / the next version fixes it."** Shalloway on stagnation at 3–6 months and companies left worse off; Shore on adoption with fanfare and silent abandonment years later.
3. **"That's bad implementation, not the framework."** The pattern holds across ten organisations, industries, countries and levels of competence.
4. **"Adoption is still growing."** The guide concedes this openly — say so, then note it is a market fact, not an outcome measure.
5. **"This is Agile-community gatekeeping."** Answered by who is speaking: former SAFe insiders, the authors of the practices SAFe assimilated, and the US Air Force.

Two sentences each. Every one ends in a guide anchor. Five is the cap.

**Must not:** grow a sixth section; editorialise; be sarcastic.

---

## `/right-of-reply/`

**Job:** be expensive to fake.

**Lenses:** Sutherland on costly signalling. Anyone can publish criticism; almost nobody publishes their opponent's rebuttal.

**Structure:** the guide's existing invitation to Scaled Agile Inc., made standing and public. How to submit a response. A commitment to publish verbatim and unedited. The same offer to any individual who believes they have been misquoted.

**Must not:** frame the invitation as a challenge or a dare. Flat and procedural.

---

## `/about/`

**Job:** satisfy the sceptic who checks who is behind it before reading a word.

**Lenses:** Weiss's peer positioning, Deming's constancy of purpose — a standing curated body of work, not a campaign.

**Structure:** curators (Luca Minudel and Yves Hanoulle) and contributors, drawn from `site/data/contributions/safe-decision-makers.yml`. Licence. How to contribute, and the discussion group. Methodology by link to the guide's premises section rather than restatement.

---

## Voice rules

- Flow language, never Agile language. "How long from idea to customer?" needs no priors.
- Loss framing, never gain framing. "Two and a half years, no lasting benefit" over "become more agile".
- Never blame a person — not the RTE, not the SPC, not the exec who signed.
- Never plead, never rant.
- The evidence delivers the verdict; the site never does. The moment a page says "should not be used" in its own voice rather than the USAF's or Equal Experts', it becomes an opinion piece and devalues the guide it exists to serve.
- "Never valuable" is stated in the guide's construction — no verifiable case shows lasting benefit — not as a universal negative, which invites "absence of evidence is not evidence of absence".

---

## Order

1. `/` — biggest gap, and it fixes the hand-copied guide prose at `site/layouts/index.html:77–194`
2. `/brief/` — reaches the buyer
3. `/getting-out/` — serves the primary reader
4. `/objections/`, `/right-of-reply/`, `/about/` — cheap, follow

---

## Open decisions

- **`site/layouts/index.html`** — it shadows a module home template. Confirm a human is content for it to be edited in place before the home rebuild starts. If not, the rebuild needs another mechanism and `/brief/` goes first.
- **Licence** — the guide is CC BY-SA 4.0 and these pages are derivative works. Footer site-wide, or per-page on the derived ones?
- **Two places the guide is softer than the premise** — Shalloway credits SAFe with useful concepts and calls it a reasonable first step above 500 developers; Hanoulle calls it "at best a gateway drug to agile". Matts pre-rebuts the stepping-stone framing, but a critic will find both. Decide whether `/objections/` addresses this head-on or leaves it.
