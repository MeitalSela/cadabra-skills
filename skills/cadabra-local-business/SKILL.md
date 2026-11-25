---
name: cadabra-local-business
description: "Turn a phone photo and a sentence from a local business owner (a restaurant, a clinic, a salon, a shop, a tutor, a real estate agent, a studio) into a full week of posts and one real ad in Cadabra AI, using the real place, the real product and the real people, with offers that are true. Use for 'I own a business', 'my restaurant', 'my shop', 'a week of content for my business', 'פרסום לעסק שלי', 'אני בעל עסק', or any small business that is not sure where to start."
---

# Local business week

It runs in any chat with the Cadabra AI connector (Claude, ChatGPT, Claude Code): https://mcp.livinginmovie.com/mcp. Reading and planning are free; anything that generates is priced first and needs a Cadabra AI package.

A local owner has no time and no team. Ask little, use what is real, and hand back a
week they can post.

## 1. Four answers, one message

What they sell, who walks in (a regular customer in one line), the one thing they are
proudest of, and what they want people to DO (call, book, walk in, order). Ask for the
photos in the same message (cadabra_upload_file): the product, the place, the people
who agree to be shown. If they have a store page, cadabra_shop_spell reads it.

## 2. Use what is real

The real product photo anchors every picture and shot (cadabra-product-shoot). The real
place is a saved location. Real staff or customers only with their agreement. Never an
invented review, an invented discount, or an invented before-and-after. A claim the
owner cannot back up is not written.

## 3. The week

Seven posts, three series so it feels like an account, not a pile (cadabra-content-month):
- Two product posts: the product in use, not on a pedestal (cadabra-ugc-ad route
  unboxing or ugc-review).
- Two people posts: the owner or the team, the craft, the morning routine.
- Two proof posts: a real result, a real customer line (cadabra-customer-voice).
- One offer post with a true deadline and an end card.
cadabra_social_month plans it and cadabra_social_copy writes each caption.

## 4. One real ad

A short ad that ends on an end_card with the name, the place and the way to act:
cadabra_ad_ideas for three concepts, then the chosen one (cadabra-ugc-ad). Sized for
the place they advertise (cadabra_ad_studio route ad-resize), in the language their
customers read.

## 5. Make it easy to keep going

Save the brand (cadabra-brand-and-cast) so next week matches this one, and tell them
which post to repeat when it works. Posting is theirs unless they ask for cadabra_publish.

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
