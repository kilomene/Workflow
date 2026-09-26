# Contributing

Thanks for considering a contribution. These are small, instruction-based skills, so
contributions are lightweight — mostly markdown edits, not code.

## Most useful contributions

1. **`skills/character-consistency/references/platform-notes.md` updates** — this is
   the file most likely to go stale. If a platform (Sora, Veo, Kling, Runway,
   Seedance, Pika, etc.) ships a new or changed reference-image/character-consistency
   feature, please open a PR or issue with:
   - Platform name and feature name
   - What it does (one or two sentences)
   - A source link (official docs preferred)

2. **New failure modes** — if you hit a specific type of character drift or visual
   quality issue not covered in either skill's "Common failure modes" section, add it
   with a short description of the symptom and the fix that worked.

3. **Additional worked examples** — a new file under `character-consistency/examples/`
   showing a filled-in character bible for a different genre/style is welcome.

## Guidelines

- Keep each `SKILL.md` under ~500 lines. If one is growing past that, propose
  splitting new content into a `references/` file instead, with a pointer from
  `SKILL.md`.
- No code dependencies, please — these skills are intentionally plain-instruction
  only, with no API or model calls of their own. A heavier, code-based variant (e.g.
  one that calls face-embedding comparison) is a good candidate for a separate
  skill/repo rather than folding it into these.
- Match the existing tone: direct, and honest about what the workflow can and can't
  guarantee. Avoid language that overpromises technical certainty these skills don't
  have.
- Keep the two skills' responsibilities separate: `character-consistency` owns
  identity/continuity/personality; `cinematic-effect-engine` owns visual/audio
  production quality. Don't let a PR blur that boundary.

## Testing a change

Since these are instructions, not code, "testing" means running the workflow with an
agent against a real (or toy) multi-scene project and checking whether the agent
follows the steps correctly.

## Reporting issues

Open a GitHub issue. Include:
- Which skill(s) and which agent/platform you were using
- What step of the workflow didn't behave as expected
- What you expected instead
