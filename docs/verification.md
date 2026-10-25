# Vérification technique — 25 octobre 2026

- `npm run build` : compilation de production réussie après les derniers changements.
- `curl -I http://127.0.0.1:5173` : HTTP 200.
- Navigateur intégré : création du ticket PIL-009 « Préparer les croquis papier », assignation à Sarah, changement vers À valider, ajout d’un commentaire.
- Recherche « croquis » dans la vue liste : seul PIL-009 retourné.
- Rechargement : nouveau ticket et compte total conservés; état et commentaire enregistrés dans les données locales.
- Filtres Sarah + priorité Haute : état sans résultat; réinitialisation rétablit le tableau.
- Présentation étroite inspectée visuellement; texte secondaire renforcé après inspection.

Limites : pas de test utilisateur réalisé, pas d’audit d’accessibilité exhaustif, pas de validation visuelle grand écran dans la fenêtre de navigateur disponible. Glisser-déposer et téléchargement JSON implémentés mais non exécutés pendant cette vérification. Changement d’état par sélecteur testé. Le ticket créé pendant la vérification reste disponible dans le navigateur de démonstration; le jeu initial dans le code contient huit tickets.

## Révision 2 — interface sombre avec une seule pile active

- Compilation de production réussie après la refonte.
- Navigateur : feuilletage suivant (PIL-003 vers PIL-004), déplacement vers En cours avec mise à jour des compteurs, annulation avec rétablissement de l’état initial.
- Changement de pile vers En cours : bonne carte et action contextuelle « Demander une validation ».
- Formulaire simplifié ouvert : titre, description facultative, responsable et pile.
- Aperçu étroit inspecté : navigation par petites piles, une carte active, boutons accessibles. Correction du texte de pagination sur téléphone et du nom accessible du bouton Nouveau ticket.
- Données existantes conservées. Les anciennes notes sur la liste, les filtres, l’export et le glisser-déposer décrivent la version 1; ces commandes ont été retirées de l’interface actuelle.
- Aucun test utilisateur; vérification visuelle grand écran et audit d’accessibilité exhaustif toujours à effectuer.

## Sous-tâches et historique

- Compilation de production réussie.
- Création de PIL-010 « Regrouper les réponses par thème » depuis PIL-004 : assignation héritée et compteur parent 0/1 vérifiés.
- Ouverture de la fiche enfant et retour au parent via le lien dédié vérifiés.
- Clôture via la case de la sous-tâche : apparition dans l’historique avec date, membre et indication Sous-tâche vérifiée; tickets historiques conservés avec date non enregistrée.
- Historique : affichage global indépendant des filtres des piles. Les tâches rouvertes ne sont pas incluses.

## Types de tickets

- Compilation de production réussie.
- Création de PIL-012 en Epic et affichage du badge vérifiés dans le navigateur.
- Changement vers Feature dans la fiche et mise à jour du badge vérifiés.
- Sélecteurs : huit types et description adaptée au choix; les anciens tickets sont conservés avec un type par défaut.
- Choix du parent exclut le ticket lui-même et ses descendants; création Sous-tâche exige un parent. La hiérarchie reste souple et ne prétend pas reproduire les règles d’une instance Jira.
