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

If the user didn't state audience, platform, or goal, infer the most likely ones from the content itself and declare your assumptions in the report header. Do not stall the evaluation to ask.

### Step 2: Load the rubric

Read `references/scoring-rubric.md` — it defines the 0–5 anchors for every dimension, the goal-based weighting, and the verdict thresholds. Score against those anchors, not your general taste.

### Step 3: Cold read as the audience

Before analyzing, read the content once as the target audience member, scrolling past it. Record three gut answers — they anchor the whole review:

1. Did the first line stop you?
2. Can you repeat the core message from memory, in one sentence?
3. Would you share it — and what would sharing it say about you?

### Step 4: Score the twelve dimensions

Score each dimension 0–5 using the rubric anchors. For every score, cite evidence — quote the exact phrase that earns or loses points. No score without a quote or a "nothing in the text does X" note.

Mark a dimension **N/A** (excluded from averages) only when the format genuinely can't express it — e.g. Public observability for a private sales email — and say why. Never use N/A to excuse a weakness the format could have addressed.

### Step 5: Check for fatal flaws

Each of these caps the verdict at "Revise" no matter how good the rest is. Because a fatal flaw overrides the arithmetic, it needs a firing condition precise enough that two evaluators reading the same text reach the same answer — so each one below states when it fires. If a weakness doesn't meet the stated bar, it belongs in Priority fixes, not here.

- **Buried lede** — the single most interesting fact sits past the opening (below the fold, after the first ~20% of the piece), where the audience has already scrolled away.
- **Curse of Knowledge** — jargon, abstractions, or insider assumptions the target audience can't decode without explanation.
- **No single core** — fires when Simple scores ≤ 2: two or more messages compete and the reader can't say what the point was.
- **Gimmick surprise** — the hook's promise is never cashed by the body, or the surprise is unrelated to the core idea.
- **Low-arousal emotional register** — fires when Emotion (arousal) scores ≤ 2 **and the goal is awareness/shares**, because low arousal is what suppresses sharing. For a conversion or recall goal, weak arousal is a scored weakness, not a fatal flaw — a calm, credible ad can convert.
- **Semantic stretch** — unverifiable superlatives ("revolutionary", "world-class", "unique") carrying a claim that no evidence in the piece supports. One stray adjective isn't enough; this fires when the superlatives *are* the argument.
- **Factual or credibility risk** — claims that are wrong, unsourced in a load-bearing position, or phrased to dodge a number the reader would want ("5 stars from everyone who reviewed it" hiding n=4).

### Step 6: Compute the verdict

Follow the rubric's weighting for the stated goal, then apply:

| Verdict | Criteria |
|---------|----------|
| ✅ **Publish** | Weighted average ≥ 4.0, no goal-critical dimension below 3, no fatal flaws |
| 🟡 **Revise** | Weighted average ≥ 2.5, fixable with targeted edits (or any fatal flaw present) |
| 🔴 **Rework** | Weighted average < 2.5, or any goal-critical dimension ≤ 1 — the core concept needs rethinking, not editing |

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
- **Be honest.** A 2/5 labeled as "solid" helps no one. The user came for standards, not encouragement.
- Cap the report's length: three priority fixes, not ten. Prioritization is part of the service.

If the user asks you to fix the content after evaluating (or asks for the improved version), apply the priority fixes yourself — and if the `viral-content-creator` skill is available, follow its workflow for the rewrite.
