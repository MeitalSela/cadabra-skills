---
name: cadabra-edit-by-words
description: "Cut talking footage and recordings by what is said in Cadabra AI: a timed transcript with speakers, cuts decided from speech and silence, hesitations and dead air removed without losing a meant word, captions from the real words, clean audio, and a check of every cut before it is shown. Use for editing a talking video, a lesson, an interview, a podcast, a Zoom, a vlog, subtitles, an SRT, 'תמלול', 'להוריד אממ', 'כתוביות', or tightening a rambling recording."
---

# Edit by the words

It runs in any chat with the Cadabra AI connector (Claude, ChatGPT, Claude Code): https://mcp.livinginmovie.com/mcp. Reading and planning are free; anything that generates is priced first and needs a Cadabra AI package.

When the footage is mostly someone talking, the words are the timeline. Cut from the
transcript, look at frames only where it matters.

## 1. The transcript first

cadabra_transcribe (word timing, the language always stated so it cannot invent; a
long recording is heard in windows). A conversation: cadabra_identify_speakers so a cut
never lands mid-sentence on the wrong person. A script they already have:
cadabra_align_script times it to the recording so the captions are exact. Words heard
wrong: cadabra_fix_words, and cadabra_pronunciation for names.

## 2. Propose the cut, then wait

Write the plan in plain words before anything renders: what stays, what goes (the
hesitations, the false starts, the pauses over half a second), where the strongest
moment moves to the front, the length. Show it and wait for their yes.

## 3. Make the cut

- Whole cut: cadabra_assemble with tighten_speech true (hesitations and long pauses out,
  every real word kept, no slivers), studio_sound for a room or a phone recording
  (cadabra_clean_audio for a track on its own), captions from the transcript
  (cadabra_translate_captions when the viewer reads another language).
- Reels from a long recording: cadabra-recording-to-reels.
- Their own pictures over the talking: cadabra_cover_shots on the exact words.

## 4. Check every cut boundary

Look at the frames and listen around each cut: no jump in the picture, no click or pop
in the sound, no word cut in half, no caption hidden behind something. Fix what you
find and render again, at most three repairs, then tell them what is still imperfect
in one line. Show before and after, with the new length.

## 5. Captions that read

Two or three words a line, in the safe zone, the spoken word lit up, the language the
viewer reads. Subtitle files come back free with every render.

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
