---
name: delivery-documentation
description: Create professional French documentation articles for Mayday product features following the company's established style guide. Use this skill when the user needs to write, create, draft, or update documentation for Mayday's help center (documentation.mayday.fr), especially after product releases. Trigger when the user mentions "documentation Mayday", "articles d'aide", "centre d'aide", "help center", "doc produit", or provides a product brief/success toolkit for documentation. Also trigger when the user asks to structure feature documentation into multiple articles or update existing Mayday documentation.
---

# Mayday Documentation Generator

## Overview

Ce skill vous aide à créer des articles de documentation Mayday professionnels en français, formatés selon les standards du centre d'aide Mayday (documentation.mayday.fr). Il guide l'utilisateur à travers un processus structuré : analyse des documents produit, validation du wording, proposition d'une architecture d'articles, puis rédaction itérative avec feedback.

Le skill est conçu pour :
- **Nouvelle documentation** : Créer des articles pour de nouvelles features
- **Actualisation** : Mettre à jour la documentation existante après des releases produit
- **Structuration** : Organiser une feature complexe en plusieurs articles (Introduction + How-to)

## Workflow

### Étape 1 : Collecte des inputs

Demandez à l'utilisateur de fournir **trois documents sources** :

1. **Product brief** : Description de la feature, contexte, objectifs
2. **Success toolkit** : Guide d'utilisation, cas d'usage, bonnes pratiques
3. **Board d'user stories** : Stories techniques, acceptance criteria, détails d'implémentation

Si l'utilisateur ne fournit pas ces trois documents, demandez-les explicitement. Ces sources sont essentielles pour comprendre la feature et extraire le bon wording.

**Format accepté** : PDF, Markdown, liens Notion, Google Docs, ou fichiers texte.

### Étape 2 : Analyse et extraction du wording

Une fois les documents reçus, analysez-les pour identifier :

1. **Terminologie produit** : Les noms exacts des fonctionnalités, boutons, menus, sections
2. **Concepts clés** : Les termes métier spécifiques à la feature
3. **Actions utilisateur** : Les verbes et formulations utilisés pour décrire les actions

**Créez une liste structurée** de tous les wordings détectés, par exemple :

```
WORDINGS DÉTECTÉS :

Fonctionnalités :
- "Élément transverse" (ou "Élément partagé" / "Contenu réutilisable" ?)
- "Bibliothèque d'éléments transverses" (ou autre terme ?)

Actions :
- "Insérer un élément" (ou "Ajouter" / "Importer" ?)
- "Transformer en élément transverse" (dans le menu contextuel)

Sections interface :
- Bouton "Éléments transverses" (dans la barre latérale)
- Menu "Ajouter un contenu"
```

**Présentez cette liste à l'utilisateur** et demandez-lui de **valider ou corriger** chaque terme. Attendez sa validation avant de passer à l'étape suivante.

⚠️ **Point critique** : Le wording doit être validé AVANT de rédiger quoi que ce soit. Des termes incorrects dans la documentation créent de la confusion pour les utilisateurs finaux.

### Étape 3 : Proposition de structure d'articles

Après validation du wording, proposez une structure d'articles :

1. **Analysez la complexité** de la feature
2. **Proposez un nombre d'articles** et leurs titres

**Format de proposition** :

```
STRUCTURE PROPOSÉE : 6 articles

Article 1 : Introduction aux éléments transverses
Article 2 : Comment créer un élément transverse
Article 3 : Comment insérer un élément transverse
Article 4 : Comment gérer et maintenir un élément transverse
Article 5 : Comment suivre l'utilisation d'un élément transverse
Article 6 : Comment gérer le multilingue avec les éléments transverses
```

**Demandez validation** : "Cette structure vous convient-elle, ou souhaitez-vous modifier le nombre d'articles ou leurs titres ?"

Attendez la validation avant de continuer.

### Étape 4 : Proposition du plan détaillé

Pour chaque article validé, proposez un **plan détaillé multi-niveaux** avec bullets longs si nécessaire.

