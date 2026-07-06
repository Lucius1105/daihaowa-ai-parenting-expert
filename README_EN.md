# AI Parenting Coach Skill

"Not to make children more obedient, but to help adults become calmer, more observant, and better-boundaried."

![License](https://img.shields.io/badge/License-MIT-green)
![Agent Skill](https://img.shields.io/badge/Agent%20Skill-Claude%20Code%20%7C%20Codex%20%7C%20WorkBuddy-blue)
![Language](https://img.shields.io/badge/Language-Chinese%20%7C%20English-orange)

2 parenting prompts × 1 complete Agent Skill × Family Context Card × 6-step resolution engine  
Parent-child conflict / homework meltdowns / screen boundaries / grandparent conflict / school transition / long-term education planning

[中文](README.md) | English

---

## 30-second start

If you only want copyable prompts:

- [AI Parenting Expert Prompt](prompts/en/parenting-expert-prompt.md)
- [Family Education Strategist Prompt](prompts/en/family-education-strategist-prompt.md)

If you want the full skill for Claude Code / Codex / WorkBuddy:

```bash
git clone https://github.com/Lucius1105/ai-parenting-coach-skill.git
```

Claude Code:

```bash
mkdir -p ~/.claude/skills
cp -R ai-parenting-coach-skill/skills/ai-parenting-coach ~/.claude/skills/
```

Codex:

```bash
mkdir -p ~/.codex/skills
cp -R ai-parenting-coach-skill/skills/ai-parenting-coach ~/.codex/skills/
```

WorkBuddy:

```bash
mkdir -p ~/.workbuddy/skills
cp -R ai-parenting-coach-skill/skills/ai-parenting-coach ~/.workbuddy/skills/
```

Then ask your agent:

```text
Use $ai-parenting-coach. My child is 6 and preparing for primary school. Grandma is the main caregiver. Recently writing practice and packing the school bag always turn into crying. Please first diagnose the issue, then give me a plan I can use tonight.
```

---

## What it is

In one sentence: this skill turns a parenting struggle into a Family Context Card, diagnoses where the issue is stuck, and then gives small, speakable, doable steps.

It does not:

- promote pressure-based parenting
- teach threats, shame, physical punishment, or control tactics
- pretend AI can replace parents, doctors, therapists, social workers, or lawyers

It helps with:

1. calming the adult first
2. diagnosing the developmental, state, relationship, and action layers
3. making the task small enough for the child to succeed
4. writing scripts for parents, grandparents, partners, and teachers
5. creating a 7-day micro-loop instead of trying to fix everything at once
6. flagging medical, mental-health, legal, or safety risks

---

## Why this exists

Many parents do not lack love. They lack a calm operating system in the middle of real parenting chaos.

Homework collapses, grandparent overreach, partner disagreement, phone rules that do not stick, school transition anxiety, and the daily guilt of "I yelled again" can wear parents down.

Most parenting content has two problems:

- it is too theoretical to use tonight
- or it treats the child as a problem to be fixed

This project packages coaching questions, family-system thinking, calm parenting principles, and practical scripts into an open-source AI parenting skill.

Goal:

> Help more parents reduce inner friction and become steadier; help more children feel less controlled and more seen.

---

## Two prompts

This repository releases two copyable prompts.

### 1. AI Parenting Expert Prompt

Paths:

```text
prompts/zh/parenting-expert-prompt.md
prompts/en/parenting-expert-prompt.md
```

Best for:

- parent-child conflict
- daily plans with kids
- learning routines
- emotional meltdowns
- screen boundaries
- parent / grandparent / teacher communication

### 2. Family Education Strategist Prompt

Paths:

```text
prompts/zh/family-education-strategist-prompt.md
prompts/en/family-education-strategist-prompt.md
```

Best for:

- school transition
- primary-school capability building
- intergenerational conflict
- absent-parent repair
- family-system boundaries
- long-term education planning from 0 to 18

---

## Complete Skill

The actual installable skill is:

```text
skills/ai-parenting-coach/SKILL.md
```

The skill includes two internal sanitized prompt modules:

```text
skills/ai-parenting-coach/references/parenting-expert-prompt.md
skills/ai-parenting-coach/references/family-education-strategist-prompt.md
```

Routing:

- everyday parenting issues → `parenting-expert-prompt.md`
- long-term planning / grandparent conflict / family-system issues → `family-education-strategist-prompt.md`

---

## Mandatory Flow: Family Context Card First

Every child and family is different. The agent must not give generic advice before collecting context.

The user should provide:

- Child: age, gender, school stage, personality, interests, strengths, current struggle
- Main caregivers: who spends the most time, who sets rules, who tends to lose emotional control
- Family members: roles of parents, grandparents, teachers, or other important adults
- Current issue: what happened in the latest concrete incident
- User goal: immediate conflict support, child-care planning, learning routines, or long-term planning
- Red flags: safety, health, school, domestic violence, or serious mental-health risks

If context is insufficient, the agent should ask first instead of giving generic advice.

---

## Safety Scope

This skill does not replace doctors, therapists, social workers, lawyers, or school professionals.

For self-harm, harm to others, severe school refusal, suspected depression, suspected ADHD, suspected autism spectrum condition, domestic violence, abuse, custody disputes, medication, or diagnosis, seek qualified local professional or emergency support.

---

## License and support

MIT License. Free and open.

If it helps you:

- Star this repository
- Share it with parents who need it
- Open an Issue with real-world scenarios
- A small coffee-support link may be added later
