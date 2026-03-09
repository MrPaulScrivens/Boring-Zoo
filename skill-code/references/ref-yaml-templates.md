# YAML Frontmatter Templates — Reference

Templates for skill YAML frontmatter (the "label on the jar").

## Basic Template

```yaml
---
name: skill-name
description: One sentence describing the transformation this skill delivers
---
```

## Naming Rules

- Lowercase letters only
- Hyphens between words (no spaces, underscores, or camelCase)
- Descriptive, not clever
- Short enough to type quickly
- Verb-noun pattern preferred

### Good Names
- `write-welcome-email`
- `build-content-calendar`
- `define-audience`
- `create-pricing-strategy`
- `audit-landing-page`

### Bad Names
- `email-wizard-pro` (clever, not descriptive)
- `step_3_content` (underscores, numbered)
- `myMethodFramework` (camelCase)
- `the-ultimate-complete-comprehensive-guide-to-emails` (too long)

## Description Guidelines

The description should:
- Complete the sentence "This skill helps you..." without starting with those words
- Be one sentence
- Name the transformation, not the process
- Be specific enough that someone knows what they'll get

### Good Descriptions
- `Craft a 5-email welcome sequence tailored to your audience and offer`
- `Identify your ideal client profile based on your best past work`
- `Build a weekly content calendar aligned with your business goals`

### Bad Descriptions
- `Helps with emails` (too vague)
- `This skill walks you through a comprehensive process for analyzing, designing, and implementing a multi-channel email marketing strategy` (too long, describes process instead of outcome)
- `Email stuff` (unhelpful)

## Hub Skill Template

```yaml
---
name: your-method
description: Your complete [method name] system — audit, build, and connect your skills
---
```

Hub skills use the method/system name and describe the scope.

## Addon Skill Template

```yaml
---
name: method-specific-task
description: [Specific transformation] using the [method name] framework
---
```

Addon skills can optionally reference the parent method in their description.
