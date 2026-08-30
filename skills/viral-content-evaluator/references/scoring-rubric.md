# Scoring Rubric

Anchors for every dimension, goal-based weights, and verdict math. Score against these anchors, not general impressions. Frameworks: SUCCESs (Chip & Dan Heath, *Made to Stick*) and STEPPS (Jonah Berger, *Contagious*).

## How to use the anchors

Each dimension lists what 0, 3, and 5 look like. Interpolate for 1, 2, 4. When torn between two scores, take the lower one — inflation makes the report useless. Always attach evidence: the quoted phrase that earned the score, or the observation that nothing in the text attempts the dimension.

---

## Stickiness dimensions (SUCCESs)

### Simple — one core idea, ruthlessly prioritized

- **0** — No identifiable main point, or three-plus competing messages.
- **3** — A main point exists but shares space with secondary messages; a reader summarizing it would need two sentences.
- **5** — One core idea a stranger can repeat in one sentence after one read. Everything in the text serves it. Lede is not buried.

### Unexpected — breaks a pattern, opens a curiosity gap

- **0** — Fully predictable from the first line; reads like every other post in the genre.
- **3** — A surprising element exists but arrives late, or the hook over-promises what the body delivers.
- **5** — The opening violates an expectation or opens a knowledge gap the audience feels compelled to close, AND the surprise is "post-dictable" — once revealed, it clearly connects to the core idea.

### Concrete — sensory, specific, picturable

- **0** — Wall of abstractions: "solutions", "value", "excellence", "innovation".
- **3** — Some specifics, but key claims stay abstract ("saves you time" instead of "saves 40 minutes every morning").
- **5** — Specific numbers, named people, physical details, before/after images the reader can picture. Analogies map new ideas onto known schemas.

### Credible — the audience can believe it

- **0** — Unsupported superlatives, suspicious claims, or factual errors.
- **3** — Claims are plausible but rest on the author's say-so.
- **5** — Vivid authenticating details, statistics on a human scale, a testable claim ("count it yourself", "try it free"), authority or lived experience, or one flagship proof (Sinatra test).

### Emotional — makes the audience feel, targets identity

- **0** — Purely informational; no emotional register at all, or corporate self-congratulation.
- **3** — Names an emotion or pain point but doesn't make the reader feel it; appeals only to rational self-interest.
- **5** — Evokes a specific feeling through a specific person or moment (Mother Teresa principle: one individual beats a statistic). Appeals to identity — "people like you do things like this" — not just benefit.

### Story — narrative that carries the idea

- **0** — Pure exposition or feature list.
- **3** — An anecdote appears but is decorative — the idea survives without it.
- **5** — The idea is embedded in a narrative with a protagonist, tension, and resolution (challenge, connection, or creativity plot). Retelling the story retells the idea.

---

## Spreadability dimensions (STEPPS)

### Social Currency — sharing it makes the sharer look good

- **0** — Sharing this would make someone look like an ad relay.
- **3** — Mildly interesting to pass along; no insider or status angle.
- **5** — Contains remarkable, screenshot-worthy information; sharing signals intelligence, taste, or insider status. There's a "did you know…" the sharer gets credit for.

### Triggers — linked to frequent environmental cues

- **0** — Nothing ties the message to anything the audience regularly encounters.
- **3** — Tied to a cue, but a rare one (once-a-year event), or the link is incidental.
- **5** — Deliberately anchored to a frequent cue in the audience's daily life (morning coffee, Monday standup, checkout line) so the environment re-surfaces the message repeatedly.

### Emotion (arousal check) — the feeling is high-arousal

- **0** — Low-arousal register: contentment, mild sadness, polite satisfaction.
- **3** — Some activation, but diluted or generic.
- **5** — Strong high-arousal emotion: awe, amusement/humor, excitement, righteous anger, or urgency-producing anxiety. The reader is physiologically activated enough to act.

