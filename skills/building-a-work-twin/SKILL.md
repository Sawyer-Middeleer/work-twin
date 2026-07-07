---
name: building-a-work-twin
description: >-
  Build a new work digital twin from a subject's work evidence, or audit an
  existing one. Use when the user wants to build a work twin, stand up a new
  digital twin of a real professional, model how X thinks from their
  correspondence and work product, or audit a twin that's gone stale. Triggers
  on phrasings like "build a work twin", "new digital twin", "model how X
  thinks", "twin from commits/PRs/docs", "audit a twin", "is this twin still
  faithful". Covers the full build lifecycle (scope → mine → provenance gate →
  dossier → Card → differential test) and the audit checklist. Calibration
  against reality is a separate skill (calibrating-a-twin).
---

# Building a work twin

A **work digital twin** is a high-fidelity model of how a specific real
professional thinks and decides — same models, same criteria, same blind spots —
reconstructed from their work correspondence and work product, and consulted
*before* the real person's time is spent. This skill builds one and audits one.

The references are the constitution. Read them before operating; the twin you
produce operates *on* them and must never contradict them:

- **`../../references/twin-contract.md`** — the contract every dossier stamps.
- **`../../references/five-dimensions.md`** — Voice / Lens / Drive / Signature /
  Shadow, and the Card schema.
- **`../../references/work-evidence.md`** — the mining method + the provenance gate.
- **`../../references/differential-test.md`** — the hollowness test, three moments.
- **`../../references/guardrails.md`** — Standards / Rules / the Forbidden Six.
- **`../../references/dossier-template.md`** — the dossier skeleton to draft on.
- **`../../references/mask-vs-mirror.md`** — why the whole method exists.

Two operations. Infer which from the request.

---

## build — stand up a new twin

### 1. Scope the subject

Confirm three things before any mining:

- **Who** — the real person being modeled.
- **Why** — what the twin is *for*: pressure-test, thought-partner, coach, board
  seat, role-play. The job determines what to mine hardest (a red-team twin lives
  or dies on its disagreement move).
- **What corpus exists** — the actual evidence you can reach. **No corpus, no
  twin.** A twin built from vibes is an archetype mirror by construction (see
  `mask-vs-mirror.md`) — it will confidently mispredict, which is worse than
  useless.

Match corpus span to the prediction domain. A twin predicts well only inside the
contexts its corpus samples; a twin mined from one repo or one quarter models the
engagement, not the person (`work-evidence.md`, anti-overfit).

### 2. Mine the two parallel briefs

Per `work-evidence.md`, mine along two tracks kept strictly separate:

- **Beliefs (content)** — mental models, decision criteria, live positions, hot
  buttons, what they optimize for. Feeds Lens, Drive, decision criteria.
