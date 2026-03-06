---
name: boring-product-marketing-context
description: "Generate a World Code Summary document that compiles all 6 World Code foundation files into a single reference. Use when you need to create a product-marketing-context.md file for non-World-Code tools, when the user says 'generate my context,' 'export my World Code,' 'create a marketing summary,' 'product context,' or 'compile my World Code.' This replaces the old product-marketing-context workflow — your World Code IS your product marketing context."
metadata:
  version: 1.0.0
---

# World Code Summary Generator

You compile the user's 6 World Code foundation files into a single product marketing context document. This is useful when working with tools that expect a traditional product-marketing-context.md file.

## Before Starting — Load Your World

Read the user's World Code foundation files:
- `world-code/voice.md`
- `world-code/climax.md`
- `world-code/method.md`
- `world-code/creation.md`
- `world-code/conversation.md`
- `world-code/crossing.md`

If ANY file is missing, tell the user:
> "This skill needs your World Code foundation. Run `/world-code-start` first to build it."

---

## What This Skill Does

Instead of asking the user dozens of questions about their product, audience, and positioning (like the old product-marketing-context workflow), this skill:

1. Reads all 6 World Code files
2. Compiles them into a single summary document
3. Maps World Code elements to traditional marketing context fields
4. Saves the result as `.agents/product-marketing-context.md`

**The World Code IS the product marketing context.** This skill just reformats it for compatibility.

---

## Compilation Mapping

| Traditional Context Field | World Code Source |
|--------------------------|-------------------|
| Product Overview | `creation.md` → Offer Name, Format |
| One-liner | `climax.md` → Transformation Promise |
| Target Audience | `climax.md` → Who This Is For |
| Primary Use Case | `climax.md` → Before State → After State |
| Jobs to Be Done | `climax.md` → Transformation Promise |
| Problems & Pain Points | `climax.md` → Before State |
| Differentiation | `method.md` → Why It Works Differently |
| Competitive Landscape | `method.md` → implied by differentiation |
| Objections | `crossing.md` → The Real Objection |
| Customer Language | `voice.md` → Vocabulary & Language |
| Brand Voice | `voice.md` → Tone & Character, Hard Rules |
| Content Pillars | `conversation.md` → Content Themes |
| Proof Points | Gathered separately (not in World Code) |
| Goals | `crossing.md` → Discovery Channel, Entry Point |
| Pricing | `creation.md` → Pricing |
| Switching Dynamics | `crossing.md` → Readiness Signals, The Real Objection |

---

## Output Format

Generate `.agents/product-marketing-context.md` with this structure:

```markdown
# Product Marketing Context — Generated from World Code

*Auto-generated from World Code foundation files. Edit the source files in `world-code/` to update.*
*Last generated: [date]*

## Product Overview
**Offer:** [From creation.md — Offer Name]
**Format:** [From creation.md — Format]
**What it does:** [From creation.md — BONES summary]
**Pricing:** [From creation.md — Pricing]

## Target Audience
**Who it's for:** [From climax.md — Who This Is For]
**Their current state:** [From climax.md — Before State]
**What they want:** [From climax.md — After State]

## The Transformation
**Promise:** [From climax.md — Transformation Promise]
**How we deliver it:** [From method.md — Method Name and Core Principle]
**Why it works differently:** [From method.md — Why It Works Differently]

## Voice & Language
**Tone:** [From voice.md — Tone & Character]
**Hard Rules:** [From voice.md — Hard Rules]
**Authenticity Markers:** [From voice.md — Authenticity Markers]

## Content Strategy
**Core Message:** [From conversation.md — Core Message]
**Wrong Belief:** [From conversation.md — Wrong Belief]
**Content Themes:** [From conversation.md — Content Themes]
**Platform:** [From conversation.md — Platform]
**Rhythm:** [From conversation.md — Posting Rhythm]

## Conversion Strategy
**Discovery Channel:** [From crossing.md — Discovery Channel]
**Entry Point:** [From crossing.md — Entry Point]
**Buying Experience:** [From crossing.md — Buying Experience]
**Real Objection:** [From crossing.md — The Real Objection]
**Readiness Signals:** [From crossing.md — Readiness Signals]

---
*Source: World Code foundation files in `world-code/`*
*To update, edit the source files and regenerate with `/boring-product-marketing-context`*
```

---

## After Generating

Tell the user:
> "Your World Code has been compiled into `.agents/product-marketing-context.md`. Non-World-Code marketing tools will use this automatically. To update it, edit your World Code files and run this skill again."

---

## References

- [World Code Audit Checklist](references/boring-ref-world-code-audit-checklist.md) — Audit any marketing asset against all 6 World Code elements

---

## Related Skills

- **world-code-start**: Build or check your World Code foundation
- All `boring-` skills read World Code directly — they don't need this summary file
