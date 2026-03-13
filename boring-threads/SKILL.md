---
name: boring-threads
description: |
  Generate Threads content — single posts, multi-post threads, and micro-essays
  — using your World Code voice and worldview. Use when the user says "write a
  thread", "Threads post", "Threads content", "post for Threads", "multi-post
  thread", "micro-essay for Threads", "write something insightful", "write
  something for Threads", "Threads idea", "give me Threads content", "what
  should I post on Threads", or any content creation request targeting the
  Threads platform. Also trigger when the user mentions creating short-form
  social content that prioritizes engagement and conversation, or when they want
  insight-dense prose adapted for Threads. Learns from your best-performing
  content when available. World Code integrated.
metadata:
  version: 1.0.0
---

# Threads Content — World Code Edition

You write Threads content that sounds like a person thinking out loud in public. Not broadcasting. Not performing. Thinking with enough conviction that people want to think alongside you.

Threads rewards two things: genuine voice and conversation starters. The algorithm favors replies, quotes, and shares — content that makes someone stop scrolling and respond. Your job is to write posts that create that pull while staying true to the user's worldview.

## Before You Write Anything

### 1. Read the World Code Files

Read these files from `world-code/` in the current working directory.

**Required (stop if missing):**
- `world-code/voice.md` — Tone, rhythm, hard rules. If this file doesn't exist, tell the user: "You need a Voice first. Run `/world-voice` to create one." and stop.

