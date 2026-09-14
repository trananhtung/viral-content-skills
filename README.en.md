# Viral Content Skills

AI skills that create and evaluate content engineered to **spread** and **stick** — built on two classic, research-backed books:

- **[Contagious: Why Things Catch On](https://jonahberger.com/books/contagious/)** by Jonah Berger — the **STEPPS** framework: Social Currency, Triggers, Emotion, Public, Practical Value, Stories.
- **[Made to Stick: Why Some Ideas Survive and Others Die](https://heathbrothers.com/books/made-to-stick/)** by Chip Heath & Dan Heath — the **SUCCESs** framework: Simple, Unexpected, Concrete, Credible, Emotional, Stories.

Works with **Claude** (Claude Code, Claude.ai, Claude API) and **ChatGPT** (workspace plugins, uploaded skills, Projects, or plain chat). The repo ships a `.claude-plugin/plugin.json` manifest, so both platforms can install it straight from GitHub.

## What's inside

| Skill | What it does |
|-------|--------------|
| [`viral-content-creator`](skills/viral-content-creator/SKILL.md) | Turns a raw idea into publish-ready content (posts, scripts, ads, emails, landing pages) by finding the core message, then deliberately applying STEPPS + SUCCESs levers. Outputs the content plus a "why this works" breakdown and alternative hooks. |
| [`viral-content-evaluator`](skills/viral-content-evaluator/SKILL.md) | Scores any content 0–5 across all 12 dimensions with quoted evidence, checks 8 fatal flaws (buried lede, curse of knowledge, valueless virality, social proof that normalizes the behavior you're fighting…), and returns a verdict — ✅ Publish / 🟡 Revise / 🔴 Rework — with concrete, prioritized fixes. |

```
.claude-plugin/
├── marketplace.json                      # manifest: Claude Code + ChatGPT plugin import
└── plugin.json                           # the plugin's own metadata
skills/
├── viral-content-creator/
│   ├── SKILL.md                          # workflow: brief → core → engineer → draft → self-check
│   └── references/
│       ├── contagious-stepps.md          # STEPPS distilled: psychology, tactics, examples
│       └── made-to-stick-success.md      # SUCCESs distilled: psychology, tactics, examples
├── viral-content-evaluator/
│   ├── SKILL.md                          # workflow: context → cold read → score → flaws → verdict
│   └── references/
│       └── scoring-rubric.md             # 0–5 anchors, goal-based weights, verdict thresholds
chatgpt/
├── content-creator-prompt.md             # self-contained prompt version for ChatGPT
└── content-evaluator-prompt.md           # self-contained prompt version for ChatGPT
```

The two skills are designed as a **bounded** loop: create → evaluate → revise once → optionally re-evaluate once → stop. The evaluator receives the brief, the evidence inventory and the draft — never the creator's "why this works" rationale, which argues the case the evaluator is supposed to test independently. Only fixes that stay inside the brief and the available evidence get applied; a score never authorizes inventing evidence.

## Using with Claude

### Claude Code

The repo is a plugin, so the shortest route is a marketplace install:

```bash
claude plugin marketplace add trananhtung/viral-content-skills
claude plugin install viral-content-skills@viral-content-skills
```

Or copy the skill folders by hand:

```bash
git clone https://github.com/trananhtung/viral-content-skills.git
mkdir -p ~/.claude/skills
cp -r viral-content-skills/skills/viral-content-creator ~/.claude/skills/
cp -r viral-content-skills/skills/viral-content-evaluator ~/.claude/skills/
```

(Or copy into a project's `.claude/skills/` to scope them to one repo.) Then just ask naturally — *"write a LinkedIn post announcing our new feature"* or *"review this tweet before I post it"* — and Claude invokes the skill. You can also trigger explicitly with `/viral-content-creator`.

### Claude.ai / Claude Desktop

Zip each skill folder (the folder containing `SKILL.md`) and upload it under **Settings → Capabilities → Skills**.

### Claude API / Agent SDK

Pass the skill folder via the skills feature of the Agent SDK, or inline `SKILL.md` + references into your system prompt.

## Using with ChatGPT

These skills already use ChatGPT's own skill format, so nothing needs converting. Which route you take
depends on your plan, and on a personal plan it takes about a minute.

### On a personal plan (Free, Go, Plus, Pro)

This covers most people. Set up one Project, drop two files in, and you are done for good.

**Step 1.** Save these two files to your computer (right-click, Save as):

- [content-creator-prompt.md](https://raw.githubusercontent.com/trananhtung/viral-content-skills/main/chatgpt/content-creator-prompt.md)
- [content-evaluator-prompt.md](https://raw.githubusercontent.com/trananhtung/viral-content-skills/main/chatgpt/content-evaluator-prompt.md)

**Step 2.** In ChatGPT, create a new Project and drag both files into its files area.

**Step 3.** Paste exactly this into the project's instructions:

```
When I ask you to write or improve content, follow the workflow in content-creator-prompt.md.
When I ask you to score, review, or judge whether content is good, follow content-evaluator-prompt.md.
```

That's it. Open that project and ask normally from now on.

For one-off use, skip the Project: start a new chat, attach one file, say "follow this file", then give
your brief.

### On a Business, Enterprise, Healthcare, or Edu workspace

These plans have Plugins and Skills, so ChatGPT invokes a skill without you opening the right project.

An admin goes to **Workspace settings → Plugins → Add → Import marketplace**, sets Source to
`https://github.com/trananhtung/viral-content-skills`, leaves Path and Branch empty, and imports. Then
open the imported plugin to set its Installation policy.

Without admin rights, zip each skill folder and use **Plugins → Skills tab → Create → Upload from your
computer**:

```bash
cd skills
zip -r viral-content-creator.zip viral-content-creator
zip -r viral-content-evaluator.zip viral-content-evaluator
```

Once installed, invoke with `@viral-content-creator` and `@viral-content-evaluator`, or let ChatGPT
pick. The marketplace syncs with the repo daily.

### A note on Custom GPTs

If you find an older guide telling you to build a Custom GPT and attach a Knowledge file, it is out of
date. OpenAI is retiring Custom GPTs: personal accounts can no longer create new ones, and Enterprise
retirement is planned for Dec 11, 2026.

## Example prompts

```
Write a launch tweet thread for a $19 budgeting app for freelancers. Goal: sign-ups.
```

```
Evaluate this LinkedIn post — audience is CTOs, goal is awareness:
[paste your draft]
```

```
This email got a 2% open rate. Diagnose it and rewrite the subject line.
```

## Examples

Real output from both skills, generated for a live store ([lunavows.com](https://lunavows.com)):

- [`examples/instagram-caption-ring-dish.md`](examples/instagram-caption-ring-dish.md) — Instagram caption, goal: shares
- [`examples/meta-ad-embroidered-sweatshirt.md`](examples/meta-ad-embroidered-sweatshirt.md) — Meta ad, goal: conversion
- [`examples/email-gothic-tapestry.md`](examples/email-gothic-tapestry.md) — marketing email, goal: conversion
- [`examples/evaluation-report-sample.md`](examples/evaluation-report-sample.md) — a full scorecard from the evaluator

### Benchmark

Three briefs were written twice — once by an agent following `viral-content-creator`, once by an agent given the identical brief and no skill — then all six were scored blind by independent evaluator agents that did not know which was which. A deliberately generic "corporate announcement" post was slipped into the same blind set as a calibration control.

| Brief | With skill | Baseline | Delta |
|---|---|---|---|
| Instagram caption (shares) | 3.8 | 3.4 | +0.4 |
| Meta ad (conversion) | 3.6 | 3.1 | +0.5 |
| Marketing email (conversion) | 3.8 | 3.0 | +0.8 |
| **Mean** | **3.73** | **3.17** | **+0.57** |
| Generic control post | — | 0.9 | — |

Largest per-dimension gains: Simple, Unexpected, Emotion (arousal), and Story vehicle, all +1.0. The control scoring 0.9 against real copy at 3.0–3.8 is the evidence that the rubric discriminates rather than flattering everything it reads.

### Reliability

The identical seven texts were then re-scored by a second, independent set of judges after the rubric fixes. Scores barely moved — mean absolute shift 0.10 points, maximum 0.2 — and the skill-versus-baseline gap held at +0.60. Per-dimension, the two judge sets agreed exactly 79% of the time and landed within one point 100% of the time. The control scored 0.9, 0.9, and 0.8 across three independent runs.

That stability is the point: a rubric whose verdict depends on which judge happens to read the piece is not a standard. These numbers say the scorecard is reproducible.

> **Note:** the benchmark and reliability numbers above were produced under the v1 rubric. The verdict
> algorithm changed in the book-fidelity revision (goal-critical minimum-score gates removed, low
> arousal demoted from fatal flaw to scored weakness, two fatal flaws added), so those scores are not
> directly comparable to scores produced today. The discrimination check was re-run under the current
> rubric and held: see below.

### Validation of the revised rubric

Five English briefs (B2B LinkedIn post, TikTok script, fundraising email, blog opening, road-safety
PSA) were written by the creator and scored blind by separate evaluator agents that never saw the
creator's rationale. Two adversarial pieces were then written specifically to trip the new fatal-flaw
gates, and two calibration pieces checked that discrimination survived the rubric change.

| Check | Under v1 rubric | Under current rubric |
|---|---|---|
| Generic corporate launch post (control) | 0.3 🔴 Rework | 0.24 🔴 Rework |
| Strong hand-written LinkedIn post | 4.1 ✅ Publish | 4.1 ✅ Publish |
| B2B LinkedIn post, awareness goal | 3.9 🟡 Revise | 3.8 🟡 Revise |
| Road-safety PSA, behavior-change goal | 3.93 🟡 Revise | **4.3 ✅ Publish** |
| Reels ad whose brand is detachable | — | 2.6 🟡 Revise, **valueless virality fires** |
| PSA leading with "84% of drivers your age text" | — | 2.9 🟡 Revise, **counterproductive social proof fires** |

The PSA gained 0.37 because the creator now gets the trigger mechanics (recurrence, association
strength, and firing where the action is possible) and the social-proof warning in the workflow itself,
rather than buried in a reference file — it dropped the 84% statistic on its own and said why. The
LinkedIn post lost 0.1 because the stricter N/A test scores a feasible-but-missing mechanism instead of
excusing it. Both new gates fired only on the pieces built to trip them, and were explicitly considered
and correctly declined on the four legitimate pieces.

### What the numbers are and aren't

The 0–5 anchors, the goal weights, and the 4.0 / 2.5 thresholds are **editorial heuristics** that make
judgement reproducible between evaluators. Neither book supplies them. They are not measured
probabilities that a piece will spread, and no result here is validated against real audience
outcomes — every score in this repository is one model judging another model's writing.

## Attribution & license

The STEPPS and SUCCESs frameworks are the intellectual work of **Jonah Berger** and **Chip & Dan Heath** respectively. This repository is an independent, educational distillation of those ideas into AI-usable instructions — it reproduces no book text and is not affiliated with or endorsed by the authors. If these skills are useful to you, buy the books; they're worth it.

Repository content is released under the [MIT License](LICENSE).
