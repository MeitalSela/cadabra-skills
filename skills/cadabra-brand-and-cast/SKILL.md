---
name: cadabra-brand-and-cast
description: "Make everything a creator or business produces in Cadabra AI look like it came from one source: a saved brand (name, colours, logo and one look image that locks the style), characters and products saved once and called by @name, a moodboard whose style transfers to every engine, and a specialist persona for a winning style. Use for a brand, a logo, 'keep the same look', 'the same character every time', 'my brand colours', 'consistent', 'מותג', 'אותה דמות', or when every image comes out different."
---

# Brand and cast consistency

It runs in any chat with the Cadabra AI connector (Claude, ChatGPT, Claude Code): https://mcp.livinginmovie.com/mcp. Reading and planning are free; anything that generates is priced first and needs a Cadabra AI package.

Words drift: two people read "warm and cinematic" differently, and a model reads it
differently on two different days. A picture, a saved identity and a saved style do not
drift. Set them once, then reuse them everywhere.

## 1. The brand, saved once

cadabra_brand_kit (read it first, before anything for a brand they worked on before):
- Name, colours as hex, the logo (their file, never redrawn by the model: the logo
  goes in by reference or is added in the edit).
- **The look image:** one picture that IS the style (the grade, the light, the texture,
  the treatment). Save the image they loved most with look_image_url, then pass it as a
  reference on every later picture and shot, and the tenth matches the first.
- A style note in words, only as a backup to the image.

## 2. People, products and places saved as identities

- A person, pet, product or place: cadabra_entities saves it once (a Cadabra ID); after
  that @name in any prompt brings back the same one, pictures attached by itself.
- A character for video: cadabra_character_sheet (turnaround and expressions) or a
  photoreal sheet, then cadabra_create_character to train it for Seedance @name or a
  Kling element. A real person only from their own photo and consent.
- Keep ONE engine per set: switching engines changes the face even with the same
  reference.

## 3. Style from pictures they love

cadabra_moodboard extracts a reusable style (palette, light, lens, mood, never the
subject) from reference pictures into a style_code that seven engines read by
themselves. Use it for a campaign look, a series, a season.

## 4. A winning style saved as a specialist

cadabra_personas saves the engine, the aspect ratio and the prompt vocabulary of a film
that worked, and applies them to the next idea with persona_id. The second film in a
series should start from the first one's persona.

## 5. Check the whole set together

Lay the last five results side by side: the same face, the same colours, the same
light, the same end. One that does not belong is redone from the look image, not
described again in words. Say so in one line, with its price, and wait for their yes.

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
