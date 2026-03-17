# Discovery Plan: Agent-Human Collaboration Infrastructure

**Date**: 2026-03-17
**Product Stage**: New (early exploration, working prototype exists)
**Founder**: Solo, side hustle
**Discovery Question**: Is "collaboration > delegation" a real need, or do people just want fully autonomous agents?

---

## Core Thesis

LLMs will commoditize. When everyone has access to the same model capability, the differentiator is how well humans collaborate with agents.

```
Human judgment × Agent capability = Result

Agent capability → commodity (same for everyone)
Human judgment → the only variable that matters
```

Tools that keep humans as a **positive multiplier** — learning, adapting, directing, deciding — win long-term. Tools that encourage passive delegation make humans irrelevant.

## Ecosystem

| Repo | Purpose | Status |
|------|---------|--------|
| [agent-board](https://github.com/xavierau/agent-board) | Collaborative workspace (kanban + audit + identity) | Working prototype |
| [agent-org](https://github.com/xavierau/agent-org) | Team directory, roles, capabilities | Early |
| agent-demon | Handoff/orchestration | Early |

## Competitive Landscape

| Product | Approach | Gap |
|---------|----------|-----|
| OpenAI Symphony + Linear | Full autonomy: poll board → dispatch agent → deliver PR | No collaboration layer. Human is a reviewer, not a teammate. |
| Vibe Kanban | Orchestrate multiple coding agents in parallel | Developer-only. Task dispatch, not collaboration. |
| Flux | MCP-first task board with dependencies | Lightweight but no identity, audit, or reasoning transparency. |
| VS Code Agent Kanban | IDE-embedded kanban for agent visibility | Scoped to VS Code. Visibility only, no collaboration protocol. |

**Our bet**: None of these enable agents and humans to work *together*. They all treat agents as workers and humans as managers.

---

## Critical Assumptions (Ranked by Priority)

| ID | Assumption | Category | Impact | Uncertainty | Priority |
|----|-----------|----------|--------|-------------|----------|
| A8 | Context loss between agent sessions is a real pain point | Value | High | High | **P1** |
| A5 | Humans will engage with agent reasoning and decision logs | Value | High | High | **P2** |
| A10 | Humans want control checkpoints, not full autonomy | Value | High | High | **P3** |
| A13 | Non-dev teams (ops, research, marketing) will adopt | Go-to-Market | High | Very High | **P4** |
| A14 | Solo founder can maintain a multi-repo infrastructure stack | Viability | Medium | Medium | **P5** |

---

## Validation Experiments

### E1: Dog-Food (Week 1-2)

**Tests**: A8 (context loss) + A5 (engaging with agent reasoning)
**Effort**: Low
**Method**: Use Agent Board + Claude to manage agent-demon development for 2 weeks.

**Protocol**:
- After each agent session, spend 10 min reviewing the audit log and decision trail
- Write a daily 3-line journal entry in `logs/dogfood/`:
  - What I learned from reviewing agent work
  - What I'd change about how I directed the agent
  - What surprised me
- At end of week 1, review journal: am I still doing it or skipping?

**Success criteria**: After 2 weeks, I can point to 3+ specific instances where reviewing agent work changed my next decision for the better.

**Kill criteria**: After 1 week, I'm skipping the review because it feels useless.

**Log location**: `logs/dogfood/YYYY-MM-DD.md`

---

### E2: Problem Interviews (Week 2-3)

**Tests**: A10 (checkpoints vs autonomy) + A5 (reasoning engagement)
**Effort**: Medium
**Method**: 5 interviews — 3 developers, 2 non-developers who use AI agents.

**Recruiting**:
- Post in relevant communities asking for 20-min chats
- Reach out to contacts who use Claude Code, Cursor, Codex, ChatGPT for work
- Offer to share findings as incentive

**Script**: See `INTERVIEW-SCRIPT.md`

**Success criteria**: 3/5 people describe a real pain around understanding agent behavior. At least 1 says "I wish I could see why it did that."

**Kill criteria**: 4/5 people say "I don't care, I just re-run it."

**Log location**: `logs/interviews/YYYY-MM-DD-participant-N.md`

---

### E3: Delegation vs Collaboration Comparison (Week 2-3)

**Tests**: Core thesis — does collaboration produce better outcomes?
**Effort**: Low
**Method**: Pick 2 similar tasks. Run each in a different mode.

**Protocol**:
- **Task A (Delegation)**: Give agent full instructions. Don't review reasoning. Accept output.
- **Task B (Collaboration)**: Agent proposes plan → I review → agent executes with checkpoints → I review reasoning at each step → adjust direction.
- **Measure**:
  - Output quality (1-10 self-assessment)
  - Time spent (total and per-step)
  - Learning: did I gain knowledge from Task B that I couldn't from Task A?
  - Would I do the next similar task differently because of what I learned?

**Success criteria**: Task B produces noticeably better output AND I learn something transferable.

**Kill criteria**: Task B takes 3x longer with no quality improvement.

**Log location**: `logs/comparison/task-a.md`, `logs/comparison/task-b.md`

---

### E4: Non-Dev Pilot User (Week 3-4)

**Tests**: A13 (non-dev adoption)
**Effort**: Medium
**Method**: Find ONE non-developer in my network. Set them up with Agent Board for a real task.

**Protocol**:
- Identify a PM, researcher, or ops person who uses ChatGPT/Claude for work
- Set up Agent Board for their use case
- Watch them use it (screen share or async recording)
- Interview them after 3 days

**Success criteria**: They find value in seeing agent activity organized on a board. They use it without me prompting.

**Kill criteria**: They abandon it after day 1 and go back to ChatGPT.

**Log location**: `logs/pilot/participant-profile.md`, `logs/pilot/observations.md`

---

### E5: Manifesto (Week 1)

**Tests**: Does the thesis resonate with forward-thinking builders?
**Effort**: Low
**Method**: Publish blog post articulating the "collaboration > delegation" thesis.

**Distribution**:
- Hacker News (Show HN)
- Reddit: r/artificial, r/LocalLLaMA
- LinkedIn
- Dev.to

**Measure**: Engagement quality, not quantity.
- Substantive comments with debate = strong signal
- "Cool!" with no discussion = weak signal
- Strong disagreement = also good signal (people care enough to argue)

**Success criteria**: 50+ substantive comments across platforms. People share it.

**Kill criteria**: Crickets. Nobody engages.

**Content**: See `MANIFESTO.md`

**Log location**: `logs/manifesto/distribution-tracker.md`

---

## Decision Framework

```
Week 4 Decision Matrix:

IF E1 success + E5 resonance
  → Double down on collaboration angle
  → Build: decision journal, progress contracts, shared context

IF E1 fail (skipping reviews)
  → Pivot to lightweight "agent dashboard" (visibility only)
  → Reduce scope to single feature

IF E2 shows "don't care about reasoning"
  → Pivot to task dispatch
  → Compete on UX/simplicity against Vibe Kanban

IF E4 success (non-dev adopts)
  → Go general-purpose immediately
  → Prioritize non-dev onboarding

IF E4 fail
  → Narrow to developer niche first
  → Expand later once pattern is proven

IF A14 confirmed (too much for solo)
  → Consolidate repos: merge agent-org into agent-board
  → Reduce surface area
```

---

## Timeline

| Week | Experiments | Deliverables |
|------|-----------|-------------|
| **Week 1** (Mar 17-23) | E5: Publish manifesto. E1: Start dog-fooding. | Manifesto live. First 5 dogfood journal entries. |
| **Week 2** (Mar 24-30) | E1: Continue dog-food. E2: First 2-3 interviews. E3: Start comparison. | Interview transcripts. Comparison task A complete. |
| **Week 3** (Mar 31-Apr 6) | E2: Complete interviews. E3: Complete comparison. E4: Find pilot user. | All interview summaries. Comparison analysis. Pilot user identified. |
| **Week 4** (Apr 7-13) | E4: Pilot user observation. Analyze ALL data. | Pilot report. Decision document. |
| **Decision Day**: Apr 13 | Review all logs. Make go/pivot/kill decision. | `logs/decision/2026-04-13-verdict.md` |

---

## Log Structure

```
logs/
  dogfood/
    2026-03-17.md
    2026-03-18.md
    ...
  interviews/
    2026-03-XX-participant-1.md
    2026-03-XX-participant-2.md
    ...
  comparison/
    task-a.md
    task-b.md
    analysis.md
  pilot/
    participant-profile.md
    observations.md
    debrief.md
  manifesto/
    distribution-tracker.md
    engagement-analysis.md
  decision/
    2026-04-13-verdict.md
```
