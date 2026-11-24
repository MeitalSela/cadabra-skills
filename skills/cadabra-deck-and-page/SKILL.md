---
name: cadabra-deck-and-page
description: "Build a pitch deck, a portfolio, a project board or a one-page landing page as a single self-contained HTML file, using the creator's own Cadabra films and pictures, with a real design direction instead of a template. Use for a deck, slides, a presentation, a landing page, a portfolio page, a pitch, or a page to show a client."
---

# Decks and landing pages

It runs in any chat with the Cadabra AI connector (Claude, ChatGPT, Claude Code): https://mcp.livinginmovie.com/mcp. Reading and planning are free; anything that generates is priced first and needs a Cadabra AI package.

You write this one yourself, as one self-contained HTML file. The media is the
creator's own: films and pictures from their Cadabra gallery (cadabra_list_creations)
or made for the page, linked by their CDN URLs.

## 1. Four answers before any code

What is it for, who will look at it, what is the ONE thing they should remember, and
what is the single action at the end. Then commit to one strong design direction
(editorial, brutal mono, dark cinema, soft luxury, bold signal) and keep it.

## 2. Decks

- 8 to 12 slides, never more than 16. A pitch: hook, problem, solution, how, proof,
  market, team, ask.
- Every slide fits one screen with no scrolling; split instead of shrinking.
- At most 4 to 6 bullets or 6 cards a slide. Never the same layout twice in a row.
- Sizes in clamp(), so it holds on a laptop and a projector. Arrow keys, F for full
  screen, a thin progress bar. Right-to-left decks swap the arrows.

## 3. Landing pages

One page, one goal, one primary button (two button styles at most). Proof right under
the hero (a real film, a real number, a real quote). Write two or three headlines and
keep the strongest: specifics beat claims. Real copy only, never placeholder text.

## 4. Taste

- A named font pair, not a system font. Hebrew: Heebo, Rubik, Assistant or Frank Ruhl
  Libre, the page dir="rtl".
- One accent colour used with intent; no purple-on-white gradient.
- An atmospheric background (a subtle grain, a soft gradient) and one staggered reveal
  when the page loads, rather than motion everywhere.
- The creator's film plays muted and looped in the hero, with a poster frame.

Hand them the file, and check it yourself at phone width before saying it is done.

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
