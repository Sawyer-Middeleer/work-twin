# Your work-twin setup

How a user's own twins and workspace are structured. The plugin is the **engine**
(skills + this protocol + the shipped demo). Your twins are the **data** the engine
operates on — they live in your environment, never in the plugin.

## The model: twins are agents, the workspace is data

- **A twin is an agent dossier** — a self-contained system prompt (it carries its
  own calibration log inside it). Being a registered agent is what lets the skills
  dispatch it: `convene-a-board`, `pressure-test`, `coach`, `role-play`, and
  `think-with-a-twin` all run a twin as a subagent.
- **The workspace is the small amount of data that isn't a dossier** — mainly the
  named board bindings and a roster. It's optional and only appears once you have
  enough twins to need it.

## Zero-config to start

A fresh install needs no setup. Run `build-a-work-twin`; the dossier lands in
`.claude/agents/` and every skill can drive it immediately. The bundled
`work-twin:sawyer` demo sits alongside as a worked reference to copy.

```
.claude/agents/
  jordan-pm.md          a twin — self-contained, carries its own calibration log
  alex-eng-lead.md
```

## The scope choice

Where `.claude/agents/` lives decides a twin's reach. Pick per twin:

- **User-level `~/.claude/agents/`** — available in *every* project, matching the
  globally-installed plugin. Best for personal counterparts you consult everywhere:
  a manager, a mentor, key stakeholders.
- **Project-level `<repo>/.claude/agents/`** — scoped to one team or codebase. Best
  for "the eng leads on this repo" or a client's people. Travels with that repo.

Default to user-level for people you carry across projects; use project-level when a
twin only makes sense inside one repo.

## The workspace (appears when you scale)

Once you have ~4+ twins or a recurring panel, add a workspace next to your agents.
It lives at `.claude/work-twin/` — user-level (`~/.claude/work-twin/`) or
project-level (`<repo>/.claude/work-twin/`), matching where the twins it indexes
live.

```
.claude/work-twin/
  roster.md       index of your twins, one line each
  bindings.md     named boards for convene-a-board
```

Nothing else belongs there. Calibration logs live inside each dossier; corpus and
evidence stay in your own systems.

### roster.md

A flat index so you — and the skills — can see the whole set at once (distinctness
is a property of the set, per `differential-test.md`).

```markdown
# Twins

- **jordan-pm** — Director of Product. Red-team roadmap calls before they happen.
- **alex-eng-lead** — Staff engineer, platform. Pressure-test RFCs; delivery feasibility.
- **sam-cfo** — CFO. Board seat on any spend or headcount decision.
```

### bindings.md

Named boards for `convene-a-board`, so a recurring panel is one word instead of a
list. Name the governor dynamics — who overrides whom, on what.

```markdown
# Board bindings

- **leadership** — jordan-pm, alex-eng-lead, sam-cfo. Full read on a strategic call.
  Governors: sam-cfo governs spend; alex-eng-lead governs delivery feasibility.
- **delivery** — alex-eng-lead, jordan-pm. Technical/scope calls. alex governs feasibility.
```

## First run — what `build-a-work-twin` scaffolds

On the first build in an environment, the skill:

1. Asks (or infers) the scope — user-level or project-level.
2. Places the dossier in the matching `.claude/agents/`.
3. Creates `.claude/work-twin/` with a `roster.md` (the new twin registered) and an
   empty `bindings.md`.

On later builds it just adds the dossier and appends the twin to `roster.md`.

## The shipped demo is not your setup

In the plugin repo, `agents/sawyer.md` (the demo twin) and `twins/sawyer/` (its
evidence notes + worked examples) are a *showcase* of the method — read them, copy
them. Your own twins never go in the plugin; they live in your `.claude/agents/`
and `.claude/work-twin/` as above.
