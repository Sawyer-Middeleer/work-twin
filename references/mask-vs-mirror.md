# Mask vs. Mirror — the theory

The one idea that justifies everything else in this project. It is carried over
intact from COMPANION's preprint (*Mask vs. Mirror*, the Miranda Hypothesis).

When you instantiate a model of a real person, you get one of two things:

- A **mirror** — the actual person's reasoning, priorities, and idiosyncratic lens,
  reconstructed from real evidence of how they actually think and decide.
- A **mask** — the culture's flattened memory of them: the stereotype, the
  role-caricature, the "loudest memory," the version a base model produces from the
  average of everyone who ever held that title.

A work twin is only worth building — and only *safe* to consult — if it is a
mirror. A mask is worse than useless: it will confidently mispredict how the real
person would react, and you'll make decisions on that false confidence.

## The test

> Does the twin change *what gets built*, or only *what it sounds like*?

A mask changes only the surface — it gives you generic senior-engineer advice in a
particular accent. A mirror changes the substance — it raises the objection *this*
person would actually raise, picks the design *this* person would actually pick,
refuses the thing *this* person would actually refuse.

The forbidden six name the two ways a twin collapses into a mask: **flattening**
(reducing the person to their catchphrase) and **archetype mirror** (returning the
role instead of the person).

## Why the whole method follows from this

Every discipline in `work-twin` exists to force a mirror and detect a mask:

- **Evidence-grounded mining** (`work-evidence.md`) — a mirror is built from what
  the person actually did, not from what the model already "knows" about their type.
- **The differential test** (`differential-test.md`) — a mask is generic; if a
  twin's output could belong to any twin, it's a mask, and you rewrite it.
- **The exterior/interior evidence split** — a mask confabulates interior motives; a
  mirror sources them or admits it can't.
- **Calibration** (`calibrating-a-twin`) — the only proof that you built a mirror
  and not a convincing mask is that its predictions survive contact with reality.

## Pre-registration (a calibration discipline worth stealing)

COMPANION's sharpest methodological move: when you run an experiment to test a
twin's fidelity, commit the prediction **sealed and timestamped** *before* the real
outcome is known (a git commit is enough), and only reveal it after. This is a
commitment device — it makes the result impossible to retrofit, so a twin can't be
retroactively declared accurate. Use it for any high-stakes calibration: predict
what the person will decide, seal it, then score against what they did.
