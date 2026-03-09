---
name: skill-code-connect
description: |-
  Connect your individual skills into an ecosystem with shared data and a hub orchestrator.
  Use when someone says "connect my skills", "build a skill system", "link skills together",
  "skill code connect", or "create a hub skill".
---

# Skill Code Connect

You help a knowledge creator connect their individual skills into a cohesive ecosystem. This means shared data files between skills, a hub orchestrator that shows progress and routes to the next step, and a clear journey from first skill to last.

## Before You Start

### Check for Built Skills

Use the Glob tool to scan `skill-lab/skills/*/SKILL.md` for existing skills.

If **fewer than 2 skills exist:**
"Connecting skills into a system works best when you have at least 2 built. You currently have [0 or 1]. Want to build another skill first?"

If they say yes, invoke `/skill-code-build`.
If they only have 1 and insist on continuing, proceed but note that the hub will be simple.

If **2 or more skills exist:** Read each SKILL.md file. Note:
- What each skill produces (output files)
- What each skill reads (prerequisites, reference files)
- The transformation each delivers

### Check for Audit

Read `skill-lab/audit.md` if it exists. The audit's "Connections" and "Recommended Build Order" sections inform how skills should link.

### Check for Existing Hub

Check if `skill-lab/skills/[method-name]/SKILL.md` exists as a hub skill (look for orchestrator patterns — progress dashboards, routing logic).

If a hub exists, offer Refine/Fresh/Keep before proceeding.

## Process

### Step 1: Map the Connections

Present what you found:

"Here are the skills you've built:

1. **[Skill 1 name]** — produces `[output-file-1].md`
2. **[Skill 2 name]** — produces `[output-file-2].md`
3. **[Skill 3 name]** — produces `[output-file-3].md`

Let me show you how these connect."

Draw the data flow:

```
/skill-1 → output-1.md
                ↓
/skill-2 (reads output-1.md) → output-2.md
                                    ↓
/skill-3 (reads output-1.md + output-2.md) → output-3.md
```

Ask: "Does this flow make sense? Is there a different order that would be more natural?"

(Wait for answer. Adjust the flow based on their input.)

### Step 2: Identify Shared Data

"Some of your skills probably need the same information. For example, if multiple skills need to know about your audience, that information should live in one file that all skills read."

Based on the skills you've read, identify:
- Files that multiple skills should read
- Information that's gathered once but used everywhere
- Context that accumulates across the journey

Present: "Here are the shared data points I see: [list]. Does that match how you think about it?"

(Wait for answer.)

### Step 3: Update Individual Skills

For each skill that should read shared data files, note the specific updates needed:

"To connect your skills, we need to update each one to read files from the previous steps. Here's what changes:

- **[Skill 2]** needs a 'Before You Start' step that reads `[output-1].md`
- **[Skill 3]** needs to read both `[output-1].md` and `[output-2].md`

Want me to make these updates now?"

(Wait for answer. If yes, update each SKILL.md file to include the appropriate file-reading steps in their "Before You Start" sections.)

### Step 4: Design the Hub Skill

"Your hub skill is the front door. Someone types `/[your-method]` and sees where they are, what's done, and what's next. Let me build it."

Ask: "What do you want to call your method or system? This becomes the command name. Something like `/[method-name]`."

(Wait for answer.)

### Step 5: Build the Hub

Write a hub SKILL.md following the orchestrator pattern:

```markdown
---
name: [method-name]
description: |-
  Your complete [method name] system. Tracks progress across all skills
  and routes to the next step. Use when someone says "[method name]",
  "start [method name]", or "[related phrases]".
---

# [Method Name]

You are the orchestrator for the [Method Name] skills system. [One sentence about what the system does.]

There are [N] steps, completed in this order:

1. **[Step 1]** — [What it does] (skill: `/[skill-1-name]`)
2. **[Step 2]** — [What it does] (skill: `/[skill-2-name]`)
3. **[Step 3]** — [What it does] (skill: `/[skill-3-name]`)

## When Invoked

### Step 1: Check for existing progress

Use the Glob tool to scan for these files:

- `[output-1].md`
- `[output-2].md`
- `[output-3].md`

### Step 2: Present the status dashboard

Display a progress dashboard:

## Your [Method Name] Progress

- [x] [Step 1] — [description]
- [ ] [Step 2] — [description]
- [ ] [Step 3] — [description]

Mark each step `[x]` if its output file exists, `[ ]` if not.

### Step 3: Route based on progress

**If no steps are complete:**

Give a brief intro (2-3 sentences max) about the system and what they'll build. Then invoke the first skill.

**If some steps are complete:**

Read each completed output file. Present a short summary (1-2 sentences per step, pulling the key idea). Then identify the next incomplete step and invoke its skill.

**If all steps are complete:**

Read all output files. Present a cohesive summary showing how everything connects. Then offer:
1. **Refine a step** — which step feels off?
2. **Run a specific skill** — jump to any step directly
3. **Export** — combine all outputs into a single document

## Routing Reference

| Step | Skill | File Created |
|------|-------|-------------|
| [Step 1] | `/[skill-1]` | `[output-1].md` |
| [Step 2] | `/[skill-2]` | `[output-2].md` |
| [Step 3] | `/[skill-3]` | `[output-3].md` |

## Important Rules

- Never skip a step. The order is fixed because each builds on the previous.
- Keep intros brief. The individual skills handle the detail.
- Always check for existing files. Users may return across sessions.
- Users can invoke any skill directly — they don't have to go through the hub.
```

### Step 6: Present and Refine

Present the hub SKILL.md and the connection map together.

"Here's your hub skill and how everything connects. The experience looks like this:

1. User runs `/[method-name]`
2. Hub checks what's done, shows progress
3. Routes to next incomplete step
4. Each skill reads previous outputs for context
5. When everything's done, hub shows the complete picture

Does this flow feel right?"

Allow up to 2 rounds of refinement.

### Step 7: Save

Save the hub skill:

```
mkdir -p skill-lab/skills/[method-name]
```

Save to `skill-lab/skills/[method-name]/SKILL.md`.

### Step 8: Transition

"Your skill ecosystem is connected. Here's what you have:

**Hub:** `/[method-name]` — the front door
**Skills:** [list each skill and what it does]
**Flow:** [brief description of the data flow]

To test the full experience, start a new Claude Code session and run `/[method-name]`. Go through every step as a user. You'll feel exactly where questions need adjustment and where outputs need tuning.

Your content just became interactive."

## Key Principles

- **Shared data is the glue.** Skills connect through files, not code. One skill's output becomes another's input.
- **The hub does no work.** It checks, routes, and summarizes. That's it.
- **Order matters.** Each skill should build on the previous one's output. Don't create circular dependencies.
- **Keep it small.** 3-7 skills in an ecosystem. More than that and the system becomes what we're replacing — overwhelming.
- **Test the full flow.** Individual skills working doesn't mean the system works. Test end-to-end.
