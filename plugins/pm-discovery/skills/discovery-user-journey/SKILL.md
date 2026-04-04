# Skill: discovery-user-journey

## Trigger
Use this skill when the user wants to map the user journey during a discovery — e.g. "mappe le parcours utilisateur", "fais le user journey", "identifie les touchpoints", "Unfold phase", "map the current and future user flow".

## Context
At Mayday, the Unfold phase (step 4 of FOCUSED) is about identifying WHERE in the user experience we can solve the problem and drive adoption. The deliverable is:
- A **current user journey** (how users experience the problem today)
- An **imagined user journey** (how users would experience the solution)
- **5 key touchpoints** where adoption and retention can be driven

The Unfold phase is sometimes optional — if the feature is very contained, it may not be needed. But it's highly valuable for designing adoption-oriented MVPs.

## What to do

### Step 1 — Gather context
Ask the user for the following if not already provided:
- The FUC (First Use Case) — what problem are we solving?
- The persona targeted
- Rough idea of what the solution might look like (even if not decided yet)
- Which surface / area of the product is involved?

### Step 2 — Map the Current User Journey

Create a step-by-step map of how the user experiences the problem TODAY, before the solution exists.

Format as a table or numbered list:

| Step | User Action | What they feel | Current pain / friction |
|------|-------------|----------------|------------------------|
| 1 | [What the user does] | [Emotion / state] | [What's wrong or missing] |
| 2 | ... | ... | ... |

Include:
- Entry point (what triggers the user to start this journey)
- Each meaningful step
- The moment where the main pain occurs (mark it clearly ⚠️)
- The outcome (often: frustration, workaround, or giving up)

### Step 3 — Map the Imagined User Journey

Create the same step-by-step map, but with the solution in place. Show how the experience changes.

| Step | User Action | What they feel | How the solution helps |
|------|-------------|----------------|----------------------|
| 1 | [What the user does] | [Emotion / state] | [What the feature does here] |
| 2 | ... | ... | ... |

Mark the key moments where value is delivered (✨).

### Step 4 — Before/After Summary

Write a brief "Before / After" narrative (3–4 sentences each) that captures the transformation in human terms.

**Before:** [Describe the frustrating current experience]
**After:** [Describe the delightful future experience]

### Step 5 — Identify the 5 Key Touchpoints

List the 5 moments in the user journey where the product should proactively engage the user to drive adoption and retention:

**Touchpoint 1: [Name]**
- Where: [In the product — which surface/screen]
- When: [Under what condition]
- How: [What the product does — nudge, notification, inline prompt, etc.]
- Goal: [Adoption / Retention / Engagement]

Repeat for 5 touchpoints.

### Step 6 — Recommended MVP entry point

Based on the journey analysis, recommend the single best entry point for the MVP:
> "The highest-value touchpoint for v0 is [X] because [reason]. This is where users feel the pain most acutely and where a well-placed intervention would have the highest impact."

## Output format
- Current journey table → Imagined journey table → Before/After → 5 Touchpoints → MVP recommendation
- Use tables for the journey maps (easier to read)
- Mark pain moments with ⚠️ and value moments with ✨
- Write in the user's language
- Be concrete about product surfaces (e.g. "in the KB editor sidebar" not just "in the product")
