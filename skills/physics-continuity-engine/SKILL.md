---
name: physics-continuity-engine
description: Use this skill whenever a user is generating AI video involving vehicles, buildings, physical objects, or human movement/interaction across multiple shots, and wants real-world physical logic and object continuity maintained — e.g. "keep the car the same," "don't let the building change," "make movement realistic," "fix wall clipping," vehicle chases, characters entering/exiting locations, or any multi-shot project where a vehicle, building, or physical interaction must stay identical and behave believably across cuts. Covers vehicle identity lock, transport continuity, human physics (doors, stairs, gravity, mounting vehicles), screen/travel direction continuity, object interaction, and environment/building lock. No API/physics-simulation access — works through disciplined tracking of physical facts and a pre-delivery realism checklist, the same instruction-only approach as character-consistency and cinematic-effect-engine, which it pairs with.
---

# Physics & Continuity Engine

## Golden Law (applies across the whole toolkit)

The viewer must believe a real camera, real actors, and a real film crew
created the scene — not artificial intelligence. See `REALISM-ENGINE.md` at the
repo root for the full cross-skill realism standard this skill serves —
including the Reality First rule, which this skill implements in detail below.

## Scope (read this first)

This skill enforces real-world physical logic, object identity, and continuity
for everything in a scene that *isn't* a character's face/voice/personality
(covered by `character-consistency`) or the camera/lighting/audio treatment
(covered by `cinematic-effect-engine`). This is the third leg: the physical
world itself — vehicles, buildings, objects, gravity, and how bodies interact
with the environment.

Objects, vehicles, buildings, and human movement must obey real-world physical
logic unless the screenplay explicitly defines supernatural or otherwise
non-physical rules for its world (e.g. a superhero who can fly, a ghost who
passes through walls) — in that case, follow the story's own stated rules
consistently rather than defaulting to real-world physics where the story has
deliberately overridden them.

Treat this as a disciplined tracking-and-review system, not a physics engine —
no instruction skill can force a video generation model to simulate gravity or
rigid-body collision. What this skill can do: maintain a written record of each
vehicle/building/object's locked identity (the same discipline
`character-consistency` applies to faces), catch physically implausible or
discontinuous results in a pre-delivery review, and describe the specific
physical actions (gripping a handle, sitting before driving) that make an
interaction read as real rather than pasted-together.

## Reality First

Reject any shot containing impossible physical behavior — wall clipping,
floating, teleporting, incorrect vehicle continuity, or wrong travel direction
— unless the screenplay explicitly establishes fantasy or supernatural rules
for its world. Where such rules are established, apply them consistently
rather than defaulting back to real-world physics. This is the specific rule
this skill exists to enforce; everything below is the detail behind it.

## Vehicle lock

Every vehicle that appears more than once gets a permanent identity, tracked the
same way a character's face is tracked. Define and record:

- Color
- Make and model
- Year
- Wheels
- License plate
- Damage (dents, scratches — and whether/when damage is added deliberately)
- Interior
- Headlights
- Window tint

A black SUV can never become a white SUV (or a different make/model) in the next
connected scene without a written story reason — treat an unexplained vehicle
change exactly like an unexplained face or wardrobe change in
`character-consistency`.

## Transport continuity

Trains, buses, aircraft, motorcycles, and bicycles must remain visually
identical across connected scenes — same identity-lock discipline as vehicles
above. Don't randomly swap a modern vehicle for an older-looking version (or
vice versa) between shots meant to be continuous.

## Human physics

Characters interacting with their environment must behave physically:

- Open doors before entering; close doors after exiting
- Sit down before driving; hold the steering wheel while driving
- Mount motorcycles correctly; wear helmets if the story requires them
- Walk around obstacles rather than through them
- Use stairs instead of floating or teleporting between levels
- Never walk through walls or solid objects

## Direction lock

Movement must stay consistent across connected shots:

- Screen direction (a character moving left-to-right should keep doing so
  across cuts of the same continuous action, per the 180° rule)
- Walking direction
- Vehicle direction
- Chase continuity (pursuer and pursued maintain consistent relative
  positioning and direction across cuts)

If a character is established traveling east, the next connected shot can't
suddenly show them moving west without an intentional transition (turning
around, taking a different route, a time-skip).

## Object interaction

Hands must correctly and physically contact objects — describe the actual
physical action rather than leaving it implied:
- Grip door handles; push/pull doors open
- Pick up phones naturally
- Press elevator buttons
- Hold cups and objects with a believable grip
- Turn a key before a vehicle starts

Never allow hands to pass through objects, or objects to move/activate with no
visible physical cause.

## Environment lock

Buildings and locations that recur across a project remain structurally
identical. Don't let these drift between appearances:
- House/building color
- Window positions
- Furniture layout
- Road markings
- Street signs
- Room dimensions

Track recurring locations with the same discipline as recurring vehicles — see
`references/object-continuity-log.md` for a template.

## Realism checklist (run before delivering any shot)

Before presenting a generated shot/scene as finished, verify:

- [ ] Vehicle identity unchanged from its locked record (or deliberately and
      explicably updated)
- [ ] Clothing/character continuity unchanged (cross-check with
      `character-consistency` if that skill is in use)
- [ ] Weather unchanged unless a scripted transition occurred (cross-check with
      `cinematic-effect-engine`'s weather-bible if that skill is in use)
- [ ] Character enters/exits vehicles and locations correctly (doors, stairs,
      mounting)
- [ ] No wall-clipping or floating through solid geometry
- [ ] Travel/screen direction is consistent with the previous connected shot
- [ ] Objects obey gravity (nothing floats or falls upward without a stated
      supernatural rule)
- [ ] Doors, gates, and mechanisms operate naturally (opened before passing
      through, closed after)
- [ ] Hands make correct physical contact with any object being used

If any check fails: regenerate only the faulty shot, with corrective language
pointing at exactly what broke (e.g. "vehicle was a black SUV in the previous
shot, this shot shows a white sedan — regenerate matching the locked black SUV
identity"). Preserve every other already-accepted shot rather than
regenerating the whole scene.

## Common failure modes to guard against

- **Letting a vehicle's color, model, or damage state drift between scenes**
  without a story reason — the single most common version of this problem.
- **Skipping physical entry/exit actions** — a character appearing already
  inside a car with no door-opening beat, or already at their destination with
  no travel shown, reads as a continuity break.
- **Direction flips with no transition** — a chase or journey that reverses
  direction between cuts without a reason confuses geography and breaks
  immersion.
- **Hands not physically registering with objects** — a hand near a door
  handle that isn't shown gripping/turning it, or an object that moves with no
  visible cause.
- **Environment drift** — a building's window layout, color, or room
  proportions changing between the establishing shot and a later scene set in
  the same location.
- **Forgetting the supernatural-rule exception** — if the story has
  established a character can fly or phase through walls, don't fight that
  with real-world physics; apply the story's own stated rules consistently
  instead.
