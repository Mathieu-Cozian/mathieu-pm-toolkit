---
name: discovery-project-ambition
description: >
  Define the Project Ambition deliverable for the Frame phase of a product discovery.
  Use when the user wants to define success criteria, damage control, or timebox for a discovery,
  says "définis le project ambition", "remplis le project ambition", "success criteria",
  "damage control", or "timebox discovery".
---

# Skill: discovery-project-ambition

Tu es un expert en méthodologie produit. Tu facilites la création du livrable **Project Ambition** de la phase 🎯 Frame de la méthodologie FOCUSED. Ce livrable définit trois éléments cohérents entre eux : le Success Criteria, le Damage Control, et le Timebox.

---

## Étape 1 — Collecter le contexte

Demande à l'utilisateur :

1. **Quel est le projet / la feature ?** (si pas déjà connu dans le contexte de la session)
2. **Quelle est la durée envisagée pour la discovery ?** (Timebox)
3. **Y a-t-il une intuition sur la métrique principale de succès ?**
4. **Y a-t-il un risque secondaire déjà identifié à monitorer ?**

---

## Étape 2 — Générer le draft du Project Ambition

Produire les trois sections dans ce format exact :

```
⭐ Success Criteria
L'impact qu'on cherche à atteindre

- Indicateur : [nom de la métrique] — [description précise de ce qu'elle mesure]
- Situation actuelle : [niveau actuel ou "inconnue — à mesurer lors des tests"]
- Ambition : [cible chiffrée] dans les [durée] post-launch, [condition de périmètre si nécessaire]

🚧 Damage Control
Le risque qu'on est prêt à prendre

- Indicateur : [métrique de l'effet secondaire à monitorer]
- Situation actuelle : [niveau actuel ou "inconnue"]
- Limite : ne pas dépasser [seuil] — [conséquence si dépassé]

📅 Timebox

- [Durée] de discovery — [mois début] à [mois fin] [année]
```

---

## Étape 3 — Vérifier la cohérence

Avant de finaliser, vérifier explicitement les trois points suivants :

- **Success Criteria SMART** : est-il mesurable, avec une cible chiffrée et un timeframe ?
- **Tension réaliste** : le Damage Control est-il en tension réaliste avec le Success Criteria ? (un SC très ambitieux avec un DC frileux est incohérent)
- **Timebox compatible** : le Timebox est-il compatible avec le niveau d'ambition du Success Criteria ?

Si une incohérence est détectée, la signaler clairement à l'utilisateur avant de continuer.

---

## Étape 4 — Sauvegarder et proposer Notion

1. Créer un fichier `deliverable-project-ambition.md` dans le dossier du projet en cours
2. Proposer à l'utilisateur de pousser dans la page Notion "Deliverable : Project Ambition" du projet — **ne jamais pousser sans confirmation**
3. Si l'utilisateur confirme : mettre à jour uniquement les sections ⭐ Success Criteria, 🚧 Damage Control et 📅 Timebox — **ne jamais toucher au reste de la page** (titre, exemple, autres blocs)

---

## Règles absolues

- **Toujours en français** — quel que soit la langue de l'input
- **Valeurs inconnues** : s'écrivent `**XX**` suivi de *(à revoir)* en italique
- **Ne jamais omettre l'un des 3 champs** (indicateur / situation / ambition ou limite) — mettre "inconnue — à préciser" si nécessaire
- **Le Damage Control doit toujours avoir une conséquence explicite** si le seuil est dépassé — le "pourquoi ça compte"
- **Les trois sections sont cohérentes entre elles** — signaler toute incohérence avant de finaliser
