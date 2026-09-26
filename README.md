# AI Video Production Skills

Installable **agent skills** for consistent, premium-quality AI-generated video —
built for use with Claude or any agent runtime that supports the same skill format
(SKILL.md + references).

These are instruction packages, not software. They contain no code and call no APIs
of their own — an agent reads them and follows the workflow while helping you
generate video, scene by scene, on whichever platform you're using (Sora, Veo/Flow,
Kling, Runway, Seedance, Pika, etc.).

## Skills in this repo

### [`character-consistency`](skills/character-consistency/)
Keeps a character's face, voice, and personality consistent across every scene of a
multi-clip project. Builds a "character bible," compiles it into a reusable prompt
block, and runs a self-review checklist after every generated clip.

### [`cinematic-effect-engine`](skills/cinematic-effect-engine/)
Applies a premium, photorealistic, cinema/streaming-quality visual and audio
treatment to every shot — cinematography, camera movement, lighting, and production
design defaults, plus a quality self-check pass before delivering a scene.

**These two skills are designed to be used together.** `cinematic-effect-engine`
explicitly defers all character identity, continuity, wardrobe, and personality
decisions to `character-consistency` — it only governs how a shot is filmed and
rendered, never who's in it or what they look like.

## What these skills actually do (and don't)

Be clear-eyed about the limits here: no instruction skill can force a closed AI video
platform to internally guarantee facial/vocal identity or specific rendering
techniques (ray tracing, true 8K, etc.) across separate generation calls. These
skills work through:
- Disciplined, reusable prompt construction (so a character or visual style isn't
  re-described differently every time, which is the #1 cause of drift/inconsistency)
- Pointing to each platform's native reference-image/character-lock features as the
  primary mechanism where available
- A self-review checklist run after each generated shot, catching and correcting
  drift rather than preventing it at the model level

If you need a hard technical guarantee rather than a disciplined workflow, you'd want
a heavier pipeline — e.g. LoRA training per character, face-embedding similarity
scoring, or voice cloning with a fixed model. These skills are the lightweight,
install-anywhere version of that discipline, not a replacement for it.

## Installation

### For Claude (claude.ai, Claude Code, Cowork)
Download the packaged `.skill` file for whichever skill(s) you want from the
[Releases](../../releases) page, and upload/attach it wherever your Claude client
supports installing a skill.

### For other agents supporting the same skill format
Clone this repo and point your agent's skill-loading mechanism at the relevant
folder under `skills/` (each contains its own `SKILL.md` and `references/`).

### Manual / no skill-loader available
Paste the contents of a skill's `SKILL.md` directly into your conversation with any
capable AI agent and say "follow this workflow." These are plain-language
instructions, so they work even without formal skill-loading support.

## Repo structure

```
ai-video-toolkit/
├── README.md                          # this file
├── LICENSE
├── CONTRIBUTING.md
├── .gitignore
└── skills/
    ├── character-consistency/
    │   ├── SKILL.md
    │   ├── references/
    │   │   ├── character-bible-template.md
    │   │   ├── continuity-log-template.md
    │   │   └── platform-notes.md
    │   └── examples/
    │       └── example-character-bible.md
    └── cinematic-effect-engine/
        ├── SKILL.md
        └── references/
            └── shot-prompt-checklist.md
```

## Keeping platform notes current

AI video platforms ship new reference-image, character-consistency, and rendering
features often. `skills/character-consistency/references/platform-notes.md` reflects
what was true as of when it was last updated (see the file header for date). PRs
and issues updating it are welcome.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md).

## License

MIT — see [LICENSE](LICENSE).
