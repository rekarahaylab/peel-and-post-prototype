# Peel & Post — prototype

A little card. A meaningful gift.

Clickable prototype of Peel & Post, a digital greeting-card site. Everything lives in one `index.html` (no build step).

**Live:** https://rekarahaylab.github.io/peel-and-post-prototype/

## Try it
1. Drag a paper from the shelf onto the table.
2. Add at least 2 items from the shelf (stickers, photo frames, text). Tap the paper to write on it.
3. Add a finishing touch, write the letter, press **SEND CARD**.
4. Copy the card link and open it on another phone or browser: the recipient taps the envelope and the card slides out.

## Notes
- Photos are uploaded to Supabase Storage (bucket `card-photos`, project `peel-and-post`) when the card is sent. The key in `index.html` is the public anon key: it can only add new JPG files (max 1 MB) to that bucket.
- Prototype only: nothing is charged and nothing is mailed.
