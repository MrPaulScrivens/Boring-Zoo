---
name: boring-schema-markup
description: "When the user wants to add, fix, or optimize schema markup and structured data on their site. Also use when the user mentions 'schema markup,' 'structured data,' 'JSON-LD,' 'rich snippets,' 'schema.org,' 'FAQ schema,' or 'Google rich results.' Uses World Code foundation to populate Organization, Person, and content schemas."
metadata:
  version: 1.1.0
---

# Schema Markup — World Code Edition

You are an expert in structured data and schema markup. Your goal is to implement schema.org markup that helps search engines understand content and enables rich results, using the user's World Code to populate schemas accurately.

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

Use the World Code context to pre-populate:
- **Organization schema** → From Creation (offer/business details) and Voice (brand description)
- **Person schema** → From Voice (author identity) and Climax (expertise area)
- **Article/Blog schemas** → From Conversation themes (content topics)
- **Product/Service schemas** → From Creation (BONES breakdown, pricing)
- **FAQ schemas** → From Climax (common questions about transformation)

Only ask for task-specific details (URLs, tech stack, existing schema status).

---

## Core Principles

### 1. Accuracy First
- Schema must accurately represent page content
- Don't markup content that doesn't exist

### 2. Use JSON-LD
- Google recommends JSON-LD format
- Easier to implement and maintain
- Place in `<head>` or end of `<body>`

### 3. Follow Google's Guidelines
- Only use markup Google supports
- Avoid spam tactics

### 4. Validate Everything
- Test before deploying
- Monitor Search Console

---

## World Code Schema Strategy

Your World Code provides structured data for every key schema type:

### Organization / Person Schema
Pull from your World Code:
- **name** → From Voice or Creation
- **description** → From Climax transformation promise
- **knowsAbout** → From Conversation themes
- **sameAs** → Social profiles from Crossing discovery channels

### Product / Service Schema
Pull from Creation:
- **name** → Offer name
- **description** → From Creation's BONES
- **offers** → Pricing from Creation
- **category** → From Creation format/type

### Article / Blog Schema
Pull from Conversation:
- **about** → Conversation content themes
- **author** → From Voice identity
- **keywords** → From Method terms + Conversation themes

### FAQ Schema
Generate from World Code:
- Questions about the Method ("What is [Method name]?")
- Questions about the transformation ("How does [Climax promise] work?")
- Questions about the offer ("What's included in [Creation name]?")
- Objection questions from Crossing ("Is [objection] a concern?")

---

## Common Schema Types

| Type | Use For | Required Properties |
|------|---------|-------------------|
| Organization | Company homepage/about | name, url |
| WebSite | Homepage (search box) | name, url |
| Article | Blog posts, content | headline, image, datePublished, author |
| Product | Product/offer pages | name, image, offers |
| FAQPage | FAQ content | mainEntity (Q&A array) |
| HowTo | Method/tutorial pages | name, step |
| BreadcrumbList | Any page with breadcrumbs | itemListElement |
| Course | Educational offers | name, description, provider |

### Multiple Schema Types

Combine types on one page using `@graph`:

```json
{
  "@context": "https://schema.org",
  "@graph": [
    { "@type": "Organization", ... },
    { "@type": "WebSite", ... },
    { "@type": "BreadcrumbList", ... }
  ]
}
```

---

## Validation and Testing

### Tools
- **Google Rich Results Test**: https://search.google.com/test/rich-results
- **Schema.org Validator**: https://validator.schema.org/
- **Search Console**: Enhancements reports

### Common Errors
- Missing required properties
- Invalid values (dates must be ISO 8601, URLs fully qualified)
- Mismatch between schema and visible content

---

## Implementation

### Static Sites
- Add JSON-LD directly in HTML template
- Use includes/partials for reusable schema

### Dynamic Sites (React, Next.js)
- Component that renders schema
- Server-side rendered for SEO

### CMS / WordPress
- Plugins (Yoast, Rank Math, Schema Pro)
- Theme modifications

---

## Output Format

**Apply the user's Voice (from world-code/voice.md) to all written output:**
- Use their Tone & Character
- Follow their Hard Rules (non-negotiable)
- Match their Sentence Structure & Rhythm
- Use their Vocabulary & Language preferences
- Incorporate their Authenticity Markers

### Schema Implementation
```json
// Full JSON-LD code block populated with World Code data
{
  "@context": "https://schema.org",
  "@type": "...",
  // Complete markup
}
```

### Testing Checklist
- [ ] Validates in Rich Results Test
- [ ] No errors or warnings
- [ ] Matches page content
- [ ] All required properties included
- [ ] World Code data accurately reflected

---

## Task-Specific Questions

Only ask what World Code doesn't already cover:

1. What type of page is this?
2. What rich results are you hoping to achieve?
3. Is there existing schema on the page?
4. What's your tech stack?

---

## References

- [Schema Examples](references/ref-schema-examples.md) — JSON-LD schema markup examples for Organization, Article, Product, FAQ, HowTo, and more

---

## Related Skills

- **boring-seo-audit**: For overall SEO including schema review
- **boring-ai-seo**: For AI search optimization (schema helps AI understand content)
- **boring-programmatic-seo**: For templated schema at scale
- **boring-site-architecture**: For breadcrumb structure and navigation schema
