---
name: cadabra-family-animation
description: "Make an animated film in the style of a feature-quality 3D family movie in Cadabra AI, from the family's own photos or from an idea: their child, pet or themselves drawn as a lovable animated character that stays the same in every shot, a warm story with a turn, an animated world, voices and music. Use for an animated film, a cartoon of my kid, my family as a 3D movie, a birthday or bedtime story film, a mascot film, 'סרט אנימציה', 'סרט מצויר', or any animation request."
---

# Animated family film

It runs in any chat with the Cadabra AI connector (Claude, ChatGPT, Claude Code): https://mcp.livinginmovie.com/mcp. Reading and planning are free; anything that generates is priced first and needs a Cadabra AI package.

## 1. The story first (free)

A small, warm want, real effort, a funny setback, escalating chaos, and a turn that
lands on warmth or surprise. One hero object the film keeps returning to. If it is a
gift (a birthday, a bedtime story), the child's real quirk or love is the heart of it.
cadabra_animation_craft kind "direct" gives the story craft; kind "dialogue" locks every
line before anything is drawn. Tell the creator the story in two lines and wait for
their yes.

## 2. Draw the cast once, then never redraw it

- From a real photo (their child, their dog, themselves): the photo is drawn into the
  animated character first (cadabra_generate_image with look "animation" and the photo
  as reference), they approve it, and THAT drawing becomes the character for every shot.
  A real child's photo only from their own parent.
- A full-body master on a plain grey studio background (kind "master"), then a sheet:
  turnaround and expressions (kind "sheet-b"). Fix it by hand now if anything is off:
  every later shot copies it. Save it with cadabra_entities.
- The world: every place as an empty location (kind "location"), no characters in it;
  key props on their own (kind "prop").
- One look for the whole film: feature-quality production CG, stylised proportions,
  readable silhouettes, art-directed colour, real catchlights in the eyes. Never a
  studio's name in a prompt, and never photoreal and animated mixed in one film.

## 3. The shots

- cadabra_animation_craft kind "seedance-25" writes each shot whole (named shots, at
  most 30 seconds per generation), rendered on cadabra_generate_video engine
  seedance-25, the character sheet and the location attached every time. One continuous
  take per call; the cuts come in the edit.
- Acting pushed to clear extremes that read at phone size (delight, shock, exhaustion),
  the body's pace matching the feeling.
- A painted storyboard first when they want to see it (kind "storyboard-sheet").
- Or the whole film planned for them: cadabra_make_film with style "animation" and the
  family photos as the cast.

## 4. Voices and music

Each character one voice for the whole film (cadabra-voice-studio): a child's voice is
designed from a description, never cloned from a real child. A song for the film with
cadabra_generate_music_v6 (Hebrew sung), or a gentle score.

## 5. Check and finish

Every shot checked for the character staying the same (face, colours, outfit, the
proportions of the sheet), hands and eyes right, no text in the picture. Then
cadabra_assemble with the music, a title, and the end card with the child's name, the
date or the dedication.

## The film spine (any film of three shots or more)

Each stage is shown, approved and checked before the next one is paid for. A mistake
costs one picture on the board, a whole take after it, and a re-edit at the end, so
everything is caught as early as it can be seen.

1. **The facts page (free).** Before the shot list, write what must hold, one line each:
   - every key prop with its PARTS ("the rod: four brass gauges, a lantern, a red grip"),
     and every state it goes through, with the shot it changes in;
   - each character's outfit, what they hold and in which hand;
   - the clock of the film: the sky, sun or moon, window and lamp of every shot, only
     moving forward;
   - what has happened and stays happened ("from shot 10 the sun is UP").
   These lines go into every prompt they touch and into every check below.
2. **The timed shot list (free).** Per shot: seconds, size, angle, ONE camera move and
   why, the action and how it ENDS, the sound heard. Then read it as a rhythm: no three
   shots in a row with the same size, angle and length; the camera moves at least where
   the feeling changes; the joke or the shock is short, the awe is long. THE MOMENT the
   story is about (the sun being caught, the box opening, the face that understands) is
   its own shot, seen happening, never only its before and after.
