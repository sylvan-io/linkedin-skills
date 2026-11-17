# Nurture Sequence (T1-T4)

The stage state machine for one-to-one outreach. It defines where a prospect
is, what this touch may and may not do, and the signal that says the stage can
advance. Scenario packs in `scenarios/` refine the stance for specific
situations; they do not replace this model.

## Core principle

Outreach that leads with a pitch skips the trust build and gets rejected. The
first three contacts give value and credibility without selling; the fourth is
the first commercial close. The close is a byproduct of accumulated trust, not
a scripted trick.

Think of it like planting: prepare the soil, water, and fertilize first; the
tree grows on its own. This is a heuristic framework, not a fixed message count
that closes on cue. A stage advances on signals, not on the number of messages
sent.

## Stage overview

| Stage | Goal | Default stance | Advance signal |
|---|---|---|---|
| T1 Value-first | Lower defenses, be seen as helpful | Pure value, no ask | They reply with more than courtesy, or say the input was useful |
| T2 Demonstrate expertise | Let them conclude you know the field | Show know-how indirectly, no self-praise | They start asking you questions and seeking advice |
| T3 Earn character trust | Prove you are dependable | Consistent, honest, willing to advise against a needless purchase | They discuss non-work topics, or refer someone to you |
| T4 Natural close | Let them raise the purchase | Keep the prior sincerity, lay out details clearly | They name the need and ask for specifics |

## T1 — Value-first

**Goal.** Lower their guard and leave the impression you are there to help, not
to earn their money.

**Allowed moves**

- Give a practical suggestion for a pain point they stated.
- Flag a recent industry change, new rule, or relevant update.
- Share a resource or material they can use, with no ask for immediate return.

**Forbidden**

- Pitch the product, quote, or meeting.
- Ask for a call, budget, or commitment.
- Frame the favor as a lead-in to a sale.

**Advance signal.** They reply with more than a courtesy thanks, or say the
input was useful.

**Surfaces.** Cold DM opener; the first value comment on their post.

## T2 — Demonstrate expertise

**Goal.** Let them conclude you understand the field, without you claiming it
yourself.

**Allowed moves**

- Discuss industry know-how and current trends.
- Diagnose a hidden risk in their current approach, then give structured advice
  backed by a relevant case.

**Forbidden**

- Self-promotion, jargon dumping, showing off.
- Badmouthing competitors or peers.

**Advance signal.** They start asking you questions and seeking your advice.

## T3 — Earn character trust

**Goal.** Prove you are dependable and will not take advantage of them.
Professional skill shows you can solve the problem; character trust is what
makes them hand you the business.

**Allowed moves**

- Keep every promise, even a small one.
- Give concrete advice; do not exaggerate or paint an overly rosy picture.
- Be willing to talk them out of a spec or purchase they do not need, and help
  them save cost.
- Admit a gap honestly. When it is not your area, say so and refer to a
  better-suited person.

**Forbidden**

- Overpromising, faking competence, taking on what you cannot deliver.

**Advance signal.** They discuss work-outside topics, or refer a friend or
colleague to you.

## T4 — Natural close

**Goal.** Let them raise the purchase; do not force it.

**Allowed moves**

- Keep the same sincerity as earlier stages. Do not switch into a sales persona
  once interest shows.
- Lay out product details, price, and process clearly.
- Use an either-or choice (option A versus option B) to help them decide.

**Forbidden**

- Pressure close, repeated nudges, or discounting to chase a non-ready buyer.
- Changing tone once interest appears.

**Advance signal.** They name the need and ask for specifics.

If they do not order, do not push back into a close. Reflect on which earlier
stage was weak and repair it. A close lands naturally only when the foundation
holds.

## Cross-stage guardrails

- No product pitch in T1-T3. The first commercial ask belongs to T4.
- Match the counterpart's register and message length. DMs are conversation,
  not content.
- Do not burst several messages in a short window. Per-account rate limits
  target automation patterns.
- Effort weighting (heuristic): most of the work sits before the close. The
  closing touch should require little force if the prior stages held.
- Regress honestly. Stalled or lukewarm replies usually mean an earlier stage
  was skipped or thin, not that the closing line needs sharpening.

## Anti-patterns

- **No prep at all.** Lead with the offer and the prospect leaves immediately.
- **Pitch in every touch.** Follow-up becomes harassment and gets blocked.
- **Nurture as sycophancy.** Smiles and freebies with no value or expertise are
  low-status, not nurturing. Nurture carries value and professionalism; it is
  not flattery.

## Map to bundle surfaces

- Public comment drop on their post: a T1 or T2 value/expertise touch. Do not
  name your own product (root voice rule 8); describe what you do instead.
- Cold DM opener: T1.
- Continued DM thread: the current stage per the connection `## Nurture` block.
  Scenario packs under `scenarios/` refine the stance for specific situations.
