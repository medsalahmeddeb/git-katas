# Git Kata: Merge Mergesort
Dans ce kata, vous serez confronté à votre premier conflit de fusion!
Il y aura deux branches différentes:

* Mergesort-Impl
* master

La tâche consiste à examiner le conflit de fusion et à le résoudre en modifiant le fichier en conséquence.

## Installer:

1. Exécutez `source setup.sh` (ou `.\setup.ps1` dans PowerShell)

## La tâche

1. Exécutez `git branch` pour voir les deux branches présentes
2. Fusionnez `Mergesort-Impl` dans `master`
3. Soit:
    1. Résolvez le conflit de fusion avec votre éditeur préféré et terminez la fusion (`git status` vous dira quoi faire), **ou**
    2. Utilisez `git mergetool --tool=emerge` (pour les fans emacs) ou` git mergetool --tool=vimdiff` (pour les fans de vim) et terminez la fusion (`git status` vous dira quoi faire)

## Commandes pertinentes
- `git branch`
- `git merge`
- `git status`
- `git mergetool --tool = emerge`
- `git mergetool --tool = vimdiff`
- `git add`
- `git commit`
