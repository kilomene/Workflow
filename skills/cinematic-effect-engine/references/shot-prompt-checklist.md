# Shot Prompt Quick-Reference

Use this as a fast checklist when constructing an actual generation prompt for a
single shot, after the Core Look defaults from SKILL.md are already understood.

## Fill in per shot

- **Shot type:** (establishing / tracking / dolly in / push-in / crane / shoulder
  follow / close-up / wide / other)
- **Lens feel:** (35mm wide / 50mm natural / 85mm compressed close-up)
- **Depth of field:** (shallow / deep / racking focus)
- **Lighting source:** (window daylight / practical lamp / overcast sky / neon
  practical / firelight / other — must be a plausible in-scene source)
- **Atmosphere:** (clear / light haze / fog / dust / rain / smoke — only if the scene
  calls for it)
- **Aspect ratio:** (2.39:1 default, or note override)
- **Story purpose of this shot:** (one sentence — what should the viewer feel/learn
  from this specific shot; use this to justify the camera movement choice)

## Quick red flags to catch before finalizing a prompt

- Did I default to a crane/push-in/dolly move out of habit rather than story need?
- Did I stack multiple atmospheric effects (fog + rain + haze + volumetric light) when
  the scene only needs one?
- Did I forget to specify a lighting source, risking flat/ambient default lighting?
- Am I asking for an aspect ratio or frame rate the platform doesn't actually support?
  Check current platform docs if unsure.
