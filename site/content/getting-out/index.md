---
title: "Getting out"
eyebrow: "If you are already running it"
description: "What you are seeing is the framework working as designed, not your implementation failing. What other organisations did next, and how they explained it."
type: wrapper
weight: 30
---

If you are running SAFe and it is not delivering what you were promised, the most common explanation offered is that you have not implemented it well enough. More training. A better Release Train Engineer. The next version.

The evidence points somewhere else.

## What you are probably seeing

None of these are signs of a stalled adoption. They are the design operating exactly as specified.

{{< src who="Volvo Cars" note="A department of 11 teams dropped it in 2022." anchor="volvo-cars" >}}

**Planning has become presentational.** The real coordination happens in the corridors and the chat channels, and the board produced by the event adds very little against the effort it consumes. A department at Volvo Cars reached exactly this conclusion before dropping it.

{{< src who="Beijer Electronics" note="Left in June 2021." anchor="beijer-electronics" >}}

**Work spills from one iteration to the next, and the spill grows.** This is not immaturity. It is what large batches do. Beijer Electronics watched spillover rise and trust between technical and product people fall, quarter after quarter, and concluded things were getting worse rather than better.

{{< src who="Peaksys" anchor="peaksys" >}}

**The time between deciding to do something and a customer having it is measured in quarters.** Peaksys measured roughly a year and treated that number as the finding. A commitment cycle that freezes priorities for a quarter produces this outcome by construction.

{{< src who="Mary Poppendieck" note="Co-author, Lean Software Development." anchor="mary-poppendieck" >}}

**Dependencies are scheduled around rather than removed.** That is the method, not a shortfall in applying it. Mary Poppendieck's position is that you do not create capable teams by adding process — you create them by breaking dependencies.

{{< src who="Capital One" note="1,100 Agile roles cut, January 2023." anchor="capital-one" >}}

**Everyone has been trained and certified, and nothing moves faster.** Capital One targeted training its entire workforce, and eliminated 1,100 of the resulting roles six years later. Training was never the constraint.

{{< src who="Al Shalloway" note="One of three original SAFe Principal Contributors." anchor="al-shalloway-former-safe-principal-contributor-and-trainer-spct" >}}

**It seemed to work for the first few months.** Al Shalloway describes adoptions stagnating after three to six months and frequently leaving organisations worse off than when they started. The early gain is people finally in one room talking to each other. You did not need to buy a framework for that.

## This is not your implementation

{{< src who="General conclusions" anchor="general-conclusions" >}}

Across every case in the guide that permits independent verification, there is no evidence of lasting benefit against the time and effort spent — and the weaknesses of the operating models these organisations were trying to leave behind were amplified rather than reduced.

The organisations are not alike. A Swedish manufacturer of industrial interfaces. A French marketplace business. An Australian bank. A car maker. A global technology consultancy. The United States Air Force. Different sectors, different countries, different levels of capability, and the same shape of outcome.

When a result is that consistent across that much variation, it is a property of the system, not of the people running it.

## What other organisations did

{{< src who="Beijer Electronics" note="Improvement continued in the years after." anchor="beijer-electronics" >}}

**Beijer Electronics** left in June 2021. They moved toward understanding customer context first, putting product and technical people in the same team rather than in separate divisions, and letting teams use what they knew.

{{< src who="Peaksys" anchor="peaksys" >}}

**Peaksys** stopped, having concluded the framework was holding back both product focus and the working conditions of their teams.

{{< src who="Volvo Cars" anchor="volvo-cars" >}}

**A department at Volvo Cars** — eleven teams, just over a hundred people including product owners, developers, designers and subject matter experts — dropped it in 2022 and found the work organised itself more fluidly without it.

{{< src who="U.S. Air Force" note="Never adopted it." anchor="us-air-force" >}}

**The United States Air Force** issued a memorandum strongly discouraging rigid, prescriptive frameworks, and confirmed later that the conclusion stood.

## Why it was the wrong shape to begin with

{{< src who="Dave Snowden" note="Creator of the Cynefin framework." anchor="dave-snowden" >}}

The framework applies methods built for ordered problems — where cause and effect are known in advance, and the work can therefore be specified, sequenced and scheduled — to work where they are not. Dave Snowden's assessment is that this makes it wrong before any question of implementation quality arises.

