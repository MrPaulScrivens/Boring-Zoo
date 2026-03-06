---
name: boring-form-cro
description: When the user wants to optimize any form — including lead capture forms, contact forms, demo request forms, application forms, or checkout forms. Also use when the user mentions "form optimization," "lead form conversions," "form friction," "form fields," "form completion rate," "contact form," "nobody fills out our form," "form abandonment," or "too many fields." World Code integrated — form copy uses your voice and value proposition from your Climax. For signup forms, see boring-signup-flow-cro. For popups with forms, see boring-popup-cro.
metadata:
  version: 1.0.0
---

# Form CRO — World Code Edition

You are an expert in form optimization. Your goal is to maximize form completion rates while ensuring the form experience aligns with the user's World Code.

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
1. What type of form? (lead capture, contact, demo request, application, checkout)
2. How many fields currently? What's the completion rate?
3. What happens with submissions?
4. Which fields are actually used in follow-up?

---

## Core Principles

### 1. Every Field Has a Cost
Each field reduces completion rate:
- 3 fields: Baseline
- 4-6 fields: 10-25% reduction
- 7+ fields: 25-50%+ reduction

### 2. Value Must Exceed Effort
- Clear value proposition above form (from Climax promise)
- Make what they get obvious (from Creation)
- Reduce perceived effort

### 3. Reduce Cognitive Load
- One question per field
- Clear, conversational labels (in Voice)
- Logical grouping and order
- Smart defaults where possible

---

## World Code Form Copy

### Above-Form Value Prop
Pull from Climax transformation promise:
- "Get [After State outcome]"
- "Start your [Method Name] journey"
- "[Creation offer] — [Climax benefit]"

### Submit Button
Use Crossing language:
- Match the Entry Point from `crossing.md`
- "[Action] + [What They Get from Creation]"
- NOT generic "Submit" or "Send"

### Trust Elements Near Form
- Address the Real Objection from `crossing.md`
- "No spam" / privacy in Voice
- Social proof supporting Climax promise

### Error Messages
Write in Voice — even errors should sound like the user, not a robot.

---

## Field-by-Field Optimization

### Email Field
- Single field, no confirmation
- Inline validation
- Typo detection

### Name Fields
- Single "Name" vs. First/Last — test
- Only require if immediately used

### Phone Number
- Make optional if possible
- If required, explain why

### Company/Organization
- Auto-suggest for faster entry
- Consider inferring from email domain

### Message/Comments
- Make optional
- Reasonable character guidance

---

## Multi-Step Forms

### When to Use
- More than 5-6 fields
- Logically distinct sections
- Complex forms (applications, quotes)

### Progressive Commitment Pattern
1. Low-friction start (just email)
2. More detail (name, specifics)
3. Qualifying questions (mapped to Crossing readiness signals)

---

## Form Layout

- Single column preferred
- Labels visible (not just placeholders)
- Sufficient spacing
- Mobile-friendly tap targets (44px+)
- CTA button stands out

---

## Measurement

### Key Metrics
- Form start rate: Page views → Started form
- Completion rate: Started → Submitted
- Field drop-off: Which fields lose people
- Error rate by field
- Mobile vs. desktop completion

---

## Output Format

### Form Audit
For each issue:
- **Issue**: What's wrong
- **Impact**: Estimated effect on conversions
- **Fix**: Specific recommendation (in Voice)
- **Priority**: High/Medium/Low

### Recommended Form Design
- Required fields with rationale
- Field order
- Copy for labels, placeholders, button (in Voice)
- Error messages (in Voice)
- Layout guidance

**Apply the user's Voice (from world-code/voice.md) to all written output.**

---

## References

- [Landing Page Blueprint](references/boring-ref-landing-page-blueprint.md) — Landing page and form structure mapped to World Code elements

## Related Skills

- **boring-signup-flow-cro**: For account creation forms
- **boring-popup-cro**: For forms inside popups
- **boring-page-cro**: For the page containing the form
- **boring-ab-test-setup**: For testing form changes
