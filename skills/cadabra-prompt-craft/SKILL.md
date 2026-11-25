---
name: cadabra-prompt-craft
description: "Write the words that make an image or video engine do what was meant, in Cadabra AI: the structure that each engine reads best, shot-labelled prompts, references each given a job, stable descriptions of a subject, behaviour instead of emotion words, and positive constraints. Use when a result ignores the prompt, when someone asks how to write a prompt, 'why does it look different from what I wrote', 'פרומפט', 'איך לכתוב', or before writing a multi-shot prompt by hand."
---

# Prompt craft

It runs in any chat with the Cadabra AI connector (Claude, ChatGPT, Claude Code): https://mcp.livinginmovie.com/mcp. Reading and planning are free; anything that generates is priced first and needs a Cadabra AI package.

A prompt is a direction to a camera crew who have never met you. Say what happens, in
the order it happens, and nothing the engine can see for itself.

## 1. The skeleton (video)

State the count and the frame at the top: "Three shots, 15 seconds, vertical 9:16." Then
each shot in order, and inside a shot always in this order: the camera (shot size, lens,
ONE move), then the action (what happens, on the clock), then what changes in the
space, then the sound. End with the constraints.
- Timed beats when the engine takes them: "0:00-0:03 ... 0:03-0:06 ...".
- cadabra_craft_prompt upgrades a rough draft for free; cadabra_prompter has modes for a
  screenwriter, a lyricist, an identity lock and a shot list. A slash code
  (cadabra_video_codes) writes the whole prompt from one picture.

## 2. Describe behaviour, not feelings

"Sad" gives a generic frown. "She stops with the cup halfway to her mouth, looks at the
door, and sets the cup down without a sound" gives a performance. Replace every emotion
word with what a camera would see: a hand, a glance, a pause, a posture.

## 3. A subject by two or three stable features

Pick the two or three features that identify them (a scar through the left eyebrow, a
mustard raincoat, grey curls) and use the SAME words in every shot. More features
contradict each other; fewer let them drift. A saved character does this for you
(cadabra-brand-and-cast).

## 4. Give every reference a job

An attached picture with no job leaks into everything. Name it and say what it
controls: "@image1 is the face and nothing else; @image2 is the colour palette only;
@video1 is the camera move only." Four or five references hold together; nine fight.

## 5. Positive constraints, last

"The face stays exactly as in the reference. The shot ends on a stable frame. No cuts,
no captions, no music in the shot." Say what the camera must NOT do when it matters (a
point-of-view shot: no cut, no zoom). Words like "cinematic" and "realistic" are
refused or ignored by some engines; describe the lens and the light instead.

## 6. The picture prompt

Subject doing something, where, the light (a named source and its direction), the lens
and distance, the mood and palette, and what must not be in it. Text inside a picture
quoted exactly, on a flat surface, on an engine that writes text.

## 7. One change per retry

After a miss, change the ONE thing that caused it and render once. Two misses: change
the method (split the shot, simplify the action, make the reference first).

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
