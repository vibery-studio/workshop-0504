---
type: workshop-slide-outline
session: 2
status: draft-for-review
created: 2026-05-09
design_principles:
  - one idea per slide
  - image > words (Moleskine hand-drawn style, reuse Session 1 pipeline)
  - speaker notes ≠ slide content
  - interactive: side-by-side comparisons, progressive reveals
  - 22pt minimum body, big quote slides, breathing room
target_count: 28-32 slides for 180 min
---

# Session 2 — Slide Outline

> Design intent: slides are **for the audience to look at and remember**, not for Tony to read. Speaker notes carry the script. Slides carry the image and ONE idea. If a slide has more than one idea, it's two slides.

## Visual system

- **Background:** Moleskine cream paper (reuse Session 1 — `images/` already has 9 comic-style frames generated via Codex)
- **Primary text:** hand-drawn-feel font, 32pt+ for headlines, 22pt min for body
- **Accents (WebMD HS color hat-tip):**
  - **Cyan/teal underline** (~`#3BC6D9`) — used under ONE key word per slide, mimicking WebMD's "Everything" highlight pattern. Quiet "I see you" without copying their layout.
  - **Navy** (~`#1E2A78`) — sparingly, for strongest single-word emphasis (e.g., circled YOU on the WebMD-echo slide)
  - **No red** — was a wrong earlier guess. Drop entirely.
- **Other:** arrows + speech bubbles for interaction; hand-drawn ink on cream remains the dominant visual.
- **Interaction patterns** (from research):
  - **Side-by-side compare** — when teaching distinctions (skill vs subagent, prompt vs skill, harness A vs B)
  - **Progressive reveal** — when teaching steps (the 4-question filter; the 5-check audit)
  - **Big quote** — survey quotes from Nga/Esteban/Duy as anchors
  - **Live whiteboard moments** — slide is a prompt, not an answer (Module 3 4-question filter, rubric scoring)

---

## Slide-by-slide map (180 min, ~30 slides)

### Part 1 — 60 min · ~12 slides

