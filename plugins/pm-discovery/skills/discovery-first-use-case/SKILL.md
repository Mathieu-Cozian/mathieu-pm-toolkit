---
name: discovery-first-use-case
description: Synthesize interview learnings into a First Use Case (FUC) statement during the Observe phase. Trigger when the user says "synthétise mes interviews en FUC", "rédige le premier use case", "j'ai fini mes interviews, aide-moi à synthétiser", "write the first use case from my interviews".
---

# Skill: discovery-first-use-case

## Trigger
Use this skill when the user wants to synthesize interview learnings into a First Use Case (FUC) — e.g. "synthétise mes interviews en FUC", "rédige le premier use case", "j'ai fini mes interviews, aide-moi à synthétiser", "write the first use case from my interviews".

## Context
At Mayday, after running the Observe phase interviews, the PM must synthesize all learnings into a single **First Use Case (FUC)** — the main problem the discovery will focus on. The FUC is a structured statement that defines: who has the problem, in what context, what they need, what's blocking them, and what workaround they use today.

The FUC is critical because it becomes the anchor for all subsequent FOCUSED phases (Claim, Execute, etc.). If the FUC is wrong or too broad, the entire discovery loses focus.

**FUC format:**
```
AS A [user persona]
WHEN [specific context / situation]
I NEED [the value / outcome they want]
BUT [current obstacle / constraint]
SO I [current workaround they use today]
```

> ⚠️ If people don't have a current workaround, the problem may not be significant enough.

## What to do

### Step 1 — Gather interview notes
Ask the user to share:
- Their interview notes or a summary of key findings
- How many people were interviewed and what types (client / internal)
- Any recurring patterns or quotes they noticed

If the user doesn't have structured notes, ask them to describe in free text what they heard — the skill will do the synthesis.

### Step 2 — Extract key patterns
Before writing the FUC, briefly summarize:
- The top 3 pain points that came up most frequently
- The most significant workarounds mentioned
- Any surprising or unexpected findings
- Quotes that capture the problem well

### Step 3 — Write the First Use Case

Write a clear, focused FUC statement using the exact format:

```
AS A [persona — be specific, e.g. "Knowledge Manager at a mid-size company"]
WHEN [precise situation — when does this problem occur?]
I NEED [the outcome they want — what value are they seeking?]
BUT [the core obstacle — what is preventing them from getting that value today?]
SO I [their actual workaround — what do they do instead?]
```

Then add a brief **"Why this FUC"** section (3–5 sentences) explaining:
- Why this is the most important problem (vs. others surfaced in interviews)
- The business impact (churn risk, adoption blocker, strategic relevance)
- Why the workaround confirms this is a real pain (not a nice-to-have)

### Step 4 — Validation checklist
Present a quick self-assessment:
- [ ] Is the persona specific enough?
- [ ] Is the "WHEN" a real, recurring situation (not an edge case)?
- [ ] Does the "I NEED" describe value, not a feature?
- [ ] Does the "BUT" describe the root obstacle, not a symptom?
- [ ] Is there a real workaround (confirming pain is genuine)?
- [ ] Is this problem business-critical?

## Output format
- Lead with the key patterns summary
- Then the FUC in the structured format (can use a code block or callout)
- Then the "Why this FUC" explanation
- Then the validation checklist
- Write in the user's language
- Keep it concise — the FUC statement itself should be 5 lines maximum

## Example (from Knowledge Quality discovery)
```
AS A Knowledge Manager at a B2B SaaS company
WHEN I want to ensure our knowledge base stays accurate and up-to-date
I NEED a way to quickly identify which content is outdated, incomplete, or low-quality
BUT I have no centralized view of my content's health and must manually export and cross-reference data
SO I spend hours on manual audits using spreadsheet exports and SAT scores as proxies
```
