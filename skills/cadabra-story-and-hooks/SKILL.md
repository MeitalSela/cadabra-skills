---
name: cadabra-story-and-hooks
description: "Find the idea and the story before anything is made in Cadabra AI, for free: five different ideas from a rough thought, the one-sentence story with its turn, the beats in order, a first frame and first line that stop the scroll, and a hook check on the opening. Use when someone is not sure what to make, has a rough idea, asks for ideas, a script, a story, a hook, 'what should I make', 'תנו לי רעיון', 'איך לפתוח', or a video that people do not watch to the end."
---

# Story and hooks

It runs in any chat with the Cadabra AI connector (Claude, ChatGPT, Claude Code): https://mcp.livinginmovie.com/mcp. Reading and planning are free; anything that generates is priced first and needs a Cadabra AI package.

Regretting a film costs credits; choosing between five ideas costs nothing. Everything
in this skill is free, and it runs before anything is generated.

## 1. Five ideas, then one

When they are not sure: cadabra_concepts with their rough thought and what it is for
(an ad, a reel, a trailer, a story). It returns five DIFFERENT ideas with the reason
each would work and the reason it might not. Say the best two in one line each, give
your pick and why, and let them choose. Never invent a sixth to please them.

## 2. The one-sentence story

"Someone wants X, Y stands in the way, so Z." If you cannot write it, there is no story
yet, only a mood. Then check it:
- **The want is visible,** shown in behaviour, never explained in a line of dialogue.
- **Each beat changes the situation.** If the beats could be shuffled without loss, it
  is a mood board: rebuild it.
- **Escalation in two or three steps,** then the turn, then the payoff held.
- **The ending answers the first shot's question** and flips how we read it. For a
  series episode, it cuts on the question instead.
- **One wild idea per scene,** on top of logic, not instead of it.
cadabra_story writes the beats in order (direct:true pushes on the ordinary world, the
rule of three, plant and payoff; lock_dialogue:true returns only the verbatim lines).
Show the beats beside the free preview and its price, so one yes approves both.

## 3. The hook (the first second decides)

- **Frame one is the most extreme, most recognisable image of the idea, already
  moving.** A face mid-reaction, an object in a hand, the trouble already started.
  Never a logo, a landscape or "hi".
- **A hook is a sentence the viewer wants resolved:** "POV: ...", "nobody tells you
  that...", "I tried X for 30 days", a number, a confession. Write it first, put it on
  screen in the first half second, and build the film to pay it off.
- **A deliberate gap invites the comment:** leave one thing unnamed or one choice
  debatable, instead of begging for comments.
- **Interactive hooks for reels** (cadabra_hook, free until the video): an app-style
  element in their own room that breaks when touched (a notification, a like, a
  follow button, the loading circle). Their full-body photo is the first frame, the
  face stays theirs, the words are theirs. Show the frame, then the video call and its
  price.

## 4. A proven shape, when they want a series

cadabra_viral_formats lists short-form shapes measured working across platforms, the
trending ones first (say honestly when one is past its peak). One format plus one
subject returns the law, the first frame, every shot prompt on the cheapest engine and
how the next episode continues. For a written story series: cadabra_series_guide.

## 5. Test the opening before paying

After the film exists, cadabra_hook_check scores the first three seconds from 0 to 10
and gives ONE fix. For a film not yet made, a free plan from cadabra_make_film comes
with its own hook notes: apply them before the price.

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
