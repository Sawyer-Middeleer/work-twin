# Mining work evidence

A work twin is built from two evidence bases most persona systems ignore:
**work correspondence** (how the subject communicates) and **work product** (what
they actually make). This file is the method for turning that trail into a
faithful twin — and the hazards specific to work artifacts.

The governing principle: **make the evidence sacred.** The twin's fidelity is to
what the corpus shows, not to what would be flattering, convenient, or generic.

---

## Two parallel briefs

Mine the corpus along two tracks, kept separate:

- **Beliefs (content)** — mental models, decision criteria, live positions, hot
  buttons, what they optimize for. Feeds Lens, Drive, and the decision criteria.
- **Form (how they sound and move)** — cadence, syntax, lexicon, and the
  *structure* of their work. Feeds Voice and Signature. A form spec describes
  cadence and moves, never positions: "believes in working backwards" is Lens;
  "opens a review with the one blocking concern, then nits" is Voice.

Form is co-equal to content, not decoration. A twin that reasons like the subject
but sounds like the base model has failed half the job.

## Registers are separate corpora

Each channel is a distinct voice; mine and spec them separately.

**Work correspondence**
- Chat / DMs (Slack, Teams) — fast, informal, reactive
- Email — structured, audience-aware
- Meeting transcripts — spoken, unedited
- Public writing — posts, talks, published articles (the most-edited register)

**Work product**
- Commit messages — terse, imperative, high-frequency
- Pull request descriptions & review comments — the disagreement register
- Design docs / RFCs / specs — discursive rationale, how they argue a decision
- Code / notebooks / analyses — structure-as-form: decomposition, naming,
  what's tested, what's documented
- Tickets / issues — how they frame and scope work

A twin that writes commit messages the way its subject talks in meetings is
miscalibrated. Extract per register: cadence, lexicon, syntax habits, tics,
openings/closings, structural habits, and the *shift pattern* between registers
(the shift itself is a fingerprint).

## How-they-disagree is the priority axis

For a twin whose job is pressure-testing, disagreement *is* the job — so the
disagreement move is the single most diagnostic thing to mine. In work product it
lives in the **review corpus**: request-changes comments, "why not X?" questions,
blocking-vs-nit calls, the architectural objection, the revert or rollback
decision, the design-doc counter-proposal. Pull 3–6 concrete moments, capture the
verbatim words, and *name the move*. If two twins share a move, re-mine — one has
defaulted to the archetype.

---

## The provenance gate (first-class, not a footnote)

Work product has a contamination problem that meeting transcripts do not:
**authorship is muddy, and increasingly synthetic.** Before any artifact becomes
voice evidence, it must pass an authorship check.

- **Commits** get co-authored, squashed, rebased, and cherry-picked. Use
  `git blame`, author-vs-committer, and `Co-authored-by` trailers — the committer
  is often not the author.
- **Docs and PRs** are collaboratively edited; a merged doc contains other
  people's sentences and suggestions.
- **AI-generated / AI-assisted content is the dominant hazard.** Code and prose
  drafted by a model are *not* the subject's voice. Mining them clones the
  assistant back into the twin — you build a twin of the tooling. Fence AI-authored
  diffs and AI-drafted prose out of the *voice* corpus entirely.

**Endorsement is not authorship.** Approving a PR, merging a design, or +1-ing a
proposal is a real and useful evidence class — but it is an *endorsed position*,
not voice evidence. Tag `authored-by-them` distinctly from `approved/merged-by-them`.

## Evidence classes (strongest first)

Tag every claim by how it's sourced. Interior claims need interior evidence.

```
(subject-attested)  >  instruments  >  verbatim-them  >  endorsed positions  >  observer-inferred
```

- **Voice, Lens, and Signature** are well-evidenced by the behavioral corpus
  (correspondence + authored work product).
- **Drive and interior Shadow** are evidenced *badly* by observation — goals,
  fears, and values are interior states an observer infers at low fidelity. Source
  them from the subject directly where possible (a short correction interview,
  self-assessment instruments, first-person writing), and tag them. Work product's
  revealed-preference signal helps here, but does not fully substitute.
- **The unverified-tension rule:** before filing a Shadow contradiction ("preaches
  X, ships Y"), look for a coherent frame that explains both. An observer's
  unresolved understanding is not the subject's unresolved tension. If you can't
  resolve it and can't ask, tag it `(unverified tension)` — never state it as
  hypocrisy. Manufactured contradictions make the twin reason from motives the
  subject doesn't have.

## Anti-overfit

Recency is a bias, not a virtue. Weight by durability: crystallized patterns
repeated across contexts outrank one busy sprint's commit volume. **The overfit
tell:** if a dossier's pushback examples, quotes, and shadow all cite one repo or
one quarter, the twin models the engagement, not the person. Match corpus span to
prediction domain — a twin predicts well only inside the contexts its corpus
samples.

## Always excluded

Never mine private secrets, credentials, personal/off-work writing, or anything the
subject hasn't consented to model. A public or shareable twin is built only from
public or explicitly-sanitized material — and says, honestly, which dimensions its
corpus leaves thin.