**Niveau de détail requis** : Niveau 3 minimum, rentrer vraiment dans le contenu.

**Exemple de plan détaillé** :

```
ARTICLE 2 : Comment créer un élément transverse

👋 Introduction
- Contexte : L'utilisateur veut centraliser une information
- Bénéfice : Créer une seule fois, réutiliser partout
- Annonce des deux méthodes disponibles

🤔 Comment ça marche ?
- Présentation des deux approches principales

🆕 Création à partir de zéro
- Étape 1 : Accéder à la bibliothèque
  * Localisation : Bouton "Éléments transverses" dans barre latérale
  * Contexte : Disponible depuis n'importe quelle collection
- Étape 2 : Cliquer sur "Ajouter un contenu"
  * Similarité avec création d'article classique
- Étape 3 : Renseigner un titre clair et explicite
  * Importance du titre pour la recherche
  * Exemples de bons vs mauvais titres
- Étape 4 : Rédiger le contenu à partager
  * Utilisation de l'éditeur Mayday
  * Fonctionnalités disponibles (formatage, images, tableaux)

♻️ Création à partir d'un contenu existant
- Cas d'usage : Réutiliser un paragraphe existant
- Étape 1 : Sélectionner le contenu à extraire
  * Types de contenu supportés (texte, tableau, image)
- Étape 2 : Cliquer sur "Transformer en élément transverse"
  * Localisation dans le menu contextuel
- Étape 3 : Donner un titre à l'élément
- Étape 4 : Sélectionner la collection de destination

✨ Bonnes pratiques
- Rédaction : Contenu autonome, éviter références locales
  * Exemple : Ne pas dire "comme mentionné ci-dessus"
  * Rester concis et aller à l'essentiel
- Titrage : Titres descriptifs pour faciliter la recherche
  * Exemple : "Politique de retour" meilleur que "Retours"
```

**Présentez ce plan détaillé** pour tous les articles d'un coup, puis **demandez validation** : "Ces plans détaillés vous conviennent-ils ?"

Attendez la validation. Si l'utilisateur demande des modifications, ajustez les plans et revalidez.

### Étape 5 : Rédaction article par article

Une fois les plans validés, rédigez les articles **un par un** dans l'ordre.

**Processus pour chaque article** :

1. **Rédiger l'article complet** en suivant le plan validé
2. **Sauvegarder dans un fichier markdown** temporaire
3. **Présenter l'article à l'utilisateur** pour feedback
4. **Attendre le feedback** et les corrections
5. **Modifier l'article** selon le feedback
6. **Redemander validation** : "Cet article vous convient-il maintenant ?"
7. **Répéter 5-6** jusqu'à validation finale
8. **Une fois validé** : Rappeler le plan global et passer à l'article suivant

**Important** : Ne passez à l'article suivant que lorsque l'article en cours est **complètement validé** par l'utilisateur.

**Rappel du plan** : Après validation de chaque article, rappelez le plan global avec indication de la progression :

```
✅ Article 1 : Introduction aux éléments transverses [VALIDÉ]
✅ Article 2 : Comment créer un élément transverse [VALIDÉ]
⏳ Article 3 : Comment insérer un élément transverse [EN COURS]
⬜ Article 4 : Comment gérer et maintenir un élément transverse
⬜ Article 5 : Comment suivre l'utilisation d'un élément transverse
⬜ Article 6 : Comment gérer le multilingue avec les éléments transverses
```

### Étape 6 : Génération du fichier consolidé

Une fois **tous les articles validés**, générez un **fichier markdown consolidé** contenant tous les articles dans l'ordre.

**Format du fichier consolidé** :

```markdown
# Documentation Mayday : [Nom de la feature]

---

## Article 1 : [Titre]

[Contenu complet de l'article 1]

---

## Article 2 : [Titre]

[Contenu complet de l'article 2]

---

[... etc pour tous les articles]
```

Sauvegardez ce fichier dans le dossier de travail de l'utilisateur et donnez le lien computer:// à l'utilisateur.

## Règles de style Mayday

Tous les articles doivent respecter ces règles impérativement :