| #   | Slide                                                       | Type           | Image / asset                                                                                                      | Speaker note hook                                                      |
| --- | ----------------------------------------------------------- | -------------- | ------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------- |
| 1   | Title — "Build Your Own Skill — From Task to Running Agent" | Hero           | Moleskine cover frame: hand drawn "skill" word with arrow                                                          | "S2 picks up where S1 ended — today we move from prompt to skill."     |
| 2   | Recap S1 in 3 icons                                         | Visual recap   | 3 hand-drawn icons: brief · iteration · context card                                                               | 60 sec recap, no speaking from slides                                  |
| 3   | Survey quote (anon)                                         | Quote slide    | Hand-drawn speech bubble with quote: *"AI as my personal assistant"* — attributed only "— a designer in this room" | "Someone in this room wrote this last week. Today we deliver it."      |
| 4   | Survey quote (anon)                                         | Quote slide    | *"Build my own skills/agents… fully automated AI workflow"* — "— a designer in this room" | Pair with #3 — this is what's coming                                   |
| 5   | **THE REFRAME — the floor moved up** (NEW)              | Side-by-side compare | LEFT: full agent stack — n8n, Dify, LangChain, Zapier — drawn neatly (NOT chaotic), labeled *"The full agent stack — still useful for what it's useful for."* RIGHT: one markdown file `my-task.md`, labeled *"The smallest thing that works for most product tasks."* Below: hand-drawn line *"Start here. Graduate when you actually need to."* (teal underline under "the floor moved up" in headline) | "Honesty check. If you've built workflows in n8n or Dify — that work is real. Those tools still earn their keep — multi-step orchestration, hosted execution, non-LLM nodes. Not going away. But here's what changed in the last 12 months: for **most product tasks** — drafting tickets, synthesizing interviews, prepping a 1:1 — you can skip that whole stack. Just a markdown file, loaded by Claude. Not because n8n is wrong, but because **the floor moved up**. The simplest thing got more capable. So today: start at the floor. If your task outgrows it — and some will — graduate. But don't start where you have to learn an orchestration framework before you can ship anything." |
| 5b  | **The comparison — pick the smallest thing that works** (NEW)  | Full-image 3-column compare | Landscape Moleskine page, 3 columns: COL 1 *"Real AI agent"* (tangled LangChain/Dify/n8n + agent loop arrows · ✓ Autonomous, branching, multi-step planning · ✗ Hosting, hard to debug, year of learning). COL 2 *"Skill + MCP + small script"* (one markdown file + plug icon + tiny script icon · ✓ Predictable, auditable, diff-able, local, editable in 60 sec · ✓ "If you can write Confluence, you can do this"). COL 3 *"When you need the big stack"* (small list: true branching · non-LLM nodes · event-driven · "Graduate when you actually need it"). Headline above: *"Both are real. Pick the smallest one that works."* | "OK so where's the line. The middle column is what we're building today. The left column is what real AI agents look like — they exist, they have a place, your engineering team probably already uses some of these for CI automation or data pipelines. But look at the middle column. Read each row. **Predictable. Auditable. Diff-able. Local. Editable in 60 seconds.** For your daily product work — drafting tickets, synthesizing interviews, prepping a 1:1, generating a digest — that's enough. That's more than enough. That's actually **better** for HIPAA-grade work, because predictable beats autonomous when a regulator's involved. The right column — that's the honest part. Some things genuinely need the bigger stack. True branching, non-LLM nodes, event-driven workflows firing 10,000 times a day. If your task is THAT, hire your engineers. But for everything else: start with the middle column. You'll know when you've outgrown it." |
| 6   | **The "you" in your work** (NEW — WebMD echo)               | Big quote      | *"We put the WE in well-being.<br>You put the YOU in your work."* — Moleskine, hand-drawn, with "YOU" circled in navy, with teal underline beneath the word YOU | "Their tagline says they put humans back in healthcare. Today we put YOU back in your AI work. me + task-extractor — the two skills that load your context before any AI does anything for you." |
| 7   | The two starter skills                                      | 2-up visual    | LEFT: `me.md` icon — labeled "WHO I am". RIGHT: `task.md` icon — labeled "WHAT I do". Arrow from both into a third box: "AI that knows you" | "Two markdown files. That's the whole trick today. Everything else builds on these."  |
| 8   | LIVE DEMO — me + task-extractor                             | Demo slide     | Just a frame border. Tony switches to terminal.                                                                    | "Watch. 5 minutes. No volunteer needed — I'll run it on myself."       |
| 9   | YOUR TURN — 15 min                                          | Activity slide | Big timer + 1 instruction: "Run /me + /task-extractor on YOUR task"                                                | Tony floats                                                            |
| 10  | **Anatomy of a skill** (NEW — big picture)                  | Visual diagram | Hand-drawn folder structure: `skills/my-task/` with `SKILL.md` (frontmatter + checklist + output schema + "When NOT to use"), optional `references/` folder (examples, vocabulary), optional `scripts/` folder (small Python helper). Caption: *"It's a folder. With markdown."* | "What's inside a skill? A folder with one markdown recipe. Optional references for lookup data. Optional script if you need it. Most skills are just SKILL.md alone — 80 lines. Fancy ones add references. Very fancy add a script. You start with just the markdown today." |
| 11  | **Where the skill lives** (NEW — harness big picture)       | Visual diagram | Hand-drawn diagram: stateless model at top → harness (Claude Code or Cowork) loads 3 things from `~/.claude/`: skills (recipes) · MCP (tools) · hooks (rules). Harness meets your work (cwd / repo). Caption: *"This is where everything lives."* | "The model doesn't remember anything. The harness loads 3 things on demand: skills, MCP, hooks. All live in `~/.claude/`. The harness meets your real work. We're building a skill today — it goes in `~/.claude/skills/` and loads via the harness." |
| 12  | Module 3 hero — When to automate                            | Big question   | Hand-drawn 4-Q filter as a flowchart                                                                               | Whiteboard moment — they answer with you. Now you have a task — should you automate it? |
| 13  | The 5th question                                            | Reveal         | Same flowchart with regulator-cares Q added in navy, with teal underline under "regulator"                                                                 | "Healthcare adds one — does a regulator care?"                         |
| 14  | What you're working INSIDE — kitchen metaphor               | Visual diagram | Hand-drawn harness as a kitchen: model is the cook, skills are recipes, MCP is the appliances, hooks are the alarm | "Same picture, different angle — the kitchen analogy. Useful when explaining to teammates who haven't taken this workshop." |
| 15  | Surface matrix (compressed)                                 | Compare        | Code CLI · Cowork · Web · Routines — 4 columns, 6 rows of capability with ✓/✗                                      | Show, don't read. Point to the row that matters per audience question. |
| 16  | The 3 tiers                                                 | Visual ladder  | Prompt → Skill → Agent — drawn as 3 rungs                                                                          | "Most teams stop at prompt. We're going to skill today."               |
| 17  | The 4 paths to a skill                                      | 2×2 grid       | A: task-extractor · B: Cowork "Turn into skill" · C: skill-creator · D: Marketplace                                | One image per quadrant, 30 sec each                                    |
| 18  | But making one isn't the skill                              | Big quote      | Tony's quote: *"Knowing if it's any good is."* (teal underline under "good")                                                                     | Cliffhanger — rubric coming Part 3                                     |

