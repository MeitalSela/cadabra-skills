---
name: cadabra-video-maker
description: "Make one great video clip in Cadabra AI: pick the right video engine for the job (a real face, a long take, sound, a cheap test, an exact last frame, Hebrew speech), turn a picture into a video that moves like it was shot, test cheap before paying for the keeper, and check the clip before showing it. Use for any request to animate a picture, make a picture move, image to video, a clip, a shot, 'which video model', 'תהפכו את התמונה לסרטון', or when a clip came back stiff, morphing or boring."
---

# Video maker

It runs in any chat with the Cadabra AI connector (Claude, ChatGPT, Claude Code): https://mcp.livinginmovie.com/mcp. Reading and planning are free; anything that generates is priced first and needs a Cadabra AI package.

## 1. Pick the engine by the job

If the creator named an engine, it runs, full stop. If not, call cadabra_pick_engine
(free) with the job in one line, tell them what you picked and why in one sentence,
and offer the cheaper alternative. The decisions that matter:

- **Still finding the shot:** seedance-20-mini (the cheapest, to try ideas), or
  seedance-25 with draft:true at 480p, then cadabra_finalize_draft renders the very same
  shot at 1080p once they love it. Never explore on a 4K tier.
- **A real person who must look like themselves:** their photo on EVERY call (image_url
  or reference_image_urls), or a saved character (@name) on Seedance 2.0 or 2.5, or a
  Kling element. Keep ONE engine for the whole set: switching engines changes the face.
  FLUX-3 takes no identity at all.
- **A long unbroken take (20 to 30 seconds):** seedance-25 (lengths 5, 10, 20, 30; a
  15 second shot is made as 20 and cut). wan-3 is the cheaper long take with sound,
  any whole 2 to 30 seconds. kling-v4 also holds 30.
- **Sound in the same pass:** seedance-25, seedance-25-flash, wan-3, ltx-25, flux3,
  vidu-q4, gemini-omni-12, h3-max.
- **Characters acting and talking (English):** vidu-q4 (needs a picture) or
  gemini-omni-12. **Hebrew speech:** never from the video engine; a voice (Eleven v4)
  laid on with cadabra_lipsync.
- **The shot must end on an exact frame:** image_url plus last_image_url on seedance,
  seedance-4k, flux3, ltx-25, wan-3 or minimax-h3. A story through set moments:
  kling-v4 keyframes.
- **Several hard-cut shots in one generation:** kling-v4 with shots.
- **Change a clip that already exists:** video_url with video_mode "edit" or "extend"
  (seedance-25, gemini-omni; flux3 edit is the cheap one and keeps the length).
- **A hero shot that will be seen big:** seedance-4k, once, at the end.

## 2. The picture is the first frame, so make the picture right

- Leave room for the move: the subject not touching the edge, space in front of them
  to walk into, the area the camera will travel to already in the picture.
- The light already has a direction (a window, a lamp, the sun low on one side). Flat
  light gives a flat video.
- Hands and props in their final positions: an engine animates a mistake it is shown.
- The same aspect ratio as the video (9:16 for reels).

## 3. Write the movement, not the picture

The engine already sees the picture. Describing it again wastes the prompt and invites
it to redraw. Write what HAPPENS:
- **The camera:** the shot size, the lens (24mm wide makes space big, 50mm sees like a
  person, 85mm flatters a face and melts the background) and ONE move with a verb
  (slow push in, orbit left, crane up, handheld follow, locked off). Two moves in one
  shot read as a mistake. cadabra_camera_fx has the named moves (camera_moves) and
  effects (vfx).
- **The action on the clock:** "0:00-0:02 she turns toward the window; 0:02-0:05 she
  smiles for half a second, then looks down." Something visible every second.
- **Everything already moving at the first frame:** hair, fabric, steam, people behind
  them, traffic. A still background is what makes AI video look fake.
- **Physics in numbers, not adjectives:** "the cup tips 20 degrees", "the camera shakes
  a few centimetres", "she walks at a normal pace".
- **The ending:** the move settles and the last second holds a stable image, so the
  clip cuts cleanly.
- **The drift guard:** no music in the shot (the edit adds it), no text or logos, the
  face stays the face in the picture, exactly the number of people in the picture.

Shortcut: cadabra_video_codes. One picture plus one code (glambot, fpvdrone,
slowmotion, orbitshot, earthzoom and more) writes the whole prompt for the engine and
locks the face. Great for a first "wow".

## 4. Length and money

5 seconds for one action. Longer only when the action needs it: a longer clip costs
more and wanders more. Quote first, say the price, wait for the yes. A failed clip
refunds itself.

## 5. Check before showing

cadabra_inspect the clip for frames (start, middle, end), cadabra_qa_shot with them,
the reference photo and the shot's prompt. Look for the four classic failures: the face
drifting, hands or objects melting, the camera move never finishing, a person
appearing or vanishing. A clip that is right until a moment and wrong after it:
cadabra_retake_moment from the last good second, priced, after their yes. Wrong from
the start: change the one cause in the prompt and render once more, never the same
prompt again.

## 6. One next step

Offer one: the next shot of the same scene (same look line, same face reference), the
finished 1080p of a draft, sound effects for a silent clip (cadabra_assemble
sound_design), or several clips cut into a reel (cadabra_assemble).

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
