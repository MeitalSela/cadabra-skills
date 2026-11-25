---
name: cadabra-micro-drama
description: "Write and produce vertical micro dramas and series episodes in Cadabra AI, Hebrew or English: a detonation in the first seconds, a cast that stays the same across episodes, dialogue that is spoken and lip-synced, a cliffhanger, and a series bible that learns from every note. Use for 'micro drama', 'מיקרו דרמה', a vertical series, an episode, a soap, or a drama reel."
---

# Micro drama

It runs in any chat with the Cadabra AI connector (Claude, ChatGPT, Claude Code): https://mcp.livinginmovie.com/mcp. Reading and planning are free; anything that generates is priced first and needs a Cadabra AI package.

## 1. The bible (free, once per series)

cadabra_series_guide for the season map and its prices. Then write, and keep for the
whole series:
- **The engine:** one want the lead has every episode, refused in a new way each time,
  and one person who wants the opposite and is not leaving.
- **The cast:** a name a real person would have (no fantasy-novel names), age, job, one
  odd true detail each, how they talk. Lock every face with cadabra_character_sheet
  and save it with cadabra_entities before episode one.
- **Places:** one or two, each a world sheet (cadabra_world_sheet), empty of people.
- **House rules:** start empty. Every note the creator gives becomes a fix in this
  episode AND a rule in the bible, so it never comes back.

## 2. The episode shape (vertical, 9:16)

- 0 to 1 second: the middle of a conflict, two people in frame, already loud or
  already wrong.
- Cold, short lines in close-ups. At most three lines in any 12 to 15 seconds, with
  air between them: a pause can be cut out later, never added.
- A silent stretch where a prop changes the scene (a phone, a ring, a letter, a key).
  Props must change who knows what or who can go where.
- The flip: status turns over.
- The payoff held three to five seconds on both faces, then the cliffhanger cut on the
  question, not the answer.
- Emotion builds across three lines (composed, cracking, breaking), never jumps.

Standalone reels travel further than numbered parts on social: every episode should
work for someone who never saw the last one.

## 3. Making it

- The whole episode: cadabra_make_film with style "series", length "long",
  aspect_ratio "9:16", speech "dialogue", the cast photos and cast_notes in the same
  order, and "micro drama" in the idea.
- Hebrew speech: never written for the video engine to say (it makes mouth noise).
  Each line is spoken with Eleven v4 (cadabra_eleven_v4_speak) and laid on its shot
  with cadabra_lipsync (veed-2 when the video cuts between shots, sync-3 for one
  unbroken shot). Best of all for Hebrew: the creator performs the
  lines themselves, and the voice is changed per character (cadabra_change_voice).
- Every shot carries an ACTING TASK per person (want, what they hide, what the eyes
  check) and the EYELINES (who looks at whom; nobody plays to the lens). Ban the words
  "emotional", "realistic" and "natural acting": describe the behaviour instead.

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

## 4. Cut-downs

From one episode: the full episode, a cold open that starts on the strongest line, and
a 20 to 25 second teaser (cadabra_campaign gives the hook cut, the 15 and the 30).

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
