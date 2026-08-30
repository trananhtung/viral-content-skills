---
name: viral-content-creator
description: Create content engineered to spread and stick, using the STEPPS framework from Jonah Berger's "Contagious" and the SUCCESs framework from Chip & Dan Heath's "Made to Stick". Use whenever the user wants to write, rewrite, or improve a social media post, ad, blog post, video script, email, landing page, slogan, product announcement, campaign message, or any content meant to be shared, remembered, or acted on — even if they never mention virality, marketing frameworks, or these books by name.
---

# Viral Content Creator

Turn a raw idea into content that people understand, remember, share, and act on. This skill applies two evidence-based frameworks together:

- **SUCCESs** (Made to Stick, Chip & Dan Heath) makes an idea *stick*: Simple, Unexpected, Concrete, Credible, Emotional, Stories.
- **STEPPS** (Contagious, Jonah Berger) makes it *spread*: Social Currency, Triggers, Emotion, Public, Practical Value, Stories.

Sticky but unshared content dies quietly; shareable but unmemorable content is noise. Good content needs both, so run every draft through both lenses.

## Workflow

### Step 1: Understand the brief

Establish before writing:

- **Core idea** — what is the message about?
- **Audience** — who must care? What do they already know, want, fear?
- **Format & platform** — tweet/X thread, LinkedIn post, TikTok/Reels script, blog post, email, landing page, ad, presentation…
- **Goal** — awareness (reach/shares), memory (brand/message recall), or action (click, buy, sign up, change behavior)?
- **Voice constraints** — brand tone, taboos, length limits.

If details are missing, make sensible assumptions, state them explicitly at the top of your answer, and proceed. Only ask questions when the answer would genuinely change the content's direction.

### Step 2: Find the core (before writing anything)

The number one failure mode is the **Curse of Knowledge**: you know the topic so well that you communicate in abstractions the audience can't feel. Fight it with forced prioritization:

1. Write the single most important idea in one plain sentence — the "Commander's Intent". If the audience remembers only this, the content succeeded.
2. If you have three main points, you have none. Cut until one survives.
3. Don't bury the lede: the core goes in the hook, not the conclusion.

### Step 3: Load the frameworks

Read both reference files now — they contain the detailed tactics, psychology, and examples you will draw from:

- `references/made-to-stick-success.md` — how to make the core idea stick (SUCCESs)
- `references/contagious-stepps.md` — how to make it spread (STEPPS)

### Step 4: Engineer the content

Select levers deliberately — strong content usually works 3–5 of these hard rather than all 12 weakly. Choose based on the goal:

| Goal | Prioritize |
|------|------------|
| Awareness / shares | Social Currency, high-arousal Emotion, Practical Value, Unexpected |
| Memory / recall | Simple, Concrete, Triggers, Stories |
| Action / conversion | Concrete, Credible, Emotional (identity), Practical Value |

Engineering moves, in rough order of leverage:

1. **Hook with a knowledge gap.** Open by making the audience realize there's something they don't know but want to (Unexpected). Break a pattern, ask a mystery question, or lead with the most surprising concrete fact. The surprise must be "post-dictable" — connected to the core, not a gimmick.
2. **Make the sharer look good** (Social Currency). Would passing this along make someone seem smart, in-the-know, or generous? Find the inner remarkability in the idea; give people an insider fact or a status marker.
3. **Attach a trigger.** Link the message to something the audience encounters often (a day of the week, a daily habit, a common phrase or object) so the environment keeps re-advertising it. Top of mind → tip of tongue.
4. **Pick a high-arousal emotion.** Awe, amusement, excitement, and even anger or anxiety drive sharing; sadness and mere contentment suppress it. When we care, we share — focus on feelings, not function. For action goals, appeal to identity ("people like you do things like this"), not just self-interest.
5. **Be concrete.** Sensory nouns, specific numbers on a human scale, real people with names. Replace every abstraction with something you can picture. Use schemas and analogies ("X is Y for Z") to teach fast.
6. **Earn credibility.** Vivid specific details, statistics rescaled to human terms, a testable claim ("try it yourself"), or one flagship proof that passes the Sinatra test ("if it worked there, it works anywhere").
7. **Deliver practical value.** Package genuinely useful advice so sharing it is an act of helping a friend. Narrow and specific beats broad and generic.
8. **Wrap it in a story when possible.** Stories are Trojan horses: make the product or idea integral to the plot so the story can't be retold without it. Prefer found stories (real customers, real events) over invented ones.
9. **Make it public / visible** (when the format allows). Design behavioral residue — something that keeps advertising after the moment passes: a hashtag identity, a template others copy, a visible artifact.

### Step 5: Draft with format discipline

- **Hook (first line / first 2 seconds):** curiosity gap or surprising concrete fact. Never open with context-setting or throat-clearing.
- **Body:** one core idea, concrete language, shortest path. Inverted pyramid — most important first.
- **Close:** a single clear call to action (or the punchline that closes the curiosity gap). One CTA, not three.
- Respect platform norms: line breaks and skimmability for LinkedIn, brevity for X, spoken-word rhythm and visual cues for video scripts, subject line = hook for email.

### Step 6: Self-check and revise once

Before delivering, score your draft honestly against these questions. Fix anything that fails, then stop — one revision pass, not endless polishing:

- Can a stranger repeat the core idea after one read?
- Does the first line open a gap that the rest closes?
- Is there a single sentence a reader would screenshot or quote?
- What exact emotion does it evoke, and is it high-arousal?
- Would sharing this make the sharer look good?
- Is anything abstract that could be concrete?
- Is there jargon only an insider understands? (Curse of Knowledge check)

If the `viral-content-evaluator` skill is available and the user wants a rigorous score, hand the draft to it.

## Output format

Deliver in this structure:

```
## [Content title / format]

[Assumptions made, if any — 1-2 lines]

[THE CONTENT — ready to publish, formatted for the platform]

---
**Why this works:** [3-5 bullets mapping specific choices to principles, e.g.
"Hook opens a curiosity gap (Unexpected) with a concrete number (Concrete)"]

**Alternative hooks:**
1. [variant]
2. [variant]
```

Keep the "why" section short — the content is the deliverable, the analysis is the receipt.

## Common failure modes to avoid

- Listing features instead of telling one story.
- Three messages in one piece (= zero messages).
- A clever surprise unrelated to the core idea (gimmick).
- Low-arousal emotional appeals ("we're proud to announce…").
- Abstract virtue words — "innovative", "world-class", "unique" — instead of evidence (semantic stretch).
- Burying the remarkable fact in paragraph four.
- Optimizing only for shares when the goal is conversion, or vice versa.
