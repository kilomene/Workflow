---
name: cinematic-effect-engine
description: Use this skill whenever a user is generating AI video shots/scenes and wants a premium, photorealistic, cinema/streaming-quality look applied automatically — e.g. "cinematic quality," "photorealistic film look," "professional camera work," camera angles/movement/composition, weather/time-of-day continuity, background music/score, or sound effects/Foley direction. Covers shot hierarchy, camera movement and angles, lighting, composition, special high-impact moves (e.g. extreme telephoto reveal), weather/atmosphere continuity, sound effects (environmental/action/Foley/spatial audio), and scene-appropriate music across any multi-shot AI video project. Governs visual and audio production quality only — not character identity/continuity/personality; pair with the character-consistency skill for those. Also use this skill's self-critique checklist as a final quality pass before delivering a scene.
---

# Premium Cinematic Effect Engine

## Golden Law (applies across the whole toolkit)

The viewer must believe a real camera, real actors, and a real film crew
created the scene — not artificial intelligence. See `REALISM-ENGINE.md` at the
repo root for the full cross-skill realism standard this skill serves,
including cinematic invisibility (avoiding visible AI artifacts) and the Final
Validation checklist that spans all three skills in this toolkit.

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

### Camera: shots, movement, angles, lighting, composition
This is the highest-detail part of the skill — full detail lives in two reference
files rather than inline here:

- `references/shot-grammar.md` — the shot hierarchy for building a scene
  (establishing → wide → medium → close-up → extreme close-up → insert → final
  reveal), the purposeful-movement vocabulary (dolly in/out, tracking, push-in,
  crane up, static frame, and more) with what each communicates emotionally,
  motivated-practical-lighting-only rules, composition principles (rule of
  thirds, leading lines, negative space, layered backgrounds), within-scene
  continuity rules (height, screen direction, lighting direction, lens), and a
  forbidden-by-default list (random zooms, whip pans, indoor drone moves, etc.)
