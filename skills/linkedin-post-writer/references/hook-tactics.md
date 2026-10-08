# Hook tactics: formats, length engineering, and 40 named moves

For the **hook-options mode** of `linkedin-post-writer`. The hook is the text
visible before LinkedIn's "...more" fold; its only job is the click. Everything
here operates in the hook zone (the first ~210 characters); the rest of the post
follows the formula skeletons in `../../../references/hook-formulas.md`.

## Relation to the F1-F20 skeletons

Tactics are line-level moves; formulas are whole-post skeletons. Use both: pick
the formula for the post, then shape the hook lines with tactics. Where a tactic
overlaps a formula (before/after ≈ F3, curiosity gap ≈ F9, contrarian ≈ F10,
time-anchor ≈ F4), apply the project's 2026 caveats from `hook-formulas.md` on
top.

## Universal hook-zone rules

- The hook occupies the visible lines before "...more" cuts in (first ~210 chars total).
- **Line breaks count as full lines.** A line break costs an entire visible line of space, not one character. Adding one is a major formatting decision.
- Max total: **210 characters**. Max single line: **75 characters** (longer wraps awkwardly on mobile).
- **No em dashes in the hook zone** — stricter than the body cap (~1 per 100 words). Use commas, periods, colons, or rephrase.
- **No emojis in hooks.**
- **No questions** (project rule: -34% median likes), with one exception: the Data-Question Opener, only when a chart/graph is attached.
- No filler adverbs (actually, basically, very, just, really, literally, honestly).
- Banned cliches: "game-changer", "deep dive", "let that sink in", "read that again", "this changed everything", "they called me crazy", "here's the thing", "the truth is", "then it hit me", "I'm excited to share".
- **Never fabricate a number.** If the draft has no real data point, use a different angle.

## The four hook formats (pick exactly one per hook)

### Format 1: DENSE

**Type:** all visible lines used as continuous text with no line breaks. Maximum information per pixel. Best when the hook needs context, a story setup, or a data point that requires a full sentence to land.

**Rules:**
- **140-160 characters total.** No exceptions on either end.
- Zero line breaks. Continuous text only.
- Must span 2-3 visible lines on mobile (what 140+ characters produces).
- Under 140 it is NOT Dense: rewrite longer to fill the format, or pick a different format. **Rewrite, do not relabel.**

**Example:** An 8k-follower account hit 58,666 impressions on a post our designer begged us not to ship. The reason has nothing to do with design.

### Format 2: PUNCHY + CONTEXT

**Type:** line 1 is a bold, short claim or pattern interrupt; line break; line 2 is the rehook — a parenthetical, a teaser, or the reason to keep reading. Best for contrarian takes, hot openers, and posts where the first line must hit like a headline. Line 1 creates the reaction; the line break creates a micro-pause; line 2 promises the payoff behind "see more".

**Rules:**
- Two lines, separated by a blank line in output (a real line break, never a slash or same-line text).
- Line 1: **≤ 50 characters.** Line 2: **≤ 50 characters.**
- Rotate sub-variants across a hook set — never use the same sub-variant for every option in one output.

**Sub-variants:**
- **Plain:** line 2 is a direct teaser or claim.
- **Parenthesis wrap on line 2:** wrap line 2 in parentheses to make it a quiet aside or self-aware admission. Best when line 2 is a confession or contradiction.
- **Strategic ALL CAPS on one word in line 1:** capitalize one high-stakes word for visual weight without shouting. One word per hook, never a full line.
- **After-Stack Setup:** both lines are setup (no punch, no rehook), each starting "After [cost/sacrifice/obstacle]..." and ending with trailing dots. Best when media is attached.

**Example:** We deliberately made a client post look ugly. / 58,666 impressions. (Our designer was pissed.)

### Format 3: SINGLE-LINE BOMB

**Type:** one short, charged sentence; then "...more" cuts in almost immediately. Maximum curiosity gap. Only works if the line is genuinely strong enough to stand alone. High risk, high reward. Fails badly when the line is generic or predictable.

**Rules:**
- **≤ 50 characters total.** One line. Zero line breaks.
- Too long → rewrite shorter or pick a different format. **Rewrite, do not relabel.**

**Example:** SEO has been dying since 1997.

### Format 4: STACKED QUOTES / LIST HOOK

**Type:** open with 2-3 short quoted phrases or a rapid-fire timeline creating a pattern the reader wants to see broken or explained. Triggers completion bias; the implied contrast between entries creates tension without stating it.

**Rules:**
- 2-3 lines, each on its own visible line (blank lines between).
- Each line: **≤ 60 characters** (sub-variant E: **≤ 50**).
- Must follow one of the sub-variants — Stacked is not free-form.

