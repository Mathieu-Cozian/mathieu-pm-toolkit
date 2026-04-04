---
name: discovery-mvp-definition
description: Define and prioritize MVP solutions using Opportunity Solution Tree and RICE frameworks during the Execute phase. Trigger when the user says "définis le MVP", "priorise les solutions", "brainstorm solutions", "Execute phase", "fais l'OST", "RICE framework".
---

# Skill: discovery-mvp-definition

## Trigger
Use this skill when the user wants to define and prioritize solutions during a discovery — e.g. "définis le MVP", "priorise les solutions", "brainstorm solutions", "Execute phase", "fais l'OST", "RICE framework", "quelles fonctionnalités pour le MVP".

## Context
At Mayday, the Execute phase (step 6 of FOCUSED) is about selecting and preparing the chosen solution. Based on all previous phases (FUC, Claim, Benchmark, User Journey), the team must:
1. Brainstorm potential solutions
2. Prioritize using a structured framework (RICE)
3. Define the MVP scope
4. Define the 3 key hypotheses to test

**Key constraint:** The solution must:
- Solve the identified FUC
- Keep the Claim promise (the value proposition defined in step 3)
- Learn from existing solutions (benchmark)
- Make sense within Mayday's product architecture

## What to do

### Step 1 — Gather context
Ask the user for the following if not already provided:
- The FUC (First Use Case)
- The Claim (value proposition / Launch Tweet)
- Key Gold Nuggets from the benchmark (patterns to inspire from)
- Key user touchpoints from the Unfold phase (if done)
- Any solution ideas already discussed?
- Rough tech feasibility input from Engineering (if available)?

### Step 2 — Opportunity Solution Tree (OST)

Structure the solution space visually:

**🎯 Goal (from FUC):** [Restate the goal]

**📌 Opportunities (sub-problems to solve):**
- Opportunity 1: [A specific sub-problem within the FUC]
  - Solution A: [Potential solution]
  - Solution B: [Potential solution]
- Opportunity 2: [Another sub-problem]
  - Solution C: [Potential solution]
  - Solution D: [Potential solution]
(etc.)

List at least 6–8 solution ideas across 2–3 opportunities before prioritizing.

### Step 3 — RICE Prioritization

Score the top solutions using the RICE framework. Create a table:

| Solution | Reach | Impact | Confidence | Effort | RICE Score | Notes |
|----------|-------|--------|------------|--------|------------|-------|
| [Solution A] | [1-10: how many users affected?] | [1-3: low/med/high impact on metric] | [%: how confident?] | [1-5: dev effort] | [(R×I×C)/E] | [Key trade-off] |

**Scoring guidance:**
- **Reach:** How many active users will benefit? (scale: 1-10)
- **Impact:** How much does this move the NSM? (1=low, 2=med, 3=high)
- **Confidence:** How sure are we this will work? (based on interviews + benchmark)
- **Effort:** Engineering effort (1=days, 2=1-2 weeks, 3=1 month, 4=2 months, 5=quarter+)

### Step 4 — MVP Definition

Based on the RICE scores, define the MVP scope:

**✅ In MVP (v0)**
List 3–5 features/capabilities that are in scope, with a one-line rationale for each.

**⛔ Out of MVP (post-v0)**
List features explicitly excluded from v0 with a rationale. (Prevents scope creep.)

**Why this MVP?**
3–4 sentences explaining the logic: why this specific scope maximizes learning while minimizing effort.

### Step 5 — 3 Key Hypotheses to test

Define the 3 most important hypotheses the MVP needs to validate before scaling:

**Hypothesis 1: [Short title]**
> We believe that [target user] will [behavior] when we [solution element]. We'll know this is true if [measurable signal — metric or qualitative indicator].

Repeat for 3 hypotheses total.

### Step 6 — Metrics definition

Define how success will be measured for the MVP:

- **NSM (from Project Ambition):** [Restate it]
- **Leading indicators:** What early signals will tell us the MVP is working before the NSM moves?
- **Guard rails:** What metrics should NOT decrease? (e.g. general engagement, support tickets)

## Output format
- OST → RICE table → MVP scope → 3 Hypotheses → Metrics
- Use a clear table for RICE (easiest format to work with in a team)
- Bold the recommended MVP solution
- Write in the user's language
- Be explicit about what's OUT of scope — this is as important as what's in
