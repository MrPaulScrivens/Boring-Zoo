# Output Formats — Reference

Common output file formats for skills.

## General Principles

- Every skill produces a tangible file
- File name should be descriptive and lowercase with hyphens
- Use markdown format (.md)
- Include clear section headers
- Present to the user for review before saving
- Allow 1-2 rounds of refinement

## Common Output Structures

### Strategy/Plan Output
```markdown
# [Strategy/Plan Name]

## Summary
[2-3 sentence overview of the strategy based on their specific situation]

## Context
- [Key fact from discovery]
- [Key fact from discovery]
- [Key fact from discovery]

## The Plan
### Phase 1: [Name]
[What to do, why, and expected outcome]

### Phase 2: [Name]
[What to do, why, and expected outcome]

### Phase 3: [Name]
[What to do, why, and expected outcome]

## Next Steps
[Immediate actions to take]
```

### Profile/Assessment Output
```markdown
# [Profile/Assessment Name]

## Overview
[Summary statement about the person/business based on discovery]

## Key Findings
### [Finding 1 Name]
[Detail based on their specific answers]

### [Finding 2 Name]
[Detail]

### [Finding 3 Name]
[Detail]

## Recommendations
1. [Specific recommendation based on findings]
2. [Specific recommendation]
3. [Specific recommendation]
```

### Content/Copy Output
```markdown
# [Content Piece Name]

## Brief
- Audience: [from discovery]
- Goal: [from discovery]
- Tone: [from voice/discovery]

## Draft
[The actual content, written using their methodology and voice]

## Notes
- [Why specific choices were made]
- [Alternatives considered]
```

### SKILL.md Output (for /skill-code-build)
```markdown
---
name: [skill-name]
description: [One sentence transformation description]
---

# [Skill Name]

[Role statement — who the skill is and what it helps with]

## Before You Start

- Check if `[output-file].md` exists
- If yes, offer Refine/Fresh/Keep
- [Any reference files to read]

## Discovery

Ask these questions ONE AT A TIME. Wait for each answer before asking the next.

1. "[Question]"
2. "[Question based on Q1 context]"
3. "[Question based on Q2 context]"

If any answer is vague, push for a specific example before continuing.

## Process

[Methodology steps using discovery answers]

## Output

Create `[output-file].md` with:

### [Section 1]
[What goes here]

### [Section 2]
[What goes here]

Present draft and ask for feedback. Allow up to 2 refinement rounds.

Save the final version.
```

## File Naming Conventions

| Output Type | Naming Pattern | Example |
|---|---|---|
| Profile/assessment | `[topic]-profile.md` | `audience-profile.md` |
| Strategy/plan | `[topic]-strategy.md` | `content-strategy.md` |
| Content draft | `[type]-draft.md` | `welcome-email-draft.md` |
| Framework/system | `[name]-system.md` | `posting-system.md` |
| Audit/analysis | `[topic]-audit.md` | `course-audit.md` |
| Skill file | `SKILL.md` (in named directory) | `my-method/SKILL.md` |
