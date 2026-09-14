---
name: viral-content-evaluator
description: Score and critique content against evidence-based stickiness and virality standards — the SUCCESs framework from "Made to Stick" and the STEPPS framework from "Contagious". Use whenever the user asks to review, rate, grade, critique, or QA any content (post, script, ad, email, headline, landing page, article), asks "is this good?", "will this go viral?", "why isn't this getting engagement?", or wants content checked against standards before publishing.
---

# Viral Content Evaluator

Judge a piece of content the way the research says audiences will: does it stick (get understood and remembered) and does it spread (get shared and acted on)? This skill produces a structured scorecard, a clear verdict, and prioritized fixes — not vague praise.

Two lenses, twelve dimensions:

- **Stickiness — SUCCESs** (Chip & Dan Heath, *Made to Stick*): Simple, Unexpected, Concrete, Credible, Emotional, Story.
- **Spreadability — STEPPS** (Jonah Berger, *Contagious*): Social Currency, Triggers, Emotion (high-arousal), Public, Practical Value, Story vehicle.

## Workflow

### Step 1: Establish context

Identify before judging:

- **The content** — exactly what text/script is being evaluated.
- **Audience** — who is it for?
- **Platform & format** — norms differ (a LinkedIn post is not a billboard).
- **Goal** — awareness/shares, memory/recall, or action/conversion.
- **Retention target** — if the piece must be remembered *for* something (a brand, a product benefit,
  a core idea), name it now. Step 5 tests whether it survives retelling.

If the user didn't state audience, platform, or goal, infer the most likely ones from the content itself and declare your assumptions in the report header. Do not stall the evaluation to ask.

Judge the piece as the brief commissioned it. Do not deduct for a delivery format the brief never
asked for — a video with on-screen cues is not penalized for failing in audio-only playback.

### Step 2: Load the rubric

Read `references/scoring-rubric.md` — it defines the 0–5 anchors for every dimension, the goal-based weighting, and the verdict thresholds. Score against those anchors, not your general taste.

### Step 3: Cold read as the audience

Before analyzing, read the content once as the target audience member, scrolling past it. Record three gut answers — they anchor the whole review:

1. Did the first line stop you?
2. Can you repeat the core message from memory, in one sentence?
3. Would you share it — and what would sharing it say about you?

### Step 4: Score the twelve dimensions

**Before scoring anything, decide which dimensions this format can carry.** Consult the applicability table in the rubric and name the N/A set for this piece up front: a single Instagram caption cannot design public observability, a 40-character headline cannot carry a story. Deciding this from the format first — rather than reaching for N/A halfway down the scorecard — is what stops you quietly assigning 2s to dimensions the brief never had room for, which silently drags strong work below the Publish line.

Then score every remaining dimension 0–5 using the rubric anchors. For every score, cite evidence — quote the exact phrase that earns or loses points. No score without a quote or a "nothing in the text does X" note.

N/A means "this brief has no room for it" — never "this piece did it badly". The test: could a better
version of *this same brief* — same medium, length, audience, available assets and scope — have scored
here? If yes, it is a low score. If no, it is N/A. You may not invent extra campaign assets to make a
dimension applicable, and a mechanism that was feasible but missing scores low rather than N/A. Say
which you concluded, in a clause, in the evidence cell. N/A dimensions are excluded from the average.

### Step 5: Check for fatal flaws

Each of these caps the verdict at "Revise" no matter how good the rest is. Because a fatal flaw overrides the arithmetic, it needs a firing condition precise enough that two evaluators reading the same text reach the same answer — so each one below states when it fires. If a weakness doesn't meet the stated bar, it belongs in Priority fixes, not here.

- **Buried lede** — unrelated or dispensable preliminary material delays *both* the core and the
  uncertainty the core answers. Quote the delayed core and the material obstructing it. An implied
  question counts, and so does context the audience genuinely needs to feel the gap: a mystery opening
  that poses the core's question is not a buried lede. Boundary cases are priority fixes, not flaws.
