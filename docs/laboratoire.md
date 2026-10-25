# Repères pour le laboratoire et les croquis

Source : énoncé fourni, GTI350, automne 2026, Lab2 « Prototype papier ». Ce document aide à organiser la suite; ce n’est pas le rapport à remettre.

## Exigences utiles pour une équipe de quatre

- Faire approuver l’application par le chargé de laboratoire.
- Consulter au moins deux utilisateurs externes à l’équipe. Présenter profils, questions et réponses, tâches actuelles et problèmes. Justifier les substituts si nécessaire.
- Choisir au moins trois tâches clés, indiquer fréquence ou importance et décomposer leur déroulement actuel. Ne pas confondre fonctionnalités et tâches.
- Faire individuellement au moins une page de croquis par personne, puis au moins une page collective. Dessins à main levée, sans règle; identifier chaque auteur. L’énoncé autorise un stylet répondant à ses conditions précises.
- Réaliser et justifier un prototype papier/carton plus détaillé; présenter clairement ses transitions.
- Faire tester toutes les tâches clés sur le prototype papier par au moins deux utilisateurs; consigner les observations et changements recommandés.
- Rapport : ordre des sections de l’énoncé, maximum dix pages de texte hors photos/schémas/tableaux/graphiques, police 11, interligne simple, sans couverture ni table des matières. Identification en haut de première page et références.
- Quatre points supplémentaires nécessaires pour obtenir tous les points du volet concerné (20 % du barème).

Exemple de combinaison atteignant quatre points, à réaliser réellement et documenter : trois utilisateurs en entrevue au total (+1), observation de chacun pendant au moins dix minutes (+2), séance de conception participative d’au moins vingt minutes avec dessins sur deux pages et explications demandées (+1). Les trois utilisateurs doivent tous être observés dans cet exemple. Les autres options et détails restent dans l’énoncé.

## Croquis à explorer

Ce prototype est une idée individuelle possible. Préserver l’exploration indépendante des autres membres plutôt que leur demander de copier le même écran.

1. Tableau à quatre piles : titres, compteurs, carte principale, bouton pour déplier.
2. Variante avec une seule pile verticale et des séparateurs d’état.
3. Variante liste compacte : tester si cacher les cartes est réellement utile.
4. Formulaire de création : titre dominant, détails facultatifs.
5. Fiche : titre, état, responsable, description et discussion.
6. État vide, recherche sans résultat et retour après création.

Dessiner d’abord les structures et actions; les couleurs, ombres et polices ne sont pas l’objectif des croquis exploratoires.

## Tâches proposées pour les tests, à confirmer par l’analyse réelle

| Tâche | Scénario donné au participant | Critère observable |
| --- | --- | --- |
| Créer une tâche | « Vous remarquez que le formulaire doit être simplifié. Gardez-en une trace pour votre équipe. » | Un ticket au titre compréhensible existe |
| Confier une tâche | « Sarah s’occupera du formulaire. Faites en sorte que l’équipe le sache. » | Sarah est responsable du bon ticket |
| Suivre l’avancement | « Le formulaire est prêt à être vérifié par un collègue. Actualisez son avancement. » | Le ticket est dans À valider |
| Discuter dans le contexte | « Vous avez une question sur les champs facultatifs. Posez-la là où l’équipe retrouvera le contexte. » | Un commentaire apparaît sur le bon ticket |
| Retrouver une tâche | « Retrouvez les travaux dont Sarah est responsable. » | Repérage des tickets de Sarah |

Ne pas donner les noms de boutons dans les consignes. Noter réussite sans aide, hésitations, erreurs, aide apportée, interprétation des piles et verbalisations. Simuler manuellement les changements d’écrans avec les feuilles/cartes. Demander ensuite ce qui était clair ou ambigu. Aucun résultat utilisateur n’a encore été recueilli par ce projet.

## Écrans et transitions à dessiner

Tableau → création → tableau avec nouveau ticket.
Tableau → pile dépliée → fiche de ticket.
Fiche → choix du responsable → fiche actualisée.
Fiche → choix de l’état → tableau avec ticket déplacé.
Fiche → commentaire → discussion mise à jour.
Tableau → filtres → résultats filtrés / aucun résultat → réinitialisation.

## Vérification technique du prototype

Compilation de production réussie. Les tests interactifs effectués sont consignés dans `verification.md`. Ces vérifications techniques ne remplacent pas les tests utilisateurs du laboratoire.

## Mise à jour pour le concept de piles, version 2

L’interface actuelle ne présente plus quatre colonnes dépliables : dessiner une grande pile centrale et quatre petites piles de navigation. Une carte est visible à la fois. Prévoir les flèches précédente/suivante, la position « N sur M », le bouton pour avancer et sa notification « Annuler ». Les transitions du scénario de recherche passent maintenant par la loupe ou par « Pour moi »; les filtres et la vue liste ont été retirés.
