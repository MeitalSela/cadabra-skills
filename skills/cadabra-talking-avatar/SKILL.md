---
name: cadabra-talking-avatar
description: "Make a talking-avatar video in Cadabra AI that people watch to the end: the creator's own face (a photo or a trained twin) speaking their script in their own or a chosen voice, Hebrew or English, the reading heard and approved before anything is filmed, gestures and looks that change, and the talking covered with proof on screen. Use for a talking head, a presenter, an avatar video, 'my avatar says', a spokesperson, an explainer, a lesson, a UGC testimonial by an avatar, or 'אווטאר שמדבר'."
---

# Talking avatar

It runs in any chat with the Cadabra AI connector (Claude, ChatGPT, Claude Code): https://mcp.livinginmovie.com/mcp. Reading and planning are free; anything that generates is priced first and needs a Cadabra AI package.

A talking head is the easiest video to make and the easiest to scroll past. What makes
people stay is a first sentence that grabs, a voice that sounds alive, and something to
LOOK at while the avatar talks.

## 1. Whose face, with whose consent

- Their own saved avatar: cadabra_my_avatars, and use its id. Never pick a different
  avatar of theirs than the one they named.
- A new one from a photo: cadabra_generate_avatar (a clear, front-facing face, good
  light, the expression they want to keep) or a trained twin with cadabra_create_avatar.
  A real person's face only with that person's own photo and consent
  (cadabra_avatar_consent).
- Other outfits and rooms for the same face: cadabra_avatar_looks / cadabra_avatar_look.

## 2. The script first (free)

- **The first sentence is the hook:** a surprising fact, a mistake people make, a
  promise ("3 things nobody tells you about..."), said in the first two seconds. Never
  "hi, my name is".
- **Spoken, not written:** short sentences, one idea each, the way they talk.
  cadabra_proofread_script (free) catches what reads badly aloud; cadabra_avatar_formats
  has proven shapes (myth or fact, stop doing this, old way vs new way, answering a
  comment).
- **The length people finish:** 20 to 45 seconds for a reel.
- **Their own words are spoken exactly.** Hebrew addresses the audience in the plural.

## 3. The voice, heard before the face

- The voice is the creator's choice: their own clone (cadabra_attach_voice once), a
  saved voice (cadabra_my_voices) or one from the library (cadabra_list_voices). Never
  pick it for them.
- Offer Eleven v4 first. Direct the read with tags inside the text ([excited],
  [whispers], [laughs], [pause], a word in CAPITALS for stress); cadabra_voice_tags
  (free) marks up a flat line. Hebrew names and brand words that come out wrong:
  cadabra_pronunciation.
- **listen_first:** make only the reading, play it to them, and wait for their yes.
  The reading costs almost nothing; a film of a bad reading costs the whole film. Never
  film before they heard it.

## 4. The face that moves

- gestures (or a motion_prompt: "leans in, counts three points on her fingers") and,
  for a reel, energetic: each sentence its own take with its own move. Keep
  expressiveness at its default unless they ask: it holds the face closest to the photo.
- Two or more looks: the face returns in a new outfit or room at each return to camera.
- Engines: the default avatar engine for their shelf; HeyGen Avatar 6 or Kling Avatar
  only when they ask which exist or name one, with its price.

## 5. Something to look at

A face alone for 40 seconds loses people. Choose with them:
- **cadabra_avatar_film** (one idea, script or document): the avatar in a corner window
  over shots filmed for the exact words, number cards, music and captions. A free
  storyboard first, changed as often as they like, then one price.
- **talking_only with reel_style:** the designed reel, the key word of each sentence in
  the accent colour, some sentences jumping to full screen, their own 3 second clip as
  the hook.
- **Their own proof over the talking:** cadabra_cover_shots lays their screenshots,
  results or product shots on the exact words ("when I say sourdough").
- Several avatars in one film (up to four), each with its own voice: cast and lines.

## 6. Check before showing

Watch the start, middle and end (cadabra_inspect): the mouth on the words, the face
the same as the photo, no frozen stretch, the hands natural, the captions spelled
right. cadabra_hook_check on the first three seconds before they post.

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
