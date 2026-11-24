---
name: cadabra-voice-studio
description: "Make voices in Cadabra AI that sound performed, not read: narration, voiceover, ad reads, character lines and dialogue in Hebrew or English, with the right voice chosen by the creator, direction tags, correct Hebrew pronunciation, the same voice held across a whole series, and a clean timed track for the edit. Use for a voiceover, narration, a voice, text to speech, a character's voice, dialogue between characters, cloning their own voice, 'קריינות', 'קול', or when a read came back flat."
---

# Voice and narration

It runs in any chat with the Cadabra AI connector (Claude, ChatGPT, Claude Code): https://mcp.livinginmovie.com/mcp. Reading and planning are free; anything that generates is priced first and needs a Cadabra AI package.

## 1. The voice is theirs to choose

Never pick a voice for them and never ask for a voice id. Offer, in this order:
- **Their own voice:** cadabra_clone_voice from a clean recording of them talking
  naturally (a quiet room, no music, a minute or more), saved under a name.
- **A saved voice:** cadabra_my_voices.
- **The library:** cadabra_list_voices, searched by language, gender, age, accent and
  use ("warm narrator", "energetic young woman", "deep trailer voice"). Play two or
  three short samples and let them choose.
- **A new voice from a description:** cadabra_design_voice. Describe the PERSON and
  their situation ("a tired night-shift nurse in her fifties, kind and dry"), not voice
  adjectives; keep the one they like.
Any voice speaks any of the 90 plus languages, Hebrew included.

## 2. Write for the ear

Short sentences, one breath each, the words they would actually say. Numbers, dates and
English brand names written the way they are said. In Hebrew, the audience in the
plural. cadabra_proofread_script (free) finds what trips the tongue. Names and words
that come out wrong: cadabra_pronunciation, or vowel marks on that one word.

## 3. Direct the read (Eleven v4 first)

cadabra_eleven_v4_speak performs the text the way an actor would, directed by tags
written inside it, in English even inside Hebrew text:
- Feeling: [excited] [warm] [whispers] [sarcastic] [nervous] [curious] [sighs].
- Breath and laughs: [laughs] [exhales] [gulps], and ... for a breath.
- Pauses: [pause] [long pause]. A word in CAPITALS gets the stress.
- Free direction beats one word: [low, slow, as if telling a secret].
A flat read is almost never the wrong voice; it is the same voice not told where to
breathe. cadabra_voice_tags (free) marks a plain line up for you. Stability low is
lively and acted, high is steady for a long narration.

## 4. Narration for a film

- ONE read of the whole script, not sentence by sentence, so the voice and the energy
  hold. A retake of one line: just that line, the same voice.
- Write to the picture: about three words a second, and a pause where the picture
  needs to breathe.
- In the edit pass the voice as voiceover_url AND the script as narration_script, so
  the captions are the approved words, not a transcription. cadabra_align_script times
  the script to a recording they made themselves.

## 5. Characters and dialogue

- One saved voice per character for the whole series, by name, every episode.
- Several characters in one file: cadabra_generate_dialogue, with natural turn-taking.
- The best Hebrew acting is often the creator's own: they perform every part, and
  cadabra_change_voice turns each performance into that character's voice with the
  timing and emotion kept.
- On screen: cadabra_lipsync lays the voice on the shot (veed-2 when the video cuts
  between shots, sync-3 for one unbroken shot). A video engine never speaks Hebrew.

## 6. Listen before it goes anywhere

Play the read to the creator before it goes into a film or an avatar. Check every
name, number and brand word yourself. Background noise or echo on their own recording:
studio_sound in cadabra_assemble cleans it, or cadabra_clean_audio.

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