**Sub-variants (pick one per hook):**

- **A. Before/After Timeline** (≈ F3): two compressed lines showing the gap between then and now. Each line: `[year/time]: [state]. [metric]. [one emotional word or phrase].` Power is in the compression; no explanation of how, just the gap.
  Example: `2023: 0 followers. $0 made. Felt invisible.` / `2026: 317k followers. $2M+ made. Forbes featured me.`
- **B. Parallel Regret Stack:** 2-3 lines on the same grammatical structure, each naming a specific avoidance behavior and a one-word emotional cause.
  Example: `I didn't promote myself for 1 year. Felt embarrassed.` / `I didn't launch my business for months. Feared failure.`
- **C. Data-Question Opener:** lead with a question that points to visual data below; line 2 delivers the buried insight that makes the data surprising. **Use ONLY when a chart/graph/infographic is attached.** The only question-hook exception to the project's no-question rule.
  Example: `What do you notice about this data?` / `Hardly anyone has realised that ~25% of AI answers now come...`
- **D. Stacked Jargon Repetition (Cut-Off):** three lines with identical structure using industry terminology; the third line cuts off before completing. In-group language signals a knowledgeable audience.
  Example: `Somebody liking your post doesn't make them TOFU.` / `Somebody reading your blog doesn't make them MOFU.` / `Somebody downloading your ebook definitely doesn't make them...`
- **E. Problem-Cost-Twist (3-line):** line 1 names the problem, line 2 the cost or contradiction, line 3 the payoff or reveal that forces the click. Each line ≤ 50 chars. Best for product/feature posts, case studies, contrarian observations; worst for personal narrative or emotional posts where the rhythm feels mechanical.
  Example: `Your brand style guide has 50+ rules.` / `Your team remembers maybe 3 of them.` / `We built a system that checks ALL of them.`

## Rewrite before relabel

When a hook violates its format's length rules, the default action is **rewrite to fit**, not relabel to another format. Relabeling is a last resort, used only when the hook genuinely cannot be expanded or compressed without padding or losing the angle. If 2 rewrite attempts still fail, **drop the hook** and write a different angle. Never present a hook with an "OVER LIMIT" warning, a "reclassified" label, or any other indication it was broken — the user sees only the final, valid set.

## Pre-output validation (mandatory)

Before showing any hook to the user:

1. **Count characters.** Confirm the hook fits its format's length rule (Dense 140-160, Punchy lines ≤50 each, Bomb ≤50, Stacked lines ≤60 each with sub-variant E ≤50).
2. **Count line breaks.** Confirm they match the format (Dense 0, Bomb 0, Punchy 1, Stacked 1-2).
3. On failure: rewrite to fit; drop after 2 failed attempts.
4. Only valid hooks enter the output — the "Characters: [count] | ok" line always reads "ok".

## 40 named hook moves

Write-hook tactics observed on high-performing LinkedIn posts. Two moves (18, and Stacked sub-variant C) open with a question and conflict with the project's no-question rule (-34%): they are opt-in, used only when the user explicitly asks for maximum-curiosity hooks or attaches a chart.

