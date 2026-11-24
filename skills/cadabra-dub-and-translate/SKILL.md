---
name: cadabra-dub-and-translate
description: "Take one finished video to other languages and markets in Cadabra AI: dubbed in the speaker's own voice with the mouth moved to match, or subtitles translated with their timing kept, or a new voiceover in a chosen voice, plus the on-screen words and the ad copy localised. Use for 'translate my video', 'dub it to English', 'the same video in Arabic', 'subtitles in English', 'תרגום', 'דיבוב', or selling the same ad in another country."
---

# Dub and translate

It runs in any chat with the Cadabra AI connector (Claude, ChatGPT, Claude Code): https://mcp.livinginmovie.com/mcp. Reading and planning are free; anything that generates is priced first and needs a Cadabra AI package.

## 1. Which kind of translation

Ask what the viewer should get, then pick:
- **They hear it in their language, in the same voice, the lips matching:**
  cadabra_translate_video with the target languages (several at once), mode
  "precision" for a face on screen, "speed" at about half the price when the face is
  small, "audio" to redub only the sound. Say how many people speak in it. Priced per
  minute of the source and per language, quoted as an estimate until measured.
- **They read it, the original voice stays:** cadabra_translate_captions (free, keeps
  each line's timing), then the edit burns them in (caption_language in
  cadabra_assemble, with language set to what is spoken).
- **A new narrator in their language:** a voice the creator picks, the translated
  script read with cadabra_eleven_v4_speak, laid on with cadabra_assemble (voiceover_url
  and narration_script).

## 2. Translate the meaning, not the words

- The hook must still be a hook in the new language: rewrite it so it lands, keep the
  claim.
- Numbers, prices, currency, dates and units changed for the market. Names and brand
  words kept.
- Jokes, idioms and cultural references adapted, and told to the creator.
- Hebrew is written right to left; Arabic too. English titles shorter than the Hebrew
  ones usually.

## 3. Everything else on screen

The titles, the end card and the call to action in the new language (cadabra_edit_ops
title_text and end_card on the cut), the caption for the post (cadabra_social_copy),
and for an ad, every placement in the new market (cadabra_ad_studio route ad-localize).

## 4. Check

Watch the start, middle and end of every language: the mouth on the words, no line cut
off, the captions inside the frame and spelled right. A speaker who is a real person:
dubbing their voice into a language needs their consent, like any use of their voice.

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
