---
name: cadabra-product-shoot
description: "Shoot a product in Cadabra AI from the creator's own photo: a white-background main image that passes marketplace rules, a full listing set (lifestyle, detail, angles, in the box, scale), lifestyle and ad stills, and a shop shelf from a store link, with the real product's shape, label and colour kept in every picture. Use for product photos, packshots, Amazon or Etsy or Shopify images, catalogue shots, or 'photos for my store'."
---

# Product photoshoot and store images

It runs in any chat with the Cadabra AI connector (Claude, ChatGPT, Claude Code): https://mcp.livinginmovie.com/mcp. Reading and planning are free; anything that generates is priced first and needs a Cadabra AI package.

## 1. Start from their real product

Ask for two or three photos of the product (front, side, label) and upload them with
cadabra_upload_file. Everything is an EDIT of the real product, never a redraw from
words. From a store link instead, cadabra_shop_spell reads the product and builds the
shelf in 1:1, 4:5 and 9:16.

## 2. Pick the model by the job

- Labels, small text, a logo that must survive: gpt-image-2.5 or gpt-image-2.6
  sunburst (cadabra_generate_image), with a mask_url when only one area should change.
- Lifestyle scenes with the product in them: nano-banana-2.1 or seedream-5.5.
- Hebrew or English text in the picture: gpt-image-2 (its 2.5 sunburst tier for small
  dense text), Grok Imagine, Ideogram 4.5 or Nano Banana, the sentence quoted, on a
  flat surface.
Quote first; resolution is the creator's choice on the models that ask.

## 3. The marketplace set (write it as a contract per image)

1. **Main image:** pure white background (#FFFFFF), the product alone filling about 85
   percent of the frame, no text, no props, no hands, no shadow box, sharp edge to edge.
2. **Lifestyle:** the product in use, in the place the buyer lives, a person only if it
   helps (and then a hand or a body, the product the hero).
3. **Detail:** a macro of the material, the stitch, the texture, the finish.
4. **Angles:** four views in one image or four images, same light, same background.
5. **In the box:** everything the buyer gets, laid out, counted.
6. **Scale:** the product next to a hand or an everyday object.
7. **Benefits card:** three benefits as short lines with icons, the product large (a
   text model only).

For a Pinterest pin use 2:3; for a carousel give every slide its own prompt, never a
paraphrase of the last one.

## 4. Check every picture

Look at each image against its contract before showing it: is it the same product
(shape, colour, label text letter by letter, number of parts), is the background what
the rule says, is any text spelled right. A picture that changed the product is not
delivered; fix it with continue_from (gpt-image-2.5) or a masked edit, after a new
quote. cadabra_magic_angles makes more angles of a product the creator approved;
cadabra_upscale_image finishes the chosen ones.

## 5. From stills to video

An approved hero still becomes the first frame of a product film (cadabra_generate_video
or cadabra_make_film with product_image_url): one slow move, the label readable at the
last frame.

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
