---
name: strategy-prioritization
description: >
  Score and rank features or initiatives using RICE to inform roadmap decisions.
  Use when the user says "priorise ces features", "aide-moi à prioriser", "RICE scoring",
  "on a trop de sujets, aide-moi à choisir", or "quel sujet tackler en premier".
---

# Prioritization — RICE Scoring

Helps rank features or initiatives using the RICE framework to make roadmap decisions defensible and data-informed.

**RICE score = (Reach × Impact × Confidence) / Effort**

## Workflow

**Step 1 — List items to score**
Ask the user to list the features or initiatives to compare. If context is missing (what problem each solves, who it affects), ask before scoring.

**Step 2 — Collect RICE inputs**
For each item, ask or estimate:

| Input | Definition | Scale |
|---|---|---|
| **Reach** | How many users affected per quarter | Absolute number |
| **Impact** | How much it moves the needle per user | 0.25 / 0.5 / 1 / 2 / 3 |
| **Confidence** | How sure you are about reach and impact | 20% / 50% / 80% / 100% |
| **Effort** | Person-weeks to ship | Absolute number |

If the user can't estimate precisely, help them reason through it: compare to past features, use Mayday's user base segments from product context if relevant.

**Step 3 — Compute and present**

| Feature | Reach | Impact | Confidence | Effort | RICE Score |
|---|---|---|---|---|---|
| [Feature A] | [N] | [x] | [%] | [weeks] | [score] |

Sort by RICE score descending.

**Step 4 — Add qualitative overlay**
Raw RICE scores are a starting point, not the answer. Flag items where:
- Score is high but confidence is low → validate first before committing
- Score is low but it's a blocker for another high-score item → may need to sequence it first
- Strategic importance (customer commitment, competitive pressure) overrides the score

**Step 5 — Recommendation**
State a clear recommendation: what to tackle first, what to defer, what to drop. Give the reasoning in 2-3 sentences.

**Step 6 — Save**
Save as `prioritization-[date].md` in the current project folder. Offer to update `project.md` if it exists.
