---
name: cadabra-picture-maker
description: "Make any picture in Cadabra AI the right way, even when the request is vague: find out what the picture is for, offer three directions, pick the engine by the job (their real face from their photo, Hebrew or English text spelled right, a product kept exact, the cheapest engine for everything else), check the picture before showing it, and offer one next step. Use for any request for a picture, an image, a photo, a poster, an avatar, a profile picture, a greeting, a meme, art, or 'תעשו לי תמונה'."
---

# Picture maker

It runs in any chat with the Cadabra AI connector (Claude, ChatGPT, Claude Code): https://mcp.livinginmovie.com/mcp. Reading and planning are free; anything that generates is priced first and needs a Cadabra AI package.

## 1. What is it for? (one question, only if it is not clear)

The job decides everything: a profile picture, a post, a poster with words, a
greeting, a gift, a product photo, art for its own sake, the first frame of a video.
Ask that one thing if you cannot tell. Then, when the request is vague, offer three
directions in one line each (different looks, not three versions of the same one) and
let them pick.

## 2. Their real face, their real things

A picture of THEM, their child, their pet, their home or their product starts from
THEIR photo (cadabra_upload_file), passed as a reference. Never invent a stand-in for
a real person or thing they own, and never put a real person they did not provide
into a picture. For the same character again and again, save it once with
cadabra_entities and write @name in the prompt.

## 3. Pick the engine by the job (cadabra_generate_image)

- Everything else, and when in doubt: the default nano-banana, or nano-banana-2.1 with
  several references. Fast and the cheapest.
- Words inside the picture (a title, a sign, a greeting, Hebrew included): gpt-image-2
  follows an exact sentence most literally; gpt-image-2.5 sunburst is the safest on
  small dense text; grok-imagine-image-2, ideogram-4.5 (keep its Hebrew short and
  large) and nano-banana also write it. Quote the exact sentence, one line, on a flat
  surface, and forbid any other text. Words that go over a video belong in the edit,
  not baked in.
- Photographic realism: seedream-5.5.
- A face, a product or a logo that must survive an edit, or one area to change: a
  gpt-image-2.5 sunburst tier, with mask_url for the area.
- Illustration and painted art: midjourney-v8.2 (draft mode gives many quick
  sketches).
- A cut-out with a transparent background: transparent_background on the models that
  support it.
Say the price before you run it; on the models where the creator chooses the
resolution, show the prices and let them choose. 1K is enough for a phone post.

## 4. Write the picture like a photographer

Subject and what they are doing, where, the light (a named source and its direction),
the lens and the distance (close portrait, wide), the mood, the colours, and what must
NOT be in it. A short request is upgraded for free by the craft pass; leave raw_prompt
off unless they wrote the prompt themselves and want it untouched. For a known look
on a photo of a person, cadabra_portrait_looks has finished prompts.

## 5. Look before you show

Open the picture and check it against what they asked: is it the same face, the right
number of people and fingers, the product unchanged, every word spelled right letter
by letter (Hebrew is written right to left), nothing extra in the frame. If something
is wrong, say so plainly and offer the fix (continue_from on gpt-image-2.5 for a cheap
correction, or a masked edit), priced, after their yes.

## 6. One next step

Offer one: make it move (the picture as the first frame of cadabra_generate_video or a
cadabra_video_codes code), a matching set, a bigger version (cadabra_upscale_image),
or a poster or cover from it.

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