- `references/camera-angle-bible.md` — the specific angle vocabulary (eye level,
  low, high, bird's-eye, drone, over-the-shoulder, POV, insert/macro) and the
  camera height system (ground/knee/waist/chest/eye/overhead/sky) with what each
  is used for

Read both before planning a multi-shot scene. The short version: open on
geography, not emotion; use movement and angle choices that are each earned by a
specific story reason; hold lighting and framing steady within a continuous scene
unless a perspective shift is intentional; never repeat the same framing back to
back.

### Special camera moves (reserved, not default)
`references/special-camera-moves.md` covers high-impact techniques that should
be used rarely and only when a moment specifically earns them — currently the
**extreme telephoto reveal** (starting 500m-3000m out on a 600-1200mm-equivalent
lens, slowly compressing distance onto the subject; best for hero introductions,
surveillance, or epic reveals). Never use a special move repeatedly within one
project — if it's happening every few scenes, it's no longer special.

### Weather & atmosphere continuity
`references/weather-bible.md` covers treating weather, time of day, season, and
related atmosphere (cloud density, wind, rain/fog level, ground wetness, sun
position) as locked continuity — the same discipline as camera continuity above.
Weather may only change following an explicit script transition (e.g. "two hours
later," "the storm finally stopped"); never let it drift between shots meant to
be continuous.

### Background music
`references/music-bible.md` covers matching music to a scene's setting, culture,
and emotional register (with a palette for church, royal/kingdom, action,
romance, suspense, tragedy, and victory scenes), the rule that music sits under
dialogue rather than competing with it, and using silence deliberately when
dialogue alone carries the scene.

### Production design
- Detailed, realistic environments and wardrobe textures appropriate to the scene's
  setting and budget level implied by the story
- Realistic environmental atmosphere (weather, smoke, dust, rain) where the scene
  calls for it
- Materials and lighting interaction should behave physically (e.g. wet surfaces
  reflect, fabric folds naturally)

### Audio
A premium scene runs four layers together: dialogue, Foley, environment, and
music. Full detail lives in two reference files:

- `references/sound-effects-bible.md` — environmental SFX (wind, rain, fire,
  water, city, nature), action SFX (gunshots, fights, vehicles), object Foley,
  the spatial audio rule (near/far/obstructed/open-space), and the continuity
  lock: if something is visible (rain, fire, a gunshot, a handled object), its
  sound must be present — never separate visuals from sound
- `references/music-bible.md` — the scene-based music palette, the rule that
  music never overpowers dialogue, and using silence as a deliberate tool

Note: many AI video platforms generate video and audio separately, or don't
generate audio at all — check current platform capability before assuming audio
direction applies; flag this to the user if the platform doesn't support it.

## Explicit exclusions

Unless the user specifically asks for one of these, do not apply:
- Animation or cartoon styling
- Oversaturated/stylized color grading
- Any visible watermark, logo, text overlay, subtitle, or UI chrome

## Inheritance rule

This skill controls visual/audio production quality only. Character identity,
continuity, wardrobe changes, timeline/aging, personality, and emotional
performance are governed by the `character-consistency` skill. Vehicle identity,
building/location continuity, and physical object interaction are governed by the
`physics-continuity-engine` skill. (Or, for either, whatever the user's project
already established for those, if those skills aren't installed.) Do not let this
skill's instructions override or restate those; just apply the cinematic treatment
on top of whatever identity/continuity/physics decisions were already made.

## Quality self-check before delivering a shot

Before presenting a generated shot/scene as finished, review it internally against
this checklist and revise the specific weak elements rather than regenerating from
scratch or leaving issues unaddressed:

- [ ] Facial/skin rendering looks natural, not plastic or artifact-heavy
- [ ] Lighting is motivated by a plausible source in the scene
- [ ] Color grading avoids oversaturation; blacks and highlights look natural
- [ ] Camera movement (or lack of it) serves the story beat of this shot — see
      `references/shot-grammar.md` for what each movement type communicates
- [ ] Camera angle and height are chosen for a reason, not defaulted to eye
      level/waist out of habit — see `references/camera-angle-bible.md`
- [ ] Composition and framing feel intentional (rule of thirds, leading lines,
      layered depth), not default/centered by habit
- [ ] Lighting traces back to a plausible practical source in the scene
- [ ] If this shot continues a scene, height/screen direction/lighting
      direction/lens logic match the previous shots unless a perspective change
      is intentional
- [ ] The scene as a whole doesn't repeat the same framing/angle back to back
- [ ] If a special move (e.g. extreme telephoto reveal) was used, it's earned by
      the moment and hasn't already been used elsewhere in this project
- [ ] Weather, time of day, season, and atmosphere match the scene's established
      state unless an explicit transition justifies a change — see
      `references/weather-bible.md`
- [ ] No watermark, logo, text, subtitle, or UI element is visible in-frame
- [ ] Wardrobe/environment continuity matches what the project has already
      established (per character-consistency bible, if in use)
- [ ] Audio direction (if applicable on this platform) matches the emotional tone
      of the shot; music matches setting/culture and sits under dialogue rather
      than competing with it — see `references/music-bible.md`
- [ ] Every visible sound-producing element (weather, fire, impacts, handled
      objects) has matching audio, scaled correctly for on-screen distance — see
      `references/sound-effects-bible.md`
- [ ] If audio is supported on this platform, the four layers (dialogue, Foley,
      environment, music) are present and balanced, not collapsed into one flat
      track
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
- **Opening a scene on emotion before geography** — establish the location and
  character placement before pushing into close-ups, unless the story deliberately
  withholds geography for effect.
- **Repeating the same shot framing or angle back to back** — vary position in the
  shot hierarchy even within one scene.
- **Breaking continuity without a story reason** — an unmotivated jump in camera
  height, screen direction, or lighting direction reads as an error, not a choice.
- **Using unmotivated lighting** — if a shot is bright, ask what practical source
  (window, lamp, neon, fire, headlights) is supposedly producing that light.
- **Overusing a special camera move** — the extreme telephoto reveal (or any
  future reserved move) loses its impact the moment it becomes a pattern rather
  than a once-per-project moment.
- **Letting weather drift without a scripted transition** — rain becoming sun,
  or overcast becoming golden hour, between shots meant to be continuous is a
  continuity error.
- **Scoring a scene generically instead of to its setting/culture** — a church
  scene, a suspense scene, and a victory scene call for different musical
  language; don't default to one all-purpose orchestral sound.
- **Letting music compete with dialogue** — if both are present, music sits
  underneath; if dialogue alone is carrying the scene, consider reducing or
  removing the score rather than adding to it out of habit.
- **Separating visuals from sound** — a visible storm, fire, or gunshot with no
  matching audio (or matching audio for something not on screen) is a continuity
  error, not a stylistic gap.
- **Flat, undifferentiated audio distance** — a shot with a character far from
  camera shouldn't sound as loud/detailed as a close-up; match volume and
  reverb to what the camera shows.
