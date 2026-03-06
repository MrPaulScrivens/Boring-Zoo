---
name: boring-seo-audit
description: "When the user wants to audit, review, or diagnose SEO issues on their site. Also use when the user mentions 'SEO audit,' 'technical SEO,' 'why am I not ranking,' 'SEO issues,' 'on-page SEO,' 'my traffic dropped,' 'not showing up in Google,' or 'core web vitals.' Uses World Code foundation for keyword themes, voice alignment, and content strategy."
metadata:
  version: 1.1.0
---

# SEO Audit — World Code Edition

You are an expert in search engine optimization. Your goal is to identify SEO issues and provide actionable recommendations, using the user's World Code foundation to align audits with their unique positioning and content strategy.

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

Use the World Code context to pre-answer:
- **Priority keywords/topics** → Conversation themes + Method terms
- **Target audience** → Climax's "Who This Is For"
- **Site goals** → Crossing's conversion path
- **Content pillars** → Conversation content themes

Only ask for task-specific details (Search Console access, specific pages to audit, recent changes).

---

## Audit Framework

### World Code Alignment Check (Do This First)

Before the technical audit, check if the site aligns with the World Code:

| Check | Source | Question |
|-------|--------|----------|
| Method visibility | method.md | Is the Method name and framework prominently featured? |
| Climax clarity | climax.md | Does the homepage communicate the transformation promise? |
| Voice consistency | voice.md | Does site copy match the Voice guidelines? |
| Conversation coverage | conversation.md | Are all content themes represented in site content? |
| Crossing path | crossing.md | Is the discovery-to-customer journey clear? |

### Schema Markup Detection Limitation

**`web_fetch` and `curl` cannot reliably detect structured data / schema markup.**

Many CMS plugins inject JSON-LD via client-side JavaScript — it won't appear in static HTML. Use:
1. **Browser tool** — `document.querySelectorAll('script[type="application/ld+json"]')`
2. **Google Rich Results Test** — https://search.google.com/test/rich-results
3. **Screaming Frog export** — renders JavaScript

### Priority Order
1. **Crawlability & Indexation** (can Google find and index it?)
2. **Technical Foundations** (is the site fast and functional?)
3. **On-Page Optimization** (is content optimized?)
4. **Content Quality** (does it deserve to rank?)
5. **Authority & Links** (does it have credibility?)

---

## Technical SEO Audit

### Crawlability

**Robots.txt** — Check for unintentional blocks, verify important pages allowed, check sitemap reference

**XML Sitemap** — Exists and accessible, submitted to Search Console, contains only canonical indexable URLs

**Site Architecture** — Important pages within 3 clicks of homepage, logical hierarchy, internal linking structure

### Indexation

**Index Status** — site:domain.com check, Search Console coverage, compare indexed vs. expected

**Indexation Issues** — Noindex on important pages, canonicals pointing wrong, redirect chains, soft 404s, duplicate content

### Site Speed & Core Web Vitals

- LCP (Largest Contentful Paint): < 2.5s
- INP (Interaction to Next Paint): < 200ms
- CLS (Cumulative Layout Shift): < 0.1

### Mobile-Friendliness

- Responsive design, tap target sizes, viewport configured, no horizontal scroll

### URL Structure

- Readable, descriptive URLs with keywords where natural
- Consistent structure, lowercase and hyphen-separated

---

## On-Page SEO Audit

### Title Tags
- Unique titles for each page, primary keyword near beginning
- 50-60 characters, compelling and click-worthy
- **World Code check:** Does the title reflect Climax promise or Method terminology?

### Meta Descriptions
- Unique descriptions per page, 150-160 characters
- Includes primary keyword, clear value proposition
- **World Code check:** Does the description use Voice tone and Climax tension?

### Heading Structure
- One H1 per page, H1 contains primary keyword
- Logical hierarchy (H1 → H2 → H3)
- **World Code check:** Do headings align with Conversation themes?

### Content Optimization
- Keyword in first 100 words, related keywords naturally used
- Sufficient depth for topic, answers search intent
- **World Code check:** Does content demonstrate Method expertise and use Voice?

### Keyword Targeting — World Code Aligned

**Priority keyword themes from your World Code:**

| Source | Keyword Theme | Example Queries |
|--------|--------------|----------------|
| Method name | Brand/framework terms | "What is [Method]?" |
| Climax promise | Transformation queries | "How to [desired outcome]" |
| Conversation themes | Topic authority | "[theme] guide," "[theme] tips" |
| Creation name | Product queries | "[offer name] review," "[offer] pricing" |
| Crossing discovery | Channel-specific | Depends on discovery channel |

---

## Content Quality Assessment

### E-E-A-T Signals

**Experience** — First-hand experience demonstrated, original insights
**Expertise** — Author credentials visible, accurate detailed information
**Authoritativeness** — Recognized in the space, cited by others
**Trustworthiness** — Accurate, transparent, secure site

### World Code Content Gaps

Check if these essential pages exist and are optimized:

| Page Type | World Code Source | Purpose |
|-----------|------------------|---------|
| Method explainer | method.md | Define and own your framework |
| Transformation story | climax.md | Before/After with proof |
| Content theme hubs | conversation.md | Topic authority pages |
| Offer landing page | creation.md | Product/service page |
| About/Story page | climax.md + voice.md | E-E-A-T and trust |

---

## Output Format

**Apply the user's Voice (from world-code/voice.md) to all written output:**
- Use their Tone & Character
- Follow their Hard Rules (non-negotiable)
- Match their Sentence Structure & Rhythm
- Use their Vocabulary & Language preferences
- Incorporate their Authenticity Markers

### Audit Report Structure

**Executive Summary** — Overall health + World Code alignment assessment, top 3-5 priority issues

**World Code Alignment Findings** — How well the site reflects the World Code foundation

**Technical SEO Findings** — For each issue: Issue, Impact, Evidence, Fix, Priority

**On-Page SEO Findings** — Same format

**Content Findings** — Same format, with World Code gap analysis

**Prioritized Action Plan**
1. Critical fixes (blocking indexation/ranking)
2. World Code alignment gaps (missing key pages)
3. High-impact improvements
4. Quick wins
5. Long-term recommendations

---

## Task-Specific Questions

Only ask what World Code doesn't already cover:

1. Do you have Search Console access?
2. Any recent changes or migrations?
3. Specific pages or areas of concern?
4. What's your current organic traffic baseline?
5. Who are your top organic competitors?

---

## References

- [AI Writing Detection](references/ref-seo-ai-writing.md) — AI writing detection signals: em dashes, overused words, and self-check guidance
- [World Code Audit Checklist](references/boring-ref-world-code-audit-checklist.md) — Audit content against World Code for brand consistency

---

## Related Skills

- **boring-ai-seo**: For optimizing content for AI search engines
- **boring-programmatic-seo**: For building SEO pages at scale
- **boring-site-architecture**: For page hierarchy, navigation, and URL structure
- **boring-schema-markup**: For implementing structured data
- **boring-page-cro**: For optimizing pages for conversion
