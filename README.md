# work-twin

![Claude Code plugin](https://img.shields.io/badge/Claude%20Code-plugin-da7756)
![license](https://img.shields.io/badge/license-MIT-blue)
![lineage](https://img.shields.io/badge/lineage-COMPANION%20(CC0)-6e5494)

**Build a digital twin of how a real professional thinks — grounded in their work — and consult it before you spend their time.**

A *work twin* is a high-fidelity model of a specific colleague, counterpart, or
yourself: the same mental models, the same decision criteria, the same blind
spots, reconstructed from the trail of real work they leave behind — their
correspondence and their work product (commits, pull requests, design docs,
reviews, analyses). You consult it to pressure-test a decision, think a problem
through in their frame, get coached on your own patterns, convene a board of
several minds, or rehearse a hard conversation — *before* any of it reaches the
real person.

This is a Claude Code plugin. It ships the method, the guardrails, and a worked
demo twin.

---

## Mirror, not mask

When you model a real person you get one of two things. A **mirror** — the actual
person's reasoning, from real evidence of how they decide. Or a **mask** — the
culture's flattened memory of them: the stereotype, the role-caricature, the
version a model produces from the average of everyone who ever held that title.

A mask is worse than useless — it mispredicts the real person with total
confidence. Everything in this plugin exists to force a mirror and detect a mask:
evidence-grounded mining, a differential test that flags generic output, an
honest split between what a corpus can and can't know about someone's interior,
and calibration that scores every prediction against what the real person
actually did. Fidelity here is not built by making the summoning sacred. It's
built by **making the evidence sacred**. See [`references/mask-vs-mirror.md`](references/mask-vs-mirror.md).

## The five things a twin is for

| Use case | Skill | What it does |
|---|---|---|
| **Pressure-testing** | `pressure-test` | Run an artifact through one twin to surface the objections that person would actually raise. Red-team before they see it. |
| **Thought-partner** | `think-with-a-twin` | Think a problem *through* in the subject's frame — reasoning, not a verdict — and crystallize it into a hand-off Seed. |
| **Coach** | `coach` | The twin reads your own patterns back to you, and names the gap where what you *say* you want diverges from what you actually *ship*. |
| **Board-room** | `convene-a-board` | Several twins over one decision, where the *collision* between them reveals the decision's real shape. Emits a Decision Record. |
| **Role-play** | `role-play` | Rehearse a real interaction — a hard conversation, a pitch, a negotiation — against a twin that reacts as the real counterpart would. |

Two more skills run the lifecycle: **`build-a-work-twin`** (build one from work
evidence, and audit it) and **`calibrate-a-twin`** (score its predictions
against reality — the only proof you built a mirror).

## Quick start

1. **Add the plugin** in Claude Code:
   ```
   /plugin marketplace add Sawyer-Middeleer/work-twin
   /plugin install work-twin
   ```
2. **Meet the demo.** This repo ships a twin of Sawyer Middeleer (built only from
   public writing — see [`twins/sawyer/`](twins/sawyer/)). Try:
   > *Pressure-test this positioning line as the Sawyer twin: "We install AI operating systems for ops teams."*
3. **Build your own.** Point the `build-a-work-twin` skill at someone's work
   corpus (with their consent) and follow the method. No corpus, no twin.

## What's in here

```
references/     the protocol — the constitution every twin is built against
  twin-contract · five-dimensions · guardrails · work-evidence
  differential-test · dossier-template · mask-vs-mirror
skills/         the seven skills (build · calibrate · 5 use cases)
agents/         runnable twins — starts with the Sawyer demo
twins/sawyer/   the demo's evidence notes + one worked example per use case
```

## What a twin is *not*

A twin is a simulation, not the person. It **simulates; it does not commit** — it
has no authority to act, approve, or decide for the real person, and it says so
whenever a decision needs their actual sign-off. Its positions decay; treat any
stance older than a quarter as a hypothesis. And it is **falsifiable by design** —
if its predictions don't survive contact with reality, you built a mask, and the
calibration loop will tell you.

Build twins only from evidence you have consent to model. This plugin's own demo
is built strictly from public material, and says plainly which parts of a person
a public corpus cannot know.

## Lineage

`work-twin` descends from **THE COMPANION DOSSIER** by Jacob E. Thomas, PhD
(public domain, CC0), and from the author's internal `managing-personas` system.
See [`ATTRIBUTION.md`](ATTRIBUTION.md).

## License

MIT. See [`LICENSE`](LICENSE).
