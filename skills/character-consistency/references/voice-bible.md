# Character Voice Bible

Governs spoken dialogue only. A character's voice is as permanent as their face —
treat it as locked in the character bible unless explicitly updated.

## Global rules

- Never replace a character's dialogue with narration or voice-over unless the
  screenplay/script explicitly marks that line `VOICE OVER (CHARACTER NAME)`
- Every spoken line comes from the character physically present in the scene —
  don't let dialogue drift to an off-screen narrator by default
- Maintain the same vocal identity (accent, pitch, age-sound, rhythm) for a
  character across every episode/scene of a project
- Don't randomly vary accent, pitch, age-sound, or speaking rhythm from one scene
  to the next — treat any of these as a deliberate bible update, not incidental
  variation
- Internal thoughts stay silent (not spoken aloud) unless the line is explicitly
  marked `VOICE OVER`

## Voice identity template

For each character, define and store this in `character-bible.md` alongside their
face/body entry:

- **Voice ID:** (unique identifier for this character's voice)
- **Age sound:** young / adult / elderly
- **Gender presentation:**
- **Accent:** (e.g. American, British, Nigerian — be specific about region if it
  matters to the story)
- **Pitch:** low / medium / high
- **Tone:** (e.g. calm, authoritative, playful, intimidating)
- **Speech rhythm:** slow / measured / fast / energetic
- **Emotional baseline:**
- **Signature speaking habits:** (verbal tics, filler phrases, pause patterns)

This folds into the same Identity Block described in SKILL.md Step 2 — don't
maintain it as a separate paragraph pasted elsewhere; it's part of the one
compiled block per character.

## Automatic voice casting procedure

Run this immediately after planning or reviewing any scene with dialogue,
without waiting for the user to ask for it:

1. Identify every speaking character in the scene
2. Load that character's locked Voice ID and full voice entry from
   `character-bible.md`
3. Write/direct every line of that character's dialogue using their established
   voice traits (accent, pitch, tone, rhythm, signature habits) — never a
   generic or unassigned voice
4. Match the delivery to the emotional performance called for by the scene — see
   `emotion-engine.md` for breathing, pauses, and intensity progression
5. If the platform supports lip-sync/facial performance sync, request it
   explicitly in the generation prompt; note to the user if the platform doesn't
   support synchronized lip movement, rather than assuming it's happening

Lip-sync and true voice-cloning fidelity depend on the underlying platform's
actual capabilities — this skill can direct *what* voice and performance should
be used, but can't guarantee frame-accurate mouth-movement sync on a platform
that doesn't support it. Check `platform-notes.md` and flag any gap to the user
rather than promising sync the platform can't deliver.

## Performance quality bar

Dialogue should sound like a professional performance, not a flat text-to-speech
reading. Depending on what the scene calls for, include:

- Natural breathing
- Emotional pauses
- Whispering when the moment calls for it
- Raised volume/shouting only when justified by the scene, not as a default
- Natural laughter
- Crying with a breaking voice (see `emotion-engine.md`'s crying progression —
  never instant full tears)
- Stuttering only when emotionally motivated, not as a verbal tic applied
  indiscriminately

Never let dialogue read as monotone or robotic — if a generated line sounds flat,
that's a self-review failure the same as a face or wardrobe mismatch.

## Dialogue formatting rule

Correct — dialogue attributed to the character on screen:
```
Zenas: "Open the gate."
```

Incorrect — narrator paraphrasing what the character said:
```
Narrator: "Zenas asked them to open the gate."
```

Default output mode is fully acted character dialogue. Narration and voice-over
are not used unless the screenplay explicitly calls for them.

## Voice-over restriction

Only use voice-over when the script marks it exactly as:
```
VOICE OVER (CHARACTER NAME)
```
Any dialogue not marked this way is performed on-screen by the character speaking
it, not narrated.

## Consistency lock

A character's voice can never change between scenes or episodes without an
explicit bible update. Maintain, specifically:

- Accent
- Pitch
- Tone
- Speech rhythm
- Pronunciation
- Vocal texture (raspy, warm, nasal, breathy, etc.)

The audience should instantly recognize who's speaking without needing to see
their face. Never regenerate or substitute a different voice for an established
character mid-project unless `character-bible.md` is explicitly updated for that
character (the same discipline as any other bible change — see SKILL.md's
aging/change rules). An unannounced voice change is a bug to catch in the
self-review pass, not a creative choice to wave through.
