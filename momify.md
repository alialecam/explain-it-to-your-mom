Break down a technical term, concept, product, or message so that anyone can understand it — no engineering background required. Think: explain this to your mom.

The input may be a single word, acronym, phrase, product name, or short sentence. If the input contains multiple technical terms, note them all and offer to explain any that weren't covered.

---

## Step 0: Ask before you dive in

Before researching, ask the following (in a single message, not separately):

1. **Where did you encounter this?** (e.g., a Slack thread, a GitHub PR, a meeting, a doc, a press release)
2. **What's the context?** (e.g., which product, team, or project area, if known — even a vague answer helps)
3. **What are you doing with this?** (e.g., briefing a journalist, understanding a meeting you were in, writing talking points, satisfying your own curiosity)

If the term or concept is so well-known that context won't change the explanation (e.g., "API", "machine learning"), skip the questions and proceed.

---

## Step 1: Research externally

Search the web for reliable, technical-but-accessible sources. Prioritize:

- Official documentation or spec pages
- Engineering blogs from recognized companies (e.g., Google, AWS, Cloudflare, Stripe)
- Wikipedia for classification and broader context
- Shopify Newsroom (https://news.shopify.com) for any public product framing

Run a dedicated search of the Shopify Engineering Blog (https://shopify.engineering) using `site:shopify.engineering [term]`. List every post that references the concept, even tangentially. For each result, note the title, URL, author (if shown), and one sentence on how the concept is used or mentioned in that post. If no posts are found, state that explicitly.

For every claim in your explanation, note the source URL. Do not present information without attribution.

---

## Step 2: Cross-check internally at Shopify

Run these in parallel:

**Vault** — Search Vault pages, projects, teams, and posts for how Shopify uses or defines this concept. Note:
- Any Vault page or project that references it (title + link)
- Which team or product area owns it
- Whether Shopify's usage matches the industry-standard definition or diverges in any meaningful way

**Shopify GitHub** — Search for any public Shopify GitHub repositories or README files that reference this concept. Include relevant repo names and links if found.

**Slack** — Search Slack for recent conversations mentioning this term. Note active channels or threads where this concept is being discussed.

---

## Step 3: Identify internal subject matter experts

Based on the Vault and Slack results from Step 2, identify 2-4 people who appear to be actively working on or knowledgeable about this topic. For each person:
- Full name
- Slack handle (if found)
- Team or role
- Why they came up (e.g., authored a Vault page, active in a relevant Slack channel, champion on a related project)

If no clear individual SMEs emerge, name the most relevant team and link to their Vault page.

---

## Step 4: Write the momified explanation

Use plain language. No jargon. No unexplained acronyms. Write as if the reader has zero technical background but is smart and curious.

Structure the output exactly as follows:

---

### [Concept name]

**What it is**
One to two sentences. Plain English only. What is this thing? What problem does it solve or what does it enable?

**How to think about it**
Two to three sentences using an analogy or concrete scenario that has nothing to do with software. The goal is to make the abstract tangible. Avoid "it's like a computer doing X" — ground it in everyday life.

**A real example**
One specific, concrete example of this concept in action. Ideally grounded in commerce or everyday life. Not hypothetical — something that actually happens.

**What Shopify does with it**
Two to three sentences. What specifically is Shopify doing with this? Which team, product, or project? Has it shipped or is it in progress? Pull from Vault and external research. Mark anything internal-only as **[INTERNAL]**.

**Why it matters broadly**
Two sentences. What does this mean for the industry, for commerce, or for the world — beyond Shopify?

**Why it matters for merchants**
Two sentences. What changes for a merchant or their customers because of this? Be concrete — not "improves performance" but what actually improves and for whom.

**Classification**
State which of the following applies (can be more than one):
- **Industry-wide** — a standard concept used across engineering, ML, infrastructure, etc.
- **Shopify-specific** — something Shopify built, named, or uses in a way that is distinct from industry usage
- **Emerging / frontier** — relatively new, not yet standardized
- **Internal terminology** — a term Shopify uses internally that maps to something known externally by a different name

If Shopify's internal usage diverges from the industry definition, flag it explicitly:
> **Divergence note:** [Explain the difference clearly]

**On the Shopify Engineering Blog**
List every Shopify Engineering Blog post that references this concept, from the dedicated search in Step 1. For each:
- Title with link
- One sentence on how the concept is used or mentioned
If no posts were found, say so plainly.

**Where this shows up at Shopify**
A bulleted list of Vault pages, projects, Slack channels, or GitHub repos where this concept appears. Include links.

**Who to ask internally**
The SMEs identified in Step 3, formatted as:
- Name (Slack handle) — Team — Why they know this

**Sound smart in the meeting**
Two to three questions you could ask in a technical meeting to show you're following along — without needing to explain yourself:
- [Question 1]
- [Question 2]
- [Question 3]

**Comms one-liner**
A single, tight sentence suitable for a press pitch, briefing note, or talking points document. No jargon. Ready to use.

---

## Step 5: Jargon radar

If the original input contained more than one technical term, list any that weren't fully explained in the output above and offer to momify them individually.

---

## Tone rules
- No em dashes
- Sentence case for headers
- American English spelling
- Active voice
- Short, medium, and long sentences — make it readable, not monotonous
- No filler, no preamble, no summaries of what you just did
- Cite every external source with a URL
