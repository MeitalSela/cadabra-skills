---
name: cadabra-family-animation
description: "Make an animated film in the style of a feature-quality 3D family movie in Cadabra AI, from the family's own photos or from an idea: their child, pet or themselves drawn as a lovable animated character that stays the same in every shot, a warm story with a turn, an animated world, voices and music. Use for an animated film, a cartoon of my kid, my family as a 3D movie, a birthday or bedtime story film, a mascot film, 'סרט אנימציה', 'סרט מצויר', or any animation request."
---

# Animated family film

It runs in any chat with the Cadabra AI connector (Claude, ChatGPT, Claude Code): https://mcp.livinginmovie.com/mcp. Reading and planning are free; anything that generates is priced first and needs a Cadabra AI package.

## 1. The story first (free)

A small, warm want, real effort, a funny setback, escalating chaos, and a turn that
lands on warmth or surprise. One hero object the film keeps returning to. If it is a
gift (a birthday, a bedtime story), the child's real quirk or love is the heart of it.
cadabra_animation_craft kind "direct" gives the story craft; kind "dialogue" locks every
line before anything is drawn. Tell the creator the story in two lines and wait for
their yes.

## 2. Draw the cast once, then never redraw it

- From a real photo (their child, their dog, themselves): the photo is drawn into the
  animated character first (cadabra_generate_image with look "animation" and the photo
  as reference), they approve it, and THAT drawing becomes the character for every shot.
  A real child's photo only from their own parent.
- A full-body master on a plain grey studio background (kind "master"), then a sheet:
  turnaround and expressions (kind "sheet-b"). Fix it by hand now if anything is off:
  every later shot copies it. Save it with cadabra_entities.
- The world: every place as an empty location (kind "location"), no characters in it;
  key props on their own (kind "prop").
- One look for the whole film: feature-quality production CG, stylised proportions,
  readable silhouettes, art-directed colour, real catchlights in the eyes. Never a
  studio's name in a prompt, and never photoreal and animated mixed in one film.

## 3. The shots

- cadabra_animation_craft kind "seedance-25" writes each shot whole (named shots, at
  most 30 seconds per generation), rendered on cadabra_generate_video engine
  seedance-25, the character sheet and the location attached every time. One continuous
  take per call; the cuts come in the edit.
- Acting pushed to clear extremes that read at phone size (delight, shock, exhaustion),
  the body's pace matching the feeling.
- A painted storyboard first when they want to see it (kind "storyboard-sheet").
- Or the whole film planned for them: cadabra_make_film with style "animation" and the
  family photos as the cast.

## 4. Voices and music

Each character one voice for the whole film (cadabra-voice-studio): a child's voice is
designed from a description, never cloned from a real child. A song for the film with
cadabra_generate_music_v6 (Hebrew sung), or a gentle score.

## 5. Check and finish

Every shot checked for the character staying the same (face, colours, outfit, the
proportions of the sheet), hands and eyes right, no text in the picture. Then
cadabra_assemble with the music, a title, and the end card with the child's name, the
date or the dedication.

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
