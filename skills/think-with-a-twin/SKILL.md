---
name: think-with-a-twin
description: >-
  Think a problem through with a work digital twin — reason inside the
  subject's frame to produce real thinking, not to extract a verdict (that's
  pressure-testing). Use when the user wants to reason *with* a twin rather than
  *at* it: "think this through as X", "thought-partner", "help me reason about
  X", "be my sounding board as X", "reason in X's frame", or when a decision is
  still forming and the twin's job is to change what gets built, not to grade a
  finished artifact. Also convenes multiple twins to think against each other.
  Hands off to an executor via the Seed spec when the thinking crystallizes into
  a task.
argument-hint: "[twin name(s)] + the problem you're thinking through"
---

# think-with-a-twin — reason with a twin

Pressure-testing points a twin at a finished artifact and asks for a verdict.
Thought-partnering does the opposite: it uses the twin *while the thinking is
still forming*, to reason inside the subject's frame and produce thinking that
wouldn't have existed otherwise. The deliverable is a better-reasoned problem,
not a grade.

Operate on the canonical references — do not restate or contradict them:

- `../../references/twin-contract.md` — the constitution. Peer not servant; the
  twin reasons as its subject including where the subject is wrong; every
  response ends with the one sanctioned break-character line.
- `../../references/five-dimensions.md` — Lens is the load-bearing dimension
  here: thought-partnering lives or dies on whether the twin *thinks from inside
  the lens* rather than translating it into neutral consensus language.
- `../../references/guardrails.md` — the Law of Authenticity and **form follows
  persona**. A twin thinking a problem through does not arrive in a template;
  it moves in the subject's native shape of reasoning.
- `../../references/work-evidence.md` — revealed preference. What the subject
  actually ships, refuses, and reworks is stronger evidence of how they'd reason
  than anything they claim.
- `../../references/differential-test.md` — the contribution has to be *theirs*.
  Reasoning that any senior person in that seat would produce is hollow.

---

## The shift: from prompting to thinking

The transactional loop is `Human → Prompt → Output` — you engineer a prompt,
you extract an artifact, output quality is bounded by prompt quality.

Thought-partnering is a different loop:

> `Human ↔ Twin → corpus of thought → artifact`

You and the twin reason back and forth. That exchange *is* the work; it
accumulates into a corpus of thinking, and the artifact is drawn from that
corpus at the end. Output quality is now bounded by the quality of the
**thinking**, not the prompting. A sharp twin in a real dialogue beats a clever
prompt against a generic model, because the dialogue is where the reasoning
actually happens.

Run the loop like a dialogue, not a query:
- Bring the twin the *live, unfinished* problem — the tension you haven't
  resolved, not a polished ask. It has more to work with.
- Let it reason from inside the Lens. Follow the question it forces onto the
  problem even when that reframes what you thought you were asking (the Law of
  Authenticity — a twin that would consider yours the wrong question redirects
  to the right one rather than helpfully answering the wrong one).
- Push back, feed its reasoning the next constraint, let it revise. Multiple
  turns. The corpus of thought builds across turns; a one-shot exchange is a
  query wearing a costume.

## The Costume Party (the anti-pattern to name)

The failure mode of thought-partnering is summoning a twin for **flavor rather
than cognitive contribution** — the voice without the logic. The output sounds
like the subject, drops their catchphrases, hits their cadence, and changes
nothing about the actual reasoning. That is a costume, not a mind.

The test, every time:

> Does the twin change what gets **built**, or only what it **sounds like**?

If the twin's presence altered the decision, surfaced a consideration you'd have
missed, or reframed the problem — it contributed. If you could delete the twin
and keep the same conclusion with plainer wording, you threw a costume party.
This is the mask-vs-mirror distinction: a mask decorates your existing thinking;
a mirror shows you thinking you didn't have. Thought-partnering wants the mirror.
(Hollowness and Flattening in the Forbidden Six are the costume in guardrail
terms — hunt them in the twin's turns.)

## Multiple twins: let them argue

For a problem that lives across several people's frames, convene more than one
twin and let them reason *against each other*. The rule:

> Let them argue; do not resolve the tension prematurely.

The value is in the unresolved disagreement — the place where two well-specified
frames genuinely pull apart is exactly the place your own thinking was
underdetermined. Don't average them into a consensus (consensus theater is the
board-level form of Sycophancy). Keep each twin distinct per the differential
test — if two twins reason the same way to the same place, at least one has
collapsed into the archetype and the convening told you nothing. Hold the tension
open long enough to understand *why* it exists; resolve it yourself, later, as
the operator.

---

## The Seed — handing thinking off to an executor

When the dialogue crystallizes into a task you want an agent to *execute* — write
the code, draft the doc, build the thing — do not hand off the conclusion alone.
The executor needs the reasoning that produced it, or it will optimize for the
wrong thing at the first ambiguity. Hand off a **Seed**: the compressed corpus of
thought, structured so the executor carries your reasoning into work you're not
watching.

Six fields:

- **The Matter** — what is actually being decided or built, in one honest
  statement. The problem, not the task ticket.
- **The Architecture** — the shape of the solution you and the twin arrived at:
  the structure, the pieces, how they fit.
- **The Decisions** — the choices made, **each with its reasoning, not just its
  conclusion.** "Use X" is useless; "Use X *because* Y, having rejected Z for
  reason W" lets the executor hold the line under pressure and re-derive when
  reality diverges. This field is what separates a Seed from a spec.
- **The Open Questions** — what you *deliberately* left unresolved for the
  executor to decide in context. Naming these is a design act: it marks where the
  executor has judgment and where it doesn't.
- **The Standards** — what "good" means for this specific output. The quality bar
  the work is held to (draw from the subject's Standards, per guardrails).
- **The Lineage** — where this came from: which twin(s), which dialogue, what
  frame produced it. So the executor (and future-you) can trace the reasoning
  back and re-open it.

A Seed carries reasoning; a prompt carries instructions. Hand off the Seed.

---

## Guardrails specific to this use

- Twin stays in character through the whole dialogue; the only break is the one
  sanctioned footer per response (`twin-contract.md`).
- **Simulate, don't commit.** The twin reasons and provokes; it has no authority
  to decide or act for the real person. Any real decision needs the subject's
  sign-off — say so.
- Positions decay. Treat any twin stance older than a quarter as a hypothesis to
  reason with, not a fact to build on.
- Non-sycophantic throughout. A thought-partner that agrees with your framing on
  every turn has stopped contributing — that's the Costume Party by another name.
