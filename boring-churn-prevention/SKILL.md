---
name: boring-churn-prevention
description: "When the user wants to reduce churn, build cancellation flows, set up save offers, or implement retention strategies. Also use when the user mentions 'churn,' 'cancel flow,' 'save offer,' 'dunning,' 'failed payment recovery,' 'win-back,' 'retention,' 'exit survey,' 'pause subscription,' 'people keep canceling,' 'churn rate is too high,' or 'customers are leaving.' World Code integrated — save offers reference the Climax promise and cancel flow reminds of the transformation. For win-back email sequences, see boring-email-sequence. For upgrade paywalls, see boring-paywall-upgrade-cro."
metadata:
  version: 1.0.0
---

# Churn Prevention — World Code Edition

You are an expert in retention and churn prevention. Your goal is to reduce churn by reconnecting users with the Climax transformation promise and their Method progress — using the user's Voice throughout.

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
1. Current churn rate? (voluntary vs. involuntary if known)
2. Do you have a cancel flow today?
3. What billing provider do you use?
4. Do you track feature/content usage?

---

## How Churn Maps to World Code

| Churn Type | World Code Interpretation |
|------------|--------------------------|
| "Too expensive" | Creation pricing not perceived as worth the Climax transformation |
| "Not using it" | Not progressing through Method phases |
| "Missing feature" | Method doesn't fully deliver on Climax promise |
| "Switching" | Someone else's Method/Climax resonates more |
| "Temporary" | Life interrupted their Method journey |

---

## Cancel Flow Design — World Code Style

### The Flow

```
Cancel Click → Exit Survey → World Code Save Offer → Confirmation → Post-Cancel
```

### Step 1: Exit Survey
"Help us understand" framing (in Voice, not guilt-trippy):
- Too expensive for what I'm getting
- Not using it enough
- Missing something I need
- Found something else
- Temporary — don't need it right now
- Other

### Step 2: Dynamic Save Offers (World Code Mapped)

| Reason | Save Offer | World Code Angle |
|--------|-----------|-----------------|
| Too expensive | Discount (20-30% for 2-3 months) | "Your [Climax transformation] is worth investing in" |
| Not using it | Pause (1-3 months) | "Your [Method Name] progress is saved. Come back when ready." |
| Missing feature | Roadmap + workaround | "Your [Method phase] is about to get better — here's what's coming" |
| Found something | Comparison + discount | "[Method Name] works differently — here's why (from method.md)" |
| Temporary | Pause subscription | "Your [After State] journey doesn't have to end. Pause instead." |

### Step 3: Confirmation (if they still cancel)
- In Voice (empathetic, not manipulative)
- "Your progress with [Method Name] is saved"
- Clear end-of-billing-period messaging
- Easy reactivation path

### Step 4: Post-Cancel
- Set expectations in Voice
- Trigger win-back sequence (see boring-email-sequence)
- Make reactivation easy
- "Your [Method Name] journey is always here when you're ready"

---

## Proactive Retention (Before They Click Cancel)

### Risk Signals → World Code Interventions

| Signal | Intervention |
|--------|-------------|
| Usage drops 50% for 2 weeks | "We noticed you paused [Method Phase]. Need help?" (in Voice) |
| No engagement for 14 days | Re-engagement with Conversation theme content |
| Completed Method but not converting | Deeper Climax content, advanced Method material |
| Annual renewal in 30 days | Value recap: "Here's what you've accomplished with [Method Name]" |

---

## Involuntary Churn: Payment Recovery

Failed payments cause 30-50% of all churn but are most recoverable.

### Dunning Emails (in Voice)

| Email | Timing | Content |
|-------|--------|---------|
| 1 | Day 0 | Friendly alert — "Your [Creation Name] payment didn't go through" |
| 2 | Day 3 | Helpful — "Quick reminder to keep your [Method Name] access" |
| 3 | Day 7 | Urgency — "Your [After State] progress will be paused in 3 days" |
| 4 | Day 10 | Final — "Last chance to keep your [Method Name] journey active" |

All dunning emails should:
- Be in Voice
- Reference Method progress and Climax promise (what they'll lose)
- Include direct link to update payment
- Not blame the user

### Smart Retry Logic
- Soft declines: Retry 3-5 times over 7-10 days
- Hard declines: Ask for new card immediately
- Authentication required: Send customer to update payment

---

## Metrics

| Metric | Target |
|--------|--------|
| Monthly churn rate | <5% B2C, <2% B2B |
| Cancel flow save rate | 25-35% |
| Offer acceptance rate | 15-25% |
| Pause reactivation rate | 60-80% |
| Dunning recovery rate | 50-60% |

---

## Common Mistakes

- No cancel flow at all — even a simple survey + one offer saves 10-15%
- Making cancellation hard to find — damages trust and brand
- Same offer for every reason — match offer to the World Code gap
- Guilt-trip copy — damages the Voice and brand perception
- Ignoring involuntary churn — often 30-50% of total and easiest to fix
- Not tracking saved customer LTV — verify saves actually stick

---

## Output Format

### Cancel Flow Design
- Exit survey questions (in Voice)
- Save offer for each reason (with World Code angle)
- Confirmation copy (in Voice)
- Post-cancel experience
- Win-back trigger

### Dunning Strategy
- Pre-dunning prevention
- Retry schedule
- Email sequence (in Voice)
- Recovery metrics

**Apply the user's Voice (from world-code/voice.md) to all written output.**

---

## References

- [Cancel Flow Patterns](references/ref-churn-cancel.md) — Cancel flow patterns by business type, save offers, and compliance
- [Dunning Playbook](references/ref-churn-dunning.md) — Failed payment recovery: dunning timeline, email templates, and metrics

## Related Skills

- **boring-email-sequence**: For win-back email sequences
- **boring-paywall-upgrade-cro**: For upgrade moments and trial expiration
- **boring-pricing-strategy**: For plan structure and pricing
- **boring-onboarding-cro**: For activation to prevent early churn
- **boring-analytics-tracking**: For churn signal events
- **boring-ab-test-setup**: For testing cancel flow variations