### Part 2 — 60 min · ~10 slides

| #   | Slide                                      | Type            | Image / asset                                                                       | Speaker note hook                                               |
| --- | ------------------------------------------ | --------------- | ----------------------------------------------------------------------------------- | --------------------------------------------------------------- |
| 19  | Part 2 frame — 4 demos = 4 shapes          | Visual map      | 4 doors labeled: skill+mcp · project+mcp · pure skill · hybrid                      | "Each demo is a different shape your task could become."        |
| 20  | Demo 1 hero — PRD → YouTrack               | Demo title      | Hand-drawn YouTrack ticket icon                                                     | "Most surveyed POs put this as their #1 task."                  |
| 21  | Demo 1 LIVE                                | Frame           | (Tony switches to Claude Code)                                                      | Pre-built skill + MCP, ~12 min                                  |
| 22  | What you just saw                          | Recap visual    | 3-step diagram: PRD doc → skill+MCP → tickets in YouTrack                           | "Same skill shape, MCP wired in. Anyone can do this in 30 min." |
| 23  | Demo 2 hero — Design system Q&A            | Demo title      | Hand-drawn book icon (knowledge)                                                    | "When it's Q&A on a corpus, not a transformation"               |
| 24  | Demo 2 LIVE                                | Frame           | (Tony switches to Claude Project)                                                   | ~12 min                                                         |
| 25  | Demo 3 hero — 1:1 prep                     | Demo title      | Hand-drawn coffee cup icon                                                          | "Pure skill. No MCP. The simplest shape — for the people-managers." |
| 26  | Demo 3 LIVE — and the me.md moment         | Frame + callout | (Tony reads aloud the line in output that came from a sample me.md)                 | THE MOMENT — point to the line on screen                        |
| 27  | Demo 4 hero — Multi-source synth + Routine | Demo title      | Hand-drawn 3 funnels merging, with clock icon                                       | "Hybrid. The destination, not today's build."                   |
| 28  | Demo 4 LIVE                                | Frame           | (Tony switches to Claude Code)                                                      | ~12 min, with the agent-vs-skill mitigation script              |
| 29  | The honest line — agent vs skill           | Big quote       | *"You're right. It's a checklist with tools. That's a feature."* (teal underline under "feature")                    | Reads aloud, lets it sit                                        |

