# Skill: discovery-product-brief

## Trigger
Use this skill when the user wants to write a PRD or Product Brief at the end of a discovery — e.g. "écris le PRD", "rédige le product brief", "Decide phase", "write the PRD".

## Context
At Mayday, the Decide phase (step 7 of FOCUSED) is the final step of a discovery. After user testing and validation, if the decision is **Go**, the PM produces a **PRD (Product Requirements Document)** that serves as the spec for the Engineering team.

Mayday uses a specific PRD format. This skill generates a PRD following that exact structure.

The PRD must:
- Summarize the discovery findings and decisions
- Define the exact MVP scope
- Document all product rules and behaviors
- Include success metrics linked to Amplitude
- Serve as the single source of truth for the Delivery phase

## What to do

### Step 1 — Gather context
Ask the user for the following if not already provided:
- Discovery link (Notion URL to the discovery project)
- Feature name
- FUC (First Use Case)
- MVP scope (from the Execute phase)
- Design link (Figma, if available)
- Key product rules and behaviors already decided
- Out-of-scope items confirmed

### Step 2 — Generate the PRD

Produce the full PRD following Mayday's exact template structure:

---

## 🔗 Discovery
[Lien vers la Discovery associée]

---

## 🧭 Overview
[2–3 sentences: context + who is impacted + why it's a problem today + what triggered this project]

**Goal:** [One sentence summarizing the objective of this feature]

---

## 🧾 Definitions
[List all key terms introduced by this feature. Format: **Term 📌:** Definition]

---

## 🎯 Feature Pitch
[2–3 sentences: start with a "need" scenario (who has what problem?), then explain how the feature responds, then list the key properties that characterize it]

---

## 📊 Key Success Metrics

### ⭐ North Star Metric
[Single primary metric. Define what "active" means in this context, what the metric actually measures, and the target with timeframe]

### 👀 Key Performance Indicators
[3–5 measurable indicators. For each: short title + formula/definition + what it measures and why it matters + whether it's in Amplitude or database only]

**1. [KPI Name]**
[Formula or definition] — *[What it measures]*

**2. [KPI Name]**
[Formula or definition] — *[What it measures]*

**3. [KPI Name]**
[Formula or definition] — *[What it measures]*

### 🔼 Supporting Metrics
[Secondary metrics to monitor but not optimize directly]

---

## 💪 Features
[List the MVP features with a brief description of each. Use the format: **Feature name:** Description + acceptance criteria summary]

---

## 🎨 Design
[Figma link or "En cours — @designer"]

---

## ⚙️ Product Rules and Behavior

### 👀 Visibility
[Who sees what, in which context (admin, agent, reader)? Differences by role or surface?]
→ *[Alignment status + date]*

### 🔐 Access Restrictions
**Édition:**
**Lecture:**
→ *[Alignment status + date]*

### 🤖 AI
**Fonctionnalités IA éditeur:**
**Agents IA (Genius):**
→ *[Alignment status + date]*

### 🔎 Search Engine
[How is this feature indexed and returned in search? Ranking rules?]
→ *[Alignment status + date]*

### 🔌 API
[Which endpoints are impacted? Expected behavior in responses?]
→ *[Alignment status + date]*

### 🌐 Languages
[Does the feature support multilingual? How are missing languages handled?]
→ *[Alignment status + date]*

### 📈 Analytics
[What analytics are available at launch (v0)? What's measurable in Amplitude vs. database?]
→ *[Alignment status + date]*

### ⛔ Limits
[Technical or product limits defined for this feature]
→ **Todo:**
- [ ] [Point to decide]

---

## ⛔️ Out of Scope (v0)
[Explicit list of everything excluded from v0 scope, with brief rationale for each]

---

## ✅ Acceptance Criteria (v0)
[List of verifiable criteria that define "done" for v0. Each must be objectively testable]
- [ ] [Criterion 1]
- [ ] [Criterion 2]
- [ ] [Criterion 3]

---

## 📚 Resources
[Links to: discovery, user interview summaries, benchmark, Figma, tech specs, etc.]

---

### Step 3 — GTM Checklist (bonus)

Add a brief **Go-To-Market checklist** to align with GTM teams:
- [ ] Target beta clients identified (prioritize discovery participants)
- [ ] In-app onboarding defined
- [ ] Help Center article planned
- [ ] Release notes drafted
- [ ] CS team briefed
- [ ] Changelog / communication timeline set

## Output format
- Follow the PRD structure exactly as shown above
- Use toggle sections (marked with `{toggle}`) for Features, Product Rules, Out of Scope, Acceptance Criteria, Delivery
- Sections with `→ Alignment status` should be marked `→ Todo` if not yet discussed
- Write in French (Mayday's working language) unless the user asks otherwise
- Mark all placeholder values in [brackets] for the user to fill in
- Do NOT invent product rules — leave them as "Todo" if not provided
