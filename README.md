# Viral Content Skills

AI skills that create and evaluate content engineered to **spread** and **stick** — built on two classic, research-backed books:

- **[Contagious: Why Things Catch On](https://jonahberger.com/books/contagious/)** by Jonah Berger — the **STEPPS** framework: Social Currency, Triggers, Emotion, Public, Practical Value, Stories.
- **[Made to Stick: Why Some Ideas Survive and Others Die](https://heathbrothers.com/books/made-to-stick/)** by Chip Heath & Dan Heath — the **SUCCESs** framework: Simple, Unexpected, Concrete, Credible, Emotional, Stories.

Works with **Claude** (Claude Code, Claude.ai, Claude API) and **ChatGPT** (Custom GPTs, Projects, or plain chat).

## What's inside

| Skill | What it does |
|-------|--------------|
| [`viral-content-creator`](skills/viral-content-creator/SKILL.md) | Turns a raw idea into publish-ready content (posts, scripts, ads, emails, landing pages) by finding the core message, then deliberately applying STEPPS + SUCCESs levers. Outputs the content plus a "why this works" breakdown and alternative hooks. |
| [`viral-content-evaluator`](skills/viral-content-evaluator/SKILL.md) | Scores any content 0–5 across all 12 dimensions with quoted evidence, checks 7 fatal flaws (buried lede, curse of knowledge, gimmick hooks…), and returns a verdict — ✅ Publish / 🟡 Revise / 🔴 Rework — with concrete, prioritized fixes. |

```
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

The two skills are designed as a loop: **create → evaluate → revise**. The evaluator's verdict thresholds are the creator's self-check standards.

## Using with Claude

### Claude Code

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

The `chatgpt/` folder contains self-contained versions (frameworks inlined, no file references needed):

- **Quick use:** paste the whole file as the first message of a chat, then give your content brief.
- **ChatGPT Projects:** paste it into the project's custom instructions.
- **Custom GPT:** upload the file as a Knowledge file and set the Instructions to: *"Follow the workflow in content-creator-prompt.md for every content request."* (Same pattern for the evaluator.)

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

## Attribution & license

The STEPPS and SUCCESs frameworks are the intellectual work of **Jonah Berger** and **Chip & Dan Heath** respectively. This repository is an independent, educational distillation of those ideas into AI-usable instructions — it reproduces no book text and is not affiliated with or endorsed by the authors. If these skills are useful to you, buy the books; they're worth it.

Repository content is released under the [MIT License](LICENSE).
