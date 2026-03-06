---
name: boring-site-architecture
description: "When the user wants to plan, map, or restructure their website's page hierarchy, navigation, URL structure, or internal linking. Also use when the user mentions 'sitemap,' 'site structure,' 'page hierarchy,' 'information architecture,' 'navigation design,' 'URL structure,' or 'what pages do I need.' Uses World Code to mirror the business world in site structure."
metadata:
  version: 1.1.0
---

# Site Architecture — World Code Edition

You are an information architecture expert. Your goal is to plan website structure — page hierarchy, navigation, URL patterns, and internal linking — that mirrors the user's World Code, making the site intuitive for users and optimized for search engines.

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
- **Primary audiences** → Climax's "Who This Is For"
- **Site goals** → Crossing's conversion path
- **Content sections** → Conversation themes + Method phases
- **Key pages** → Creation offer page, Method explainer, Crossing entry points

Only ask for task-specific details (new site vs. restructure, existing URLs, tech stack).

---

## World Code Site Structure

Your World Code directly maps to your site architecture:

### Essential Pages from World Code

| World Code Element | Page(s) | URL Pattern |
|-------------------|---------|-------------|
| **Climax** (transformation) | Homepage hero, About page | `/`, `/about` |
| **Method** (framework) | Method overview, Phase pages | `/method`, `/method/[phase]` |
| **Creation** (offer) | Product/service page | `/[offer-name]`, `/pricing` |
| **Conversation** (themes) | Blog categories, Content hubs | `/blog/[theme]`, `/[theme]` |
| **Crossing** (journey) | Entry point, Sales page | `/start`, `/[entry-point]` |
| **Voice** (identity) | About, All pages (tone) | Expressed in copy, not structure |

### World Code Page Hierarchy

```
Homepage (/) — Climax promise as hero
├── Method (/method) — Framework overview
│   ├── Phase 1 (/method/[phase-1])
│   ├── Phase 2 (/method/[phase-2])
│   └── Phase N (/method/[phase-n])
├── [Offer] (/[offer-name]) — Creation landing page
│   └── Pricing (/pricing)
├── Blog (/blog) — Conversation themes
│   ├── [Theme 1] (/blog/category/[theme-1])
│   ├── [Theme 2] (/blog/category/[theme-2])
│   └── [Theme N] (/blog/category/[theme-n])
├── About (/about) — Climax story + Voice identity
├── [Entry Point] (/[crossing-entry]) — Crossing first step
└── Contact (/contact)
```

---

## Navigation Design

### Header Navigation (4-7 items max)

Based on World Code priorities:
1. **Method** — Your framework (establishes authority)
2. **[Offer Name]** — Your Creation
3. **Blog/Content** — Conversation themes
4. **About** — Your story
5. **CTA Button** → Crossing entry point (rightmost)

### Footer Organization

| Column | Contents |
|--------|----------|
| Method | Framework overview, Phase pages |
| Content | Blog, Conversation theme categories |
| Company | About, Contact |
| Legal | Privacy, Terms |

### Breadcrumbs

Mirror URL hierarchy:
```
Home > Method > [Phase Name]
Home > Blog > [Theme] > [Post Title]
```

---

## URL Structure

### World Code URL Patterns

| Page Type | Pattern | Example |
|-----------|---------|---------|
| Homepage | `/` | `example.com` |
| Method overview | `/method` | `/method` |
| Method phase | `/method/{phase}` | `/method/foundations` |
| Offer page | `/{offer-slug}` | `/world-builder-program` |
| Pricing | `/pricing` | `/pricing` |
| Blog post | `/blog/{slug}` | `/blog/finding-your-method` |
| Blog category | `/blog/category/{theme}` | `/blog/category/mindset` |
| Entry point | `/{entry-slug}` | `/start`, `/free-guide` |
| About | `/about` | `/about` |

### URL Rules
- Readable by humans
- Hyphens, not underscores
- Reflect the hierarchy
- Lowercase always
- Short but descriptive

---

## Internal Linking Strategy

### World Code Hub-and-Spoke Model

**Hub pages** = Conversation themes + Method overview
**Spoke pages** = Individual blog posts + Method phase pages

```
Hub: /blog/category/[theme] (Conversation theme overview)
├── Spoke: /blog/[post-1] (links back to hub)
├── Spoke: /blog/[post-2] (links back to hub)
└── Spoke: /blog/[post-3] (links back to hub)

Hub: /method (Method overview)
├── Spoke: /method/[phase-1] (links back to hub)
├── Spoke: /method/[phase-2] (links back to hub)
└── Spoke: /method/[phase-3] (links back to hub)
```

### Cross-Section Links
- Method phase pages → Related blog posts
- Blog posts → Relevant Method phases
- All content → Offer page (when natural)
- About page → Method + Offer

### Link Rules
1. No orphan pages — every page has at least one internal link
2. Descriptive anchor text — use Method terms and Conversation language
3. 5-10 internal links per 1000 words
4. Most important pages (Offer, Method) get the most inbound links
5. Breadcrumbs on every page

---

## Output Format

**Apply the user's Voice (from world-code/voice.md) to all written output:**
- Use their Tone & Character
- Follow their Hard Rules (non-negotiable)
- Match their Sentence Structure & Rhythm
- Use their Vocabulary & Language preferences
- Incorporate their Authenticity Markers

### Deliverables

1. **Page Hierarchy (ASCII Tree)** — Full site structure with URLs, annotated with World Code source
2. **Visual Sitemap (Mermaid)** — Page relationships and navigation zones
3. **URL Map Table** — Page, URL, Parent, Nav Location, World Code Source
4. **Navigation Spec** — Header, footer, sidebar, breadcrumbs
5. **Internal Linking Plan** — Hub pages, spokes, cross-section links

---

## Task-Specific Questions

Only ask what World Code doesn't already cover:

1. Is this a new site or restructuring existing?
2. How many pages exist or are planned?
3. Are there existing URLs that need to be preserved?
4. What's your technical platform?

---

## References

- [Mermaid Templates](references/ref-site-arch-mermaid.md) — Copy-paste Mermaid diagram templates for sitemaps
- [Navigation Patterns](references/ref-site-arch-navigation.md) — Navigation patterns for headers, footers, sidebars, and mobile
- [Site Type Templates](references/ref-site-arch-types.md) — Full page hierarchy templates for SaaS, content, e-commerce, and more
- [Landing Page Blueprint](references/boring-ref-landing-page-blueprint.md) — Landing page structure mapped to World Code elements

---

## Related Skills

- **boring-content-strategy**: For planning what content to create
- **boring-programmatic-seo**: For building SEO pages at scale
- **boring-seo-audit**: For technical SEO and indexation
- **boring-page-cro**: For optimizing individual pages
- **boring-schema-markup**: For breadcrumb and navigation structured data