That distinction matters because it decides what can be planned. Ordered work can be laid out a quarter ahead because the answer is known and only the execution remains. Product development mostly is not that: what to build is discovered by building, showing it to someone, and being wrong in public. A method that freezes a quarter of priorities is not badly run — it is answering a question nobody asked.

{{< src who="Ken Schwaber" note="Co-creator of Scrum; Agile Manifesto signatory." anchor="ken-schwaber-and-jeff-sutherland-co-authors-of-the-agile-manifesto" >}}

{{% editor label="How this reads to us" %}}
The deeper pattern is older than any of this. Separating the people who decide from the people who do is the defining move of scientific management — designed for manual work, where the task genuinely can be specified in advance by someone else.

It does not transfer. In knowledge work the person doing the job knows more about it than anyone who could write the plan, which is why Ken Schwaber's position is that the people doing the work are the ones best placed to work out how, and that management's job is to help rather than to suffocate.

A role hierarchy, a requirements hierarchy and a quarterly planning ceremony are all instruments for moving the thinking away from the doing. That is what they are for. It is also why the training never fixed it: the constraint was never how much your people knew.
{{% /editor %}}

## Stopping is a management discipline

{{% editor label="How this reads to us" %}}
Deciding what to stop is not an admission of failure — it is one of the ordinary jobs of management, and organisations that never do it accumulate commitments until nothing can move. Every programme should have to re-earn its place, and one that has run two years without producing the outcome it was funded for has not earned it.

That framing matters practically, because it changes what you are announcing. You are not reversing a decision. You are doing the thing that should have been scheduled from the start.

Three things appear to make the conversation easier, based on how the organisations above described their own.

**Report the measurement, not the verdict.** "Our time from decision to customer is currently around a year" is a fact a board can act on. "SAFe isn't working" is an opinion a board can argue with. Peaksys led with the number.

**Treat the programme as having produced information.** The adoption revealed where the dependencies actually are and what the coordination genuinely costs. That is a real return, and it is the return you are now acting on.

**Bring the next step, not just the stop.** The question that will be asked is *by what method?* Have the answer ready before you open the conversation.
{{% /editor %}}

## By what method, then

{{< src who="Recommended alternative" note="Going to the source of the original ideas." anchor="recommended-alternative-going-to-the-source-of-original-ideas" >}}

The guide's answer is not another framework, and that is deliberate — the organisations that recovered did not replace one package with another.

**Take the ideas from their source.** Nearly everything the framework contains was invented elsewhere and altered on the way in. Scrum, Kanban, Continuous Delivery, Lean UX, Team Topologies and the rest are all documented publicly by the people who created them, usually for free. The guide lists them with links.

{{< src who="Koen Vastmans" note="On practices absorbed and misrepresented." anchor="koen-vastmans-the-agile-blender-blunder" >}}

This is the part most often skipped, and it is why training did not help: people were taught an altered version and then blamed for the results. Going to source costs nothing and is the shortest available route to the thing you actually wanted.

**De-scale before you scale.** Reduce the coordination load rather than industrialising it — teams aligned to products and customers, dependencies removed rather than scheduled around, architecture that lets teams move without asking permission.

**Proceed by experiment.** Start small, learn, adapt, and let the approach grow out of your own circumstances rather than arriving pre-formed. This is the one point every recovered organisation in the guide has in common.

{{% editor label="How this reads to us" %}}
It is worth being honest that this is a harder thing to present than a named framework with a certification path and an implementation roadmap. It has no logo. That is a genuine disadvantage in a steering committee, and pretending otherwise would be useless to you.

What it has instead is that it is what the organisations who got out actually did, and it can be described in a sentence: *we are taking these practices from the people who created them, reducing the dependencies between our teams, and changing our approach as we learn rather than committing to a plan we cannot yet write.*
{{% /editor %}}

- [The original ideas and where they came from →](/safe-decision-makers/#appendix-2---original-ideas-assimilated-by-safe)
- [What worked instead →](/safe-decision-makers/#appendix-3---safe-alternatives-to-safe)
- [What the guide advises against →](/safe-decision-makers/#non-recommended-alternatives)
