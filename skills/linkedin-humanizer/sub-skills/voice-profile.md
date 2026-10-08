# Sub-skill: Build / update the Voice & Brand Profile

Builds or refreshes `../../../references/voice-profile.md` so every writing skill in
this bundle drafts in the user's real voice instead of a generic "human" voice.
It needs only the user's own writing, pasted into the conversation. No accounts,
no tokens, no third-party services.

## When this runs

- User says "build my voice profile", "learn my voice", "set up my profile", or
  invokes `linkedin-humanizer` profile mode.
- Also offer it the first time a writing skill runs and finds `filled: no`.

## Inputs (any one is enough)

1. **Pasted samples (default).** Ask for 3-6 of the user's own real LinkedIn
   posts or comments. This alone is enough — paste the text, or upload a
   screenshot of their post history and read it with `Read`.
2. **Manual.** The user can also just tell you their niche, rules, and links.

## Steps

1. **Gather 3+ real samples** of the user's writing (pasted or read from screenshots).
2. **Extract the voice fingerprint** from the samples, not from assumptions:
   - sentence-length rhythm (short/medium/mixed, and how often a long line appears)
   - recurring openers and transitions they actually use
   - punctuation habits (soft `..` pause? never em dashes? line breaks per idea?)
   - vocabulary they lean on, and any words/cliches they clearly avoid
   - emoji and hashtag behavior
3. **Infer niche, ICP, and pillars** from the sample topics; confirm with the user
   rather than guessing.
4. **Capture hard rules and CTA/link style** the samples reveal or the user states.
5. **Write `../../../references/voice-profile.md`**: fill sections 1-5, copy the 2-4
   strongest lines verbatim into "Signature examples", and set the Status block to
   `filled: yes`, `source: <pasted|manual>`, `updated: <today's date>`.
6. **Show the user the filled profile for approval** before saving, and tell them
   any writing skill will now match it automatically. They can edit the file anytime.

## Hard rules

- Build the fingerprint from the user's ACTUAL samples. Never invent a voice.
- Preserve their quirks (a favorite phrase, an unusual rhythm). Those are the
  point. Only the generic AI-tell scrub still applies to drafts later, not to the
  profile itself.
- Keep it honest about coverage: with 3 samples say the profile is a first pass and
  will sharpen as they add more; suggest re-running after 10+ posts.
- Never put secrets, private data, or anything the user did not provide into the file.

## Related

- The filled profile is read by `linkedin-post-writer`, `linkedin-comment-drafter`,
  `linkedin-reply-handler`, and `linkedin-repurposer` before they draft.
- Re-run this any time the user's voice or focus shifts to refresh the profile.
