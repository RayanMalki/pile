# Pile

Prototype exploratoire d’un outil de tickets en français, réalisé comme référence avant les croquis papier du laboratoire GTI350, automne 2026.

## Démarrer

Node.js 22.12+ ou version récente compatible avec Vite 7.

```sh
npm ci
npm run dev
```

Ouvrir l’adresse indiquée par Vite. `npm run build` compile la production et `npm run preview` permet de la vérifier localement.

## Concept actuel : feuilleter plutôt que surveiller

Interface sombre, sans barre latérale ni tableau en colonnes. Une seule pile active et une seule carte visible à la fois. Quatre petites piles servent de navigation : À faire, En cours, À valider et Terminé. Les flèches permettent de parcourir une pile. Un bouton contextuel fait avancer le ticket à l’étape suivante; une notification permet d’annuler le déplacement.

La carte montre uniquement un identifiant discret, un titre, un responsable et le nombre de commentaires s’il y en a. Les descriptions et discussions sont accessibles en ouvrant la carte. La création demande un titre; description, responsable et état sont facultatifs. Recherche cachée derrière une icône et sélection « Toute l’équipe / Pour moi ».

## Périmètre technique

React, Vite et Lucide. Sauvegarde locale automatique par origine dans localStorage. Les données déjà présentes de la première version sont conservées. Les priorités et étiquettes historiques restent dans les données, mais ne sont plus affichées. Pas de backend, collaboration temps réel, comptes ni service IA. Alex est le membre courant fictif. Le navigateur initialise huit tickets de démonstration si aucun stockage n’existe. Un autre navigateur ou port constitue un stockage distinct.

Polices Google Fonts avec repli système hors ligne. Interface adaptative, libellés d’accessibilité, focus visible et dialogue utilisable au clavier avec fermeture Échap. Aucun audit exhaustif d’accessibilité n’est revendiqué.

## Documents

- `docs/conception.md` : recherche et décisions.
- `docs/laboratoire.md` : exigences et scénarios papier.
- `docs/verification.md` : vérifications techniques et limites.

Le numérique est une exploration, pas un remplacement des croquis individuels, entrevues ou tests papier demandés au laboratoire.

## Sous-tâches et historique

Dans une fiche, saisir un titre sous « Sous-tâches », puis cliquer sur +. Une sous-tâche est un ticket à part entière, assigné initialement au même membre, avec sa propre fiche et son propre état. Le lien « Tâche parent » en haut permet de remonter. Les cases permettent de terminer ou rouvrir les sous-tâches; le parent affiche la progression. Les états parent/enfants restent indépendants.

L’icône d’horloge dans l’en-tête ouvre l’historique de toutes les tâches et sous-tâches actuellement terminées, même hors du filtre « Pour moi ». Recherche par titre, membre ou numéro et ouverture des fiches. Les nouvelles clôtures sont horodatées; les anciennes tâches terminées sans date restent indiquées comme telles. Une tâche rouverte quitte l’historique jusqu’à sa prochaine clôture. Il s’agit d’une liste des tâches terminées, pas d’un journal de toutes les modifications.

## Types de tickets

Epic, Feature, User story, Tâche, Bug, Amélioration, Spike et Sous-tâche sont disponibles à la création et dans les fiches, avec une explication courte. Un badge discret apparaît sur la carte et le type est inclus dans la recherche principale et celle de l’historique. Les anciens tickets sans type explicite sont interprétés comme Tâche (ou Sous-tâche s’ils ont un parent).

Un parent peut être choisi à la création et modifié ensuite. Les liens vers soi-même et ses descendants sont exclus pour éviter les cycles. Une Sous-tâche nécessite un parent; retirer son parent la transforme en Tâche. Les types restent indépendants des quatre états des piles. La hiérarchie est volontairement souple : Epic et Feature n’imposent pas de niveaux ni de clôture automatique des descendants.

Références Atlassian : [types de tickets](https://support.atlassian.com/jira-cloud-administration/docs/what-are-issue-types/) et [hiérarchie configurable](https://support.atlassian.com/jira-cloud-administration/docs/configure-the-issue-type-hierarchy). Feature, Amélioration et Spike sont des choix ajoutés dans Pile; leur disponibilité dans Jira dépend de la configuration, et ils ne constituent pas tous des types universels par défaut.
