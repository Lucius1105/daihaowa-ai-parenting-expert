# DaihaoWa | AI Parenting Expert

"Not to make children more obedient, but to help adults become calmer, more observant, and better-boundaried."

![Version](https://img.shields.io/badge/Version-v1.0.1-blue)
![License](https://img.shields.io/badge/License-Free%20Non--Commercial-red)
![Agent Skill](https://img.shields.io/badge/Agent%20Skill-Claude%20Code%20%7C%20Codex%20%7C%20WorkBuddy-blue)
![Language](https://img.shields.io/badge/Language-Chinese%20%7C%20English-orange)

2 parenting prompts × 1 complete Agent Skill × Family Context Card × 6-step resolution engine  
Parent-child conflict / homework meltdowns / screen boundaries / grandparent conflict / school transition / long-term education planning

Current version: v1.0.1. Free for personal, family, public-interest, and non-commercial education use. Commercial use requires written permission.

[中文](README.md) | English

---

## 30-second start

If you only want copyable prompts:

- [AI Parenting Expert Prompt](prompts/en/parenting-expert-prompt.md)
- [Family Education Strategist Prompt](prompts/en/family-education-strategist-prompt.md)

If you want the full skill for Claude Code / Codex / WorkBuddy:

```bash
git clone https://github.com/Lucius1105/daihaowa-ai-parenting-expert.git
```

Claude Code:

```bash
mkdir -p ~/.claude/skills
cp -R daihaowa-ai-parenting-expert/skills/ai-parenting-coach ~/.claude/skills/
```

Codex:

```bash
mkdir -p ~/.codex/skills
cp -R daihaowa-ai-parenting-expert/skills/ai-parenting-coach ~/.codex/skills/
```

WorkBuddy:

```bash
mkdir -p ~/.workbuddy/skills
cp -R daihaowa-ai-parenting-expert/skills/ai-parenting-coach ~/.workbuddy/skills/
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

This project packages coaching questions, family-system thinking, calm parenting principles, and practical scripts into a source-available AI parenting skill that is free for personal and family use.

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

## Age Scope

v1.0 covers ages 0-18, but it does not treat every child the same.

The strongest and most recommended range in v1.0 is ages 3-12, especially:

- everyday parenting from preschool to primary school
- school transition
- homework, routines, procrastination, emotional meltdowns
- disagreement between parents and grandparents
- family rules, screen time, and parent-child connection

Other age ranges can also use it:

- Ages 0-3: better for safety, rhythm, attachment, and caregiver response.
- Ages 12-18: better for respect, negotiation, boundaries, privacy, study pressure, and long-term planning.

For diagnosis, medication, self-harm, harm to others, domestic violence, abuse, severe school refusal, or ongoing mental-health crisis, seek qualified local professional support first.

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

## Free License and Non-Commercial Use

This project is free for parents and caregivers. It is not sold as a course, and there is no paywall.

You may:

- use it for your own family
- share it with friends and other parents
- use it in public-interest, school, community, and non-commercial education settings
- study, copy, and adapt it while keeping attribution and the project link

Without prior written permission from the author, you may not use this project or derivative versions for commercial purposes, including but not limited to:

- paid courses, bootcamps, coaching, consulting, or paid communities
- commercial software, agents, SaaS products, plugins, prompt libraries, or membership materials
- rebranding and redistributing it for a fee
- commercial advertising, lead generation, or paid client delivery
- model training, dataset construction, or closed-source commercial products

The author reserves the right to pursue unauthorized commercial use. See [LICENSE](LICENSE) for the full terms.

---

## Support

If this skill helps you yell less, helps a child suffer less, or gives your family more clarity for long-term education, you are welcome to support the project at any level that feels right.

A child's education is a long-term and important project. One private tutoring session often starts around 200 RMB; if you find this prompt valuable for your family's long-term education, your support helps us keep maintaining and improving it for more children and families.

I am also a father. I want to create value openly and legitimately, including earning tuition for my own child through useful work. Thank you for your support and investment.

Suggested tiers:

- RMB 9.9: buy me a coffee
- RMB 199: buy me a meal
- RMB 1999: patron-level recognition

Donations are not purchases of services and do not create a consulting, course, or delivery relationship. The project remains free for personal, family, and non-commercial use. Commercial use still requires prior written permission.

![WeChat support QR code](assets/wechat-pay-qr.jpg)

---

## Author and Channels

Author: Xu Peilin / 阿徐教练 / Founder of 雨后甘霖

All-channel name: 阿徐教练 | 雨后甘霖

WeChat Official Account / WeChat Channels: 阿徐教练

---

## Version and Updates

- Current version: [v1.0.1](VERSION)
- Changelog: [CHANGELOG.md](CHANGELOG.md)
- License: [LICENSE](LICENSE)

If it helps you:

- Star this repository
- Share it with parents who need it
- Open an Issue with real-world scenarios
