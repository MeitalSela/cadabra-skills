---
name: cadabra-music-video
description: "Make a song and a music video in Cadabra AI: a Suno V6 song written to the brief (Hebrew sung), every sung line timed and sliced from the clean voice, singing shots that land on the words, and B-roll cut on whole bars, all built in code. Use for a music clip, a song for a film, a jingle, a lyric video, a performance video, or 'make a song'."
---

# Music video

It runs in any chat with the Cadabra AI connector (Claude, ChatGPT, Claude Code): https://mcp.livinginmovie.com/mcp. Reading and planning are free; anything that generates is priced first and needs a Cadabra AI package.

## 1. The song

cadabra_generate_music_v6 (every run returns two takes of the same brief: play both).
- **Custom mode** when the words matter: style, title and lyrics, sung as written.
  Hebrew lyrics come back sung in Hebrew; run them through cadabra_hebrew_lyrics
  (free) first for vowel marks and syllables.
- **Style line:** genre, mood, instruments, vocal style, tempo or BPM, and a scene
  ("late-night highway drive", "a wedding at 4am"), 8 to 15 short descriptors. A scene
  beats a list of sounds. Never an artist's name; describe the sound instead.
- **Lyrics structure:** section tags ([Intro] [Verse] [Pre-Chorus] [Chorus] [Bridge]
  [Outro]), production cues in tags ([Build up] [Drop] [Whisper]), the hook line in
  CAPITALS where it peaks. The chorus is the line people will sing in the comments:
  short, repeatable, said once in the title.
- **Length:** in custom mode set duration to what the film needs; it costs the same.
  A short cue wants a sparse style line, a dense one runs long.
- A song FOR a finished video: simple mode with video_url, and Suno writes to it.

## 2. Timing (free)

cadabra_song_phrases on the song: the voice is separated, every sung line is timed,
the chorus is found by repetition, and each line gets a clean-voice slice starting 0.3
seconds early. Read cadabra_editor_manual section "music-clip" before planning.

## 3. The shots

- **Singing shots** (3 to 10 seconds, chorus lines first): each made from its own
  voice slice, never from the full mix (drums under the voice keep the mouth half
  closed). Write the shot in labelled parts: initial state, the performance, end
  state, the camera ("locked from first frame to last" when the angle matters), and
  "lip-sync to the exact vocal in the audio; no added music".
- **B-roll** that tells the song's story, one idea per line of the verse, the wild
  image on the drop.
- One performer stays the same: their character sheet on every shot.

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
6. **Before they post:** cadabra_hook_check (free) on the finished film, then
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

## 4. The cut, built in code

cadabra_music_video_cut with the song, the performances (each with its phrase_start)
and the B-roll: singing shots start 0.3 seconds before their line, gaps are filled on
whole bars at the song's own tempo, clips are muted, the song is mastered loud for
social. For a vertical 15 to 30 second version, pass range_start and range_end around
the chorus.

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
