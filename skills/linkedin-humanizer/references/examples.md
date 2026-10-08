# Examples — LinkedIn Humanizer

## Example

> **Input:**
> "In today's fast-paced landscape, businesses must fundamentally leverage AI to unlock robust ROI. It's not just about adoption, it's about transformation. As of my last update in January 2024, the trends are clear — here's what I've learned."
>
> **Output (default mode = forensic + strict):**
> "businesses need AI to cut costs. adoption is the easy part. transformation is the actual work. here's what we learned running 35k LinkedIn profiles through our system daily."
>
> **Diff:**
> - FORENSIC: removed "As of my last update in January 2024" disclaimer
> - STRICT: paragraph scored 5 markers (fast-paced landscape, fundamentally, leverage, unlock, robust) = rewrite the paragraph, not word-by-word
> - STRICT: removed "It's not just X, it's Y" negative parallelism (single-hit rule), replaced with paired declaratives
> - PASS 1: the one em dash was under the cap (~1 per 100 words); it went only because the sentence around it was rewritten. It was not replaced with a period
> - PASS 3: added a number with a referent (35k LinkedIn profiles, daily) from the user's own input; nothing fabricated, no hedge, no "let me be honest" frame
> - PASS 4: two fragments in the output ("adoption is the easy part." "transformation is the actual work.") are within the 2-per-post cap and are paired declaratives, not a "The result?" reveal; left as is
> - AESTHETIC was NOT applied

## Example: Corporate-speak + false agency + vague declarative (V3.1)

> **Input:**
> "Moving forward, the data tells us that the stakes are high. We need to double down on lean into collaboration and circle back on the roadmap. The implications are significant."
>
> **Output (default mode = forensic + strict):**
> "Our usage logs show the next two quarters decide the roadmap. We committed to the collaboration plan and revisited the roadmap. Losing this client ends the quarter in the red."
>
> **Diff:**
> - V3.1 CORPORATE-SPEAK: "moving forward" → "next" (dropped), "double down on" → "committed to", "circle back" → "revisited"
> - V3.1 FALSE-AGENCY: "the data tells us" → "our usage logs show" (named the actor)
> - V3.1 VAGUE-DECLARATIVE: "the stakes are high" and "the implications are significant" → the specific ("next two quarters decide the roadmap", "ends the quarter in the red")
> - STRICT: paragraph scored 4+ markers → rewritten as a paragraph, not word-by-word
> - PASS 3: no fabricated numbers; the specifics came from the user's own brief

## Example: Meta-commentary + rhetorical setup + lazy extreme (V3.1)

> **Input:**
> "Let me walk you through this. What if I told you that everyone struggles with pricing? Think about it: pricing is genuinely hard, and that's okay. As we'll see, the reasons are structural."
>
> **Output (default mode = forensic + strict):**
> "Pricing is hard. The three teams we audited all undercharged the same way: nobody had a number with a referent. Two of them fixed it in a week."
>
> **Diff:**
> - V3.1 META-COMMENTARY: "Let me walk you through this." and "As we'll see," deleted
> - V3.1 RHETORICAL-SETUPS: "What if I told you that..." → direct claim; "Think about it:" deleted; "and that's okay." removed
> - V3.1 LAZY-EXTREMES: "everyone" → "the three teams we audited" (specific)
> - V3.1 VAGUE-DECLARATIVE: "the reasons are structural" → the actual reason
> - PASS 4: the two-fragment close is within the 2-per-post cap and reads as paired declaratives, not a reveal bridge; left as is
