---
name: cadabra-events-and-memories
description: "Make a film that people keep, in Cadabra AI, from photos, voices and a few sentences: a birthday, a wedding, a memorial, a baby, a trip, a graduation, a holiday, a family history, with slow movement, a song, the right words on screen and careful, respectful handling of faces and loss. Use for a film for an event, a gift, a birthday film, a wedding, a memorial, a tribute, a holiday greeting, 'סרט לאירוע', 'מתנה', 'הנצחה', 'חג שמח', or photos they want to bring to life."
---

# Events and memories

It runs in any chat with the Cadabra AI connector (Claude, ChatGPT, Claude Code): https://mcp.livinginmovie.com/mcp. Reading and planning are free; anything that generates is priced first and needs a Cadabra AI package.

These films are gifts. The goal is not spectacle, it is the feeling of being seen. Care
matters more than effects.

## 1. Ask gently, once

Who it is for, the occasion, three things the person loves or is known for, one
sentence they would say to them, the tone (joyful, tender, funny, quiet), and the
length. Their photos, a voice message or a recording, in one go (cadabra_upload_file).
For a memorial, never press: take what they give and no more.

## 2. The base: their real photos

The photo-film recipe: their photos become one finished film with slow movement, music
and titles (cadabra_assemble handles photos directly, with the aspect ratio). Bring a
still to life only when they ask, with the face kept exactly as photographed; never
change a face, an age or an expression in a memorial. Restoring an old photo keeps the
person, it does not make a new one.

## 3. The words and the sound

- A short title and the person's name, large, readable (cadabra_edit_ops title_text).
- A voice: their own recording, or a narration they approve in the voice they choose
  (cadabra-voice-studio). Never clone a voice, living or gone, without the person's or
  the family's clear consent.
- A song that fits the tone (cadabra_generate_music_v6, Hebrew sung if they want it),
  with a gentle ending (music_ending natural), not a loop.

## 4. Occasion shapes

- Birthday: a life in years, one photo per year, the last frame today.
- Wedding: the story of how they met, a line from each, the first dance moment.
- Baby: the months in order, the sounds, the name card at the end.
- Memorial: a few photos, a voice, a quiet piece of music, a line they said, no effects.
- Holiday greeting: a short warm film with the family, the greeting in their words, in
  the language the receiver reads (Hebrew right to left).
- Family history: names and dates written exactly, checked against what they gave.

## 5. Check

Every name and date letter by letter, every face the right person, the length not
longer than the feeling. Watch it once through before saying it is ready, and tell them
it is theirs to share only with the people who are in it.

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
