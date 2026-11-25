---
name: cadabra-virtual-influencer
description: "Create an invented character that people follow, in Cadabra AI: a face that is the same in every picture and clip, a voice, a look and a world, a set of recurring post types, and a weekly rhythm, with clear labels that it is AI. Use for a virtual influencer, an AI character, a brand mascot that posts, an AI persona, 'דמות שמפרסמת', 'משפיענית AI', or a faceless brand that wants a face."
---

# Virtual influencer

It runs in any chat with the Cadabra AI connector (Claude, ChatGPT, Claude Code): https://mcp.livinginmovie.com/mcp. Reading and planning are free; anything that generates is priced first and needs a Cadabra AI package.

A character followers recognise is built once, carefully, and then reused. Everything
that makes it feel real is consistency.

## 1. Invent the person (never a real one)

The character is INVENTED. Never a real person's face, a lookalike of a famous person,
or a child. Write who they are in six lines: name, age, what they love, how they talk,
what they want, one odd true detail. Add a world: the home, the street, the recurring
places.

## 2. The face, locked

Make a batch of portraits with cadabra_generate_image, choose one together, then build
the master and the sheet (cadabra_character_sheet: turnaround and expressions on a plain
grey). Fix by hand anything off now. Save it (cadabra_entities, and
cadabra_create_character to train it for video). Keep one engine for the set. Record
the look words once and reuse them word for word.

## 3. The voice and the look

A designed voice (cadabra_design_voice: describe the person and their situation), saved
by name. Two or three outfits and settings saved as looks, so the wardrobe has a
logic. Save the style so every picture matches (cadabra-brand-and-cast).

## 4. Four post types, no more

A beginner account needs a rhythm of recurring types, for example: a talking post
(cadabra-talking-avatar), a day-in-the-life picture set, a reaction to something
trending, a behind-the-scenes. Each one a template the creator can fill in a minute.

## 5. The honest part

Say it is AI: the platform's AI label ON, and the profile says so. No fake testimonials,
no pretending to be a real customer, no claims about a product by a character
presented as a real person. A character that sells needs a disclosure line on every
ad.

## 6. Check every post

Place the new picture beside the sheet: the same face, the same proportions, the same
colours. One that drifts is redone from the sheet, never described again in words.

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