1. **Body first.** The best hook is almost never the first thought; it lives in the most surprising result, the most specific number, or the thing you almost didn't say.
2. **Lead with the tension element.** A specific number, a contrarian take, a before/after, an unexpected result — never bury it behind setup.
3. **Reader-first framing.** "That's my problem" must land before the reader realizes it's a case study or promotion. Their pain precedes your credentials or brand.
4. **Numbers beat adjectives.** "$4.8M in 2 years (200% Quota)" beats "crushed their number".
5. **No setup openers.** Kill: "I want to share...", "Here's what I learned...", "Let me tell you about...", "In this post...", "I've been thinking about...", "Today I want to talk about...", "Here's the thing/why".
6. **Contrarian over agreeable.** "This will not be a popular thing to say on LinkedIn, but..." signals something real is coming.
7. **Tension over resolution.** Open a loop, don't close one; the reader should feel a question forming, not an answer arriving.
8. **Caps sparingly.** One or two capitalized words create visual punch; an ALL CAPS line reads as shouting.
9. **No questions** (exception: Data-Question with a chart attached).
10. **Parentheticals as rehooks.** "(the exact setup behind our $5K-$20K/month clients, free)" adds specificity and lowers the cost of the click.
11. **Never fabricate numbers.** No real data point, no number in the hook — switch angles.
12. **The reframe hook.** "We were worried about X, but what if Y is the real problem?" hijacks existing anxiety and redirects it.
13. **Compression is the skill.** A whole journey in two lines ("2023: 0 followers. $0 made. Felt invisible." / "2026: 317k followers. $2M+ made. Forbes featured me."); don't soften the gap, let numbers work.
14. **"Wrong"-framing invites collaboration.** "I built my first business by doing everything 'wrong'" signals the author knows the rules and broke them on purpose.
15. **Short bomb + long reframe beats two long lines.** Lead short when the claim is strong ("SEO has been dying since 1997.").
16. **Numbers with parenthetical confessions.** "I'm 28 with 4 businesses and (still) no home." — the "(still)" does more emotional work than the numbers.
17. **"Hot Take:" is a pattern interrupt.** Names the format, reduces resistance, and must be followed by a specific, arguable statement — never a vague one.
18. **Rhetorical question + incomplete answer.** "Why do we pay copywriters... Because AI still cannot..." — only works if the answer starts mid-thought, not with a satisfying full sentence. (Opt-in; conflicts with the no-question rule.)
19. **Real-time urgency.** "In less than 3 hours..." creates non-deferrable FOMO — use sparingly and only with a genuine live event or real-time stake.
20. **Outcome-signal hook.** "You'll know your positioning is working if..." gives the reader a condition to test against their own situation; it tests, doesn't teach.
21. **Anti-hype beats announcements.** "I'm putting it here, so it's likely not a single person will see this" out-performs polished launch framing.
22. **The load-bearing period.** "Most GTM stacks are bloated. Mine is not." — a full stop between two contrasting sentences makes the counter-claim hit like a verdict.
23. **"(but isn't)"** signals the knowing-doing gap: "Something that should be obvious (but isn't)" puts the reader in the position of knowing the right answer while implying they're not applying it.
24. **Audience segmentation.** "Marketing agencies that follow Fletch, this is for you (normies, keep scrolling)" makes the included group feel chosen; the excluded reader scrolls on smiling.
25. **Identity disclaimer flip.** "I'm not a developer. I don't write code. But [tool] is the most powerful thing I've used in years." — the recommendation lands harder from a peer.
26. **Credential + constraint.** "Covers 135 frameworks. If you forced me to pick 9, I'd pick these." — the constraint signals considered judgment; pair authority with a filtering mechanism.
27. **Soft warning over hard accusation.** "Please don't turn all your content into Q&A-style blogs. I get why marketing teams obsess over it." — validate before correcting.
28. **Failure-first list.** "9 channels that didn't help us get there... and 5 that did" signals honesty before authority.
29. **Split-list with a negative number.** "6 things I like about my CEO. And 3 things I absolutely don't." — the negative number is what earns the click.
30. **Meta-hook.** "*insert vague caption teasing biggest announcement ever dropping at 8am tomorrow here*" mocks the genre; only when the author's voice can carry the irony.
31. **Transparency parenthetical.** "(that aren't just another paid post)" does the disclaimer's work inside the hook, pre-empting skepticism.
32. **Problem-origin hook.** "Every conference I attend feels like it was built for someone more senior than me, so I'm creating one that isn't." — the logic of the solution is already in the problem; no mission statement needed.
33. **Acknowledgment list.** "I just wanted to acknowledge people who:" — generosity, not instruction; the relatable first item (cut off before the fold) makes the reader click to check inclusion.
34. **"I used to think X. But..."** — the "but" is the entire curiosity gap; start with the wrong belief, not the right answer.
35. **Mirror hook.** "You know what's holding you back. I do too." — five words that make the reader feel seen before the click.
36. **Result credentials.** "We are able to pay 60 salaries from posting on LinkedIn. So it's fair to say we understand the platform." — proof before lesson.
37. **External prediction + personal override.** "My high school teacher told me I'd never speak English. Today I work, think, and dream in English." — a limiting belief used as a foil.
38. **Family/community norm deviation.** "Nobody in my family has ever quit a job without another one lined up. I've done it twice." — a shared baseline broken is the hook.
39. **Scene-setting story hook.** "Sales and Marketing have a KPI meeting with their CEO. It gets awkward fast." — open the curtain, don't explain the play.
40. **Jargon cut-off.** Three identical structures with in-group terms (TOFU/MOFU/BOFU), third line cut off — completion bias in an expert audience.

## Hook-options output format

Present each hook option exactly like this (plain text, not a code block for the top-3 list):

```
[N]. [HOOK TEXT EXACTLY AS IT WOULD APPEAR ON LINKEDIN]

Format: [Dense / Punchy+Context / Single-Line Bomb / Stacked]
Characters: [count] | ok
Why: [one sentence on why this angle works for this post]
```

Every hook in the output is valid — the "Characters" line always reads "ok".
After all options, present the top 3 picks as plain text (NOT inside a code block):

```
TOP 3 PICKS:
#[X] - [one line reason]
#[X] - [one line reason]
#[X] - [one line reason]
```
