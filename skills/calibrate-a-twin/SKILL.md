---
name: calibrate-a-twin
description: >-
  Score a work digital twin against reality and correct it when it misses — the
  falsifiability engine that proves a twin is a mirror, not a mask. Use when the
  user wants to calibrate the twin, score the twin, log that the twin was wrong
  about X, record a divergence between what the twin predicted and what the real
  person did, pre-register a high-stakes prediction, or backtest the twin's calls
  over time. Triggers on phrasings like "calibrate the twin", "score the twin",
  "the twin was wrong about X", "log a divergence", "pre-register this
  prediction", "backtest the twin", "amend the doctrine". Building and auditing a
  twin is a separate skill (build-a-work-twin).
---

# calibrate-a-twin — score a twin against reality

A twin is only proven a **mirror** — the real person's reasoning — and not a
**mask** — the culture's flattened caricature of their role — if its predictions
survive contact with reality (`../../references/mask-vs-mirror.md`). A twin that
is never scored is never known to be faithful; a twin that is never wrong is never
being checked (`../../references/twin-contract.md`). Calibration is the only proof
you built a mirror. This skill runs the loop.

Reference material:

- **`../../references/mask-vs-mirror.md`** — why calibration is the load test, and
  pre-registration.
- **`../../references/twin-contract.md`** — the falsifiability clause; positions
  decay.
- **`../../references/dossier-template.md`** — the Calibration log format and which
  section owns what.
- **`../../references/five-dimensions.md`** — the dimension whose spec each miss
  type points back to.

---

## The predict → measure loop

1. **Gather the prediction.** Pull what the twin actually said — a recent
   pressure-test, panel record, review, or decision-proxy call. If it wasn't
   written down, there's nothing to score; going forward, capture the twin's calls
   so they're scoreable.
2. **Gather the actual.** Pull what the real person did — their call notes, Slack,
   email, review comments, the decision they actually made. Compare *substance*,
   not surface: did the twin raise the objection they raised, pick what they
   picked, refuse what they refused (the mirror test), or only sound like them?
3. **Log every divergence.** Append to the dossier's **Calibration log** (append-
   only, one entry per miss):

   ```
   YYYY-MM-DD — predicted: […] / actual: […] / correction: [section updated]
   ```

4. **Refresh live positions** while you're in the file — anything older than a
   quarter is a hypothesis, not a fact.

A match is worth logging too when it was a real test — it's evidence the mirror
holds. But the misses are where the fidelity is won.

## Correct the section that produced the miss

Route each miss to the dimension that caused it, not to wherever it's convenient:

- **Wrong objection / wrong decision criteria** → the **Lens** and the decision-
  criteria / "How X thinks" sections. The twin framed the problem wrong; the
  load-bearing dimension is off.
- **Right substance, wrong tone / cadence / register** → **Voice & style**. The
  reasoning held; the form didn't.
- **Missed an override** — predicted the subject would hold a line they actually
  conceded (or vice versa) because of who was in the room → the **relationship
  map** / governor dynamics. Name who overrides whom, on what.
- **Wrong disagreement move** — the twin blocked where the subject reframed, or
  nitted where the subject killed → the **Signature** / "How X pushes back"
  section. This is the most diagnostic miss for a red-team twin; fix it precisely.
- **Shadow surprise** — the subject did something the twin thought them incapable
  of, or the twin invented a tension that isn't real → the **Shadow** section.
  Evidence it or tag it `(unverified tension)`; never state hypocrisy you can't
  source.

Small corrections batch into the next PR touching the dossier. A **systematic**
miss — reliably too agreeable, too aggressive, consistently wrong on a governor
dynamic — is not a one-line fix; see doctrine amendments below.

---

## Pre-registration (commitment device for high-stakes calls)

COMPANION's sharpest move: for any high-stakes prediction, commit the twin's call
**sealed and timestamped before the real outcome is known**, and reveal only
after. A git commit is enough. This makes the result impossible to retrofit — a
twin can't be retroactively declared accurate once you've seen what happened.

1. Have the twin make the concrete prediction: what the person will decide, which
   objection they'll lead with, whether they'll greenlight.
2. Write it to a file and **commit it** — the commit timestamp is the seal. Do not
   edit it after.
3. When the real outcome lands, reveal the sealed prediction and score it against
   what happened. Log the result to the Calibration log either way.

Use it whenever the stakes make hindsight bias tempting — a big deal, a
contentious design call, a hiring decision the twin is standing in for.

## Quantitative backtesting (where outputs are measurable)

When the twin's output is a measurable decision — a forecast, a go/no-go, a
priority ranking, an estimate — score it numerically over time:

1. **Freeze the twin's decision** as a timestamped prediction (pre-register it as
   above).
2. **Score it against the real outcome or a benchmark** when reality resolves —
   did the deal close, did the design ship, was the estimate right.
3. **Track the hit rate over a run of calls**, not one. One correct call is
   anecdote; a scored series is calibration. Watch for *directional* bias (the
   twin is systematically optimistic, or systematically over-blocks) — that's a
   spec problem, not noise.

## Versioned doctrine amendments (for systematic misses)

When backtesting or a run of the log shows a *systematic* miss — the twin is
reliably wrong in one direction, not just wrong once — the dossier needs
re-speccing, not a one-line correction. Treat it as a versioned amendment:

- Name the pattern explicitly ("twin over-blocks on infra risk the subject
  actually waves through when the deadline is real").
- Amend the responsible section (usually Lens, Signature, or the relationship map)
  and note the amendment in the Calibration log with the date and the evidence run
  that justified it.
- Ship it as its own PR so the change to the twin's doctrine is reviewable and
  reversible — a doctrine amendment is a bigger claim than a divergence log entry,
  and should be visible as one.

---

## Invariants

- The Calibration log is **append-only**. Never rewrite history to make the twin
  look better — that defeats the entire falsifiability contract.
- **Positions decay.** Treat any "current stance" older than a quarter as a
  hypothesis; a stale un-scored twin is drifting toward a mask whether or not it
  has been touched.
- Calibrate against **substance**, not voice. A twin that sounds right but decides
  wrong is a mask with a good accent — the divergence to log is the decision, not
  the phrasing.
- Score both hits and misses when the interaction was a genuine test; suppressing
  the hits inflates the miss rate as surely as suppressing the misses hides drift.