### Langue et ton

- **Langue** : Toujours en français
- **Tutoiement/Vouvoiement** : Toujours vouvoyer ("vous")
- **Ton** : Chaleureux, accessible, encourageant
- **Emojis** : Obligatoires dans les titres de sections

### Structure obligatoire

Chaque article doit suivre cette structure :

```markdown
👋 Introduction
[Contexte, problème résolu, annonce du contenu]

[Sections métier avec emojis]
[Contenu principal organisé en sections thématiques]

ℹ️ Pour en savoir plus
[Si plusieurs articles : liens vers les autres articles de la série]
```

### Formatage markdown

**Titres et dividers** :
- Mettre un divider (`---`) **sous chaque titre** (H1, H2, H3)
- **Pas de divider au-dessus** des titres
- **Sauter une ligne** entre la dernière ligne d'une section et le prochain titre

**Exemple de formatage correct** :

```markdown
## 🆕 Création à partir de zéro
---

La création d'un élément transverse se fait depuis la bibliothèque d'éléments transverses de Mayday.

Étapes à suivre :
1. Accédez à la bibliothèque
2. Cliquez sur "Ajouter un contenu"

## ♻️ Création à partir d'un contenu existant
---

Vous avez déjà rédigé un excellent paragraphe dans un article et souhaitez le réutiliser ailleurs ?
```

**Prose vs Bullets** :
- **Préférer la prose** pour les explications générales
- **Utiliser les bullets** uniquement pour :
  * Listes d'items distincts
  * Étapes numérotées d'un guide pas-à-pas
  * Points de bonnes pratiques
- **Éviter les bullets excessifs** : Si possible, intégrer dans des paragraphes fluides

**Exemple - MAUVAIS (trop de bullets)** :

```markdown
Les éléments transverses sont particulièrement utiles pour :
- Centraliser des informations communes
  - Politiques d'entreprise
  - Disclaimers légaux
  - Coordonnées de contact
- Maintenir des procédures transverses
  - Procédures d'escalade
  - Étapes de dépannage
```

**Exemple - BON (prose + bullets judicieux)** :

```markdown
Les éléments transverses sont particulièrement utiles pour centraliser des informations communes (politiques d'entreprise, disclaimers légaux, coordonnées de contact) et maintenir des procédures transverses utilisées dans plusieurs contextes.

**Exemples concrets** :
- Politique de retour : Créez-la une fois, insérez-la dans 15 articles. Une modification met à jour les 15 instantanément ✨
- Procédure d'escalade : Synchronisée automatiquement dans tous les guides support
```

### Emojis dans les titres

**Obligatoires** pour tous les titres de sections. Choisissez des emojis pertinents et cohérents.

**Exemples d'emojis par type de section** :

- Introduction : 👋
- Qu'est-ce que : ❓
- Comment ça marche : 🤔
- Nouveau/Création : 🆕
- Réutilisation : ♻️
- Bonnes pratiques : ✨
- Cas d'usage : 🎯
- Accessibilité/Sécurité : 🔐
- Identification visuelle : 🔵
- Synchronisation : 🔄
- Information : ℹ️
- Attention/Important : ⚠️
- Recherche/Trouver : 🔍
- Gestion/Administration : ⚙️

### Callouts et encadrés

Utilisez des callouts pour les informations importantes :

**Info/Note** :
```markdown
ℹ️ **Bon à savoir** : Les modifications sont enregistrées automatiquement.
```

**Attention/Warning** :
```markdown
⚠️ **Point critique** : Lors de l'insertion, vous devez sélectionner manuellement la bonne version linguistique.
```

**Astuce/Tip** :
```markdown
💡 **Astuce** : Utilisez Ctrl+clic (Cmd+clic sur Mac) pour ouvrir un article dans un nouvel onglet.
```

### Exemples concrets

Incluez toujours des exemples concrets et réalistes pour illustrer les concepts abstraits.

**Exemple - MAUVAIS (abstrait)** :
```markdown
Les éléments transverses sont utiles pour centraliser du contenu.
```

