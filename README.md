# Peel & Post — prototype

A little card. A meaningful gift.

Clickable prototype of Peel & Post, a digital greeting-card site. Everything lives in one `index.html` (no build step).

**Live:** https://rekarahaylab.github.io/peel-and-post-prototype/

## Try it
1. Tap **Open the shop**: the lights come on, Pospus says hi and opens the door.
2. Browse the shelves, then tap **Create your card**. Drag (or tap) a paper onto the table.
3. Add at least 2 items from the shelf (stickers, photo frames, text, confetti backgrounds). Tap the paper to write on it.
4. Write a letter or address the envelope, pick the envelope, stamp, wax seal and an optional song (Spotify/YouTube link).
5. **Preview as recipient**, then press **SEND CARD**, pay with the demo QRIS and copy the short link.
6. Open the link on another phone or browser: the envelope opens, the card flips over and the stickers fade in. The recipient can save or share it.

## Notes
- Photos are uploaded to Supabase Storage (bucket `card-photos`, project `peel-and-post`) when the card is sent. The key in `index.html` is the public anon key: it can only add new JPG files (max 1 MB) to that bucket.
- Short card links are stored in Supabase (`public.short_cards`, reached only through the `put_short_card` / `get_short_card` functions). If that fails the long link is used.
- Music and sound effects are synthesised in the browser; the 🔊 button sets on/off and volume.
- Prototype only: the QRIS payment is a demo, nothing is charged and nothing is mailed.
