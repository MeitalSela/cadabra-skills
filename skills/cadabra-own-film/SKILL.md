---
name: cadabra-own-film
description: "Build a film with a creator who has their own script, shots or way of working, shot by shot in Cadabra AI: their words kept exactly, one look and one cast held across every shot, each shot checked before the next one is built on it, a budget that is never crossed, and one edit at the end. Use when someone writes their own shots, says 'I want to build it myself', 'my script', 'shot by shot', 'שוט אחרי שוט', brings a storyboard, or wants to approve every shot."
---

# Your own film, shot by shot

It runs in any chat with the Cadabra AI connector (Claude, ChatGPT, Claude Code): https://mcp.livinginmovie.com/mcp. Reading and planning are free; anything that generates is priced first and needs a Cadabra AI package.

The creator is the director. Your job is to make every shot they describe land exactly,
keep the film looking like one film, and never let a mistake in shot 2 get copied into
shots 3 to 10.

## 1. Before shot one (free)

Ask once, in one message:
- Their script or shot list, as they wrote it (it is never rewritten: raw_prompt:true
  on their own prompts).
- Their engine, if they have one (it runs for every shot), and their budget in credits,
  if they have one.
- Their photos: the people, the place, the product (cadabra_upload_file).
Then lock what repeats, so it holds in every shot:
- **The cast:** cadabra_character_sheet per person, saved with cadabra_entities, the
  sheet attached to every shot they are in.
- **The place:** cadabra_world_sheet, empty of people.
- **The look line:** one sentence of camera, lens, light and palette, written into
  every shot word for word. If they wrote one, theirs.
Keep one engine for the whole film: switching engines changes the faces.

## 2. One shot at a time, or all at once

- **Approve each shot:** cadabra_generate_video per shot, quote, yes, make, show, next.
- **Send it all with a budget:** cadabra_mission, every shot one item on their engine,
  budget_credits set, the edit as the last item. The free board shows every prompt and
  price; a board over the budget is re-planned until it fits. At most 12 shots.
- Cheap first when the shot is not decided: seedance-20-mini, or seedance-25 with
  draft:true and cadabra_finalize_draft for the keeper.

## 3. Carry everything forward

From the second shot on, every prompt restates the START STATE: what each person wears,
holds and where they stand at the first frame, the props, the light, the time of day.
Write it again in full; "same as before" is forgotten by the engine. A shot that must
continue from the last one: the previous shot's last frame as this shot's first frame
(cadabra_inspect gives the frame), or last_image_url when it must land somewhere.

## 4. Check each shot before building on it

cadabra_inspect the shot (start, middle, end) and cadabra_qa_shot with the frames, the
cast sheet and the shot's prompt. Look for the face changing, the outfit or prop
changing, a person appearing or vanishing, the camera move never finishing. Show the
creator what you found in one line. Wrong from a moment: cadabra_retake_moment from the
last good second. Wrong from the start: change the one cause and render once, after
their yes. Never move on with a broken shot: everything after it inherits the mistake.

## 5. The edit, once, at the end

After the last shot, ask whether they want it cut. cadabra_assemble with every shot in
THEIR order (may_reorder stays off), a brief in their words, target_seconds if they
named a length, their music or a song (cadabra_generate_music_v6), sound_design for
silent shots, and end_card on an ad. Then cadabra_review_film and cadabra_hook_check,
free, before they post.

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

On a creator's own film the spine never rewrites them: their shots, words and order stay
exactly theirs. The facts page is read back from THEIR script, and a jump is told to
them in one line for them to decide.

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
