# Git kata: Commit sur la mauvaise branche II

## L'historique

Vous développez une nouvelle fonctionnalité sur la branche «new-feature».implémenté la première partie d'une fonctionnalité, lorsque vous êtes averti d'un bug qui doit être corrigé tout de suite sur la branche `master`.

Après la correction du bogue, vous continuez à travailler sur la new-feature.
après avoir commité la deuxième partie de la fonctionnalité, vous vous rendez compte que vous avez fait votre commit sur la branche `master` au lieu de la branche de new-feature.

## Installer:

1. Exécutez `source setup.sh` (ou`.\setup.ps1` dans PowerShell)

## La tâche

1. Déplacez le commit défectueux de la branche `master` vers la branche` new-feature`.
2. Comment apporteriez-vous également la correction de bogue à votre branche new-feature?

## Commandes utiles

* `git reset HEAD~1` pour déplacer la branche actuelle d'un pas en arrière. Cela a pour conséquence de _supprimer_ le dernier commit d'une branche
* `git stash` pour enregistrer temporairement vos modifications afin de pouvoir changer de branche
* `git cherry-pick` pour ajouter le changeset du commit sur la branche actuelle
