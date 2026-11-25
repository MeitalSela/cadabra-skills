---
name: cadabra-preflight
description: "Protect the creator's credits in Cadabra AI before anything is generated: find the problems that waste a render (an unlocked character, a clip too long to hold, the wrong engine, a prompt that will be misread, a word the engine refuses) and decide Ship, Hold or Block, then check the result after. Use before any paid generation or film, for 'is this ready', 'will this work', 'check my plan', 'don't waste my credits', 'לפני שאני משלם', or after a render that came out wrong."
---

# Preflight before you spend

It runs in any chat with the Cadabra AI connector (Claude, ChatGPT, Claude Code): https://mcp.livinginmovie.com/mcp. Reading and planning are free; anything that generates is priced first and needs a Cadabra AI package.

Most wasted credits come from a few predictable mistakes. Finding them is free;
fixing them after the render is not.

## 1. The free reading

For the plan in front of you (a shot, a mission board, the free preview of a film):
cadabra_quote or the tool's own quote for the price, cadabra_pick_engine for whether
the engine fits the job, cadabra_craft_prompt to see the prompt as it will go, and for
a film the preview's own hook notes. Nothing here spends.

## 2. The pitfalls (any one is a Hold)

- **A character not locked:** a recurring person with no sheet or reference on every
  shot they appear in. Name in the words is not identity.
- **A clip longer than the engine holds well:** one take past about fifteen seconds on
  an engine that drifts, or a duration the engine snaps up (a 15 second ask billed as
  20).
- **The wrong engine for the job:** Hebrew speech on a video engine, a real face on an
  engine that takes no identity, text in a picture on an engine that garbles it.
- **A prompt that fights itself:** two camera moves, an emotion word instead of a
  behaviour, music words in a video prompt, a brand name or logo asked of the model.
- **No hardest-shot-first:** ten shots queued before one was seen.
- **No reference:** a product or face described in words only.
- **A budget crossed:** the board is over the number they named.

## 3. The verdict

- **Ship:** no pitfall; say the price and what they will get in one line.
- **Hold:** fixable; list the fixes (free), apply them, check again.
- **Block:** a rule is broken (a real person's face without their consent, text the
  engine cannot spell, a budget they did not agree to); say why and offer the safe
  alternative.
Never push a Hold through because the creator is in a hurry. The cheapest tier proves it
first (seedance-20-mini, seedance-25 draft).

## 4. After the render

cadabra_inspect the clip, cadabra_qa_shot with the frames and the contract, and say Ship
or Redo in one line. A redo changes the one cause, never the same prompt again, and
needs a new quote and a new yes. A failed generation refunds itself; say so.

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
