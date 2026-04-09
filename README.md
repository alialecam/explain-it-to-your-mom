# Explain it to your mom — tech terms simplified

A [Claude Code](https://claude.ai/code) custom skill that breaks down technical terms, products, and concepts so anyone can understand them. No engineering background required.

Drop a term, acronym, product name, or short phrase. Get back plain language, a real-world analogy, a concrete example, internal references, subject matter experts to ask, and a ready-to-use comms one-liner.

---

## What it does

For any technical input, `/momify` produces:

- **Plain English explanation** — what it is, in language anyone can follow
- **Analogy** — a real-world comparison with nothing to do with software
- **Concrete example** — something that actually happens, not a hypothetical
- **Classification** — is this industry-wide, company-specific, emerging, or internal jargon?
- **Shopify Engineering Blog** — every published post that references the concept
- **Internal references** — where this shows up in internal docs, projects, and channels
- **Who to ask** — internal subject matter experts, with context on why they came up
- **Sound smart in the meeting** — 2-3 questions you can ask to show you're following along
- **Comms one-liner** — a press-ready sentence, ready to drop into a pitch or briefing

It also runs a **jargon radar**: if your input contains multiple technical terms, it lists any it didn't fully cover and offers to explain them.

---

## Installation

1. Copy `momify.md` into your Claude Code commands directory:

```bash
cp momify.md ~/.claude/commands/momify.md
```

2. Restart Claude Code (or open a new session).

3. Invoke with:

```
/momify [term or phrase]
```

**Examples:**
```
/momify RAG
/momify transformer architecture
/momify multi-cloud GPUs
/momify Chinese restaurant process
```

---

## How it works

When invoked, the skill:

1. **Asks for context** — where you encountered the term, what area it relates to, what you're doing with it. Skips this for well-known concepts.
2. **Searches externally** — web search across official docs, engineering blogs, Wikipedia. Every claim gets a source URL.
3. **Searches the Shopify Engineering Blog** — dedicated `site:shopify.engineering` search to surface any published narrative.
4. **Cross-checks internally** — searches Vault, Shopify GitHub, and Slack for internal usage, team ownership, and any divergence from the industry definition.
5. **Identifies subject matter experts** — surfaces names, Slack handles, teams, and why each person came up.
6. **Writes the momified explanation** — structured output in plain language, ready to use.

---

## Shopify-specific features

Some sections require internal tools:

| Section | Requires |
|---|---|
| Shopify Engineering Blog | Web search (built in) |
| Internal references (Vault) | [Vault MCP](https://vault.shopify.io) |
| Who to ask + Slack channels | [Slack MCP](https://github.com/shopify-playground/playground-slack-mcp) |
| Shopify GitHub references | Web search or GitHub MCP |

If you're not at Shopify, the internal sections will return no results — everything else works for any technical term.

---

## Example output

### Multi-cloud GPUs

**What it is**
"Multi-cloud GPUs" means running AI workloads across GPU chips rented from multiple different cloud providers at the same time, rather than being locked into just one. It's how companies avoid paying too much, running out of capacity, or going down if one provider has a problem.

**How to think about it**
Imagine you run a bakery and need commercial ovens to bake at scale. You could rent ovens from one supplier, but if they run out of ovens, raise their prices, or break down, you're stuck. So instead, you have agreements with three different oven rental companies — you send your baking jobs to whichever one has availability at the best price that day. Multi-cloud GPUs work the same way: GPUs are the ovens, and AWS, Google Cloud, and Nebius are the rental companies.

**Sound smart in the meeting**
- "Are we running training and inference workloads on the same providers, or are those separated by cost?"
- "How does the scheduler decide which cloud gets a job — is it purely cost, or does latency factor in?"
- "Is GCP still in the mix for anything, or have we fully migrated training off it?"

**Comms one-liner**
Shopify built a system that automatically routes AI workloads to the cheapest available GPU hardware across multiple cloud providers, cutting costs without slowing down the AI features merchants rely on.

---

## Background

Built for communications and non-technical stakeholders who need to follow, brief on, or write about deeply technical concepts without a software engineering background. Useful for:

- Media relations and journalist briefings
- Technical talking points and messaging
- Understanding meetings and Slack conversations in real time
- Connecting engineering work to merchant and business impact
