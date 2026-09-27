# Shot Prompt Quick-Reference

Use this as a fast checklist when constructing an actual generation prompt for a
single shot, after the Core Look defaults from SKILL.md are already understood.
For the full vocabulary behind each field below, see `shot-grammar.md` (shot
hierarchy, movement, lighting, composition, continuity) and
`camera-angle-bible.md` (angle and height systems).

## Fill in per shot

- **Shot hierarchy position:** (establishing / wide / medium / close-up / extreme
  close-up / insert / final reveal)
- **Camera angle:** (eye level / low / high / bird's-eye / drone / over-the-
  shoulder / POV / insert-macro)
- **Camera height:** (ground / knee / waist / chest / eye / overhead / sky)
- **Movement:** (dolly in / dolly out / tracking / push-in / crane up / static
  frame / shoulder follow / slow reveal pan / handheld / none)
- **Lens feel:** (35mm wide / 50mm natural / 85mm compressed close-up)
- **Depth of field:** (shallow / deep / racking focus)
- **Lighting source:** (window daylight / practical lamp / street light / neon /
  moonlight / fire / vehicle headlights / other — must be a plausible in-scene
  source)
- **Composition principle in use:** (rule of thirds / leading lines / foreground
  depth / negative space / symmetry / layered backgrounds)
- **Atmosphere:** (clear / light haze / fog / dust / rain / smoke — only if the scene
  calls for it)
- **Aspect ratio:** (2.39:1 default, or note override)
- **Story purpose of this shot:** (one sentence — what should the viewer feel/learn
  from this specific shot; use this to justify the angle, height, and movement
  choices above)
- **Continuity check (if continuing a scene):** does height, screen direction,
  lighting direction, and lens logic match the prior shot unless a perspective
  change is intentional?

## Quick red flags to catch before finalizing a prompt

- Did I default to a crane/push-in/dolly move out of habit rather than story need?
- Did I stack multiple atmospheric effects (fog + rain + haze + volumetric light) when
  the scene only needs one?
- Did I forget to specify a lighting source, risking flat/ambient default lighting?
- Am I asking for an aspect ratio or frame rate the platform doesn't actually support?
  Check current platform docs if unsure.
