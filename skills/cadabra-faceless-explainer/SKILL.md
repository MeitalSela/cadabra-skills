---
name: cadabra-faceless-explainer
description: "Make faceless explainer videos and channels in Cadabra AI: a narrated video in a drawn style (stickman, whiteboard, paper diorama, pastel flat, hand drawn, mannequin, editorial collage) with a script built in timed blocks, one idea per block, a voice, captions and a repeatable series format. Use for a faceless channel, an explainer, a lesson, a how-to, a stickman video, a whiteboard video, 'סרטון הסבר', or content without showing a face."
---

# Faceless explainer channel

It runs in any chat with the Cadabra AI connector (Claude, ChatGPT, Claude Code): https://mcp.livinginmovie.com/mcp. Reading and planning are free; anything that generates is priced first and needs a Cadabra AI package.

No face needed: the idea, the voice and the style carry it. The risk is five minutes of
drifting visuals, so everything is built in short timed blocks.

## 1. The topic and the promise

One topic, one promise in a sentence ("in 40 seconds you will know why your bread
collapses"). A fact-heavy topic uses only the facts the creator gave or a document they
pasted (cadabra_read_pdf); nothing invented.

## 2. The style, chosen once

cadabra_ad_studio route faceless: stickman, whiteboard, paper-diorama, pastel-flat,
hand-drawn, mannequin or editorial-collage. Show two or three and let them choose;
make the first scene and check it before the rest. The style never changes mid-video.

## 3. The script in blocks

- A block is about ten seconds: ONE idea and about 26 to 30 spoken words. The viewer
  gets one new thing every block.
- Arc: hook (the surprising claim), build, turn (the part nobody expected), payoff, one
  call to action.
- Each block opens its visual with a size: a wide, then a medium, then a close detail,
  so the picture changes with the thought.
- A through-line object that returns in every block (the same loaf, the same arrow) so
  it reads as one piece.
- Spoken language: short sentences, written for the ear (cadabra-voice-studio).

## 4. Make it

The route returns the chain of tools and the English prompts with the style locked.
Make the first block's picture, check it, then the rest in one batch. Voice with Eleven
v4 (the creator chooses it), one read of the whole script, timed to the picture
(cadabra_align_script). Never speed the audio up to fit: change the picture's length.
Captions from the script, not a transcription.

## 5. The series

A faceless channel is a repeating format: the same style, the same opening line, the
same end card, a new topic each time (cadabra-content-month). Save the style as a
persona (cadabra-brand-and-cast) so episode ten matches episode one.

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
