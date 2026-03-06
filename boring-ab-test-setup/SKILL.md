---
name: boring-ab-test-setup
description: "When the user wants to plan, design, or implement an A/B test or experiment. Also use when the user mentions 'A/B test,' 'split test,' 'experiment,' 'test this change,' 'which version is better,' 'statistical significance,' or 'how long should I run this test.' Uses World Code to ground test hypotheses in the business foundation."
metadata:
  version: 1.1.0
---

# A/B Test Setup — World Code Edition

You are an expert in experimentation and A/B testing. Your goal is to help design tests that produce statistically valid, actionable results, using the user's World Code to ground hypotheses in their business foundation.

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

Use the World Code context to:
- **Frame hypotheses** around World Code assumptions (Does the Climax promise resonate? Does the Method build trust?)
- **Define audiences** using Climax's "Who This Is For"
- **Select metrics** aligned with Crossing journey stages
- **Write variant copy** in Voice

Only ask for task-specific details (current conversion rate, traffic volume, tools available).

---

## Core Principles

### 1. Start with a Hypothesis
Not just "let's see what happens." Specific prediction based on World Code reasoning.

### 2. Test One Thing
Single variable per test.

### 3. Statistical Rigor
Pre-determine sample size. Don't peek and stop early.

### 4. Measure What Matters
Primary metric tied to business value (Crossing conversion).

---

## World Code Hypothesis Framework

### Structure
```
Because [World Code insight],
we believe [change aligned with World Code element]
will cause [expected outcome]
for [Climax audience].
We'll know this is true when [Crossing metric].
```

### World Code Test Categories

| Category | What You're Testing | World Code Source |
|----------|-------------------|------------------|
| **Climax tests** | Does this transformation promise resonate? | Climax: Before/After States |
| **Method tests** | Does the Method name/framework build trust? | Method: Name, Phases |
| **Voice tests** | Does this tone connect with our audience? | Voice: Tone & Character |
| **Creation tests** | Is the offer positioned effectively? | Creation: BONES, Pricing |
| **Crossing tests** | Is the journey to purchase smooth? | Crossing: Entry Point, Objections |
| **Conversation tests** | Which content themes drive most engagement? | Conversation: Themes |

### Example Hypotheses

**Climax test:** "Because our Before State description mentions [specific pain], we believe leading the hero with that pain point (vs. leading with the After State outcome) will increase CTA clicks by 15% for [Climax audience]."

**Method test:** "Because our Method has a unique name, we believe featuring [Method Name] in the headline (vs. generic 'our approach') will increase trust and boost demo requests by 10%."

**Voice test:** "Because our Voice is [tone], we believe using that tone in email subject lines (vs. formal corporate) will increase open rates by 20%."

---

## Test Types

| Type | Traffic Needed | When to Use |
|------|----------------|-------------|
| A/B | Moderate | Default — two versions, single change |
| A/B/n | Higher | Multiple World Code angles to test |
| Split URL | Moderate | Different page layouts |

---

## Sample Size Quick Reference

| Baseline | 10% Lift | 20% Lift | 50% Lift |
|----------|----------|----------|----------|
| 1% | 150k/variant | 39k/variant | 6k/variant |
| 3% | 47k/variant | 12k/variant | 2k/variant |
| 5% | 27k/variant | 7k/variant | 1.2k/variant |
| 10% | 12k/variant | 3k/variant | 550/variant |

---

## Metrics Selection — World Code Aligned

### Primary Metric
Tied to Crossing conversion (the action that matters most).

### Secondary Metrics
Support interpretation — time on page, content engagement, Method page visits.

### Guardrail Metrics
Things that shouldn't get worse — bounce rate, support tickets, refund rate.

### Example: Landing Page Test
- **Primary**: Crossing entry point conversion (signup, purchase)
- **Secondary**: Time on page, scroll depth, Method section engagement
- **Guardrail**: Bounce rate, support tickets

---

## Designing Variants

### What to Vary (World Code Elements)

| Element | Control | Variant |
|---------|---------|---------|
| Headline | Climax Before State pain | Climax After State outcome |
| Subheadline | Generic description | Method Name + differentiator |
| CTA text | "Get Started" | Crossing-specific language |
| Social proof | Generic testimonial | Transformation story |
| Page structure | Features-first | Story arc (Before → Method → After) |

---

## Running the Test

### Pre-Launch Checklist
- [ ] Hypothesis documented with World Code reasoning
- [ ] Primary metric defined (Crossing conversion)
- [ ] Sample size calculated
- [ ] Variants implemented and QA'd
- [ ] Tracking verified
- [ ] Both variants use Voice consistently

### During the Test
**DO:** Monitor for technical issues, document external factors
**DON'T:** Peek and stop early, make changes, add new traffic sources

---

## Analyzing Results

### Analysis Checklist

1. Reached sample size?
2. Statistically significant? (95% confidence)
3. Effect size meaningful?
4. Secondary metrics consistent?
5. Guardrail metrics safe?
6. **World Code learning:** What does this tell us about our World Code assumptions?

### Building a World Code Testing Roadmap

Each test teaches you something about your World Code. Document learnings:

```
## Test: [Name]
- **World Code element tested:** [Climax/Method/Voice/Creation/Crossing]
- **Hypothesis:** [What we believed]
- **Result:** [What happened]
- **World Code learning:** [What we now know about our audience/positioning]
- **Next test:** [What to test next based on this learning]
```

---

## Output Format

**Apply the user's Voice (from world-code/voice.md) to all written output:**
- Use their Tone & Character
- Follow their Hard Rules (non-negotiable)
- Match their Sentence Structure & Rhythm
- Use their Vocabulary & Language preferences
- Incorporate their Authenticity Markers

---

## Common Mistakes
- **No hypothesis** — "Let's just test two versions" misses the learning opportunity
- **Testing copy without Voice** — Both variants should be in Voice; test the angle, not the tone
- **Ignoring World Code learnings** — Every test validates or challenges your World Code assumptions
- **Stopping early** — Pre-commit to sample size
- **Testing trivial changes** — Button color matters less than Climax promise framing

---

## Task-Specific Questions

Only ask what World Code doesn't already cover:

1. What's your current conversion rate?
2. How much traffic does this page get?
3. What change are you considering and why?
4. What tools do you have for testing?

---

## References

- [Sample Size Guide](references/ref-ab-test-sample-size.md) — Quick-reference tables and duration calculators
- [Test Templates](references/ref-ab-test-templates.md) — Test plan, results documentation, and hypothesis bank templates

## Related Skills

- **boring-page-cro**: For generating test ideas based on CRO principles
- **boring-analytics-tracking**: For setting up test measurement
- **boring-copywriting**: For creating variant copy in Voice
