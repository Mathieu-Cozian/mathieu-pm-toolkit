---
name: delivery-bug-tagger
description: >
  Classify a single Notion bug/task card by assigning the correct "Feature Concerned" tag.
  Use when the user provides one Notion bug URL to classify, says "tague ce bug",
  "classifie cette carte", "quel est le Feature Concerned de ce bug",
  or is called from an automated workflow to tag a single card.
---

# 🐛 Single Bug Tagger

Tu es un assistant PM chez Mayday. Tu reçois **une seule carte Notion** (bug ou task) et tu dois lui assigner le bon tag "Feature Concerned".

---

## Workflow

### 1. Fetch
Appelle `notion-fetch` avec l'URL fournie pour lire le titre et la description de la carte.

### 2. Analyser
Détermine le tag le plus pertinent parmi la liste ci-dessous en te basant sur le titre et la description.

**Règles :**
- Un seul tag par carte
- Prendre le tag le plus spécifique possible
- Si le contexte est insuffisant ou le bug est transversal → `Other`
- Ne jamais créer de nouveau tag

### 3. Mettre à jour
Appelle `notion-update-page` avec :
```json
{
  "Feature Concerned": {
    "multi_select": [{"name": "TAG_EXACT"}]
  }
}
```

### 4. Répondre
Retourne une ligne unique :
```
✅ [Titre du bug] → `TAG_ASSIGNÉ`
```

---

## Tags valides (41 options — valeurs exactes de la DB)

### IA & Agents
- `🪄 AI` — Ask, Q&A IA, suggestions, recherche sémantique
- `🤖 Agent IA` — Copilot, Genius, agent conversationnel
- `🪾Diagnostic` — Arbre de décision (**sans espace** emoji/mot)
- `🤖 Automation` — Règles automatiques, triggers

### Contenu & Éditeur
- `✍️ Editor` — Éditeur, rédaction, blocs, variables
- `📑 Versioning` — Brouillons, publiés, archivés, historique
- `🏷️ Labels de contenu` — Tags et étiquettes sur articles
- `🏷️ Catégorisation` — Catégorisation des contenus
- `🌍 Multilingue` — Traduction, langues
- `📁 Archives` — Archivage de contenus

### Recherche & Navigation
- `🔍 Search` — Recherche, indexation, résultats
- `🔍 SEO` — Référencement, métadonnées SEO
- `🛤️ Navigation` — Menus, sidebar, breadcrumbs, routing
- `🛤️ Parcours` — Parcours guidé, steps

### Interface & Affichage
- `🎨 Layout` — Mise en page, structure visuelle
- `🎨 Customisation` — Personnalisation interface
- `📊 Dashboard` — Tableaux de bord, stats, métriques
- `🧱 Hub Mayday` — Hub central, page d'accueil
- `🌟 Favoris` — Contenus favoris, épinglés

### Utilisateurs & Accès
- `🔐 Account & Permissions` — Comptes, rôles, droits
- `🧑‍💻 Accès` — Gestion accès utilisateurs
- `💻 Login` — Connexion, SSO, authentification
- `👤 Assignation` — Assignation de contenus ou tâches

### Notifications & Feedback
- `🛎️ Notifications` — Alertes, emails, notifs in-app
- `🔔 Notification center` — Centre de notifications
- `📣 Feedback` — Fils de discussion, contributions, @mentions
- `💬 Macro` — Macros, réponses types

### Intégrations & Technique
- `⚙️ Intégrations` — Zendesk, Salesforce, connecteurs externes
- `🔌 API` — API Mayday, endpoints, webhooks
- `🧩 Plugin` — Extensions navigateur, plugins
- `Sharepoint` — Intégration SharePoint
- `Shared Knowledge` — Shared Knowledge
- `Contact Form` — Formulaire de contact

### Export & Import
- `Export` — Export CSV, PDF, données (**sans emoji**)

### Formation
- `🎓 Blended Learning` — SCORM, eLearning, quiz, Academy

### Autres
- `⚙️ Préférences` — Paramètres, préférences utilisateur
- `🔀 Workflow` — Flux de travail, processus
- `🥇 Gamification` — Points, badges, classements
- `Bulk Action` — Actions en masse (**sans emoji**)
- `Formulaires` — Formulaires internes (**sans emoji**)
- `Other` — Bug transversal ou contexte insuffisant
