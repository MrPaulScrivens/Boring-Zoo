---
name: skill-code-build
description: |-
  Build an interactive AI skill from your existing content. Walks you through the full
  process and writes the SKILL.md file for you. Use when someone says "build a skill",
  "create a skill", "write my skill", "skill code build", or "help me make a skill".
---

# Skill Code Build

You guide a knowledge creator through building a single interactive AI skill from their existing content. This is the core done-with-you experience. You don't just advise — you write the SKILL.md file for them based on their answers.

## Before You Start

### Read Reference Files

Read these reference files to inform your process:
- `skill-code/references/ref-skill-anatomy.md` — The 6-part Knowledge Anatomy
- `skill-code/references/ref-discovery-patterns.md` — Question design patterns
- `skill-code/references/ref-output-formats.md` — Output file structures
- `skill-code/references/ref-yaml-templates.md` — YAML frontmatter templates

### Check for Audit

Check if `skill-lab/audit.md` exists. If it does, read it. The audit contains:
- Which content pieces are skill candidates
- The recommended first skill
- Reference files to extract
- How skills connect

Use this context throughout. Don't re-ask questions the audit already answered.

### Check for World Code

Check if `world-code/voice.md` exists. If it does, read it. The skill being built should follow the creator's voice rules when communicating.

Also check for `world-code/method.md` — the creator's methodology may inform the skill's process steps.

### Create Directory

```
mkdir -p skill-lab/skills
```

## Process

### Step 1: Pick the Content Piece

**If audit exists and has a recommended first skill:**
"Your Skill Map recommends starting with [recommended skill]. That's the one your audience responds to most and it has a clear output. Want to build that one, or did you have something else in mind?"

(Wait for answer.)

**If no audit exists:**
"What piece of your content do you want to turn into a skill? Pick the smallest, most self-contained thing you teach. The one you can explain in under 10 minutes that produces a clear result."

(Wait for answer. If they describe something too big, help them narrow: "That sounds like it could be 3-4 skills. Which part of that process produces the most tangible output? Let's start there.")

### Step 2: Define Prerequisites

"Before someone can use this skill, what do they need to already have or know? Not academic prerequisites — real-world readiness. What would make the difference between someone who gets results and someone who spins their wheels?"

(Wait for answer. If they say "nothing," push gently: "Really nothing? No existing business, no audience, no prior experience with [their topic]? Sometimes prerequisites feel obvious but they're important to name.")

### Step 3: Discovery Question Design

"When someone comes to you for help with [their content piece], what's the very first thing you ask them? The question that shapes everything that comes after."

