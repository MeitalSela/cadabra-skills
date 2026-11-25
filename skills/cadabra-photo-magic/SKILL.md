---
name: cadabra-photo-magic
description: "Turn one photo of a person, a pet or a family into the pictures people share, in Cadabra AI: ready-made viral looks (action figure, movie poster, trading card, animation still, minifigure, editorial headshot), a game-style kit from one selfie, a themed photo shoot, more angles of the same shot, and a sticker pack, with the face kept exactly theirs. Use for 'turn my photo into', 'make me an action figure', 'a poster of me', 'profile pictures', 'a gift', 'stickers', 'תמונה שלי כ', 'פוסטר', 'מדבקות', or any photo a beginner wants to make special."
---

# Viral photo looks

It runs in any chat with the Cadabra AI connector (Claude, ChatGPT, Claude Code): https://mcp.livinginmovie.com/mcp. Reading and planning are free; anything that generates is priced first and needs a Cadabra AI package.

These are the quickest, cheapest wins for a beginner, and the ones people send to
their friends. Always from THEIR photo, always with the face theirs.

## 1. The photo that works

One clear, front-facing, well-lit photo; for a full-body look, the whole person with
space around them. Not blurry, no sunglasses, no heavy filter. Several photos of the
same person from different angles make a better result. A child's or another person's
photo only from the person themselves or their parent. Ask for it once, with
cadabra_upload_file (no arguments opens the upload button).

## 2. Pick the look

- **cadabra_portrait_looks:** 44 finished looks for a photo of a person: LinkedIn and
  CEO headshots, editorial and noir, and the viral ones (action figure in its box,
  animation still, brick minifigure, trading card, movie poster). Offer three that fit
  what it is for (a profile picture, a gift, a post), with one line each.
- **cadabra_game_kit:** one selfie becomes a set of six game-style pictures.
- **cadabra_magic_shoot:** a themed set of scenes with them in it.
- **cadabra_magic_angles:** more angles of a shot they already love.
- **A sticker pack** (the sticker-pack recipe): one character, pet or the person as
  stickers on transparent backgrounds, ready for WhatsApp.
- A pet or a family: the same with every member's photo attached.

## 3. Words in the picture

A name on a trading card, a title on a poster, a greeting: only on the engines that
write text (gpt-image-2 and its tiers, Grok Imagine, Ideogram 4.5, Nano Banana), the
exact sentence quoted, on a flat surface. Hebrew is written right to left; check every
letter. Otherwise add the words in the edit.

## 4. Check before showing

Is it the same face (not a prettier stranger)? The right number of people, fingers and
pets? Any text spelled right? Never make a face look different or "better" than the
photo unless they asked. A picture where the face drifted is redone, with a new quote
and their yes.

## 5. One next step

Offer one: make it move (cadabra-video-maker), a matching set for the family, a bigger
file (cadabra_upscale_image), or a cover and caption to post it.

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
