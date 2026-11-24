---
name: cadabra-recording-to-reels
description: "Turn a long recording (a podcast, a Zoom class, a talk, an interview, a lesson, a vlog, a live) into the short reels worth posting, in Cadabra AI: every word timed, the strongest standalone moments found and scored, each cut into a vertical reel that opens on its hook and ends on the punchline, hesitations removed, captions in the safe zone, the speaker framed. Use for 'make reels from my podcast', 'clips from my Zoom', 'cut my talk into shorts', 'רילים מהפודקאסט', or any recording longer than a few minutes."
---

# Long recording to reels

It runs in any chat with the Cadabra AI connector (Claude, ChatGPT, Claude Code): https://mcp.livinginmovie.com/mcp. Reading and planning are free; anything that generates is priced first and needs a Cadabra AI package.

## 1. The recording

A direct link to the file (cadabra_upload_file; a YouTube page link does not work). A
very long video: send a light audio copy as audio_src for the words, and the reels are
still cut from the video. Always say the spoken language.

## 2. Find the moments

cadabra_find_moments with what the clips are for in their words (goal: "sell the
course", "grow the channel", "one strong opinion a day") and how many. The quote is the
transcription price; nothing else is paid to find them. Each moment comes back with a
score in four parts (hook, standalone, payoff, energy), a hook title and why a stranger
keeps watching. Show the moments with their scores and let them pick. A flat recording
is told it is flat: say so kindly, and suggest the one moment that works.

What makes a moment travel: it stands alone without the context before it, it opens on
a claim, a number, a question or a confession, and it ends on a line people would
quote.

## 3. Cut each reel

cadabra_cut_reel with the moment's start and end (or spans: the build, then the
punchline, skipping what lies between):
- **Open on the hook:** the strongest fact or question first, even if it comes later in
  the moment; a hook_title that the first line answers.
- **Clean:** hesitations and pauses longer than half a second removed, never a meant
  word.
- **Readable:** captions two or three words a page inside the safe zone; small for a
  calm talk, large for a shout.
- **Framed:** the face of whoever is talking.
- **Optional, each priced:** B-roll made to the words (an English prompt that shows
  what is being said, never the speaker's face), or their own avatar speaking the
  moment in their real voice when their face is small or missing (a Zoom tile).
A confirmed reel runs in the background: wait for it with its job_id and never send
the confirm twice. Several reels at once: one cadabra_mission.

## 4. Before posting

cadabra_hook_check on each reel, a cover (cadabra-covers-thumbnails), and the caption
(cadabra_social_copy) per platform.

For a whole course from a long recording instead of reels: cadabra_course.

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
