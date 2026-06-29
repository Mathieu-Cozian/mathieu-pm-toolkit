<!--
TEMPLATE DE CARD BUG — Mayday
Fichier de référence du skill de qualification de bug (séparé du SKILL.md).
Conçu à partir des exigences de « Comment qualifier un Bug ? »
https://app.notion.com/p/389d8524798880df97edcfe87f7ffab0

Règles de rendu pour le skill :
- Pour tout champ manquant dans le transcript : d'abord RELANCER le CSM dans la conversation
  pour obtenir l'info. Si le CSM ne l'a pas / passe, inscrire `[TO FILL]` à l'emplacement.
- Ne JAMAIS inventer un identifiant (userId, companyId, ID entité).
- Les identifiants doivent rester en TEXTE COPIABLE (jamais seulement dans la vidéo).
- Le Criticity Score : le skill DEMANDE au CSM dans la conversation les éléments nécessaires
  (impact, tiering, contexte commercial), calcule le total avec lui et l'inscrit. Le CSM valide.
- La section « Investigation Tech » est laissée vide (réservée à la Tech).
-->

# {{PRODUIT}} — {{Titre court et explicite du bug}}

> **Type :** 🐞 Anomaly  ·  **Statut :** 🚨 Not started  ·  **Créée le :** {{JJ/MM/AAAA}}

---

## 🧑‍💻 Contexte

> *Permet à la Tech de retrouver et reproduire le problème dans le bon environnement.*

| | |
|---|---|
| **Produit concerné** | {{Knowledge / Academy / Selfcare}} |
| **Fonctionnalité** | {{Feedback / Notifications / Hub / Dashboard / Search / …}} |
| **Client** | {{Nom du client}} — `companyId: {{companyId}}` |
| **Utilisateur impacté** | {{email}} — `userId: {{userId}}` |
| **Entité en cause** | `{{type + identifiant copiable}}` *(contenu / fiche / workflow…)* |

---

## 🐞 Le bug

**✅ Comportement attendu**
> {{Ce que le client / l'utilisateur attendait}}

**❌ Comportement constaté**
> {{Ce qui se passe réellement}}

*Détails utiles :* {{période, groupes/profils impactés, fréquence, environnement…}}

---

## 🔁 Reproduire le bug

**Étapes de reproduction**

1. {{Action 1}}
2. {{Action 2}}
3. {{… → le bug se produit}}

**🎬 Loom du flow (console ouverte)** : {{lien Loom}}
> Rappel : console + onglet Network ouverts pendant la démo — les erreurs navigateur sont souvent décisives.

---

## 📸 Preuves visuelles

> *Screenshots collés directement dans la page (pas de liens externes qui se périment). La vidéo montre le comportement, le screen fige l'état.*

> ⚠️ **Screenshots = dépôt manuel par la CS.** Le skill ne peut pas uploader une image brute dans Notion ; il insère une image **seulement si elle a déjà une URL publique**. Sinon, il laisse l'emplacement ci-dessous et la CS glisse-dépose ses captures.

- `[TO FILL — screenshot : glisser-déposer ici]`
- {{légende éventuelle}}

---

## 🔍 Tests réalisés par le CSM

- [ ] 🥵 Reproduit sur le **compte client**
- [ ] 🥵 Reproduit sur le **compte démo CSM**
- [ ] 🥵 Reproduit en **impersonation** (Back Office / Retool)

*(cocher selon ce qui a été testé ; préciser le résultat si « non reproduit » ou « test impossible »)*

---

## 🎚️ Criticité — *renseignée via les questions du skill au CSM*

> Le skill demande au CSM : impact fonctionnel, tiering client, contexte commercial. Score = **Impact** + **Tiering client** + **Contexte commercial**, calculé avec le CSM. Une fois le score renseigné, le niveau de `Criticity` se met à jour automatiquement (automation Notion).

| Élément | Valeur retenue | Points |
|---|---|---|
| Impact fonctionnel | {{Critique / Majeur / Mineur}} | {{4 / 2 / 1}} |
| Tiering client | {{Platinum / Golden / Silver / Bronze}} | {{5 / 4 / 2 / 1}} |
| Contexte | {{Renewal-insatisfaction +2 / Upsell +1 / —}} | {{+2 / +1 / 0}} |
| **Criticity Score** | | **{{TOTAL}}** |

> ⚠️ **Bloquant** (connexion / recherche / consultation KO) → ne pas scorer : basculer sur le **process d'incident** et alerter immédiatement.
> ⚠️ **Plafond mineur** : un bug mineur ne dépasse jamais **4**.

---

## 👨‍🚒 Investigation Tech

*Réservé à l'équipe Tech — laisser vide à la création.*
