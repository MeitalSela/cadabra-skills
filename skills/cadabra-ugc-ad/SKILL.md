---
name: cadabra-ugc-ad
description: "Make ads that sell in Cadabra AI: UGC testimonials, how-tos, unboxings, try-ons, faceless explainers, product hero shots, hook tests and ads rebuilt from one they admire, with the real product locked in every shot and phone-footage realism that reads as real. Use for any ad, UGC, testimonial, product video, Meta or TikTok ad, or 'an ad for my business'."
---

# UGC and performance ads

It runs in any chat with the Cadabra AI connector (Claude, ChatGPT, Claude Code): https://mcp.livinginmovie.com/mcp. Reading and planning are free; anything that generates is priced first and needs a Cadabra AI package.

## 1. Find the angle (free)

No idea yet: cadabra_ad_ideas for three. Then cadabra_ad_studio with the route that
fits (ugc-review, ugc-tutorial, unboxing, try-on, faceless, hero-shot,
headline-multiplier, hook-multiplier, recreate, customer-voice, ad-strategist,
ad-resize, ad-localize). It returns the chain of tools and the prompts with the
product and face locks already written in.

The best ads open on the viewer's problem or desire, not the product: one insight in
one line, then the product as the turn, then one clear claim, then the call to action.

## 2. The product never changes

The creator's real product photo goes in every shot (product_image_url, plus up to
three more angles in product_image_urls). Write its shape, label and colour into the
locks. A generated stand-in product is worse than asking for a photo.

## 3. Phone footage that reads as real

"Shot on a phone" alone does nothing. Write the causes:
- **Optics:** wide phone lens, deep focus, the background as sharp as the face.
- **Processing:** flat phone HDR, lifted shadows, slightly over-sharpened.
- **Light:** a named real source (a window on the left, the fridge light, a ring
  light), ideally two sources of different colour.
- **Imperfection:** a tilt, a mid-blink, a real cluttered room, a hand that covers the
  lens for a moment.
- **Who holds it:** to camera (selfie) or someone else filming.
Repeat the same look line, word for word, in every shot; written once at the top it
drifts by the fourth shot.

## 4. Hooks

Offer two or three opening hooks, each a different mechanism (a question, a bold
claim, a visual pattern-break, a POV line, a mistake people will want to correct).
cadabra_ad_studio route hook-multiplier makes several openings on one body. Test them,
do not argue about them.

## The quality loop (what makes the result jump)

1. **Write the contract before the prompt.** For every shot, the lines a viewer must
   be able to check on the frames: who is in frame and how many, where each one
   stands at frame one, what each one does in order, what is in whose hand, what the
   camera does, what is on screen at the last frame, and what must NOT appear. Pin
   every touch to its target and name the wrong one ("her hand lands on the red
   button, not the blue one").
2. **Write the prompt from the contract,** never from memory. Restate everything in
   every shot: wardrobe, props, wounds, who is where. A prompt that says "same as
   before" loses it.
3. **Render one shot first,** the hardest one (the hook, the face, the product, the
   stunt). If it holds, the rest go out together; if it fails, only one shot was
   spent learning.
4. **Check it blind.** cadabra_inspect the clip for frames (start, middle, end), then
   cadabra_qa_shot with those frames, the reference photo, and the contract lines as
   shot_prompt. Then look yourself, line by line: PASS or FAIL, with the frame time.
   Judge the frames, not your prompt: a wrong prompt always passes a check by the
   person who wrote it.
5. **Fix the smallest thing.** A shot right up to a moment and wrong after it:
   cadabra_retake_moment from the last good second, with the one fix in what_changes.
   Wrong from frame one: rewrite the one cause (the contract line that failed) and
   render once. Never re-roll the same prompt unchanged. Two failed fixes: change the
   method (split the shot, simplify the action, make the reference picture first).
   Every fix is a new quote and a new yes.
6. **Between the shots.** A film of three shots or more: cadabra_inspect include
   ["continuity"] (free) on the board, on the shots and on the finished film, with the
   film's facts. The worst faults live between two good shots.
7. **Before they post:** cadabra_hook_check (free) on the finished film, then
   cadabra_review_film (free). Offer the one fix that matters, with its price.

## The drift guard (what engines add when nobody forbids it)

Put the lines that apply into the shot's own constraints, every shot, in these words:
- Music: "No music, no score, no soundtrack in this shot; only the sounds of the scene."
  Music comes from the edit.
- Camera: "One camera move only, [the move]; no zoom, no push-in, no reframing
  otherwise." Or for a locked shot: "The camera does not move at all."
- Acting: "Restrained, true-to-life acting; no wide eyes, no gasping, no looking into
  the lens unless written."
- Text: "No captions, no subtitles, no letters, no logos, no watermark." Titles come
  from the edit.
- People: "Exactly [N] people in frame." Extras are written with what they do.
- Faces and skin: "The face stays the face in the reference; natural skin texture."
- Objects: "Props obey gravity; the [product] keeps its exact shape, label and colour."
- Time: "Everything is already in motion at the first frame."

## 5. Finish

Every ad ends on an end_card (headline and the call to action) in cadabra_assemble.
cadabra_campaign makes the 6 second hook cut, the 15 and the 30 from the finished ad;
route ad-resize makes every placement. Shot prompts end with "no captions, no
subtitles, no extra text": the edit writes the words, so they stay correct.

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
