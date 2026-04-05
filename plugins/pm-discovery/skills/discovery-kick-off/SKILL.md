---
name: discovery-kick-off
description: >
  Start a new product discovery project with a Kick Off doc and Project Ambition sheet.
  Use when the user wants to launch a discovery, frame a new product initiative, or says
  "lance le kick off", "démarre une discovery", "prépare le doc de kick off".
---

# Skill: discovery-kick-off

## Trigger
Use this skill when the user wants to start a new Discovery project — e.g. "lance le kick off de ma discovery", "démarre une discovery", "prépare le doc de kick off", "create a discovery kick off".

## Context
At Mayday, all product discoveries follow the FOCUSED framework (Frame → Observe → Claim → Unfold → Steal → Execute → Decide). The Frame phase is the first step. Its goal is to formally define WHY this discovery was launched, the success criteria, the risks, and the timebox.

Two documents are produced during the Frame phase:
1. **Discovery Kick Off** — the full context document
2. **Project Ambition sheet** — the concise strategic anchor (NSM, damage control, timebox)

## What to do

### Step 1 — Gather context
Ask the user for the following if not already provided:
- What is the feature / problem area this discovery is about?
- What triggered this discovery? (client feedback, churn risk, strategic bet, etc.)
- Who are the target users / persona?
- What is the approximate timebox? (e.g. 2 months)
- Any known problem hypotheses already?

### Step 2 — Generate the Discovery Kick Off document

Produce a structured document with the following sections. Write in the same language as the user (French if they write in French).

---

**🌍 Context & Background**
2–3 sentences. What is the current situation? What has changed in the market or product that makes this discovery necessary?

**🎯 The "Why" & Objectives**
Why are we launching this discovery now? What business risk or opportunity does it address? What do we want to achieve?

**💡 Problem Hypotheses**
List 2–4 hypothesis statements (not solutions). Format each as:
> **Hypothesis N: [Short title]**
> We believe [user/persona] [does/has/faces] [X]. This leads to [negative outcome]. [Why this matters for the business].

**🔍 Learning Goals**
What do we need to understand to validate or invalidate the hypotheses? Use "Understand:" as a header, then bullet the specific questions to answer.

**📈 Success Metrics**
- **NSM (North Star Metric):** One primary metric with a target and a timeframe. Explain why this metric was chosen.
- **Feature KPIs:** Adoption rate, retention rate, SAT / NPS (as relevant)
- **Business NSM:** The related business-level metric (churn, revenue, etc.)

**👥 Key Clients & Persona**
Which persona is targeted? Which client segments / accounts should be interviewed?

**📊 Methodology & Data**
- **Qualitative:** Internal interviews (who?), client interviews (how many?), forms if needed
- **Quantitative:** Which data / metrics will be pulled (Amplitude, Metabase, etc.)

**🗓️ Timeline & Milestones**
Month-by-month milestones for the discovery period.

---

### Step 3 — Generate the Project Ambition sheet

Produce a concise separate section titled **⭐ Project Ambition** with:

- **Success Criteria:** The NSM with a precise target (SMART). Explain why this metric proves value.
- **Other Key Metrics:** Business NSM + 2–3 feature KPIs
- **Damage Control:** List 2–3 risks or ways this could go wrong. Be specific.
- **Timebox:** Duration + hard deadline if known.

## Output format
- Present both documents clearly separated
- Use Notion-compatible markdown (headers with ##, bullet lists, bold)
- Write in the user's language
- Be specific and business-oriented — avoid vague statements
- The Project Ambition NSM must be SMART: measurable, with a target percentage/number and a timeframe

## Example NSM (from Knowledge Quality discovery)
> "Knowledge Quality WAU Rate, with a target of 70% of eligible users (AI admins) by 3 months post-release."
