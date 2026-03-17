# Problem Interview Script: Agent-Human Collaboration

**Duration**: 20-25 minutes
**Target**: People who use AI agents for work (devs and non-devs)
**Goal**: Understand if humans care about collaborating with agents or just want outputs

---

## Before the Interview

- Do NOT pitch Agent Board
- Do NOT explain your thesis
- You're here to LISTEN, not validate
- Record (with permission) or take detailed notes
- Follow The Mom Test: no leading questions, no pitching, focus on past behavior

---

## Warm-Up (3 min)

> "Thanks for chatting. I'm exploring how people work with AI tools day-to-day. No sales pitch — I'm just trying to understand how people actually use these tools. Everything you share stays anonymous."

1. "What's your role? What kind of work do you do?"
2. "Which AI tools do you use regularly?" (ChatGPT, Claude, Cursor, Copilot, etc.)
3. "Roughly how often? Daily? A few times a week?"

**Write down**: Role, tools used, frequency. Dev or non-dev.

---

## Current Workflow (5 min)

> "Let's talk about how you actually use these tools."

4. "Walk me through a recent task where you used an AI agent. What were you trying to do?"
5. "How did you set up the task? Did you give detailed instructions or just a quick prompt?"
6. "What did the agent deliver? Was it what you expected?"

**Listen for**: How much direction they give. How much they trust the output. Do they review carefully or accept blindly?

---

## Failure & Surprise (7 min) — THIS IS THE CORE

> "I'm interested in times when things didn't go as expected."

7. "Tell me about a time the agent's output surprised you — either positively or negatively."
8. "What did you do when that happened? How did you figure out what went wrong?"
9. "Did you re-run it? Modify your prompt? Give up? Something else?"
10. "How long did it take to get to a good result? Was that frustrating?"

**Then dig deeper:**

11. "When the agent made a choice you disagreed with — like picking a certain approach or making an assumption — how did you find out about it?"
12. "If you could have seen the agent's reasoning at each step, would that have changed anything?"
13. "Have you ever wished you could say 'stop, let me look at this before you continue'?"

**Listen for**:
- Pain around lack of transparency → supports thesis
- "I just re-run it" (no engagement with reasoning) → challenges thesis
- Desire for checkpoints → supports progress contracts idea
- "I don't care why, just give me output" → challenges thesis

---

## Learning & Growth (5 min)

> "Let's talk about how your usage has changed over time."

14. "Do you feel like you've gotten better at working with AI agents? How?"
15. "What did you learn? Was it trial and error, or did you get that insight from somewhere?"
16. "When the agent does something well, do you understand WHY it worked, or is it a black box?"
17. "If you could look back at everything you and an agent worked on together — all the decisions, changes, results — would that be useful? Why or why not?"

**Listen for**:
- People who actively learn from agent interactions → early adopters for collaboration tools
- People who don't reflect at all → not your target user
- Interest in history/audit → supports decision journal and shared context ideas

---

## Team Dynamics (3 min) — if applicable

> "If you work on a team..."

18. "Does anyone else on your team use AI agents? Do you share what you learn?"
19. "Has an agent ever done work that affected someone else's work? How did that go?"
20. "If you had multiple agents working alongside your team, what would concern you most?"

**Listen for**:
- Coordination problems → supports shared workspace protocol
- Trust issues → supports audit trail and transparency
- "I wouldn't trust an agent to touch shared work" → barrier to address

---

## Future Vision (2 min)

> "Last couple of questions, more speculative."

21. "Imagine AI agents are 10x better than today. They can do most of your work. What's YOUR role in that world?"
22. "What would need to be true for you to trust an agent as a real teammate, not just a tool?"

**Listen for**: The emotional response. Do they see themselves as directors? Collaborators? Obsolete? This reveals their mental model.

---

## Wrap-Up

> "This has been really helpful. One last thing — is there anything about working with AI that I didn't ask about but you think is important?"

(Often the best insights come here.)

> "Thanks so much. I'll share what I learn from these conversations if you're interested."

---

## After the Interview

Fill out the log template:

```markdown
# Interview: Participant [N]

**Date**: YYYY-MM-DD
**Role**: [their role]
**AI tools used**: [list]
**Frequency**: [daily/weekly]
**Dev/Non-dev**: [dev/non-dev]

## Key Quotes
- "[exact quote]" — re: [topic]
- "[exact quote]" — re: [topic]

## Pain Points Observed
1. [pain point]
2. [pain point]

## Engagement with Agent Reasoning
- [ ] Actively reviews agent reasoning
- [ ] Reviews output but not reasoning
- [ ] Doesn't review, just re-runs
- [ ] Wants transparency but lacks tooling

## Checkpoint Desire
- [ ] Wants to approve plans before execution
- [ ] Wants mid-task check-ins
- [ ] Prefers full autonomy
- [ ] Depends on task importance

## Learning Pattern
- [ ] Actively learns from agent interactions
- [ ] Learns by trial and error
- [ ] Doesn't reflect on process

## Thesis Signal
- [ ] SUPPORTS collaboration > delegation
- [ ] NEUTRAL
- [ ] CHALLENGES (wants pure delegation)

## Surprising Insights
[anything unexpected]

## Relevant for
- [ ] A8 (context loss)
- [ ] A5 (agent reasoning engagement)
- [ ] A10 (checkpoints vs autonomy)
- [ ] A13 (non-dev adoption)
```

---

## Recruiting Message Template

> Subject: Quick chat about how you use AI tools? (20 min)
>
> Hey [Name],
>
> I'm researching how people work with AI agents day-to-day — not just chatbots, but tools like Claude Code, Cursor, ChatGPT for actual work tasks.
>
> Would you be up for a 20-min call this week? I'm not selling anything — just trying to understand real workflows. Happy to share what I learn across all the conversations.
>
> [Your name]
