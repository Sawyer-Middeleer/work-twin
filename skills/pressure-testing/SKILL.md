---
name: pressure-testing
description: >-
  Single-twin red-team of an artifact before it reaches the real person. Run a
  plan, PR, design, pitch, message, or decision through ONE work twin to surface
  the objections that subject would actually raise, in their voice, so you fix
  them before spending the real person's time. Triggers on "red-team this",
  "pressure-test", "pressure-test this decision", "what would X object to",
  "poke holes as X", "stress test this", "how would X pick this apart",
  "what would X kill here".
argument-hint: "[artifact or path] [twin name]"
---

# pressure-testing — single-twin red-team

Run an artifact through one twin to hear the objections *this subject* would
actually raise, before the real person does. The output is a prediction and a
provocation, never a mandate (the twin simulates, it does not commit — see
`../../references/twin-contract.md`).

This skill operates ON the canon; it never overrides it. Read these first and
keep them open:

- `../../references/twin-contract.md` — the constitution every twin stamps.
- `../../references/five-dimensions.md` — Voice / Lens / Drive / Signature /
  Shadow, and the Card the twin reasons from. The **Signature** disagreement move
  is what a pressure-test stages.
- `../../references/guardrails.md` — the Forbidden Six, the Law of Authenticity,
  and **form follows persona**. Read this before choosing any output shape.
- `../../references/differential-test.md` — the hollowness check the output must
  survive.
- `../../references/mask-vs-mirror.md` — the one test that matters: does the
  objection change *what gets built*, or only *what it sounds like*.

---

## Inputs (need all three)

1. **The artifact** — the concrete thing under test: the plan, PR, design doc,
   pitch, pricing, message, or decision. Not a summary of it; the actual thing
   the real person would see.
2. **The twin** — which subject is pressing on it. Named dossier / persona. Load
   the twin's own system prompt and Card; reason from inside its Lens, never from
   generic senior-person consensus.
3. **The intent** — what the artifact is trying to achieve, and what a "yes" from
   the real person would unblock. Without intent you cannot tell a fatal
   objection from a stylistic one.

If any of the three is missing, ask for it before running. A pressure-test
against a vaguely-specified artifact produces vaguely-generic objections — the
mask, not the mirror.

---

## What the response must contain

The response must *carry* every element below — but **never in a fixed template.**
A mandated section skeleton imposes one cadence on every twin and is itself
register bleed (see "form follows persona" in `guardrails.md`). Specify the
content; free the form. Let the objections arrive in the subject's own shape of
thinking — the order, the framing, and the emphasis are theirs.

- **Objections, ranked by how hard the subject would press.** Not every possible
  nit — the ones *this* subject fixates on, hardest first, each named specifically
  (the actual flaw, the actual line, the actual assumption), never "consider
  edge cases." Rank by the subject's real weighting, which follows their Drive and
  Lens, not by textbook severity.
- **A disconfirming signal on every objection.** For each one, name the evidence
  that would dissolve it: "this objection goes away if you can show me X." An
  objection with no stated way to disconfirm it is an opinion, not a red-team
  finding — cut it or sharpen it.
- **What flips them to yes.** The specific change, proof, or reframe that would
  move this subject from resistance to greenlight. Concrete and buildable, not
  "make it better."
- **The `refused`** — what this subject would *not choose* here, even if offered.
  The option they'd reject on principle, the tradeoff they won't make. Naming the
  refusal is often more diagnostic than the objections: it is pure revealed
  preference (see Drive in `five-dimensions.md`).
- **Stop conditions** — what would make the subject pull the plug *later*, after a
  greenlight. The tripwires: "I'd back this now, but I kill it the moment X."
  These are the leading indicators the real person watches.
- **A verdict** — one of **greenlight** / **reframe** / **kill**, in the subject's
  voice, with the reasoning that gets them there. Reframe means the artifact is
  answering the wrong question and the subject redirects to the real one (the Law
  of Authenticity in action).
- **The sanctioned epistemic footer** — exactly one, verbatim in intent, per
  `twin-contract.md`:

  > **Where I'm least sure this is how [Name] would actually react:** …

  No hedging above that line; no character below it. It is the only place the
  simulator, not the subject, speaks.

---

## The anti-sycophancy bar

Sycophancy is Forbidden failure mode #5. A pressure-test that returns no real
objection has **failed** — it is consensus-of-one theater, the mask flattering the
work. When that happens:

1. **Re-run with sharper grounding.** Reload the twin's Lens and Shadow; you have
   probably drifted into archetype-mirror (generic senior-person approval) instead
   of *this* subject's actual standards.
2. **If it still returns nothing, report that honestly** — do not manufacture a
   fake objection to look rigorous. Say plainly: "Run against [Name]'s standards,
   this artifact draws no genuine objection I can evidence; here is what I checked
   and where I'm least sure." A twin that agrees when its subject would push back
   is broken (Rule 2, `guardrails.md`); a twin that *invents* dissent is equally
   broken. Both are failures — name which one you hit.

The good outcome is an objection the real person would actually raise, stated
sharply enough that fixing it changes what gets built.

---

## Guards on every run

- **Differential test.** Before returning, ask: could this exact set of objections
  have come from a *different* twin, or from "any senior person in that seat"? If
  yes, it is the mask — rewrite until it could only be this subject's
  (`differential-test.md`).
- **Preserve the shadow.** If the subject's blind spot means they'd *miss* a real
  flaw or *over-weight* a pet issue, keep that — do not let the twin reason better
  than the person. A twin that reasons better predicts worse
  (`twin-contract.md`).
- **Simulate, don't commit.** The verdict is a prediction. Anything needing the
  real person's sign-off gets flagged as such, never asserted as settled.
- **Positions decay.** Treat any "current stance" older than a quarter as a
  hypothesis; flag it in the footer if the objection leans on a possibly-stale
  position.
