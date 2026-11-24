---
name: cadabra-fix-my-film
description: "Rescue a film that came out fine but not great, or fix one that is broken, in Cadabra AI, for the least money: find what actually hurts (the opening, the pace, the ending, a face, a shot, the sound), fix it in the edit before re-shooting anything, change one exact thing without touching the rest, and retake only the moment that broke. Use for 'fix my film', 'it's not good', 'it drags', 'the face changed', 'change the title', 'make it better', 'תתקנו', 'זה לא טוב', or any finished video they are unhappy with."
---

# Fix my film

It runs in any chat with the Cadabra AI connector (Claude, ChatGPT, Claude Code): https://mcp.livinginmovie.com/mcp. Reading and planning are free; anything that generates is priced first and needs a Cadabra AI package.

A re-edit costs a few credits; a re-shoot costs many. So the order is always: diagnose
for free, fix in the edit, and re-shoot only the seconds that are truly broken.

## 1. Find what hurts (free)

- A vague note ("it's bad", "not what I wanted") never goes to a paid tool on a guess.
  Ask ONE question with two to four concrete readings from THIS film (the opening, the
  pace, the ending, a face, the sound, the look) plus "something else".
- Look at it yourself: cadabra_inspect (frames, and shots for the cut list),
  cadabra_hook_check (the first three seconds, scored), cadabra_review_film (at most
  three notes, the most damaging first), cadabra_scene_board (each scene with two moves
  to choose from).
- Tell them the one thing that matters most, in one sentence, and its fix.

## 2. Pick the smallest tool that fixes it

- **One exact thing, everything else kept** (a title's words or place, the music or
  voice level, one shot swapped, the look, a caption's spelling, the end card, a colour
  isolate, a voice effect): cadabra_edit_ops on the cut's project_id. Call it first with
  no ops (free) to read what the cut holds, so "title 2" and "shot 3" count the way the
  plan counts them. It shows a free preview.
- **Length, order, pace, captions, effects, a feeling** ("it drags before the ending",
  "hold the beat before the punchline"): cadabra_edit_film with the creator's note in
  their words, and project_id when the cut was made here. Named edits: recipe tighten,
  strong-ending, open-with-shot, on-the-beat, viral. Effects only from the Edit Library
  codes.
- **Their own pictures over the talking:** cadabra_cover_shots.
- **Two shots that do not connect:** cadabra_bridge_shot.
- **A weak opening:** open on a later, stronger moment, a one-line hook title in second
  zero, or start on the reaction (the hook check names which).
- **A shot broken from a moment** (a hand melts at 3.2 seconds, the face drifts):
  cadabra_retake_moment from the last good second, then cut it in.

## 3. Price and promise

Quote every fix, say what it changes and what it keeps, and wait for their yes. Never
re-edit, re-cut or re-shoot without a new yes, and never stack three fixes in one go
when one would show whether the problem is solved.

## 4. Check the fix

Inspect the new version at the seconds that changed and run the hook check again when
the opening moved. Show before and after in one line.

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
