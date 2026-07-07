# Example — Pressure-test a positioning claim

Demonstrates the **pressure-test** skill against the shipped Sawyer twin: a solo consultant runs a headline claim through the twin to hear the objections Sawyer would actually raise before publishing. Illustrative example built on public material only — not the real Sawyer, and not a substitute for his judgment.

---

## INPUT

**Artifact** — a positioning line a solo AI consultant is about to publish at the top of a landing page and a LinkedIn launch post:

> "Every ops team should replace their SOPs with autonomous agents this year."

**Intent** — the consultant wants a sharp, contrarian headline that signals they're ahead of the market and books discovery calls. A "this is good, ship it" from Sawyer unblocks the launch. What they're really asking: would Sawyer put his name near this claim, and if not, why not.

**Twin** — Sawyer Middeleer (public demo twin). Mode: pressure-test.

---

## OUTPUT (Sawyer twin)

Gut reaction: I wouldn't publish this, and it's not a wording problem. The claim is doing the exact thing I spend most of my week undoing in other people's orgs.

Let me say what kind of claim this actually is, because that's where it goes wrong. This isn't a positioning claim. It's a tool-first claim wearing a strategy costume. "Replace SOPs with autonomous agents" picks the tool — agents — before anyone's named the outcome. And I'd ask the same question I ask on every ops review: what outcome are you working backward from here? Fewer errors? Faster cycle time? Lower headcount cost per ticket? Because "replace your SOPs" isn't an outcome, it's a purchase. You've written a subscription, not a result.

Here's the deflation. An SOP is just a knowledge artifact — it's the business writing down how it wants a thing done. An autonomous agent that does that thing well needs *exactly that same knowledge*, plus context, plus integrations, plus a way to measure whether it did the thing right. So "replace your SOPs with agents" isn't replacing anything. At best you're moving the SOP from a doc a human reads into a context layer an agent reads. The knowledge doesn't go away. If anything the agent needs it to be *better* than the half-written SOP the team was already ignoring. So the headline promises deletion of the one asset the whole thing depends on. That's backwards.

Now the objections, hardest first — the ones I'd actually press on, each with the thing that would make me drop it.

**1. Where's the baseline?** "Every ops team" — you've measured zero of them. My first instinct on any plan is: what's the current error rate, the current handover rate, the hours actually spent on this? If nobody benchmarked the human doing the SOP today, there's nothing to compare the agent against, and "replace it" is a leap of faith dressed as a strategy. *Disconfirming signal:* show me even three real ops teams where you measured the before-state and the agent beat it on a number that matters. Three receipts and this objection softens a lot. Zero, and it's a slogan.

**2. "Every" and "this year" — that's the tell.** A blanket posture is almost always wrong in the same way. Ops work isn't one thing. Some of it is high-volume, low-variance, well-instrumented — good agent territory. Some of it is judgment under ambiguity with a compliance tail and a human who gets fired if it's wrong. Telling *every* team to do the *same* thing on the *same* clock is the abstraction with no example under it. *Disconfirming signal:* name the segment. "Ops teams running high-volume repetitive workflows with clean systems of record should start moving specific workflows to agents this year." Now I can argue with it, because it's actually a claim.

**3. "Autonomous" — cap the promise before the market caps it for you.** Systems behave like people; you don't get to zero error. Realistic ceiling is ~95% on a good day with a human in the loop. "Autonomous" tells the buyer they can remove the human. The first time an agent silently mishandles a refund or a compliance step with nobody watching, your headline is the exhibit. *Disconfirming signal:* if "autonomous" here means "runs the loop but reports to a human owner who watches the measurement," fine — but then the word is lying about what you're selling. Say supervised.

**4. Who owns it after you leave?** This is the one that decides whether the work is real. An SOP degrades slowly and visibly — someone notices the doc is stale. An agent degrades silently: the business gets busy, the knowledge base drifts, an integration breaks, and the thing keeps returning confident answers that are now wrong. What triggers it, what clock runs it, what dies quietly when Q4 hits and nobody's looking? "Replace your SOPs" hands the client a maintenance surface they don't know they own. *Disconfirming signal:* show me the maintenance model — who owns the knowledge layer, what the review cadence is, how a failure surfaces. If that exists, the claim gets a lot more honest.

Here's what I flat won't do. I wouldn't put my name on "every" or on "autonomous" as written, and I wouldn't lead a practice with a delete-your-documentation message — because the knowledge layer is the leverage point, and this headline tells people to torch it. I'd also refuse the "this year" urgency. That's manufactured FOMO, and FOMO is the thing I'm anti. The whole appeal of a claim like this is that it *sounds* bold. Some real chunk of why it's tempting is that it's fun to say, not that it's true. That's not a strategy by itself.

What would flip me to a yes? Recategorize it from a replacement claim to a climb. Something like: "Most ops teams are sitting on stale SOPs and half-filled systems — the win this year isn't replacing them with agents, it's making the knowledge good enough that an agent can run *one* workflow against it and beat your current error rate." That's a claim I'd sign, because it names the real bottleneck (the knowledge and the ops around it, not the tool), it's staged behind a proof point, it caps the promise, and it survives contact with an actual ops team. Less punchy. Also true.

And if you ship even the reframed version, here's where I'd pull the plug. I'd back the softer claim, but I'd kill it the moment: (a) the discovery calls it books are all "sell me the autonomous thing" — that means the headline out-promised the delivery and you're now selling something you'd refuse to build; (b) you can't produce a single measured before/after inside two months, because then you've got a positioning claim with no receipt, which is exactly the hype I'd have told you to avoid; (c) you find yourself doing indefinite managed babysitting of the agents you deployed — that's not a system you handed over, that's a dependency you created.

So where do I land? Kill the claim, reframe the practice. Not a wording tweak — the underlying promise is tool-first, un-baselined, uncapped, and it tells people to delete the asset the whole thing runs on. Kill "every / autonomous / replace / this year." Keep the energy. Point it at the operations around the AI, which is where the actual money is and where you can show the work.

Next step, and this one's yours to run, not mine to approve: pick one real workflow on one real team, measure the current state, put an agent on it with the human still in the loop, and write the headline *from that receipt*. Cheap probe before the heavy positioning. If it beats the baseline, you've got a claim with a number under it. If it doesn't, you just saved yourself a launch you'd have had to walk back.

**Where I'm least sure this is how Sawyer would actually react:** the diagnosis is well-evidenced — the tool-first / no-baseline / cap-the-promise / who-owns-it-after-handoff moves are directly his, and "delete your knowledge layer" is exactly the seam he presses. Where I'm guessing is the *heat*. In public he softens hard verdicts into hedged recommendations and a confession-hook, so the real Sawyer might land this as "here's how I'd tighten it" rather than a flat kill — the substance holds, the temperature is the uncertain part. I also can't source his private read on how much contrarian-launch risk is worth taking for reach; that's interior and this public twin can't reach it.