### Part 3 — 60 min · ~8 slides

| #   | Slide                              | Type             | Image / asset                                                                                             | Speaker note hook                                                   |
| --- | ---------------------------------- | ---------------- | --------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------- |
| 30  | The rubric — 6 dimensions          | Visual scorecard | Hand-drawn 6 dials, each 0-5                                                                              | Walk left to right, ~30 sec each                                    |
| 31  | The 5-check Internet Skill audit   | Reveal           | 5 magnifying glass icons revealing one at a time                                                          | Kitchen-sink? Injection? Fluff? Wrong SOP? Schema?                  |
| 32  | YOUR TURN — pick your option (A–E) | Activity slide   | 5 doors labeled A through E                                                                               | "A is for everyone. C if you can install. E if you have a cadence." |
| 33  | LIVE BUILD — 35 min                | Activity + timer | Big timer                                                                                                 | Tony floats by shape                                                |
| 34  | Score your skill cold              | Activity slide   | 1 number, big                                                                                             | "Lowest dim = your upgrade target. 5 minutes."                      |
| 35  | Round-robin commit                 | Activity slide   | Speaking-bubble icon: *"task · shape · score · upgrade · 30-day measure"*                                 | Each person, 30 sec                                                 |
| 36  | The 30-day plan                    | Visual timeline  | 4 weeks, 4 actions: ship · score · organize · maintain                                                    | "By month 3 = 3 maintained skills."                                 |
| 37  | Closing quote                      | Big quote        | *"Một skill là demo. Năm skills là một hệ thống. Năm skills không có discipline là một bãi rác."* (teal underline under "discipline")         | Lets it land. Q&A.                                                  |

---

## Image generation list (for Codex)

Reuse Moleskine cream-paper hand-drawn aesthetic from `session-1/images/`. Each prompt should reference that style explicitly.

