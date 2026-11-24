---
name: cadabra-viral-remake
description: "Turn a viral reel, TikTok, Short or ad someone loves into their OWN version in Cadabra AI: measure it shot by shot, read the story it sells, agree the formula with them, then make theirs on the original's rhythm with their face, topic or product, checked frame by frame. Use for 'make me one like this', 'how was this made', 'remake this', or any shared video they want to copy the success of."
---

# Viral remake

It runs in any chat with the Cadabra AI connector (Claude, ChatGPT, Claude Code): https://mcp.livinginmovie.com/mcp. Reading and planning are free; anything that generates is priced first and needs a Cadabra AI package.

You copy the FORMAT of a hit (its hook, its gag, its rhythm, its camera, its ending),
never its footage, its music, its people or its brand. The reference video is studied,
never fed into a generation.

## 1. Measure (free)

cadabra_video_xray on a direct link to the file (a page link does not work: ask them
to save the video and upload it with cadabra_upload_file). You get every cut, each
shot's length and movement, a still from inside every shot, the pace, how many cuts
land on the beat, and what the file says made it.

Then classify the music: a real added track (named, loud, cuts land on it) or the
engine's own bed (generic, low, never on the cuts). An engine bed means your remake
has no music either; an added track means the edit gets its own song.

## 2. Read the story it sells

For every shot, how it was made (phone footage, AI video, avatar, screen recording,
motion graphic, text card, a still with a zoom) and what job it does. Then:
- **The illusion in two sentences:** what the reel makes the viewer believe, and why
  people send it.
- **One line per story beat** (beats, not cuts): who wants or wins what, what is
  hidden, how it is revealed, the payoff.
- **The tell-back:** three to five lines to the creator. Wait for their yes. This is
  the most expensive mistake to skip: everything after it builds on this reading.

## 3. The formula

Numbered rules, each with its evidence (a shot number and a time, a measured number,
or the creator's own words): the hook at 0.0 seconds (already moving, the most extreme
image), the gag mechanic, the pace (average and longest shot, cuts on the beat), the
look, the ending.

Then decide what the original never says out loud, one line each: how many shots per
take, whether people in the background react, who holds the camera and why, who looks
into the lens, extras per shot, sound in the takes, where the music comes from. Wrong
answers here are what make a remake feel off even when every shot is pretty.

## 4. Their version

- Their face, product or topic in the original's structure. Invented people only:
  made with cadabra_generate_image, picked from a batch, locked with
  cadabra_character_sheet, saved with cadabra_entities.
- One EMPTY location picture per place (no hero in it), attached with its role, never
  as the first frame.
- Same number of shots, the same lengths (within a fraction of a second), the hook
  shot made first.
- The whole plan as one cadabra_mission board with every price, or shot by shot if
  they want to approve each.

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
6. **Before they post:** cadabra_hook_check (free) on the finished film, then
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

## 5. The cut

cadabra_assemble on the measured rhythm: shot lengths from the X-ray, music on the
same beat grid, enter each shot late and leave early, order the beats by escalation,
end on the biggest laugh or reveal. Then cadabra_hook_check: the remake's first three
seconds must score at least as well as the original's.

If a remade line is weak, make it bigger and clearer, never safer. Keep the wording of
approved beats exactly, and never put a rejected take back into the cut.

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
plural (בחרו, תרצו, לחצו). Prompts to engines are written in English; spoken or sung
Hebrew goes through the tools that speak it (Eleven v4, Gemini Omni, Suno), and Hebrew
text inside a picture only on the models that spell it (gpt-image-2 and up, Grok
Imagine).

**Finish here.** The deliverable is a finished file in this chat, in their gallery.
Never send them off to do steps somewhere else.

**Never.** No real person's face without their own photo and consent. No logo, brand,
music or footage that is not theirs. No other company named.
