---
name: cadabra-learn-from-results
description: "Close the loop after posting, in Cadabra AI: read what worked and what flopped from the numbers the creator shares, find where viewers drop off, decide what to repeat, change and stop, and feed the lesson into the next batch and the brand notes. Use for 'which video worked', 'why did it flop', 'my numbers', 'an ad report', 'what should I post next', 'מה עבד', 'ניתוח תוצאות', or after any campaign."
---

# Learn from results

It runs in any chat with the Cadabra AI connector (Claude, ChatGPT, Claude Code): https://mcp.livinginmovie.com/mcp. Reading and planning are free; anything that generates is priced first and needs a Cadabra AI package.

Making more of what failed is the most expensive way to run an account. Read the
results, decide in writing, and carry the lesson forward.

## 1. Get the real numbers

Ask them to paste or upload what they have: views, average watch time or retention,
shares, saves, comments, follows, clicks and, for ads, spend and results. An ad export
(English or Hebrew): cadabra_campaign_analyst computes, per ad, what to scale, stop,
keep or wait on, and where each ad loses people. Never invent a number; say what is
missing.

## 2. Read them in this order

- **The first three seconds:** the drop at second one or two is the hook. Re-check the
  video with cadabra_hook_check and compare it with the best one.
- **The middle:** a steady fall means the story does not turn; a cliff at one moment
  means that moment is the problem (a long shot, a repeated beat).
- **The end:** shares and saves say the idea landed; comments say it provoked.
- **The outliers:** one video ten times above their usual is worth a whole page of
  analysis: what was its first frame, its length, its format, its words?

## 3. Three lists

- **Repeat:** what worked, as a format they can make again (cadabra_viral_formats,
  cadabra-content-month).
- **Change:** one thing per video, with a hypothesis that can lose (cadabra-ad-angles).
- **Stop:** what flopped twice for the same reason.
Say how sure each is: a single post proves little; three of a kind proves a pattern.

## 4. Feed it forward

Write the lesson as one line in their brand notes (cadabra_brand_kit style note and the
series bible), for example "the 'one mistake' hook beat the 'three tips' hook". The next
plan (cadabra_social_month with what_worked and what_flopped) starts from it.

## 5. Keep it honest

Tell them what the numbers cannot say (a platform's reach changes week to week). One
variable at a time, and give a result a fair week before deciding.

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
