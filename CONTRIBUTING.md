# Contributing

`work-twin` is a method plus a plugin. Contributions of both kinds are welcome:
sharper protocol, better skills, and new demo twins built from public evidence.

## Ground rules

1. **Consent and evidence.** Never contribute a twin — or evidence for one — built
   from material you don't have the right to model. The demo in this repo is built
   strictly from public writing. Anything you submit must clear the same bar.
2. **No corpus, no twin.** A twin built from vibes is a *mask*, not a mirror (see
   [`references/mask-vs-mirror.md`](references/mask-vs-mirror.md)). Every claim in a
   dossier traces to evidence, tagged by class per
   [`references/work-evidence.md`](references/work-evidence.md).
3. **The differential test is the bar.** A new twin or skill ships only if its
   output could not have come from any other twin or from "any senior person in
   that seat." See [`references/differential-test.md`](references/differential-test.md).
4. **No private data in public files.** No client names, credentials, financials,
   or interior-attested material in anything committed here. Sanitize or generalize.

## Adding a twin

Use the `build-a-work-twin` skill and follow
[`references/dossier-template.md`](references/dossier-template.md). Put the runnable
dossier in `agents/` and its evidence notes + worked examples in `twins/<name>/`.

## Changing the protocol

The `references/` files are the constitution — every skill and dossier is built
against them. A change there ripples: update the affected skills in the same PR,
and re-run the audit checklist in `build-a-work-twin` on the demo twin.

## Conventions

- No emojis in skill or reference files.
- Dense, plain prose. No filler.
- Match the lean, operational tone of the existing skills.
- Validate the plugin before submitting: `/plugin validate` in Claude Code.
