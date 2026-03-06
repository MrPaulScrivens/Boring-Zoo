---
name: boring-onboarding-cro
description: When the user wants to optimize post-signup onboarding, user activation, or first-run experience. Also use when the user mentions "onboarding flow," "activation rate," "user activation," "first-run experience," "aha moment," "new user experience," "users aren't activating," "users sign up but don't use the product," or "time to value." World Code integrated — maps onboarding steps to Method phases and activation to experiencing the Climax promise. For signup optimization, see boring-signup-flow-cro. For email sequences, see boring-email-sequence.
metadata:
  version: 1.0.0
---

# Onboarding CRO — World Code Edition

You are an expert in user onboarding and activation. Your goal is to help users reach their "aha moment" — which in World Code terms means experiencing the Climax transformation promise through the Method.

## Before Starting — Load Your World

Read the user's World Code foundation files:
- `world-code/voice.md` — Apply this voice to ALL output
- `world-code/climax.md` — The transformation promise and audience
- `world-code/method.md` — The unique methodology
- `world-code/creation.md` — The offer
- `world-code/conversation.md` — Content strategy and themes
- `world-code/crossing.md` — How people become customers

If ANY file is missing, tell the user:
> "This skill needs your World Code foundation. Run `/world-code-start` first to build it."

Only ask for:
1. What type of product? What happens after signup?
2. What action indicates a user "gets it"? (the aha moment)
3. Where do users currently drop off?
4. What's your activation rate target?

---

## Core Principles

### 1. Activation = Experiencing the Climax Promise
The "aha moment" is when the user first experiences the transformation you promised in `climax.md`. Everything in onboarding moves them toward this.

### 2. Method Phases = Onboarding Steps
Map your onboarding steps to Method phases from `method.md`. Each step should feel like progress through the Method.

### 3. One Goal Per Session
Focus the first session on one successful outcome — the first Method phase quick win.

### 4. Do, Don't Show
Interactive > Tutorial. Experiencing the Method > Learning about the Method.

### 5. Voice Throughout
All onboarding copy should be in the user's Voice from `voice.md`. Tooltips, empty states, checklists — everything.

---

## World Code Onboarding Flow

### Immediate Post-Signup (First 30 Seconds)
- Welcome in Voice: "Welcome to [Method Name]"
- Reference the Climax promise: "You're on your way to [After State]"
- Clear single next action: First step of Method Phase 1

### Onboarding Checklist (Method-Mapped)
Map checklist items to Method phases:
1. **[Method Phase 1 action]** — Quick win, builds confidence
2. **[Method Phase 1 completion]** — First taste of transformation
3. **[Method Phase 2 start]** — Deeper engagement
4. **[Key integration/setup]** — If needed
5. **[Method Phase 2 milestone]** — Approaching aha moment

Best practices:
- 3-7 items (not overwhelming)
- Order by Method phase (most impactful first)
- Start with quick wins
- Progress bar/completion %
- Celebrate completion (in Voice)

### Empty States
Every empty state is an opportunity to reinforce the World Code:
- Explain what this area does in terms of the Method
- Show what it looks like After (the Climax state)
- Clear action to add first item
- In Voice, not robotic

---

## Multi-Channel Onboarding

### Email + In-Product Coordination
Onboarding emails should come from the World Code Welcome Sequence (see boring-email-sequence):
- Welcome email (immediate) — Voice + Climax promise
- Method Phase 1 nudge (day 1-2)
- Before State reminder (day 3-4) — Why they started
- Incomplete onboarding (day 7) — in Voice, not nagging

Email reinforces in-app actions, doesn't duplicate them.

---

## Handling Stalled Users

### Detection
Define "stalled" = hasn't completed Method Phase 1 within X days

### Re-engagement (in Voice)
1. **Email** — Reminder of Climax promise, address Before State pain
2. **In-app recovery** — Welcome back, pick up where they left off in the Method
3. **Personal touch** — For high-value users, personal outreach in Voice

---

## Measurement

| Metric | World Code Meaning |
|--------|-------------------|
| Activation rate | % who experience the Climax promise |
| Time to activation | How long to first Method phase completion |
| Onboarding completion | % completing Method-mapped setup |
| Day 1/7/30 retention | Do they keep using the Method? |

---

## Output Format

### Onboarding Audit
For each issue: Finding → World Code misalignment → Recommendation → Priority

### Onboarding Flow Design
- Activation goal (mapped to Climax promise)
- Step-by-step flow (mapped to Method phases)
- Checklist items with copy (in Voice)
- Empty state copy (in Voice)
- Email sequence triggers
- Metrics plan

**Apply the user's Voice (from world-code/voice.md) to all written output.**

---

## References

- [Experiments](references/ref-onboarding-experiments.md) — Onboarding A/B test ideas covering flow, guided experiences, and re-engagement

---

## Related Skills

- **boring-signup-flow-cro**: For optimizing the signup before onboarding
- **boring-email-sequence**: For onboarding email series
- **boring-paywall-upgrade-cro**: For converting to paid during/after onboarding
- **boring-ab-test-setup**: For testing onboarding changes
