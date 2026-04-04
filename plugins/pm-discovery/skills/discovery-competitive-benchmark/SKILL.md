# Skill: discovery-competitive-benchmark

## Trigger
Use this skill when the user wants to run a competitive benchmark during a discovery — e.g. "fais un benchmark concurrentiel", "analyse les solutions existantes", "steal phase", "what are competitors doing on X", "trouve des gold nuggets pour ma discovery".

## Context
At Mayday, the Steal phase (step 5 of FOCUSED) is dedicated to benchmarking existing solutions before designing anything. The goal is NOT to copy, but to identify patterns, UX models, and "Gold Nuggets" — the 5 most inspiring solutions that can inform Mayday's design.

Benchmark sources to cover:
1. **Direct competitors / ecosystem actors** (tools in the same space as Mayday)
2. **Usual suspects** (industry leaders that likely solve a similar problem: Notion, Stripe, Linear, Figma, Google, etc.)
3. **Adjacent industries** (tools from other sectors solving the same underlying UX challenge)

> Pro tip: Use web search to find changelogs, product documentation, and reviews — these are more accurate than marketing pages.

## What to do

### Step 1 — Gather context
Ask the user for the following if not already provided:
- What is the FUC (First Use Case) or problem being solved?
- Which direct competitors / ecosystem actors should be checked?
- Any specific UX patterns or capabilities to focus on?

### Step 2 — Run the benchmark
For each product analyzed, produce a structured entry:

**[Product Name] — [One-line description]**
- **Why relevant:** How does this relate to the FUC?
- **How they solve it:** Describe the UX flow or feature in concrete terms
- **Key UX patterns:** The specific interaction patterns worth noting
- **Limitations / feedback:** What users complain about, what's missing
- **🔗 Source:** Link to documentation, changelog, or review

Analyze at minimum:
- 2–3 direct competitors
- 2–3 "usual suspects" (Notion, Linear, Figma, Stripe, etc. depending on the problem)
- 1–2 from an adjacent industry if relevant

### Step 3 — Extract the 5 Gold Nuggets

After analyzing all products, extract the **5 most inspiring patterns or solutions** — things that should influence Mayday's design:

**🥇 Gold Nugget 1: [Short title]**
> [What it is, why it's powerful, what Mayday should steal from it]

Repeat for 5 nuggets total.

### Step 4 — Key patterns synthesis

End with a brief synthesis section:
- **Recurring patterns across solutions:** What do most products do the same way?
- **Gaps / opportunities:** What are competitors NOT doing well that Mayday could own?
- **Recommendation:** Based on the benchmark, what approach makes the most sense for Mayday?

## Output format
- One section per product analyzed
- Then the 5 Gold Nuggets highlighted
- Then the synthesis
- Use headers, bold text, and emoji for scanability
- Include real links and source references where possible
- Write in the user's language
- Be specific about UX patterns — describe the actual interaction, not just "it has a good UI"

## Example Gold Nugget format (from Knowledge Quality benchmark)
**🥇 Gold Nugget: Cursor — Multi-file diff review**
> When an AI agent modifies multiple files, Cursor shows each impacted file in a sidebar with a before/after diff, letting the user accept or reject changes file by file. The key insight: each change includes a brief rationale ("why this file was touched"), which builds trust. For Mayday: this "impacted document list + rationale + per-item accept/reject" is the exact mental model for KB quality recommendations.
