# Mayday Knowledge — Module Context

**Baseline** : Centralisez, harmonisez et diffusez la connaissance. **Key metric** : −20% agent search time.

Internal knowledge base for customer service agents. KMs maintain a single source of truth; agents consult it in context across their tools.

## Interfaces
- **Mayday Admin** — KM/admin platform for creating and managing content, users, and settings
- **Mayday Desk** — standalone web app for agents
- **Mayday Widget** — Chrome extension overlaying Mayday on any tool the agent uses
- **Zendesk app** — Mayday embedded inside Zendesk tickets

## Content Formats
- **Article** — linear content on a specific theme or procedure
- **Diagnostic / Guide** — interactive decision tree for complex step-by-step procedures
- Both support rich media (video, PDF, Google Slides, images, iframes)
- **Shared Elements** — reusable content blocks referenceable across articles and diagnostics; also available on Selfcare portals

## Content Management
- **Status lifecycle** — Draft → Published → Archived; version control with archive access
- **Content labels** — metadata tags applied to content for filtering, search scoping, and organization; displayed as breadcrumbs in navigation
- **Content verification** — KMs set verification schedules per content piece; overdue content triggers obsolescence alerts in Mayday Hub
- **Multiple knowledge bases** — an account can have several KBs (e.g. by language, BU, or product); access scoped per group
- **Multilingual** — knowledge bases support multiple languages; content can be maintained per language; AI translation available to automatically translate content from one language to another (with custom translation instructions configurable per language)
- **Import** — import existing content into the KB
- **Custom plugins** — extend the agent interface with: custom HTML (iframe), latest published content, trending content, smart buttons, suggested responses

## Permissions Model
- **Group** — defines content scope (which KBs and collections a user can see); one group per user
- **Role** — defines feature access (read, edit, verify content; send notifications; access Hub, dashboards, settings, AI); multiple roles per user; permissions combine
- **User Labels** — segmentation tags (axes + values, e.g. Location > Paris); used for analytics filtering and auto-assignment; one label per axis per user
- **Provisioning** — automated account creation via SSO; can auto-assign group, role, and labels based on SSO profile; three models: default, mapping, synchronization

## Key Features
- **Search** — keyword search with exact match (`"term"`); AI search via Ask Mayday; filter by content labels; configurable synonyms and label search logic (OR/AND)
- **Notifications** — admins push notifications to agents; AI-assisted drafting
- **Mayday Hub** — Kanban-based feedback and task management center; agents submit feedback on content; KMs review, prioritize, assign, and respond; obsolescence alerts triggered automatically on schedule; task workflow: Backlog → À faire → En cours → Terminé
- **Analytics** — content performance (consultations, satisfaction, reliability score, search success/failures); usage (adoption rate, agent activity); filterable by KB, date, group, label; exports: content, users, AI usage, Hub feedbacks

## Integrations
Zendesk, Salesforce, Intercom, Notion, Slack — full catalog available in-product
