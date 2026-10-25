# Pile — notes de conception, version exploratoire

## Intention

Pour une petite équipe débutante : savoir quoi faire, qui s’en occupe et ce qui attend un retour. La référence personnelle exprimée par le porteur du projet est Linear. Les piles sont sa proposition de départ, pas un résultat d’étude utilisateur.

## Recherche publique — 25 octobre 2026

Recherche qualitative exploratoire, non représentative. Ces commentaires publics ne remplacent pas les entrevues, réponses au formulaire, observations et tests exigés au laboratoire. Ne pas présenter ces avis comme des réponses de vos utilisateurs.

1. [Discussion r/agile, 22 mai 2025 — frustrations autour de Jira](https://www.reddit.com/r/agile/comments/1kshdkm/whats_the_most_frustrating_part_of_using_jira_or/) : des participants reprochent les nombreux champs imposés pour alimenter des rapports et les processus de suivi perçus comme de la microgestion. Un autre nuance que la complexité vient surtout de l’administration/configuration et qu’un environnement bien configuré peut être simple pour l’utilisateur. Conséquence retenue : un seul champ obligatoire pour créer un ticket; aucun rapport de productivité individuel.
2. [Discussion r/ProductManagement — alternatives à Jira et Confluence](https://www.reddit.com/r/ProductManagement/comments/1nok9of/) : un auteur travaillant en petite équipe décrit trop de réglages inutilisés et des configurations complexes pour des besoins simples. Conséquence retenue : un processus fixe de quatre états et une navigation courte. Ce choix peut devenir une limite pour une équipe plus complexe.
3. [Linear — refonte de l’interface, mars 2024](https://linear.app/changelog/2024-03-20-new-linear-ui) : l’équipe décrit un travail sur la hiérarchie, la densité, le contraste et la réduction du bruit dans les barres latérales, filtres et panneaux. Inspiration : une action principale claire, des propriétés secondaires dans la fiche, une structure visuelle stable.
4. [Documentation Linear](https://linear.app/docs) : gestion des tickets, états, commentaires et vues constituent des références fonctionnelles. Pile réduit volontairement le périmètre aux besoins exprimés; il ne reproduit pas l’ensemble des projets, cycles, intégrations et automatisations.

## Décisions et compromis

| Décision | But | Question à tester |
| --- | --- | --- |
| Une pile par état, une carte visible au repos | Réduire la densité et conserver les quatre étapes visibles | Les personnes comprennent-elles que des cartes sont cachées ? |
| Compteur et bouton « Voir les N tickets » | Rendre le contenu caché découvrable | Cherchent-elles spontanément le bouton ? |
| Vue liste alternative | Aider au repérage global de tous les titres | La préfèrent-elles aux piles ? |
| Un titre suffit pour créer | Réduire la saisie initiale et faciliter un premier usage | Le manque de contexte crée-t-il des retours inutiles ? |
| Un seul responsable par ticket | Clarifier la responsabilité | Les personnes comprennent-elles la différence entre responsable et participants ? |
| Statut textuel, forme et couleur | Ne pas dépendre uniquement de la couleur | Les quatre états sont-ils compris sans explication ? |
| Commentaires dans la fiche | Garder le contexte au même endroit | Les personnes trouvent-elles où poser une question ? |
| Glisser-déposer + sélecteur explicite | Permettre plusieurs façons de changer d’état | Quel mécanisme est découvert en premier ? |

Principes appliqués : visibilité de l’état (compteurs, progression, responsable), reconnaissance plutôt que mémorisation (libellés et actions explicites), divulgation progressive (fiche détaillée et piles dépliables), cohérence (mêmes quatre états partout), contrôle au clavier (focus visible, dialogues, Échap). Les contrastes ont été renforcés lors de la vérification visuelle; aucune certification d’accessibilité complète n’est revendiquée.

## Hypothèses à valider

- Des débutants interprètent « À valider » comme une étape nécessitant le retour d’une autre personne.
- Une carte au-dessus d’une pile fournit assez de contexte pour suivre les travaux.
- L’assignation unique convient aux tâches de la cible.
- Quatre états suffisent à la majorité des tâches observées.
- Le vocabulaire français aide le public visé.

L’IA est une piste future, pas un bouton factice : il faudrait d’abord identifier un besoin concret, par exemple reformuler une description ou résumer une discussion, puis prévoir validation humaine et gestion des données transmises. Aucun appel à une IA dans cette version.

## Réception des réponses Google Forms

À chaque lot reçu : conserver la date et le nombre de réponses, anonymiser les participants, distinguer citation et interprétation, relever tâches actuelles/problèmes/fréquence, puis mettre à jour les hypothèses. Choisir une modification observable, refaire le même scénario et consigner la différence. Ne pas inventer de profils, fréquences ou résultats en attendant.

| Date | Source / participant anonymisé | Observation réelle | Hypothèse affectée | Changement | Résultat du nouveau test |
| --- | --- | --- | --- | --- | --- |
| À compléter | | | | | |

## Révision 2 — retour du porteur du projet

Le premier essai ressemblait encore trop à Jira et affichait trop d’informations. La nouvelle direction remplace totalement le tableau : une seule pile active au centre, des cartes superposées à feuilleter, et quatre petits jeux de cartes pour naviguer entre les étapes. Interface sombre, sans barre latérale, filtres avancés, étiquettes, priorités ni vue liste. Ces descriptions antérieures documentent l’exploration abandonnée.

Le twist : le ticket du dessus devient la seule tâche à lire; une action contextuelle sous la pile le fait avancer et révèle le suivant. L’utilisateur peut annuler ce déplacement. Les détails restent dans une fiche secondaire. Cette proposition réduit la quantité d’information visible mais limite la comparaison simultanée des tickets : tester particulièrement la recherche d’une tâche précise et la compréhension des flèches. La simplicité de cette version n’est pas encore validée par des utilisateurs.
