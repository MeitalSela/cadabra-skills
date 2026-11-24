---
name: cadabra-covers-thumbnails
description: "Design reel covers, YouTube thumbnails and carousel covers in Cadabra AI that get the tap: one face, one idea, zero to three words, tested at phone size, consistent across a series. Use for a cover, a thumbnail, a carousel first slide, or when a video is not getting clicks."
---

# Covers and thumbnails

It runs in any chat with the Cadabra AI connector (Claude, ChatGPT, Claude Code): https://mcp.livinginmovie.com/mcp. Reading and planning are free; anything that generates is priced first and needs a Cadabra AI package.

## 1. One idea, three seconds

A cover sells one idea in the time it takes to scroll past. Write it as a sentence
first ("she put her son inside a video game"), then choose:
- **The face:** the creator or the character, close, eyes visible, one clear
  expression. A confident closed-mouth look reads better than a shocked open mouth.
- **The object or proof:** the one thing that makes the idea specific (the result, the
  before and after, the number).
- **The words:** zero to three, huge, never over the face. Vary the idea between
  versions, not the wording.

## 2. Make it

- A frame from the video itself first (cadabra_inspect gives stills; pick the
  strongest), then cadabra_make_thumbnail, or cadabra_generate_image on a model that
  writes text (gpt-image-2 and its tiers, Grok Imagine, Ideogram 4.5, Nano Banana)
  when the words are baked in.
- When the type garbles twice, make the picture without text and put the words on in
  the edit or a cover layout (cadabra_compose).
- A series keeps one layout: the same face position, the same type, the same colour,
  only the word and the picture change.

## 3. Test before posting

- Look at it at phone-grid size (about 170 pixels wide). If the idea does not read,
  simplify.
- Look at it in black and white. If the subject does not separate from the background,
  fix the light or the colour, not the text.
- Two or three versions, different ideas, and let the creator choose.

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
