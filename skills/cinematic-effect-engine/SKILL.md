---
name: cinematic-effect-engine
description: Use this skill whenever a user is generating AI video shots/scenes and wants a premium, photorealistic, cinema/streaming-quality look applied automatically — e.g. "make this look like a Netflix show," "cinematic quality," "photorealistic film look," "professional camera work," or any multi-shot AI video project where consistent high-end visual/audio production value matters across every shot. This skill governs visual and audio production quality only — it does not control character identity, continuity, wardrobe, or personality; pair it with the character-consistency skill for those. Also use this skill's self-critique checklist as a final quality pass before delivering any generated cinematic scene.
---

# Premium Cinematic Effect Engine

## Scope (read this first)

This skill controls **visual and audio production quality** — the "how it looks and
sounds" layer applied to every shot. It does not control character identity,
continuity, wardrobe, timeline, or personality — those belong to the
`character-consistency` skill. If both skills are installed, always apply
character-consistency's Identity Block for who/what is in the shot, and this skill's
Core Look for how the shot is filmed, lit, and rendered.

Apply the Core Look below to every generated shot by default, unless the user's scene
description explicitly overrides a specific element (e.g. "black and white,"
"handheld shaky cam," "1.85:1 aspect ratio" should override the corresponding default
below rather than being fought).

Treat this as a **prompt-construction and quality-review discipline**, not a
technical guarantee — no instruction skill can force a video generation model to
produce ray-traced reflections or true 8K fidelity if the underlying model can't
produce those. Translate the intent (premium, photorealistic, cinema-grade) into the
best prompt language for whichever platform is being used, and note plainly to the
user if a specific platform is known to struggle with a specific element (e.g. very
shallow depth of field, anamorphic aspect ratios) rather than promising it anyway.

## Core Look — apply to every shot

### Image quality
- Photorealistic, live-action; premium streaming-original visual quality
- Natural, realistic skin texture and facial detail — avoid smooth/plastic "AI face"
  rendering
- Physically plausible lighting and shadow behavior; realistic reflections
- Rich color grading with deep blacks and natural highlight roll-off (avoid
  oversaturation)
- Subtle, natural film grain rather than a fully clean/digital look
- Actively avoid: visible AI artifacts, warped hands/faces, plastic-looking skin,
  watermarks, logos, text overlays, subtitles, or UI elements appearing in-frame

### Cinematography defaults
- Widescreen cinematic aspect ratio (2.39:1) unless overridden
- Film-like 24fps motion and natural motion blur
- Lens language: describe shots in terms of real cinema lenses (e.g. 35mm, 50mm,
  85mm equivalent) to steer toward a photographic rather than video-game look
- Shallow depth of field for emotional/close-up moments where appropriate; not
  every shot needs to be shallow — use it purposefully
- Volumetric/atmospheric elements (fog, light rays, dust) where the scene calls for
  it, not as a blanket filter on every shot
- Lighting should be motivated by an actual light source in the scene (window,
  practical lamp, sky) rather than flat/ambient studio lighting

### Camera movement
- Prefer purposeful camera movement over static locked-off shots by default:
  establishing aerial, tracking, dolly in/out, slow push-in, crane reveal, shoulder
  follow, close-up emotional framing, smooth gimbal movement
- Every movement choice should serve the story beat of that shot (e.g. push-in for
  emotional emphasis, wide establishing for orientation) — don't add movement for
  its own sake if a static frame serves the moment better

### Production design
- Detailed, realistic environments and wardrobe textures appropriate to the scene's
  setting and budget level implied by the story
- Realistic environmental atmosphere (weather, smoke, dust, rain) where the scene
  calls for it
- Materials and lighting interaction should behave physically (e.g. wet surfaces
  reflect, fabric folds naturally)

### Audio
- Natural-sounding dialogue delivery
- Ambient/environmental sound appropriate to the setting
- Foley detail (footsteps, cloth movement, object handling) where relevant
- Score/music only where it serves the emotional beat, not wall-to-wall
- Note: many AI video platforms generate video and audio separately, or don't
  generate audio at all — check current platform capability before assuming audio
  direction applies; flag this to the user if the platform doesn't support it

## Explicit exclusions

Unless the user specifically asks for one of these, do not apply:
- Animation or cartoon styling
- Oversaturated/stylized color grading
- Any visible watermark, logo, text overlay, subtitle, or UI chrome

## Inheritance rule

This skill controls visual/audio production quality only. Character identity,
continuity, wardrobe changes, timeline/aging, and personality are governed by the
`character-consistency` skill (or whatever the user's project already established for
those) — do not let this skill's instructions override or restate those; just apply
the cinematic treatment on top of whatever identity/continuity decisions were already
made.

## Quality self-check before delivering a shot

Before presenting a generated shot/scene as finished, review it internally against
this checklist and revise the specific weak elements rather than regenerating from
scratch or leaving issues unaddressed:

- [ ] Facial/skin rendering looks natural, not plastic or artifact-heavy
- [ ] Lighting is motivated by a plausible source in the scene
- [ ] Color grading avoids oversaturation; blacks and highlights look natural
- [ ] Camera movement (or lack of it) serves the story beat of this shot
- [ ] Composition and framing feel intentional, not default/centered by habit
- [ ] No watermark, logo, text, subtitle, or UI element is visible in-frame
- [ ] Wardrobe/environment continuity matches what the project has already
      established (per character-consistency bible, if in use)
- [ ] Audio direction (if applicable on this platform) matches the emotional tone
      of the shot
- [ ] Overall shot reads as premium/cinematic rather than as a generic AI clip

This review happens silently — don't narrate a step-by-step scoring process to the
user for every single shot, since that adds noise without helping them. Present the
finished, reviewed shot. That said, if the user directly asks what was weak or what
you changed and why, answer honestly and specifically — the self-check is there to
improve output quality, not to hide information from the user about their own
project.

## Common failure modes to guard against

- **Applying every stylistic element to every shot regardless of story need** — e.g.
  shallow depth of field or volumetric fog on a shot that calls for a clean, deep-
  focus wide. Use these tools purposefully, not as a blanket filter.
- **Letting the cinematic treatment override established character/continuity
  decisions** — this skill never changes what a character looks like, wears, or how
  they behave; it only changes how the shot is filmed and rendered.
- **Promising technical fidelity the platform can't deliver** — if a platform
  consistently struggles with a specific element (true shallow DOF, specific aspect
  ratios, audio generation at all), say so rather than repeating the instruction and
  hoping.
- **Treating "premium/cinematic" as "more of everything"** — real cinematography uses
  restraint; not every shot needs a crane move or maximum atmospheric haze.
