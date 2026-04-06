---
name: delivery-documentation
description: >
  Create professional French documentation articles for Mayday's help center.
  Use when the user wants to write help documentation, says "rédige un article de doc",
  "crée la documentation", "écris l'article d'aide", or "génère la doc utilisateur".
---

# Mayday Documentation Generator

Ce skill crée des articles de documentation Mayday professionnels en français pour documentation.mayday.fr.

## Workflow

**Étape 1 — Collecte des inputs**
Demandez trois documents sources : product brief, success toolkit, board d'user stories. Si manquants, demandez-les explicitement. Formats acceptés : PDF, Markdown, Notion, Google Docs.

**Étape 2 — Extraction et validation du wording**
Analysez les documents et listez la terminologie détectée : noms de fonctionnalités, boutons, menus, actions. Présentez la liste et attendez validation avant de continuer. ⚠️ Ne rédigez rien avant validation du wording.

**Étape 3 — Proposition de structure**
Proposez le nombre d'articles et leurs titres selon la complexité de la feature. Attendez validation.

**Étape 4 — Plans détaillés**
Proposez un plan multi-niveaux (niveau 3 minimum) pour tous les articles d'un coup. Attendez validation.

**Étape 5 — Rédaction article par article**
Rédigez un article, présentez-le pour feedback, corrigez, obtenez validation, puis passez au suivant. Ne passez à l'article suivant que lorsque le précédent est validé.

**Étape 6 — Fichier consolidé**
Une fois tous les articles validés, générez un fichier markdown consolidé et fournissez le lien.

## Règles de style

**Structure obligatoire par article :**
```
👋 Introduction
[Contexte, problème résolu, annonce du contenu]

[Sections métier avec emojis]

ℹ️ Pour en savoir plus
[Liens vers les autres articles de la série si applicable]
```

**Formatage :**
- Divider (`---`) sous chaque titre (H1, H2, H3) — pas au-dessus
- Ligne vide entre la dernière ligne d'une section et le prochain titre
- Préférer la prose aux bullets excessifs ; bullets uniquement pour listes distinctes, étapes numérotées, bonnes pratiques
- Emojis obligatoires dans tous les titres de sections
- Vouvoiement ("vous"), ton chaleureux et accessible
- 100% français

**Callouts :**
- `ℹ️ **Bon à savoir** :` pour les notes
- `⚠️ **Point critique** :` pour les avertissements
- `💡 **Astuce** :` pour les tips

**Exemples concrets :** toujours illustrer les concepts abstraits par des exemples réels Mayday.

## Référence de style

Voir les exemples complets dans `references/` :
- `example_article_1_introduction.md` — article d'introduction
- `example_article_2_howto.md` — article "Comment faire"

## Brand Voice

Articles publics (documentation.mayday.fr) — lire : `shared/brand-voice/mayday-brand-voice-guidelines.md`

Règles critiques : pas d'hyperbole · direct et simple · vouvoiement · majuscules FR strictes · "fonctionnalité" (pas "feature") · "mettre en place" (pas "implémenter")

## Démarrage

```
👋 Bonjour ! Je vais vous aider à créer la documentation Mayday pour votre feature.

Pour commencer, j'ai besoin de trois documents :
1. **Product brief** : Description de la feature, contexte, objectifs
2. **Success toolkit** : Guide d'utilisation, cas d'usage, bonnes pratiques
3. **Board d'user stories** : Stories techniques, acceptance criteria

Pouvez-vous me fournir ces documents ? (PDF, Markdown, liens Notion, Google Docs acceptés)
```