**Use if they exist (don't stop if missing):**
- `world-code/climax.md` — The transformation promise. Shapes the stakes behind the post.
- `world-code/conversation.md` — Walls, struggles, goblins, treasures. This is your topic engine.
- `world-code/crown.md` — The territory the user claims. Posts should feel like dispatches from this territory.
- `world-code/method.md` — The user's methodology. Reference it when relevant, never force it.
- `world-code/creation.md` — The user's offer. Never pitch directly. Let posts make the offer feel inevitable.
- `world-code/crossing.md` — The conversion path. Only use when the user specifically asks for conversion content.

### 2. Check for High-Performing Content

Look for a `content/hits/threads/` folder.

**When it exists and has files:**

Read every file. These are posts that actually worked — the user put them here because they got engagement. Analyze the patterns:

- Hook style (question, bold claim, personal moment, contradiction)
- Length and rhythm (short punchy vs. longer narrative)
- Which topics generated the most response
- Tone temperature (vulnerable, aggressive, playful, contemplative)
- Structural patterns (single sentence paragraphs, lists, storytelling arcs)
- What kind of engagement they got (replies vs. shares vs. likes — if noted)

Present a brief **"What's Hitting"** summary to the user before generating content. Use these patterns as a compass — lean toward what's already resonating, but don't clone the hits. The goal is to understand why they worked, not to repeat them.

**When it doesn't exist or is empty:**

Mention it once:

> "Tip: Save your best-performing Threads posts to `content/hits/threads/` and I'll learn from what's already working for you."

Then move on. Without hit data, you're in experiment mode — lean into variety and try multiple angles to discover what works.

### 3. Ask Only What You Need

The World Code files pre-answer most questions. Only ask:

1. **What do you want to post about?** (topic, idea, rant, observation — or "pick something for me")
2. **What format?** Single post, multi-post thread, or micro-essay? (or "you decide")
3. **Any keywords to hit?** (optional — specific words or phrases the user wants in the post for algorithm discovery, e.g., "ADHD," "solopreneur," "AI")
4. **Is there a conversion goal?** (only if the user brings it up — default is pure engagement)

If the user says "pick something for me," pull from their Bridge in `world-code/conversation.md`. Pick the struggle with the most tension. Tell them what you picked and why before writing.

If the user gives a vague topic like "write something about marketing," look at their walls and goblins to find a specific angle. Vague posts die on Threads. Specific ones spark conversation.

---

## How Threads Content Works

### The Platform Reality

Threads is not Twitter. It's not Instagram captions. It's a space where people scroll fast, engage with things that feel like real thoughts, and punish anything that smells like marketing. The algorithm rewards conversation — replies matter more than likes.

What works on Threads:
- Opinions stated without hedging
- Personal observations with enough specificity to feel real
- Questions that people actually want to answer (not rhetorical)
- Vulnerability that isn't performative
- Humor that comes from a genuine worldview, not jokes for engagement
- Contrarian takes backed by experience, not controversy for its own sake

What dies on Threads:
- Generic advice ("focus on your goals!")
- Overly polished, copywriter-sounding posts
- Obvious templates (the "I did X. Here's what I learned:" format is burned out)
- Anything that reads like a LinkedIn post that wandered into the wrong platform
- Pure promotion without earned context
- Threads that could have been one post

### Keywords and Algorithm Discovery

When the user provides a keyword or topic, two things need to happen:

1. **The keyword appears in Post 1.** The algorithm indexes the first post most heavily. If the user wants to be discovered for "ADHD" or "solopreneur" or "AI," that word needs to show up naturally in the opening post. Not hashtag-style. Not forced. Woven into the thought so it reads like a person talking, not a person optimizing.

2. **The topic connects back to the World Code.** The keyword is the door. The World Code is the room. If the user says "write about ADHD," don't write a generic ADHD post. Find where ADHD connects to their walls, struggles, or goblins. ADHD and business structure. ADHD and the myth of hustle. ADHD and why systems matter more than discipline. The keyword is the entry point for the audience. The World Code is what makes the post theirs.

If the keyword feels forced in Post 1, the post isn't about that topic yet. Rethink the angle until the keyword belongs there naturally.

### Single Posts vs. Multi-Post Threads

**Single post (1 post):** One complete thought. The constraint forces clarity. Best for strong opinions, observations, questions, and moments. This is the bread and butter. Most content should be single posts.

**Multi-post thread (2-7 posts):** A sequence of connected posts that build on each other. Best for stories, breakdowns, arguments with multiple parts, and teaching. Each post must stand on its own AND push the reader to the next one. If removing a post from the middle doesn't break anything, it shouldn't be there.

The decision between single and multi-post depends on the idea, not a formula. If the idea can land in one post, don't stretch it. If it genuinely has parts that build on each other, thread it out.

---

## Writing Single Posts

### Pre-Write (Internal — Don't Output This)

Before writing, answer:
1. What's the one thing this post says?
2. Why would someone reply to this? (If you can't answer this, the post isn't ready.)
3. What tension does it create? (Disagreement, curiosity, recognition, discomfort)

### Structure

There's no one structure. But there are patterns that work:

**The Claim.** One bold statement. No preamble, no softening. The reader's reaction IS the engagement.
> Example energy: "The best marketing strategy is having something worth talking about."

**The Observation.** Something specific you noticed. The more precise, the more universal it feels.
> Example energy: "Every time I simplify my offer, more people buy. Every time I add options, fewer people do."

**The Question.** A real question — one you're genuinely curious about or one that makes people examine their own assumptions.
> Example energy: "What's the last piece of advice you followed that turned out to be completely wrong?"

**The Story Beat.** A moment from real life — compressed, specific, and resonant. Not the whole story. Just the beat that matters.
> Example energy: "I spent three months building something nobody asked for. The thing that worked was the throwaway idea I mentioned in a DM."

**The Contradiction.** Two things that seem true but create tension when placed together.
> Example energy: "Everyone says consistency is key. The people I know who broke through did it by being inconsistent in the right direction."

**The Permission Slip.** Give the reader permission to stop doing something they secretly want to stop doing.
> Example energy: "You don't have to post every day. You have to post things that matter when you post them."

### Length

Threads posts can be up to 500 characters. You don't need to use them all. Some of the best posts are under 100 characters. Let the idea determine the length. Don't pad to fill space. Don't truncate a good thought to seem pithy.

---

## Writing Multi-Post Threads

### When to Thread

Thread it when:
- The idea has genuine parts that build on each other
- You're telling a story with a setup, tension, and resolution
- You're making an argument that needs evidence layered in
- You're breaking down a process or framework (use sparingly — this is the most overused thread format)

Don't thread it when:
- You could say it in one post and you're just adding filler
- Each "post" is really just a sentence fragment of one paragraph
- You're threading just because threads get more reach (they don't anymore, unless they're genuinely good)

### Thread Architecture

**Post 1 — The Hook Post**
This is everything. If post 1 doesn't work, nobody sees post 2.

The first sentence should stand on its own. One line that creates enough tension, curiosity, or recognition that the reader has to keep going. Not a paragraph. Not a setup. A single sentence that hits. Then let the rest of the post (if there is any) open the gap that the thread fills.

Don't open with "Thread:" or "A thread on..." Just start.

The hook post should NOT give away the conclusion. It should create a gap that the thread fills.

**Posts 2-6 — The Build**
Each post advances the idea. One move per post. Moves include:
- A piece of the story (next beat)
- A supporting point or evidence
- A pivot or complication (things aren't what they seemed)
- A concession (acknowledging the counterargument)
- A cross-domain reference that reframes the point

Each post should end in a way that creates pull toward the next one. Not cliffhangers — just incomplete energy. The thought is advancing but hasn't landed yet.

**Final Post — The Landing**
This is where the point crystallizes. Options:
- Restate the claim with the weight of everything that came before it
- A permission slip or diagnostic question
- A callback to the hook post that now hits differently
- A bridge to the user's worldview (not their offer — their worldview)

If the thread has a conversion goal, the final post is where a soft invitation lives. Not a CTA. An invitation. "If this is how you think about X, here's where I go deeper" or similar. Use Crossing language from `world-code/crossing.md`.

### Thread Length

3-5 posts is the sweet spot. 2 posts is fine for a setup/payoff structure. 6-7 if the story genuinely requires it. Beyond 7, you're losing people. Compress.

---

## Writing Micro-Essays

A micro-essay is a different animal from a regular thread. Regular threads are sequences of connected punches. A micro-essay is one continuous piece of thinking split across posts. It reads like prose, not bullet points. The reader should forget they're reading separate posts and feel like they're inside an argument that's building toward something.

Micro-essays are the highest-trust content on Threads. They prove you can think, not just quip. They're what makes someone follow you instead of just liking a post.

### Pre-Write (Internal — Don't Output This)

Before writing, work through these questions. They shape the essay. Skip them and it meanders.

1. **What is the one claim?** One sentence. If you can't say it in one sentence, you don't have a micro-essay yet.
2. **What belief does this give the reader permission to abandon?** Every good micro-essay frees the reader from something they suspected was wrong but couldn't articulate. Often this IS a goblin voice from the Bridge.
3. **What cross-domain reference is load-bearing?** The reference must shape the argument, not decorate it. Pull from mental models (inversion thinking, second-order effects, feedback loops), other domains (physics, biology, psychology, history), or specific named examples. If you can remove the reference and the essay still works, pick a different reference.
4. **What specific detail makes this credible?** A real number, a real timeline, a real named failure, a real concrete moment. The weirder and more specific, the better.
5. **What does the close allow the reader to do or stop doing?** The ending isn't a summary. It's a permission slip or a question that lands differently now.
6. **What's the offer bridge?** How does this essay's argument naturally connect back to the user's worldview? Not their product. Their way of seeing the world. This is one sentence, woven in, never bolted on.

### Structure Across Posts

A micro-essay thread is 4-7 posts. Each post is a paragraph or two of prose that flows into the next.

**Post 1 — The Opening**
The first sentence stands alone. One line that hooks. Then the rest of the post opens the door.

Pick one opening mode:
- Cold claim. Start with the thesis, no warmup.
- Scene. Drop the reader into a specific moment.
- Question. A real question, not rhetorical.
- Contradiction. Two things that seem true but can't both be.
- Number or fact. A specific data point that creates tension.

The opening must establish a personal stake within the first 2-3 lines. Not "you've been told" but "I've always thought" or "I spent two years doing this wrong" or a scene from lived experience. The reader should know where the writer stands before they know what the topic is.

**Posts 2-5 — The Middle**
This is where the thinking happens. Combine 2-3 of these moves:
- The cross-domain reference that reframes the whole topic
- A personal anecdote with a specific, almost absurd detail
- Conventional wisdom stated and dismantled (concede what's true about it first, then show why it's incomplete)
- The mechanism explained (why something works, not just that it works)
- A named example (person, company, moment)
- A concession (what the counterargument gets right)

Each post should feel like a paragraph in an essay. It continues the thought from the previous post and sets up the next. The posts don't stand alone the way regular thread posts do. They flow.

**Final Post — The Close**
Pick one close mode:
- Permission slip. Tell the reader what they're now allowed to stop doing.
- Diagnostic question. One question that reveals where they actually stand.
- Reframe of the opening claim with new weight.
- Worldview bridge. The essay's argument connects back to how the user lives and works. This is the offer bridge. One sentence, maybe two. It reads as "I practice what I just preached."

### Voice Rules Still Apply

A micro-essay is prose, but it's not an essay in a magazine. It's still this person's voice. The paragraph rhythm from `voice.md` applies throughout. If the voice file says short paragraphs, one-sentence paragraphs, fragments as punctuation — that's how the micro-essay reads too.

The trap is writing dense blocks of text because "it's an essay." It's not. It's an argument written in the user's voice with the same rhythm they'd use in any other format.

### Write It as One Piece

Don't split the micro-essay into individual Threads posts. Write it as one continuous piece of prose. The user or their scheduling tool will handle splitting it into posts. Your job is to write the best possible essay, not to worry about where the 500-character breaks fall.

This means no `---` separators. No "Post 1, Post 2" labels. Just the essay.

### Cross-Domain Reference Pool

Draw from this pool. The reference must be named explicitly and load-bearing.

**Mental models:** Inversion Thinking, Second-Order Effects, Feedback Loops, Survivorship Bias, First Principles, Pareto Principle, Antifragility, Opportunity Cost, Compounding, Activation Energy, Loss Aversion, Dunning-Kruger, Network Effects

**Other domains:** Physics (entropy, thermodynamics, Newton's laws), Biology (evolution, symbiosis, immune response), Psychology (cognitive load, flow states, hedonic adaptation), History (specific figures with specific contributions), Philosophy (Stoicism, pragmatism)

One reference per micro-essay. Two if they genuinely interact. Never three.

### What Makes It a Micro-Essay and Not Just a Long Thread

The difference is prose flow. A regular thread is a sequence of standalone punches. A micro-essay is one argument that breathes across multiple posts.

Signs you wrote a micro-essay:
- You could paste all the posts together and it reads as one coherent piece
- There are no headers, no bullet lists, no numbered steps
- The cross-domain reference does structural work, not decoration
- The reader walks away with a new way to think about something, not just a new fact
- It has an opinion. A real one. Something a reasonable person could disagree with.

Signs you accidentally wrote a regular thread:
- Each post could be rearranged without losing anything
- The posts are standalone observations loosely connected by topic
- There's no argument building across the posts
- You could remove a post from the middle and nobody would notice

---

## Engagement Mechanics

### The Reply Magnet Principle

The goal isn't just to be read — it's to start a conversation. Every post should have at least one of these engagement pulls:

- **Recognition:** "That's exactly what I experience." (Posts about shared struggles, named goblin voices)
- **Disagreement:** "I don't agree with that." (Strong opinions, contrarian takes)
- **Self-reflection:** "Hm, let me think about that." (Good questions, contradictions)
- **The urge to add:** "I want to share my version of this." (Open-ended observations, "What's yours?" energy)

You don't need all four. One strong pull is enough. Two is ideal. Trying for all four makes the post feel manipulative.

### Conversion Without Selling

When the user wants posts that convert:

The post itself should never be the pitch. The post builds the worldview. The worldview makes the offer make sense. Conversion on Threads works through identity — people see themselves in your thinking, they click your profile, they see what you offer.

The sequence:
1. Post that nails a struggle or goblin voice from the Bridge (recognition)
2. The reader's identity activates: "This person gets it"
3. They check the profile, click the link (the Crossing entry point)

If you must include a conversion element in the post, it goes at the very end, framed as an invitation, not an announcement. And only do this occasionally — most posts should have zero conversion intent. The ratio matters. If every post has a CTA, none of them work.

---

## Voice and Anti-Slop

### Voice Rules

Everything in `world-code/voice.md` is absolute. Every post must sound like the person described in that file. Read the hard rules. Follow them without exception.

Threads has a specific voice challenge: it's a casual platform, but casual doesn't mean careless. The writing should feel effortless but be precise. Every word is chosen, but it doesn't feel like every word was chosen.

### Anti-AI (Baked In)

Threads users have the sharpest AI detector of any social platform. One whiff of generated content and you lose trust permanently.

**While writing, avoid:**
- Significance inflation ("game-changing," "transformative," "powerful")
- AI vocabulary (delve, landscape, foster, leverage, nuanced, robust, navigate)
- Template openers ("Here's the thing about X:" — "Let me tell you something about X:")
- Forced rule-of-three lists
- Synonym cycling
- Generic positive conclusions ("The possibilities are endless")
- Hedge stacking ("could potentially perhaps")
- "Not just X, it's Y" constructions
- Every sentence being the same length

**After drafting, audit:**
- Read it out loud. Does it sound like a person or a press release?
- Is there a real opinion? Could someone disagree? If not, push harder.
- Is there unnecessary padding? Cut it.
- Does it sound like it came from a template? Rewrite.
- Would the person in voice.md actually post this? If not, start over.

---

## Experiment Mode

When there's no high-performing content to learn from, you're in experiment mode. This means:

- **Vary everything.** Don't settle into one style. Try claims, observations, questions, story beats, contradictions, and permission slips across different posts.
- **Vary length.** Some posts under 50 characters. Some at 400+. See what the user's voice sounds best at.
- **Vary intensity.** Some posts aggressive and opinionated. Some quiet and reflective. Some playful.
- **Suggest batches.** Instead of one perfect post, offer 3-5 different posts on the same topic with different approaches. The user posts them over time and sees what resonates.

When you generate experimental batches, label each one by its approach (e.g., "The bold claim version," "The question version," "The story beat version") so the user can see the variety and learn their own patterns.

---

## Output

### For Single Posts
Present the post. No explanation of what you did or why unless the user asks. The post should speak for itself.

If you're generating multiple options, present them labeled by approach with a one-line description of the angle.

### For Multi-Post Threads
Present each post numbered (Post 1, Post 2, etc.) with clear separation. Each post should be visually distinct so the user can see exactly what they'll paste into each field.

### Saving

After presenting, save automatically:

1. **Location:** `content/threads/` in the current working directory. Create the directory if it doesn't exist.
2. **Filename:** `YYYY-MM-DD-slug.md` where the date is today and the slug is a short kebab-case description. Example: `2026-03-11-consistency-myth.md`
3. **File contents:** For single posts, just the post text. For multi-post threads, posts separated by `---` with `Post 1`, `Post 2`, etc. labels. For micro-essays, the full essay as one continuous piece of prose. No separators, no labels. No metadata, no frontmatter, no explanation.
4. Tell the user where you saved it.

---

## Content Strategy Connection

When `world-code/conversation.md` exists, posts should connect to the Bridge:

- **Walls** are content pillars. Each wall generates dozens of post angles.
- **Struggles** are specific topics. A struggle IS a post waiting to happen.
- **Goblin voices** are engagement gold. Name a false belief people hold — they'll reply to tell you you're right or wrong. Either way, engagement.
- **Treasures** are micro-outcomes. Show what's on the other side of a wall. Recognition posts.
- **The Culprit** ties everything together. Posts that name the real enemy behind the struggles create the strongest identity resonance.

Don't force every post to map to the Bridge. Some posts are just good observations. But when you need topic ideas, the Bridge is infinite.

---

## References

- [Social Templates](references/boring-ref-social-templates.md) — Hook formulas and post structures by type
- [Content Themes to Posts](references/boring-ref-content-themes-to-posts.md) — Turn Bridge elements into content angles

---

## Related Skills

- **boring-essay** — For longer-form ideas that start as Threads posts and want to grow
- **boring-content-strategy** — For planning content across platforms including Threads
- **boring-human** — Run as a final pass if anything sounds AI-generated
- **boring-remix** — Turn a Threads post into other formats (email, essay, etc.)
- **boring-copywriting** — For conversion-focused copy that isn't social content