| Slide # | Image needed | Prompt seed |
|---------|--------------|-------------|
| 1 | Hero cover — "skill" word with arrow | "Hand-drawn 'SKILL' on cream Moleskine page, with curved arrow pointing right, sketchy ink style" |
| 5 | **Reframe — the floor moved up** | "Hand-drawn Moleskine page split into two halves. LEFT: neat (NOT chaotic) diagram of boxes labeled 'n8n', 'Dify', 'LangChain', 'Zapier', connected by clean lines forming an orchestration graph. Caption beneath: *'The full agent stack — still useful for what it's useful for.'* RIGHT: one tidy markdown file icon labeled 'my-task.md' with 3 visible checklist lines. Caption beneath: *'The smallest thing that works for most product tasks.'* Below both, hand-drawn horizontal line with arrow: *'Start here. Graduate when you actually need to.'* Headline above with teal underline (~#3BC6D9) under the phrase 'the floor moved up'. Ink on cream paper, no faces, dignified balanced composition." |
| 5b | **3-column comparison — Real AI agent vs Skill+MCP vs When big stack wins** | "Hand-drawn landscape Moleskine page, 3 vertical columns separated by faint vertical lines. COL 1 header: 'Real AI agent.' Below: small tangled diagram of LangChain/Dify/n8n boxes with curved agent-loop arrows. Then a checklist: '✓ Autonomous · ✓ Branching · ✓ Multi-step planning · ✗ Hosting · ✗ Hard to debug · ✗ Year of learning.' COL 2 header: 'Skill + MCP + small script.' Below: one markdown file icon next to a plug icon (MCP) next to a tiny gear icon (script). Then a checklist: '✓ Predictable · ✓ Auditable · ✓ Diff-able · ✓ Local · ✓ Editable in 60 sec · ✓ If you write Confluence pages, you can do this.' COL 3 header: 'When you need the big stack.' Below: small bulleted list: '• True branching · • Non-LLM nodes · • Event-driven · • 10,000 fires/day.' Below the list, in handwritten script: *'Graduate when you actually need it.'* Above all 3 columns, the headline: *'Both are real. Pick the smallest one that works.'* Ink on cream Moleskine, balanced, no faces, no smug." |
| 6 | **WebMD echo — "you in your work"** | "Hand-drawn Moleskine page, two stacked phrases in handwriting: 'We put the WE in well-being.' (smaller, top) / 'You put the YOU in your work.' (bigger, bottom). The word 'YOU' circled in navy ink (~#1E2A78), with a teal underline (~#3BC6D9) beneath the word YOU." |
| 7 | **Two starter skills (me + task)** | "Hand-drawn Moleskine page: two markdown file icons side by side, left labeled 'me.md — WHO I am', right labeled 'task.md — WHAT I do', both arrows merging into a third box labeled 'AI that knows you'. Ink on cream paper." |
| 10 | **NEW — Anatomy of a skill (folder structure)** | "Hand-drawn Moleskine page showing a folder tree: outer folder labeled 'skills/my-task/'. Inside, three children: (1) prominent SKILL.md file with 4 sub-callouts in handwriting — 'frontmatter', 'checklist', 'output schema', 'When NOT to use'; (2) smaller folder 'references/' with 2 file icons inside (examples.md, vocabulary.md), labeled 'optional: lookup data'; (3) smallest folder 'scripts/' with one Python file icon, labeled 'optional: helper'. Caption at bottom in handwriting: *'It's a folder. With markdown.'* Ink on cream, balanced layout." |
| 11 | **NEW — Where the skill lives (harness diagram)** | "Hand-drawn Moleskine architecture diagram. Top: a small sketch of Claude (the model) labeled 'stateless'. Arrow down with words 'loads on demand' to a horizontal row of 3 boxes: 'SKILLS (recipes)', 'MCP (tools)', 'HOOKS (rules)'. A bracket below all three says 'all live in ~/.claude/'. Below the bracket: a labeled box 'THE HARNESS — Claude Code or Cowork'. Arrow down to bottom: 'YOUR WORK — cwd, repo, real files'. Headline at top: *'Where the skill lives.'* Ink on cream Moleskine, clean diagram." |
| 12 | 4-question filter flowchart | "Hand-drawn flowchart on Moleskine page, 4 yes/no decision diamonds in a row, ink + light yellow highlight" |
| 14 | Harness as kitchen | "Hand-drawn kitchen scene on Moleskine: chef = model, recipe book = skills, appliances labeled MCP, alarm bell = hooks" |
| 16 | 3 tiers ladder | "Hand-drawn 3-rung ladder labeled Prompt / Skill / Agent on cream Moleskine, simple ink" |
| 17 | 4 paths 2×2 grid | "Hand-drawn 2x2 grid on Moleskine, 4 small icons: clipboard (task-extractor), cursor click (Turn into skill), gear (skill-creator), shop window (Marketplace)" |
| 19 | 4 doors | "Hand-drawn row of 4 doors on Moleskine, each labeled: skill+mcp · project+mcp · pure skill · hybrid" |
| 22 | PRD-to-tickets flow | "Hand-drawn 3-step diagram: doc icon → gear+plug icon → ticket cards stacked, ink on Moleskine" |
| 26 | me.md tie-in callout | (No new image — point at live screen) |
| 27 | 3 funnels + clock | "Hand-drawn 3 funnels merging into one output, clock face above, ink on Moleskine" |
| 30 | 6 dials scorecard | "Hand-drawn 6 dial gauges in a 2x3 grid, each labeled: trigger · token · schema · tool · failure · reuse, ink + cream paper" |
| 31 | 5 magnifying glasses | "Hand-drawn 5 magnifying glass icons in a row on Moleskine, each over a different page snippet" |
| 32 | 5 doors A-E | "Hand-drawn 5 doors labeled A through E on cream Moleskine, ink sketch" |
| 36 | 30-day timeline | "Hand-drawn 4-week timeline on Moleskine, week 1 ship · week 2 score · week 3 organize · week 4 maintain, with arrow forward" |
| 31 | 30-day timeline | "Hand-drawn 4-week timeline on Moleskine, week 1 ship · week 2 score · week 3 organize · week 4 maintain, with arrow forward" |

