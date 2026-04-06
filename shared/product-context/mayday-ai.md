# Mayday AI — Feature Context

**Mayday AI is not a standalone product.** It is a package of AI features extending Knowledge, Selfcare, and Academy. AI quality depends on knowledge base quality — No KM, No AI.

**Two core components:**
- **Mayday Genius** — side panel UI available across all surfaces (Mayday Admin, Mayday Desk, Widget, Zendesk app, iAdvize app); gives access to AI agents in context
- **AI Agents** — specialized agents each with a defined purpose, data sources, and action capabilities; standard agents are built by Mayday; custom agents (create your own) are a planned capability

## Available Agents

| Agent | What it does | Key sources |
|---|---|---|
| **Ask Mayday** | Answers questions about the KB and Mayday environment | Knowledge bases |
| **Answer Generator** | Generates ticket responses; reads the currently open ticket in Zendesk/Widget | KB + ticketing content + open ticket |
| **Knowledge Insider** | Insights on content performance, gaps, and audience engagement | KB + Hub feedbacks + dashboard data |
| **Knowledge Builder** | Transforms any input (text, doc, existing content) into ready-to-publish articles or diagnostics | KB + external sources (SharePoint, files) |
| **Notification Generator** | Drafts agent notifications | Knowledge bases |
| **Module Generator** | Creates complete Academy training modules from any input | KB + external sources |
| **Quiz Generator** | Generates quiz questions integrable into Academy modules | KB content + module elements |

## AI Features by Product

**Mayday Knowledge — KM:**
Write, edit, and translate content with inline AI; draft notifications; use Knowledge Builder, Knowledge Insider, Notification Generator agents; receive proactive content insights

**Mayday Knowledge — Agent:**
Ask Mayday agent for in-context answers; Answer Generator for suggested ticket responses (reads open ticket automatically in Zendesk/Widget)

**Mayday Selfcare — KM:**
Configure and customize Ask Mayday per portal; track Ask Mayday usage and content gap analytics

**Mayday Selfcare — End user:**
Ask Mayday assistant on the public portal — natural language Q&A sourced from the KB

**Mayday Academy — KM:**
Module Generator to create full training modules; Quiz Generator to generate quiz slides directly inside a module (accepts @ KB references or natural language)

## Configuration
Managed in Mayday Admin > Preferences > AI Settings:
- **Global toggles** — enable/disable AI Agents, Ask Mayday, Translation (with per-language instructions)
- **Agent access** — assigned per role; new roles have no AI access by default; three conditions required: agent globally active + role has access + agent enabled on user's interface
- **Agent sources** — configurable per agent: KB content (filterable to KB/collection/content level), Hub feedbacks, ticketing platform content (including open ticket), dashboard data, external files, internet access
