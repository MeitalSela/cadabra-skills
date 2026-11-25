---
name: cadabra-cinema-craft
description: "Give a film or a shot a director's eye in Cadabra AI: the camera move, the lens and aperture, the light, the colour palette, the era and the emotion of each character, chosen on purpose from the camera and look library and held across the whole film. Use for 'make it look cinematic', 'a camera move', 'a dolly', 'a crane', 'lighting', 'a film look', 'emotion', 'שפת מצלמה', or when a film looks flat and generic."
---

# Cinema craft

It runs in any chat with the Cadabra AI connector (Claude, ChatGPT, Claude Code): https://mcp.livinginmovie.com/mcp. Reading and planning are free; anything that generates is priced first and needs a Cadabra AI package.

Flat AI video usually has no decisions in it. Cinema is decisions: where the camera
stands, what it does, what the light does to a face, what each person feels.

## 1. Decide the six things once

- **The camera body and the era:** 35mm film, 8mm home video, a phone, CCTV, a 90s
  camcorder, anamorphic cinema.
- **The lens:** 24mm wide makes a space big, 50mm sees like a person, 85mm flatters a
  face and melts the background, 135mm compresses a crowd, a macro sits on a detail.
- **The aperture:** f1.4 to f2 throws the background away, f8 keeps it readable.
- **The light:** one named source and where it falls (a window left, practicals only,
  contre-jour, a neon sign, overhead fall), and how hard or soft.
- **The palette:** a few colours with roles, one reserved for the thing the story is
  about.
- **The emotion of each person,** by name, and how it changes across the film.
These go into the film as dials (dials in cadabra_make_film: camera, era, emotion,
palette, lens, lighting, genre, tempo, cast emotions) or into every shot's look line.

## 2. The library

cadabra_camera_fx lists the options: shot types (33), camera moves (70: dolly, crash
zoom, orbit, crane, FPV, bullet time, robo arm, dolly zoom and more), looks, and
effects (114). Offer three that fit the scene, in plain words with one line each. A
shot takes one shot type, up to three stacked moves in one continuous take, one look
per kind and at most one effect; they ride the prompt and do not change the price.

## 3. Move the camera for a reason

A push in closes the distance to a feeling. A pull back reveals what they cannot see. An
orbit gives a person weight. A handheld follow says something is wrong. A locked frame
says someone is trapped or calm. Two moves in one shot read as a mistake unless they
are stacked on purpose.

## 4. The light carries the mood

Low and hard for threat, soft and wide for tenderness, a single source for a secret.
The same light words in every shot of a scene, or the cuts will not match.

## 5. Check it was heard

Look at the frames: is the lens the lens you asked for, is the light coming from where
you said, does the palette hold from shot to shot? A shot that ignored the look is
redone with the look line moved to the top of the prompt, after a new quote.

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