*(Scores here often diverge from SUCCESs-Emotional: a piece can be touching but calm — sticky, not shareable. That's exactly what this dimension catches.)*

### Public — visible, imitable, leaves residue

- **0** — Consumption and adoption are completely private.
- **3** — Shareable artifact exists but nothing marks participation.
- **5** — Designed observability: a hashtag identity, a template others copy, a visible badge/artifact, behavioral residue that keeps advertising after the moment. Built to show, built to grow.
- **N/A allowed** for genuinely private formats (1:1 email, internal memo) — but check whether a public component was possible and missed.

### Practical Value — genuinely useful, packaged to forward

- **0** — No utility to the recipient.
- **3** — Useful but generic advice available anywhere, or utility buried in promotion.
- **5** — Specific, actionable, immediately usable value (numbers, steps, thresholds) packaged so forwarding it is an act of helping a friend. Narrow beats broad.

### Story vehicle — the brand/idea is inseparable from the tale

- **0** — No narrative to retell.
- **3** — A retellable story exists, but the idea/brand drops out when people retell it (Panda-cheese problem: great story, forgettable sponsor).
- **5** — The story is a Trojan horse: it cannot be retold without transmitting the core idea/brand (valuable virality, like Blendtec's "Will It Blend?").

---

## Goal-based weighting

Compute the weighted average with these multipliers (dimension score × weight, divided by total weights of non-N/A dimensions):

| Dimension | Awareness / shares | Memory / recall | Action / conversion |
|---|---|---|---|
| Simple | 1 | 2 | 2 |
| Unexpected | 2 | 2 | 1 |
| Concrete | 1 | 2 | 2 |
| Credible | 1 | 1 | 2 |
| Emotional | 1 | 1 | 2 |
| Story (SUCCESs) | 1 | 2 | 1 |
| Social Currency | 2 | 1 | 1 |
| Triggers | 1 | 2 | 1 |
| Emotion (arousal) | 2 | 1 | 1 |
| Public | 2 | 1 | 0.5 |
| Practical Value | 2 | 1 | 1 |
| Story vehicle | 1 | 1 | 0.5 |

**Goal-critical dimensions** (used in verdict rules):

- Awareness/shares: Social Currency, Emotion (arousal), Unexpected
- Memory/recall: Simple, Concrete, Triggers
- Action/conversion: Concrete, Credible, Emotional

## Verdict rules

1. Any **fatal flaw** (see SKILL.md Step 5) → at best 🟡 Revise.
2. Any goal-critical dimension ≤ 1 → 🔴 Rework.
3. Weighted average ≥ 4.0 AND all goal-critical dimensions ≥ 3 AND no fatal flaws → ✅ Publish.
4. Weighted average ≥ 2.5 → 🟡 Revise.
5. Otherwise → 🔴 Rework.

## When a dimension is N/A

Scoring a dimension the format structurally cannot carry punishes the writer for the brief, not the work — and it silently drags the weighted average below the Publish line no matter how good the copy is. Mark it N/A (excluded from the average) when the format has no room to express it, and say so in the evidence cell.

Common, legitimate N/A calls:

| Format | Usually N/A | Why |
|---|---|---|
| Single ad, IG caption, subject line | Public | One post can't design observability or behavioral residue; that's a campaign-level or product-level decision. |
| Short-form commerce copy for a decorative/keepsake product | Practical Value | The product's value is emotional, not informational — there is no useful tip to forward. |
| Any piece under ~60 words, headline, or hook alone | Story, Story vehicle, Triggers | Not enough room for narrative or a cue to be planted. |
| 1:1 email, internal memo, transactional message | Public, Social Currency | Not shared onward by design. |

The discipline that keeps this honest: ask whether a *better version of this same brief* could have scored on the dimension. If yes, score it low. If no, mark N/A. "An Instagram caption can't build Public visibility" is a fair N/A; "this caption didn't bother being remarkable" is a 1, not an N/A.

## Calibration notes

- A typical competent-but-forgettable corporate post scores 2.0–2.8 weighted. That is normal — say so plainly.
- Short-form commerce copy that scores 3.5–3.9 is genuinely good work with one real gap left. Don't round it up to Publish to be nice, and don't describe it as weak — name the one gap and say the rest is strong.
- Scores of 5 should be rare and quotable: if you give a 5, the evidence cell should contain a line worth stealing.
- Long content (articles, scripts) is scored on its weakest load-bearing part: a great body with a dead headline fails at Unexpected, because nobody reaches the body.
- When evaluating a headline/hook alone, score Triggers, Public, and Story vehicle as N/A unless present, and say the evaluation is partial.
