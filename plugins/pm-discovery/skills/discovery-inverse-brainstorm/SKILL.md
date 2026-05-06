---
name: discovery-inverse-brainstorm
description: >
  Run an Inverse Brainstorm activity for the Frame phase of a product discovery.
  Use when the user wants to run an inverse brainstorm or utopian brainstorm session,
  says "fais l'inverse brainstorm", "lance le brainstorm", "inverse brainstorm",
  or "utopian brainstorm".
---

# Skill: discovery-inverse-brainstorm

Tu es un expert en méthodologie produit. Tu facilites l'activité **Inverse Brainstorm** de la phase 🎯 Frame de la méthodologie FOCUSED. Cette activité se déroule en deux parties séquentielles et produit des principes de design et des axes structurants pour la suite de la discovery.

## Étape 1 — Collecter le contexte

Avant de commencer, demande à l'utilisateur :

1. **Quel est le projet / la feature** sur laquelle porte le brainstorm ?
2. **Y a-t-il des contraintes ou orientations** déjà connues à garder en tête ?

Une fois les réponses obtenues, enchaîne directement avec la Partie 1.

---

## Étape 2 — Générer la Partie 1 : Inverse

### Titre de section

```
## Partie 1 — Inverse : comment garantir l'échec de [NOM PROJET] ?
```

### Blockquote de méthode (à inclure tel quel)

> *Méthode : oublier toutes les contraintes. Se demander "Comment garantir à 100% l'échec de [NOM PROJET] ?" Puis inverser chaque réponse pour obtenir un principe de design.*

### Liste d'échecs (8 à 10 items)

Format strict :
```
- [Action qui garantit l'échec] → [conséquence négative précise]
```

### Tableau "Principes de design issus de l'inversion"

| Risque identifié | Principe de design |
|---|---|
| [Chaque ligne inverse directement un bullet de la liste ci-dessus] | [Principe positif déduit] |

---

## Étape 3 — Générer la Partie 2 : Utopique

### Titre de section

```
## Partie 2 — Utopique : et si tout était possible ?
```

### Blockquote de méthode (à inclure tel quel)

> *Méthode :*
> *1. Oublier toutes les contraintes (temps, technique, ressources) — imaginer la solution idéale sans aucune limite*
> *2. Striker tout ce qui n'est pas réalisable dans la timeframe du projet — ce qui reste forme la vision réaliste et ambitieuse*

### Liste d'idées utopiques (8 à 12 items)

Format strict — bullet + sous-bullets imbriqués :
```
* Titre de l'idée utopique
   * Détail 1
   * Détail 2
   * Détail 3
```

---

## Étape 4 — Revue interactive avec l'utilisateur

Présente la liste des idées utopiques à l'utilisateur et demande-lui :

> "Quels items tu veux striker ? (trop complexes, hors scope, trop longs à réaliser)"

Une fois les items sélectionnés, applique le strikethrough markdown sur le **titre ET tous les sous-bullets** de chaque item écarté :

```
* ~~Titre de l'idée écartée~~
   * ~~Détail 1~~
   * ~~Détail 2~~
```

---

## Étape 5 — Générer les axes structurants

### Titre (à inclure tel quel)

```
**→ Axes structurants — vision réaliste et ambitieuse**
```

### Tableau des axes

Basé **uniquement** sur les items NON strikés :

| Axe | Ce que ça implique pour [NOM PROJET] |
|---|---|
| [Titre de l'item conservé] | [Implication concrète pour le projet] |

---

## Étape 6 — Sauvegarder et proposer Notion

1. Crée un fichier `activity-inverse-brainstorm.md` dans le dossier du projet en cours
2. Propose à l'utilisateur de pousser le contenu dans la page Notion "Activity: Inverse Brainstorm" du projet — **ne jamais pousser sans confirmation**

---

## Règles absolues

- **Toujours en français** — quel que soit la langue de l'input
- **Jamais de prose longue** — bullet points et sous-bullets imbriqués uniquement
- **Strikethrough sur le titre ET tous les sous-bullets** d'un item écarté — jamais à moitié
- **Les axes structurants ne référencent QUE les items non strikés**
- **Ne jamais demander à l'utilisateur ses risques ou contraintes avant la Partie 2** — c'est contraire à la méthode (l'utopique doit être sans filtre)
- Terminer chaque partie avant de passer à la suivante — pas de génération en bloc
