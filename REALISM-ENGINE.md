# The Realism Engine (Golden Rule)

This is the highest-priority production law across all three skills in this
toolkit. It doesn't replace `character-consistency`, `cinematic-effect-engine`,
or `physics-continuity-engine` — it's the standard all three are already trying
to serve, stated once, in one place, so it's consistent no matter which skill
an agent loads first.

## Golden Law

**The viewer must believe a real camera, real actors, and a real film crew
created the scene — not artificial intelligence.**

Every generated scene should be indistinguishable from real live-action
filmmaking. If any visual, movement, dialogue, sound, or object feels
artificial, regenerate the specific faulty shot before final output — don't
ship it and hope it's close enough.

## Reality First (physical behavior)

Reject any shot containing impossible physical behavior — wall clipping,
floating, teleporting, incorrect vehicle continuity, wrong travel direction, or
objects passing through each other — unless the screenplay explicitly
establishes fantasy or supernatural rules for its world. Where such rules are
established, follow them consistently rather than fighting them with default
physics. Full detail: `skills/physics-continuity-engine/SKILL.md`.

## Human reality

People on screen should behave like real humans, not animated puppets:
- Natural eye movement and realistic blink intervals
- Continuous, visible breathing
- Subtle facial muscle movement, not a static mask
- Believable weight and balance while walking, sitting, standing
- Correct hand/finger interaction with objects
- A beat of realistic reaction before speaking, not instant response

Never produce robotic or mechanical movement. Full detail on physical
interaction: `skills/physics-continuity-engine/SKILL.md`. Full detail on
emotional performance: `skills/character-consistency/references/emotion-engine.md`.

## Real-world physics

Everything on screen obeys gravity and physical law unless the story says
otherwise:
- Objects have weight and move accordingly
- Water flows naturally; smoke rises correctly; fire emits light and heat
- Shadows match their light sources; reflections match their surroundings
- Vehicles accelerate and handle realistically
- No floating, no clipping through geometry

## World consistency

The world remembers itself. Maintain identical, scene to scene and cut to cut,
unless a written story reason changes one of them:
- Buildings and streets
- Vehicles
- Weather and time of day
- Clothing
- Props
- Lighting direction

Nothing changes without a story reason. This is the same discipline each
individual skill already applies to its own domain (faces, vehicles, weather) —
stated here as one unified expectation.

## Cinematic invisibility

The audience should never notice the hand of AI. Actively avoid:
- Plastic-looking skin
- Morphing or unstable faces
- Extra or malformed fingers
- Warped objects
- Random, unscripted costume changes
- Lip-sync errors or audio desynchronization
- Physically impossible camera movement

Every frame should look like it was captured by a professional film crew, not
generated.

## Emotional truth

Characters don't perform emotions for the camera — they experience them.
Allow:
- Silence and hesitation
- Visible breathing
- Imperfect, natural speech (not overly clean delivery)
- Genuine laughter
- Voice cracks
- Tears developing naturally rather than appearing instantly

Never force a dramatic reaction that the moment hasn't earned. Full detail:
`skills/character-consistency/references/emotion-engine.md`.

## Location authenticity

Every environment behaves and sounds correctly for what it is:
- Hospital → medical ambience
- Church → worship acoustics
- Court → restrained silence
- Market → layered crowd activity
- Stadium → spatial, crowd-scaled cheering
- Rain → wet surfaces with matching sound

The environment should actively support the story at all times, not sit as
generic backdrop. Full detail: `skills/cinematic-effect-engine/references/sound-effects-bible.md`.

## Final validation (run silently before delivering any scene)

- [ ] Looks like real live-action footage
- [ ] Sounds like real humans (natural, not synthesized-flat)
- [ ] Physics are believable
- [ ] Character identity is unchanged (or deliberately, explicably updated)
- [ ] Each voice belongs to its correct character
- [ ] Weather is consistent with the established scene state
- [ ] Objects (vehicles, props, locations) are consistent
- [ ] Camera behaves like a professional operator would
- [ ] Music matches the scene's setting and emotion
- [ ] No visible AI artifacts

If any item fails, regenerate only the failing shot while preserving every
other already-accepted shot's continuity — never regenerate a whole scene to
fix one broken element.

This checklist runs silently — don't narrate a step-by-step scoring process to
the user for every shot. That said, if the user directly asks what was weak or
what changed and why, answer honestly and specifically; the check exists to
improve output, not to withhold information from the user about their own
project.
