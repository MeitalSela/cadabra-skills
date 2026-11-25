---
name: cadabra-film-director
description: "Direct a short film, a trailer, a story reel or a character piece from one idea to a finished, edited film in Cadabra AI, with a story that holds, shots written like a director's page, every shot checked against a contract before the creator sees it, and broken moments fixed from the last good second. Use when someone wants a film, a short, a scene, a trailer or a story video, or says the results are not wild enough."
---

# Film director

It runs in any chat with the Cadabra AI connector (Claude, ChatGPT, Claude Code): https://mcp.livinginmovie.com/mcp. Reading and planning are free; anything that generates is priced first and needs a Cadabra AI package.

The difference between a pretty clip and a film people send to each other is a story
that turns, a first frame that grabs, and shots that actually do what was written.
This skill gets all three, and it checks the frames before anyone pays for the next
step.

## 1. The story gate (free, before any shot)

Write the film in ONE sentence: "someone wants X, Y stands in the way, so Z." If you
cannot, there is no film yet. Then:
- **Frame one** is the most extreme, most recognisable image of the whole idea, already
  moving. Not a logo, not a landscape, not a slow build.
- **Why now?** For every beat, the viewer must have seen the reason it happens. If a
  beat needs an explanation, it is in the wrong place.
- **Escalate in steps:** each beat bigger, stranger or more personal than the last,
  two or three steps, then the turn.
- **The turn:** the last shot answers the question the first shot asked, and flips how
  we read it.
- **One wild idea per shot:** the "how did they do that" moment (a scale jump, a
  frozen moment, an object behaving like a character, a camera that travels through
  something). Logic holds the story; the wild idea rides on top.

Tell the creator the sentence and the turn in two lines, and wait for their yes. This
is the cheapest moment to make it bolder.

## 2. Who makes it

- The creator asked Cadabra to plan the whole film: cadabra_make_film with their idea in
  their own words (never your rewrite), their photos in the typed slots (cast,
  product, place, look), their engine if they named one. The preview is free; show the
  idea line, the shots and every resolution price; offer "bolder" (bolder:true, free).
- **Read the free preview's hookCheck before you show any price.** It lists what is
  wrong with the plan (OPENING IS SETUP or UNCLEAR, FIRST CUT IS LATE, REPEATED SHOT,
  PREMISE LOST, an ending that answers its question). The planner repairs a plan only
  once on its own and often does not manage it, so you finish the job: call
  cadabra_make_film again with change set to the exact notes, in the creator's words
  ("shot 2 repeats shot 1: give it a new event; the starter must visibly talk in shot
  1"), free. Up to two rounds, then show the creator the plan with what is still
  weak said in one line, never a plan you know repeats itself. Check that the idea's
  own central event is on screen in the first two shots.
- The creator has their own shots or wants to build it with you: shot by shot with
  cadabra_generate_video (or many at once with cadabra_mission and a budget), then
  cadabra_assemble.
- Recurring people or places: lock them first with cadabra_character_sheet and
  cadabra_world_sheet, save them with cadabra_entities, and attach the same sheet to
  every shot they are in.

## 3. Writing each shot like a director

For every shot, in this order (Seedance 2.5 reads a labelled structure far better than
a paragraph):
- **LOOK (locked):** the same paragraph, word for word, in every shot of the film:
  camera body and lens, depth of field, light quality, palette. One camera for the
  whole film is what makes the cuts feel like one film.
- **START STATE:** where everyone and everything is at the first frame, wardrobe and
  props included. From the second shot on this is required.
- **ACTION, timed:** the beats on the clock ("0:00-0:02 ...", "0:02-0:05 ..."), each
  with an adverb and a duration ("she laughs for half a second, then goes flat").
  Write something visible for every second; a thin prompt gets a thin shot.
- **ACTING TASK:** for each person, what they want in this shot, what they hide, and
  what their eyes check moment to moment. The drama is in the eyes, not the face.
- **EYELINES:** who looks at whom, and that nobody looks into the lens unless written.
- **CAMERA:** where it stands and why (a person standing there, at what height), and
  ONE move with a verb. A change of size is a cut, written as a cut.
- **SOUND:** the scene's own sounds, and the drift-guard music line.
- **LOCKS:** the drift-guard lines that apply, and the final image.

Longer takes beat many short pieces on engines that hold them: write a 10 to 20 second
shot with its cuts inside it rather than five 3 second clips.

## The quality loop (what makes the result jump)

1. **Write the contract before the prompt.** For every shot, the lines a viewer must
   be able to check on the frames: who is in frame and how many, where each one
   stands at frame one, what each one does in order, what is in whose hand, what the
   camera does, what is on screen at the last frame, and what must NOT appear. Pin
   every touch to its target and name the wrong one ("her hand lands on the red
   button, not the blue one").
2. **Write the prompt from the contract,** never from memory. Restate everything in
   every shot: wardrobe, props, wounds, who is where. A prompt that says "same as
   before" loses it.
3. **Render one shot first,** the hardest one (the hook, the face, the product, the
   stunt). If it holds, the rest go out together; if it fails, only one shot was
   spent learning.
4. **Check it blind.** cadabra_inspect the clip for frames (start, middle, end), then
   cadabra_qa_shot with those frames, the reference photo, and the contract lines as
   shot_prompt. Then look yourself, line by line: PASS or FAIL, with the frame time.
   Judge the frames, not your prompt: a wrong prompt always passes a check by the
   person who wrote it.
5. **Fix the smallest thing.** A shot right up to a moment and wrong after it:
   cadabra_retake_moment from the last good second, with the one fix in what_changes.
   Wrong from frame one: rewrite the one cause (the contract line that failed) and
   render once. Never re-roll the same prompt unchanged. Two failed fixes: change the
   method (split the shot, simplify the action, make the reference picture first).
   Every fix is a new quote and a new yes.
6. **Between the shots.** A film of three shots or more: cadabra_inspect include
   ["continuity"] (free) on the board, on the shots and on the finished film, with the
   film's facts. The worst faults live between two good shots.
7. **Before they post:** cadabra_hook_check (free) on the finished film, then
   cadabra_review_film (free). Offer the one fix that matters, with its price.

## The drift guard (what engines add when nobody forbids it)

Put the lines that apply into the shot's own constraints, every shot, in these words:
- Music: "No music, no score, no soundtrack in this shot; only the sounds of the scene."
  Music comes from the edit.
- Camera: "One camera move only, [the move]; no zoom, no push-in, no reframing
  otherwise." Or for a locked shot: "The camera does not move at all."
- Acting: "Restrained, true-to-life acting; no wide eyes, no gasping, no looking into
  the lens unless written."
- Text: "No captions, no subtitles, no letters, no logos, no watermark." Titles come
  from the edit.
- People: "Exactly [N] people in frame." Extras are written with what they do.
- Faces and skin: "The face stays the face in the reference; natural skin texture."
- Objects: "Props obey gravity; the [product] keeps its exact shape, label and colour."
- Time: "Everything is already in motion at the first frame."

## 4. The edit

cadabra_assemble (or the film's own edit) with a brief in the creator's words: where
the title lands, what the ending holds on, the tempo they chose. Pass target_seconds
when they named a length, music_ending "natural" when there is a song, end_card on any
ad. Effects come from the Edit Library codes (cadabra_edit_library), never promised in
prose.

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