**Exemple - BON (concret)** :
```markdown
**Exemple** : Votre politique de retour apparaît dans 15 articles. Créez-la une fois comme élément transverse et insérez-la partout. Lorsque la politique change, une seule modification met à jour les 15 articles instantanément. ✨
```

### Liens "Pour en savoir plus"

Si vous créez plusieurs articles sur une même feature, ajoutez une section finale avec liens vers les autres articles :

```markdown
ℹ️ Pour en savoir plus, consultez la documentation dédiée aux éléments transverses :
- Article 1 : Introduction aux éléments transverses
- Article 2 : Comment créer un élément transverse
- Article 3 : Comment insérer un élément transverse
- Article 4 : Comment gérer et maintenir un élément transverse
- Article 5 : Comment suivre l'utilisation d'un élément transverse
- Article 6 : Comment gérer le multilingue avec les éléments transverses
```

**Note** : Laissez les liens vides (pas d'URLs) - ils seront ajoutés par l'équipe Mayday lors de la publication.

## Exemples de référence

Pour vous inspirer du style Mayday, consultez les exemples de référence :

- `references/example_article_1_introduction.md` : Exemple d'article d'introduction
- `references/example_article_2_howto.md` : Exemple d'article "Comment faire"

Ces exemples montrent le ton, la structure, et le formatage attendus.

## Checklist finale

Avant de présenter chaque article à l'utilisateur, vérifiez :

✅ **Wording** : Tous les termes validés sont utilisés correctement
✅ **Structure** : Introduction + Sections métier + Pour en savoir plus
✅ **Emojis** : Présents dans tous les titres de sections
✅ **Dividers** : `---` sous chaque titre (H1, H2, H3)
✅ **Espacement** : Ligne vide entre section et prochain titre
✅ **Ton** : Vouvoiement, chaleureux, accessible
✅ **Prose** : Préférée aux bullets excessifs
✅ **Exemples** : Concrets et réalistes
✅ **Callouts** : Utilisés pour les points importants
✅ **Langue** : 100% français

## Template de démarrage

Lorsque l'utilisateur active ce skill, commencez par :

```
👋 Bonjour ! Je vais vous aider à créer la documentation Mayday pour votre feature.

Pour commencer, j'ai besoin de trois documents :
1. **Product brief** : Description de la feature, contexte, objectifs
2. **Success toolkit** : Guide d'utilisation, cas d'usage, bonnes pratiques
3. **Board d'user stories** : Stories techniques, acceptance criteria

Pouvez-vous me fournir ces documents ? (PDF, Markdown, liens Notion, Google Docs acceptés)
```

## Gestion des cas particuliers

### Feature très simple (1 seul article)

Si la feature est simple et ne nécessite qu'un seul article, suivez quand même le processus :
1. Validation du wording
2. Proposition de structure (1 article)
3. Plan détaillé
4. Rédaction avec feedback
5. Fichier consolidé (même s'il ne contient qu'un article)

### Feature très complexe (>6 articles)

Si la feature nécessite plus de 6 articles, proposez une organisation en "groupes thématiques" :

```
STRUCTURE PROPOSÉE : 8 articles

Groupe "Introduction et concepts"
- Article 1 : Introduction
- Article 2 : Concepts clés

Groupe "Utilisation"
- Article 3 : Créer
- Article 4 : Insérer
- Article 5 : Modifier
- Article 6 : Supprimer

Groupe "Cas avancés"
- Article 7 : Multilingue
- Article 8 : Permissions
```

### Actualisation de documentation existante

Si l'utilisateur demande de mettre à jour de la doc existante :
1. Demandez la documentation actuelle
2. Identifiez les sections à modifier/ajouter
3. Suivez le même workflow mais en mode "update" plutôt que "création"
4. Générez un fichier consolidé avec les modifications en surbrillance (ou commentaires)

## Ressources

### references/

- `example_article_1_introduction.md` : Exemple complet d'article d'introduction
- `example_article_2_howto.md` : Exemple complet d'article "Comment faire"