- **Form (how they sound and move)** — cadence, syntax, lexicon, tics, and the
  *structure* of their work (decomposition, naming, what's tested vs documented).
  Feeds Voice and Signature. Form is co-equal to content, not decoration.

Mine each **register as a separate corpus** — chat, email, meeting transcripts,
public writing; commits, PR/review comments, design docs, code, tickets. The
shift pattern *between* registers is itself a fingerprint. Prioritize the
**disagreement move**: pull 3–6 verbatim moments from the review corpus and name
the move precisely (block / reframe / relocate / feasibility-test / question-stack
/ defer-then-veto). It is the single most diagnostic feature of a red-team twin.

Drive and interior Shadow are evidenced *badly* by observation. Source them from
the subject where possible (short correction interview, self-assessment, first-
person writing) and tag them. Do not confabulate interior motives — that is how a
mirror collapses into a mask.

### 3. Run the provenance / authorship gate (first-class)

Before any artifact becomes *voice* evidence, it passes an authorship check.
Work product has a contamination problem transcripts don't:

- **Commits** get co-authored, squashed, rebased. Use `git blame`,
  author-vs-committer, and `Co-authored-by` trailers — the committer is often not
  the author.
- **Docs and PRs** are collaboratively edited — a merged doc carries other
  people's sentences.
- **AI-generated / AI-assisted content is the dominant hazard.** Model-drafted
  code and prose are *not* the subject's voice; mining them clones the assistant
  into the twin. Fence AI-authored diffs and AI-drafted prose out of the voice
  corpus entirely.
- **Endorsement is not authorship.** An approved PR or merged design is an
  *endorsed position*, a real evidence class — but tag `authored-by-them`
  distinctly from `approved/merged-by-them`. Never treat a +1 as voice evidence.

### 4. Draft the dossier

Draft on `../../references/dossier-template.md` — a self-contained system prompt,
typically 20–35 KB, density over completeness. Stamp the **Twin Contract** from
`twin-contract.md` near-verbatim, adapting only name, pronouns, the subject's own
disagreement verbs, and the role archetype the twin must not collapse into. Do
not soften it. Keep the section order (identity + contract first, Card early,
evidence-dense middle, voice adjacent to the quote bank at the end).

Evidence every Shadow claim or tag it `(inferred)` / `(unverified tension)`.
Before filing a contradiction, look for a coherent frame that explains both sides
— an observer's unresolved understanding is not the subject's unresolved tension.

### 5. Write the Card contrastively

Write the five-dimension Card (`five-dimensions.md`) **against every other twin
you have, side by side.** Distinctness is a property of the *set*, not the
individual — no sentence should survive being lifted into a different twin's card.
Prefer texture words over trait words ("request-changes on the test file first",
not "detail-oriented"). Lead the Signature line with the disagreement move.

### 6. Run the differential test before shipping

Per `differential-test.md`, run **blind attribution** on the new Card + voice spec
against the stable: a reviewer with no labels attributes each excerpt to a twin.
Anything attributable to two-plus twins, or to "any senior person in that seat,"
fails — sharpen and rerun. Apply the **quote-bank test**: every quote is selected
for voice-distinctiveness, not content-importance (if any other subject you model
could plausibly have said it, cut it). Ship only when each line could only be
this subject's.

### Public / sanitized-demo variant

A twin built only from public or explicitly-sanitized evidence follows the same
skeleton but (per `dossier-template.md`): drops or thins **Drive** and interior
**Shadow** — those are interior-attested and a public corpus can't source them,
so say so in the honesty notes rather than faking them; marks the quote bank and
pushback examples as public-sourced; keeps the calibration log. Never mine
private secrets, credentials, personal/off-work writing, or anything the subject
hasn't consented to model.

---

## audit — check an existing twin

Run when a dossier feels stale, after the references change, or on request. Work
through the checklist; each miss is a fix to the dossier, not a note to file.

- [ ] **Contract current** — the Twin Contract is stamped and matches the current
      `twin-contract.md` (re-stamp if the reference moved).
- [ ] **Five dimensions populated** — Voice / Lens / Drive / Signature / Shadow
      all present with depth, not stubs.
- [ ] **Card contrastive** — each line fails to transplant into any other twin's
      card; blind-attribution still resolves to this subject alone.
- [ ] **Pushback section evidenced** — "How X pushes back" names the disagreement
      move and carries 3–6 verbatim examples; not shared with another twin.
- [ ] **Shadow evidenced, not decorative** — every entry evidenced or tagged
      `(inferred)` / `(unverified tension)`; no manufactured hypocrisy.
- [ ] **Live positions dated** — every stance dated; anything older than a quarter
      flagged as a hypothesis, not a fact.
- [ ] **Forbidden-six pass on a sample output** — generate one response and hunt
      the six (`guardrails.md`): register bleed, archetype mirror, self-narration,
      flattening, sycophancy, hollowness.
- [ ] **Quote-bank distinctiveness** — every quote still passes "no other subject
      I model could have said this"; move important-but-generic quotes out to the
      Lens / decision-criteria sections.
- [ ] **Provenance intact** — spot-check that voice evidence is `authored-by-them`,
      not AI-drafted or merely endorsed.

A single-section miss batches into the next PR touching the dossier. A systematic
miss — the twin reasons better than its subject, or has drifted toward the
archetype — warrants its own re-spec.

---

## Invariants (both operations)

- The dossier is a **self-contained system prompt**: stamp shared text in; never
  make the running twin reference these files at runtime.
- **Preserve the shadow.** A twin that reasons better than its subject predicts
  worse. Don't sand off the blind spots.
- **Twins simulate; they don't commit.** No outward or irreversible action; any
  decision needing the real person's sign-off says so, at the sanctioned footer.
- The proof you built a **mirror and not a mask** is that its predictions survive
  contact with reality — that lives in `calibrating-a-twin`.