3. **The sheets.** One per character (cadabra_character_sheet, or the kept drawing), one
   per key prop with its parts (cadabra_animation_craft kind "prop"), and one per place
   FOR EACH light it appears in (cadabra_world_sheet: the same place at night and at
   dawn are two sheets, the second made from the first as its reference). Save them with
   cadabra_entities, so @name brings back the same one.
4. **The board.** One opening frame per shot, every sheet that shot shows attached as a
   reference (a prop that is only described comes back as a different prop). A shot that
   must land somewhere also gets its END frame, and the next shot opens from a frame
   that agrees with it.
5. **The board check, before one second is animated (free).** cadabra_inspect include
   ["continuity"], url the first panel, next_urls the rest in order, facts the facts
   page. Fix every jump on the still. This is the stage others skip.
6. **The proof.** The hardest shot first, at the cheapest tier (seedance-20-mini, or
   seedance-25 with draft:true), from its board frame. Only when it holds do the rest go
   out: cadabra_mission with one item per shot, each with ITS OWN length, image_url its
   board frame, last_image_url its end frame on an engine that takes one, and the
   creator's budget_credits as a wall.
7. **Each shot checked,** then **all of them together:** cadabra_qa_shot per shot, then
   cadabra_inspect ["continuity"] on the clips in order, before any edit is paid for.
8. **Sound is half the film.** Music written to the film's own curve, the place's own air
   under every scene, and a sound on every touch, step and turn of the story: named per
   shot in the list, placed in the edit (sound_design, or sfx_add and ambience in
   cadabra_edit_ops). A silence before the big moment is a choice, so make it.
9. **The edit** once, in their order, with the rhythm from stage 2.
10. **The last look (free).** cadabra_inspect ["continuity"] on the finished film with the
    same facts, then cadabra_review_film. Say what was found, shot by shot, with the
    cheapest fix first. Nothing found is said as "nothing found in the pictures", with
    the line that stills cannot judge motion or sound.
11. **The receipt.** What each stage really charged (sheets, board, proof, shots, sound,
    edit), as it was quoted and approved. Never a guess before, always the facts after.

Animation adds three lines to the facts page: the material (clay, felt, painted CG) and
how its surface shows it (fingerprints, stitches, brush), the frame feel (on twos for
stop motion, smooth for CG), and the character's proportions in heads, so a close-up and
a wide are the same puppet.

## The Cadabra house rules (every skill)

**Money.** Every paid Cadabra tool answers first with a quote. Show the creator that
exact price and wait for a clear yes before calling it again with confirm:true. Never
confirm on your own, never re-send a job that already went out, never retry a failed
job without a new yes. A failed generation refunds itself; say so in one line.

**Cheapest first, finest last.** Prove an idea at the cheapest tier the tool offers
(Seedance 2.5 at 480p, Seedance 2.0 mini, a 1K still), show it, and only then offer the
finish (cadabra_finalize_draft, a higher resolution, an upscale). Words like "cinematic",
"final" or "professional" are a creative brief, never permission to raise the
resolution. When a tool asks the creator to choose the resolution, show every price
and let them choose.

**Their words win.** An engine, a length, a look, a script or a shot the creator named
is used exactly. Their own script goes in with their_script:true and is never
rewritten. Ask one question at a time, never a menu, and collect their files in one
go with cadabra_upload_file (no arguments opens the upload button).

**Hebrew.** Answer in the creator's language. In Hebrew address them in the inclusive
plural (בחרו, תרצו, לחצו). Prompts to engines are written in English. A video engine
never speaks Hebrew (it makes mouth noise): spoken Hebrew is a voice (Eleven v4) laid on
the shot with cadabra_lipsync, sung Hebrew comes from Suno. Several picture engines
write Hebrew text (gpt-image-2 and its 2.5 and 2.6 tiers, Grok Imagine, Ideogram 4.5,
Nano Banana): quote the exact sentence, one line, right to left, on a flat surface,
and no other text.

**Finish here.** The deliverable is a finished file in this chat, in their gallery.
Never send them off to do steps somewhere else.

**Never.** No real person's face without their own photo and consent. No logo, brand,
music or footage that is not theirs. No other company named.