13 new images. Each ~3 min via Codex (per session-1 pipeline). ~40 min total generation time.

---

## What a slide should NOT contain (banned patterns)

- ❌ More than ONE idea per slide
- ❌ Speaker notes printed on the slide
- ❌ Bullet lists longer than 3 items
- ❌ Body text under 22pt
- ❌ Stock photos (Moleskine hand-drawn only)
- ❌ Code blocks longer than 5 lines (use the live screen instead)
- ❌ The word "leverage", "robust", "seamless", or "synergy"
- ❌ Tables wider than 4 columns (split into two slides)

If a slide breaks one of these, it's two slides or it goes to the speaker notes.

---

## Speaker notes — separate file, separate concern

Speaker notes will live in `slides/SPEAKER-NOTES.md` (separate file). They contain:
- The full script for each slide
- Time hints
- Transition cues to next slide
- The agent-vs-skill mitigation script (Slide #24) verbatim
- Stage cues for live demos (when to switch to terminal, what to type, what to say while it loads)

The slides themselves carry NO speaker notes embedded. If Tony forgets a beat, he checks the printed notes — never reads from the screen.

---

## Interactive moments (5 named)

These are slides where the audience actively participates, not just watches.

| Slide | Interaction | What attendees do |
|---|---|---|
| 5 (4-Q filter) | Whiteboard answer | Tony reads each Q, audience votes hand up/down or shouts |
| 13 (Your turn — me + task-extractor) | Hands-on | 15 min run on their own task |
| 21 (me.md tie-in) | Point + react | Tony points at the line; ask "see the difference?" |
| 26 (5-check audit) | Group spot-check | Tony shows a sketchy "internet skill" frontmatter, audience names which check fails |
| 28 (Live build) | Hands-on | 35 min build their own skill |

5 interactive moments in 180 min = 1 every 36 min. Standard workshop cadence.

---

## What this beats vs Session 1 deck

Session 1 had ~50 slides, lots of text, comic-frame images on key slides only. Some slides functioned as speaker notes. This deck:
- 32 slides max (180 min ÷ ~6 min/slide on average)
- Image on EVERY slide (13 new + reuse 9 from S1)
- ZERO slides function as notes
- Big-quote slides anchor key transitions (3 quote slides: Nga, Esteban, Tony's mitigation)
- 5 explicit interactive moments named on the schedule

---

## Next steps

1. Tony reviews this outline — confirm slide count, interaction count, image list
2. If approved → generate the 13 new images via Codex (~40 min)
3. Build `slides.html` using Session 1's HTML structure as base (reuse CSS, reuse keyboard shortcuts, reuse "S" toggle for stage strips)
4. Build `SPEAKER-NOTES.md` separately — full script, time hints, demo cues
5. Saturday rehearsal: run slides + demos end-to-end once, time it, cut anything that runs long

## Sources for this design

- [Tips for effective slide design — University of Iowa](https://journalism.uiowa.edu/news/2025/11/clear-compelling-and-visual-tips-effective-slide-design)
- [Visual presentation guide — SessionLab](https://www.sessionlab.com/blog/visual-presentation/)
- [Workshop presentation template — Pitch](https://pitch.com/templates/Workshop-4RZSj72xM7JY4iYJmw2VJ1XB)
- [Interactive presentations 2026 — Prezlab](https://prezlab.com/the-world-of-interactive-presentations/)
- Reuse pipeline: `session-1/scripts/` for Codex image generation
