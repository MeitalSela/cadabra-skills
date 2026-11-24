---
name: cadabra-campaign-launch
description: "Turn one finished film into a full launch in Cadabra AI: the hook cut, the 15 and the 30, alternative openings to test, every placement size, a cover per platform, the caption and hashtags per platform, and a posting plan, with nothing new generated unless they ask. Use for 'launch this', 'make versions for every platform', 'a campaign from this video', 'social launch', 'קמפיין', 'השקה', or when a film is finished and has to go out."
---

# Campaign and launch

It runs in any chat with the Cadabra AI connector (Claude, ChatGPT, Claude Code): https://mcp.livinginmovie.com/mcp. Reading and planning are free; anything that generates is priced first and needs a Cadabra AI package.

A finished film is half the work. A launch is the package that makes it reach people:
the right length and shape for every feed, openings to test, covers and copy.

## 1. Know the goal (one question)

Views, followers, leads or sales, and where they post (Instagram, TikTok, YouTube,
Facebook, LinkedIn). The goal decides the call to action and the first second.

## 2. The cuts (from the same film, nothing new generated)

- cadabra_campaign: a 6 second hook, a 15 second reel cut, a 30 second story cut and two
  alternative openings (the strongest frame first, the closest face first). Use only to
  pick a subset.
- More openings to test on the same body: the hook-variants recipe or cadabra_ad_studio
  route hook-multiplier. Score each opening with cadabra_hook_check (free) and lead
  with the best.
- Every placement size for an ad (feed, stories, in-stream): cadabra_ad_studio route
  ad-resize.
- An ad must end on an end_card (the name and the call to action).

## 3. Covers and copy, per platform

- A cover per platform in one series layout (cadabra-covers-thumbnails), or
  cadabra_make_thumbnail.
- The caption per platform with cadabra_social_copy: the hook line first, one clear call
  to action, the hashtags that platform uses. The same words are not right everywhere:
  LinkedIn wants the lesson, TikTok the hook, YouTube the searchable title.
- Another market or language: cadabra-dub-and-translate.

## 4. The plan

A simple plan they can follow: which cut goes where and when, one post a day rather
than everything at once, the best opening first and the others tested after it.
cadabra_social_month fills a month of posting days when they want more than this one
launch. Nothing is posted unless they ask; when they do, cadabra_publish.

## 5. Check

Every cut watched at its start and end (no black frames, no cut-off words), every cover
read at phone size, every caption read once more for names and numbers.

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
