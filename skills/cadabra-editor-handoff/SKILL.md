---
name: cadabra-editor-handoff
description: "Move work between Cadabra AI and the editing software a professional already uses: export the cut as a real sequence for Premiere or Final Cut, edit the open After Effects composition by sentence through the Director panel, and pull layers, depth and clean cut-outs out of pictures and clips. Use for Premiere, Final Cut, DaVinci, After Effects, 'export my timeline', 'XML', 'layers', 'a cut-out', 'a green screen', 'הייצוא לעורך', or a pro who wants to finish in their own tools."
---

# Hand off to your editor

It runs in any chat with the Cadabra AI connector (Claude, ChatGPT, Claude Code): https://mcp.livinginmovie.com/mcp. Reading and planning are free; anything that generates is priced first and needs a Cadabra AI package.

Many professionals want Cadabra to make the material and their own editor to finish.
Make that smooth.

## 1. A cut into a real sequence

cadabra_export_xml hands a cut made here to Premiere or Final Cut as a real sequence,
with the clips on the timeline, so nothing has to be rebuilt by hand. Tell them what
travels (the cuts and their timing) and what does not (an effect that exists only in
Cadabra's editor), before they export. Keep their project_id so a later fix can be
exported again.

## 2. After Effects, by sentence

The Cadabra Director panel (cadabra_director) edits the open composition from a
sentence through the connector. Use it for a layout change, a text change or a timing
change they can describe, and keep each request to one change they can verify.

## 3. Material out of pictures and clips

- **Cut-outs and green screen:** cadabra_remove_video_background for a clip,
  transparent_background on the picture engines that return a real alpha, and
  cadabra_split_layers to split a picture into layers they can animate.
- **Depth:** cadabra_depth_map makes a per-pixel depth map for fake depth of field, a
  parallax move on a flat image, or a mask that knows what is in front.
- **Sound stems:** cadabra_separate_audio splits voice and music; cadabra_trim_audio cuts
  a bed to length.
- **Higher quality for the finish:** cadabra_upscale_video and cadabra_upscale_image,
  once, on the final choice only.
- **A real 3D move:** cadabra_blender plans an exact camera path first, free, then the
  shot is rendered along it.

## 4. Formats they need

Say the frame size, the frame rate and the codec in plain words and check them against
what their editor wants before they import. Deliver the highest resolution that was
quoted and approved, never an upscale pretending to be a render.

## 5. Check the round trip

Ask them to open it in their editor and say what is missing. Fix the cause on the
Cadabra side, and keep a note of what their editor needs next time.

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