- **Curse of Knowledge** — jargon, abstractions, or insider assumptions the target audience can't decode without explanation.
- **No single core** — fires when Simple scores ≤ 2: two or more messages compete and the reader can't say what the point was.
- **Gimmick surprise** — the hook's promise is never cashed by the body, or the surprise is unrelated to the core idea.
- **Valueless virality** — fires for awareness/shares or recall goals. Write the piece's retellable
  content as one actor–action–outcome sentence, keeping whatever makes it worth repeating. If the
  retention target named in Step 1 is absent from that sentence and unnecessary to its payoff —
  appearing only as detached sponsorship or a sign-off — the piece buys attention it cannot keep
  (Evian's Roller Babies took a viewing record while sales fell). Ambiguous linkage is a priority fix.
- **Counterproductive social proof** — fires for behavior-change goals. The piece explicitly frames the
  unwanted conduct as widespread, normal, or socially endorsed among the audience's peers ("84% of
  young drivers text at the wheel"), which is how anti-drug ads raised drug use. Quote the framing.
  Harm statistics and plain mention of the behavior do not qualify.
- **Semantic stretch** — unverifiable superlatives ("revolutionary", "world-class", "unique") carrying a claim that no evidence in the piece supports. One stray adjective isn't enough; this fires when the superlatives *are* the argument.
- **Factual or credibility risk** — claims that are wrong, unsourced in a load-bearing position, or phrased to dodge a number the reader would want ("5 stars from everyone who reviewed it" hiding n=4). A widely known figure is not exempt: if it carries the argument and has no source, this fires.
- **Low-arousal emotional register — NOT a fatal flaw.** This was one in earlier versions of this
  skill; it is not one now. Do not list it as a fatal flaw, at any arousal score, for any goal. Low
  arousal is a scored weakness that the weighting already penalizes for awareness goals, and Berger's
  own evidence has genuinely useful content spreading with no arousal at all (hikers on a trail
  comparing vacuum cleaners). If arousal is weak, it belongs in Priority fixes.

That list is exhaustive. Do not invent additional fatal flaws, and do not reinstate retired ones.

### Step 6: Compute the verdict

Follow the rubric's weighting for the stated goal, then apply:

One algorithm, applied to the unrounded weighted average of non-N/A dimensions:

| Verdict | Criteria |
|---------|----------|
| 🔴 **Rework** | Weighted average < 2.5 — the core concept needs rethinking, not editing |
| 🟡 **Revise** | Weighted average < 4.0, or any fatal flaw present |
| ✅ **Publish** | Weighted average ≥ 4.0 and no fatal flaws |

There are no separate minimum-score gates on individual dimensions: the goal weighting already doubles
the dimensions that matter for the goal, and Berger's principles are independent enough that one
strong lever can carry a piece. The weights and the 4.0 / 2.5 thresholds are editorial heuristics for
consistent judgement — not measured probabilities that content will spread.

### Step 7: Write the report

ALWAYS use this exact template:

```
# Content Evaluation: [short label]

**Assumptions:** [audience / platform / goal, as stated or inferred]
**Verdict:** [✅ Publish | 🟡 Revise | 🔴 Rework] — [one-sentence justification]
**Weighted score:** X.X / 5

## Cold-read reactions
[The three gut answers from Step 3]

## Scorecard

### Stickiness (SUCCESs)
| Dimension | Score | Evidence |
|-----------|-------|----------|
| Simple | n/5 | "..." |
| Unexpected | n/5 | "..." |
| Concrete | n/5 | "..." |
| Credible | n/5 | "..." |
| Emotional | n/5 | "..." |
| Story | n/5 | "..." |

### Spreadability (STEPPS)
| Dimension | Score | Evidence |
|-----------|-------|----------|
| Social Currency | n/5 | "..." |
| Triggers | n/5 | "..." |
| Emotion (arousal) | n/5 | "..." |
| Public | n/5 or N/A | "..." |
| Practical Value | n/5 | "..." |
| Story vehicle | n/5 | "..." |

## Fatal flaws
[List any, or "None detected"]

## What works (keep these)
1. [strength + why, citing the principle]
2. ...

## Priority fixes
1. [Highest-leverage fix — state the problem, the principle, AND a concrete rewrite of the offending line]
2. ...
3. ...

## Suggested hook rewrite
[One rewritten opening line demonstrating the fixes]
```

## Judging discipline

- **Evidence over vibes.** Every claim in the report points at specific text.
- **Score the content, not the topic.** A boring treatment of an exciting subject scores low; a brilliant treatment of a dull subject scores high.
- **Calibrate to the goal.** A conversion email doesn't need viral reach; don't punish it for weak Social Currency — weight per the rubric.
- **Fixes must be actionable.** "Make it more emotional" is not a fix. "Replace the feature list with the customer's before/after moment — e.g. '...'" is.
- **Never invent evidence in a rewrite.** Your suggested lines are bound by the same rule as the
  writer's: no customer counts, review totals, performance figures, dates, or guarantees that the
  piece or brief did not supply. Where a rewrite needs a number the author has and you don't, leave a
  placeholder and say so. Preserve the exact claim when you restate it — "a plumber *starts* within 48
  hours" is not "installed within 48 hours".
- **Be honest.** A 2/5 labeled as "solid" helps no one. The user came for standards, not encouragement.
- Cap the report's length: three priority fixes, not ten. Prioritization is part of the service.

If the user asks you to fix the content after evaluating (or asks for the improved version), apply the priority fixes yourself — and if the `viral-content-creator` skill is available, follow its workflow for the rewrite.
