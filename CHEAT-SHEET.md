---
title: AI Orchestration · Cheat Sheet
workshop: WebMD Health Services VN · 04/05/2026
instructor: Tony Bùi
purpose: 1-page reference. Print it. Pin it. Pass it to a teammate.
---

# AI Orchestration · 1-Page Cheat Sheet

> Same model. Same task. Different prompt. **That gap is the work.**

---

## RCTCO — the 5 slots every prompt needs

| Slot | Question | One-line example |
|---|---|---|
| **R** Role | Who is the AI being? | *"You are a senior BA reviewing a wellness-platform spec."* |
| **C** Context | What can't AI guess? | *"WebMD ONE · members · HIPAA · 2-week sprints. Spec attached."* |
| **T** Task | One verb · one outcome | *"Draft 5 user stories with AC for the consent flow."* |
| **C** Constraints | What NOT to do | *"Cite spec section. Don't invent regulations. Mark unknowns [TBC]."* |
| **O** Output | Force a shape | *"Markdown table. Columns: Story \| AC (G/W/T) \| Spec ref \| Flag."* |

**Skip a slot → fail one of the 5 tests below.**

---

## The 5 patterns — what your work actually is

| # | Pattern | Verb | Use when… |
|---|---|---|---|
| 1 | **Drafter** | draft | You need a first version (stories, copy, spec, email) |
| 2 | **Synthesizer** | synthesize | Many inputs → one summary (interviews, research, threads) |
| 3 | **Reviewer** | review | Score existing work (specs, PRDs, designs, prompts) against your explicit rubric |
| 4 | **Critic** | critique | Stress-test an unproven plan — find edge cases, failure modes, missing scenarios |
| 5 | **Translator** | translate | One format → another (PRD → tickets, spec → AC, EN → VN) |

**Senior move:** name the pattern *before* you write the prompt. RCTCO follows.

---

## The 5 tests — does your prompt pass?

Score 1–5 each. **Total /25.** Below 18 = personal trick. 18+ = team asset. 22+ = context-injected.

| # | Test | Question |
|---|---|---|
| 1 | **Reproducibility** | Can a teammate paste this and get the same shape of output? |
| 2 | **Boundedness** | Does it tell AI what NOT to do? (no invented regs, no paraphrased AC, no fake quotes) |
| 3 | **Testability** | Can you score the output against an explicit rubric? |
| 4 | **Reusability** | Will you / your team run this 5+ times this quarter? |
| 5 | **Auditability** | Can compliance / a reviewer trace every claim back to source? |

---

## The 3-turn loop — iterate, don't restart

```
TURN 1 · BUILD     paste bare task → Coach asks 5 RCTCO questions → assemble draft
TURN 2 · AUDIT     paste draft → Coach scores /25 → names 2 highest-impact fixes
TURN 3 · INJECT    add team vocab + DoD + 1 real example → re-audit → 22+/25
```

**Most prompts hit 14-16 on first try.** Adding Constraints + Output shape jumps to 19-22. Inject context → 22+.

---

## Context Card — the asset that compounds

Paste this **before** any prompt. Edit once. Reuse forever.

```
TEAM CONTEXT (paste me first)

Vocab — words my team uses:
  • "member" not "user"
  • "engagement" not "DAU"
  • [your team's words]

DoD — definition of done:
  • AC in Given/When/Then format
  • [COMPLIANCE — HIPAA] flag if PHI touched
  • Story points TBC if unknown
  • [your team's bar]

Example — one real past output:
  [paste a real ticket / story / spec your team shipped]

When I ask for X, mirror this style.
```

**This is the leverage Coach can't give you. Only you can.**

---

## When a prompt breaks — diagnose by RCTCO

| Symptom | Likely missing slot | Fix |
|---|---|---|
| Output invents facts / quotes | **Constraints** | Add "Don't invent X. Mark unknowns [TBC]." |
| Wrong format / shape | **Output** | Force exact structure (table columns, JSON keys) |
| Generic / doesn't sound like your team | **Context** (no vocab/DoD) | Paste Context Card first |
| Skips compliance / safety items | **Constraints** | Add explicit flag rule per regulated item |
| Too long / wrong length | **Output** | Specify length: "max 5 bullets · max 200 words" |
| Output is good but inconsistent run-to-run | **Role + Output** | Add Role line + force exact output shape |

---

## The ladder — where good prompts live

```
PROMPT  →  PROJECT  →  REPO  →  SKILL
1 chat     1 team       team-shared      production / autopilot
```

- **Prompt** — what most people stop at. Lucky in your hands only.
- **Project** — Coach lives here. Knowledge files attached. Reusable.
- **Repo** — `prompts/<pattern>/` folder in Git. Versioned. PR-reviewed. Team standard.
- **Skill** — deployable wrapper around a Project. Runs on autopilot. Session 2 territory.

---

## Coach commands (paste any of these)

| Mode | What you paste | What Coach does |
|---|---|---|
| **Build** | a bare 1-line task | asks 5 RCTCO questions tailored to your task → assembles + audits |
| **Audit** | a drafted prompt | scores /25 on the 5 tests → names 2 highest-impact fixes |
| **Diagnose** | an output that disappointed you | traces failure to which RCTCO slot you missed |

**Coach never runs your prompt for you.** It coaches the prompt. You run it. *That separation is the discipline.*

---

## The contract

By 12:30 you walk out with **4 things in your pocket**:

1. **Coach** — same link, opens Monday afternoon
2. **Context Card** — YOUR team's voice (you made it in Round 3)
3. **This cheat sheet** — print it, pin it
4. **The repo idea** — bring `prompts/` folder to your tech lead Monday

**If you leave without all four — the session failed.**

---

*Tony Bùi · vibery.app · See you May 11 for Session 2 — we turn Coach into a skill that runs on autopilot.*