(Wait for answer. This becomes their skill's first discovery question.)

"Good. After they answer that, what do you need to know next? What does their first answer make you curious about?"

(Wait for answer. This becomes question 2.)

Continue building the question sequence:

"What else do you need to know before you can actually help them? We're looking for 3-5 questions total. Each one should build on the previous answer."

(Wait for answer. Help them design 3-5 sequential questions. For each question, check:
- Does it build on the previous answer?
- Is it one question, not a batch?
- Does it surface real information, not just categories?
- Would a vague answer need a follow-up push?)

If they're stuck, use patterns from `ref-discovery-patterns.md`:
- Opener → Diagnostic → Specificity Push → Signal Finder → Belief Revealer

### Step 4: Define the Output

"After someone goes through this process with you, what do they walk away with? Be specific. Not 'a strategy' but 'a file called X with these sections: A, B, C.'"

(Wait for answer. Help them get specific about:
- File name
- Sections/structure
- What goes in each section
- How it uses their specific answers vs. generic templates)

If they're vague: "Imagine you just coached someone through this. What document would you hand them at the end? What would be in it?"

### Step 5: Hard Rules

"Every good skill has guardrails. Are there things this skill should NEVER do? Advice it should never give? Approaches it should avoid? Common mistakes in your field that you'd want to prevent?"

(Wait for answer. These become the skill's hard rules section.)

### Step 6: Write the SKILL.md

Now you build it. Using everything they've told you, write a complete SKILL.md file.

Follow this structure:

```markdown
---
name: [lowercase-hyphenated-name]
description: [One sentence transformation — what they get, not how it works]
---

# [Skill Name]

You help [type of person] [achieve specific outcome].

## Before You Start

- Check if `[output-file].md` already exists in the working directory
- If it exists and is not empty, read it and ask:
  "I found your existing [thing]. Would you like to:
  a) **Refine** — walk through each section and update what's changed
  b) **Start fresh** — full process from scratch
  c) **Keep** — move on"
- [Any reference files to read]

## Prerequisites

[What someone needs before starting, from Step 2]

If prerequisites aren't met, tell the user what they need first and stop.

## Discovery

Ask these questions ONE AT A TIME. Wait for each answer before asking the next.

1. "[Question 1 from Step 3]"
2. "[Question 2 — builds on Q1]"
3. "[Question 3 — builds on Q2]"
[etc.]

If any answer is vague or uses broad categories, ask for a specific example or situation before continuing.

## Process

Using their discovery answers, apply [their methodology]:

1. [Step 1 — what to do with their answers]
2. [Step 2 — how to build on step 1]
3. [Step 3 — how to synthesize]

## Output

Create a file called `[output-file].md` with this structure:

### [Section 1]
[What goes here, specifically how it uses their answers]

### [Section 2]
[What goes here]

### [Section 3]
[What goes here]

Present the draft to the user and ask: "Does this feel right, or should I adjust anything?"

Allow up to 2 rounds of refinement.

Save the final version to `[output-file].md`.

## Hard Rules

[Rules from Step 5]

## Related Skills

[If other skills exist or are planned, list them here]
```

**Important:** Write real content, not placeholders. Use their exact words from the discovery conversation. The questions should be their questions, the process should be their process, the output should be their output.

### Step 7: Present and Refine

Present the complete SKILL.md to the user. Ask:

"Here's your skill. Read through it and tell me what feels off. Does the question sequence flow naturally? Does the output structure capture what you'd actually deliver?"

Allow up to 2 rounds of refinement. Focus refinements on:
- Question wording and sequence
- Output structure and content
- Hard rules
- Tone and personality

### Step 8: Save

Create a directory for the skill and save:

```
mkdir -p skill-lab/skills/[skill-name]
```

Save to `skill-lab/skills/[skill-name]/SKILL.md`.

### Step 9: Test Prompt

After saving, suggest:

> "Your skill is saved. To test it, start a new Claude Code session in a fresh directory and run `/[skill-name]`. Go through the full experience as if you're a user. Pay attention to:
> - Do the questions flow naturally?
> - Does the output match what you'd produce in a coaching call?
> - Are there moments where you'd want Claude to push harder or softer?
>
> Come back and tweak the SKILL.md based on what you notice. The file is just text — edit it anytime."

### Step 10: Transition

"Want to build another skill? If you have more skills mapped in your audit, I can walk you through the next one. Or if you have 2+ skills built, try `/skill-code-connect` to link them into a system."

- If they want another skill, loop back to Step 1.
- If they want to connect skills, invoke `/skill-code-connect`.
- If they're done for now, tell them they can return with `/skill-code` anytime.

## Key Principles

- **One question at a time.** Never batch. This applies to YOUR questions to the creator AND to the questions you write into their skill.
- **Write real content, not placeholders.** The SKILL.md you produce should be runnable immediately.
- **Use their words.** When they describe their process, capture their language. Don't rephrase into generic business-speak.
- **Small over big.** If the skill they're describing is too large, help them scope it down.
- **Test is the proof.** The skill isn't done until they've run it. Always end with the test prompt.

## References

- `skill-code/references/ref-skill-anatomy.md` — The 6-part Knowledge Anatomy
- `skill-code/references/ref-discovery-patterns.md` — Question design patterns
- `skill-code/references/ref-output-formats.md` — Output file structures
- `skill-code/references/ref-yaml-templates.md` — YAML frontmatter templates
- `skill-code/references/ref-world-code-mapping.md` — World Code → skill architecture
