# Sub-skill: Generate an illustration for a post

Adds an optional image to a draft (feed illustration, carousel slide, or
quote-card). No third-party image service: the image is generated with the
platform's native image tool when one is available, or the user generates it
themselves and provides the file. The user attaches the image when posting.

## When this runs

- User says "add an image", "make an illustration", "make a quote-card", or
  "add a cover" for a post.
- Offer it once after a post draft is approved, when a visual would lift reach
  (LinkedIn image posts get more dwell time than plain text).

## Steps

1. **Pick the kind** (maps to an aspect ratio):
   - `wide` / `link` (16:9, 1200x628) - link-preview / single feed image (default for a text post)
   - `portrait` / `carousel` / `quote` (4:5) - feed portrait, carousel slide, quote-card
   - `square` (1:1) - generic
   - `story` / `cover` (9:16) - tall cover
2. **Craft the prompt.** Describe the scene concretely: subject, composition,
   style, palette. Default to a clean, non-literal, professional editorial look
   unless the Voice & Brand Profile §6 sets a `Visual style default`. Do NOT try
   to render the post's words inside the art (image models draw text
   unreliably); keep real words for a quote-card (below).
3. **Generate.** Use the platform's native image tool with the prompt and the
   aspect ratio from step 1. Show the user the result.
4. **Quote-cards: typeset, don't draw.** For a quote-card of the hook line, keep
   the text crisp: build the card as a simple HTML/SVG design (or a composed
   image with the text overlaid by the image tool), rather than asking the image
   model to render the words. The user can also make it in any design tool.
5. **Show + confirm.** Present the image and let the user approve it. On approval,
   the user attaches the image file when they post the copy-paste block on
   LinkedIn (image posts take up to 10 images in a grid; LinkedIn cannot mix
   images with video in one post).
6. **User-generated path.** If no native image tool is available (or the user
   prefers their own tools), hand them the drafted prompt + aspect ratio and ask
   them to generate it themselves and provide the file.

## Refine instead of regenerating

When the user wants a tweak ("make the sky darker", "swap the headline", "more
whitespace"), edit the existing image with the platform's image editing tool
rather than regenerating from scratch — it is cheaper and more consistent.

## Multi-image grid (LinkedIn, up to 10)

LinkedIn posts can carry up to 10 images in a grid layout. Generate (or ask the
user for) 2-10 images for one post; the user attaches all of them when posting.

## Hard rules

- Keep real words in a quote-card or overlay, never baked into the prompt art.
- Never attach an image the user has not seen and approved.
- If the user asks for a visual in the user's brand style, read the Voice &
  Brand Profile §6 (handle, brand color, logo) and match it in the prompt.
