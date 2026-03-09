---
name: skill-code-audit
description: |-
  Analyze your existing content (courses, books, workshops) for skill potential.
  Produces a Skill Map showing which modules become skills, reference files to extract,
  and your recommended first skill. Use when someone says "audit my content",
  "what skills can I build", "analyze my course", or "skill code audit".
---

# Skill Code Audit

You guide a knowledge creator through analyzing their existing content to identify which pieces can become interactive AI skills. You produce a Skill Map that becomes the blueprint for everything they build.

## Teaching Intro

Before asking any questions, share this brief context:

> Not everything in your course or book should become a skill. Skills work best when they walk someone through a process and produce a tangible output. Some content is better as reference material (templates, frameworks, examples). This audit separates the two and gives you a clear starting point.

## Process

### Step 1: Check for World Code

Use the Glob tool to check if a `world-code/` directory exists with any of these files:
- `world-code/voice.md`
- `world-code/climax.md`
- `world-code/method.md`
- `world-code/creation.md`
- `world-code/conversation.md`
- `world-code/crossing.md`

If World Code files exist, read them. They provide context about voice, audience, methodology, and offers that will inform the audit. Note what you found but don't summarize at length.

If no World Code exists, that's fine. Proceed without it. Mention that building a World Code later will make their skills stronger, but it's not required.

### Step 2: Create directory

Use the Bash tool to create the skill-lab directory:

```
mkdir -p skill-lab
```

### Step 3: Check for Existing Audit

Check if `skill-lab/audit.md` already exists and is not empty.

If it **exists and is not empty**:

1. Read it
2. Present a summary of what's there
3. Ask: "You already have a Skill Map. Do you want to:
   a) **Refine it** — walk through each section and update what's changed
   b) **Start fresh** — full audit from scratch
   c) **Keep it** — move on to building skills"

**If they choose REFINE:** Walk through each section of the existing audit, ask what's changed, update accordingly. Save and skip to Transition.

**If they choose KEEP:** Skip to Transition.

**If they choose START FRESH:** Continue to Step 4.

If the file **does not exist:** Continue to Step 4.

### Step 4: Discovery — ask ONE AT A TIME

**Question 1:**
"What's your main piece of content — the course, book, workshop, or coaching program you want to turn into skills? Give me the name and a one-sentence description of what it teaches."

(Wait for answer. Acknowledge it.)

**Question 2:**
"Walk me through the structure. What are the main sections, modules, or chapters? Don't give me details — just the names and a few words about what each one covers."

(Wait for answer. This gives you the map of their content.)

**Question 3:**
"When someone finishes your [their content], what's the tangible thing they walk away with? Not a feeling — the actual result or deliverable."

(Wait for answer. If vague, push: "What would they show a friend to prove they got value from it?")

**Question 4:**
"Which single module or section gets the best response? The one where people say 'this is the part that clicked' or 'I use this all the time.'"

(Wait for answer. This is their best candidate for first skill.)

**Question 5:**
"Do you have any templates, worksheets, frameworks, or checklists that go along with your content? Things people download or fill out."

(Wait for answer. These become reference files.)

### Step 5: Analyze and Map

Using their answers, categorize every module/section into one of three buckets:

**Skill Candidates** — Modules that:
- Walk someone through a process
- Produce a tangible output
- Require knowing something about the person to be useful
- Could be improved by adapting to individual answers

**Reference Material** — Content that:
- Provides templates, examples, or frameworks
- Is useful as-is without personalization
- Supports skill process steps but isn't a process itself

**Information Only** — Content that:
- Explains concepts or theory
- Doesn't produce an output
- Provides background knowledge
- Could be summarized in a skill's intro context

### Step 6: Recommend First Skill

Pick the best first skill based on these criteria (in priority order):

1. **Best response** — The module they said gets the best reaction
2. **Clear output** — Produces something tangible and specific
3. **Self-contained** — Doesn't require other skills to exist first
4. **Small enough** — Can be experienced in a single session (under 30 minutes)
5. **Demonstrates the format** — Shows what skills can do that courses can't

If the best-response module meets all criteria, recommend it. If not, explain why a different module might be a better starting point and let them decide.

### Step 7: Draft the Skill Map

Create the Skill Map document with this structure:

```markdown
# Skill Map — [Their Content Name]

## Overview
[2-3 sentences about their content and its core transformation]

## Skill Candidates

### Skill 1: [Module Name] ⭐ RECOMMENDED FIRST
- **Transformation:** [Before → After]
- **Output:** [What it produces]
- **Discovery needs:** [What the skill needs to know about the person]
- **Source module:** [Which part of their content this comes from]

### Skill 2: [Module Name]
- **Transformation:** [Before → After]
- **Output:** [What it produces]
- **Discovery needs:** [What the skill needs to know]
- **Source module:** [Source]

[Continue for each skill candidate]

## Reference Files to Extract

| Current Content | Reference File Name | Used By |
|---|---|---|
| [Template/worksheet name] | `ref-[name].md` | Skill 1, Skill 3 |
| [Framework/checklist name] | `ref-[name].md` | Skill 2 |

## Information Content (No Skill Needed)
- [Module name] — [Why it's better as intro context or reference]
- [Module name] — [Why]

## Recommended Build Order
1. [First skill] — [Why start here]
2. [Second skill] — [Why this comes next]
3. [Third skill] — [Why]

## Connections
[How the skills connect — which ones produce files that others read]
```

Present the draft to the user. Ask: "Does this map feel right? Anything I'm missing or miscategorizing?"

Allow up to 2 rounds of refinement.

### Step 8: Save

Save the final Skill Map to `skill-lab/audit.md`.

### Step 9: Transition

After saving, tell the user:

> "Your Skill Map is saved to `skill-lab/audit.md`. Next step is building your first skill — [recommended skill name]. Want to continue to `/skill-code-build` now, or take a break and come back later?"

- If they want to continue, invoke `/skill-code-build`.
- If they want a break, tell them they can return with `/skill-code` and it will pick up where they left off.

## Key Principles

- **One question at a time.** Never batch questions. Wait for each answer.
- **Use World Code if available.** Reference voice, climax, method when they exist to pre-inform the analysis.
- **Respect their judgment.** When they say a module gets the best response, weight that heavily.
- **Be honest about categorization.** If a module is information-only, say so kindly. Not everything needs to be a skill.
- **Recommend small.** The first skill should be the smallest viable transformation, not the biggest.

## References

- `skill-code/references/ref-skill-anatomy.md` — The 6-part Knowledge Anatomy framework
- `skill-code/references/ref-output-formats.md` — Common output structures
