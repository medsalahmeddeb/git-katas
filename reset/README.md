# Git katas: réinitialisation de Git
Nous pouvons très bien manipuler l'Historique. Nous ne devrions jamais  bricoler que notre historique locale. En tant que release publique, les commits doivent être immuables.

Nous utilisons la **reset** pour annuler le changement, mais nous pouvons également faire beaucoup plus de choses différentes.

## Installer

1. Exécutez `source setup.sh` (ou`.\setup.ps1` dans PowerShell)

## Tâche

1. À quoi ressemble votre répertoire de travail?
2. À quoi ressemble votre journal? À quoi ressemble votre stage?
3. Essayez d'exécuter `git reset --soft HEAD ~ 1`
4. Qu'arrive-t-il à votre répertoire de travail, à votre journal et à votre stage?
5. Exécutez `git reset --mixed HEAD ~ 1`
6. Qu'arrive-t-il à votre répertoire de travail, à votre journal et à votre stage?
7. Exécutez `git reset --hard HEAD ~ 1`
8. Qu'arrive-t-il à votre répertoire de travail, à votre journal et à votre stage?
9. Essayez maintenant d'utiliser `git revert HEAD ~ 1`
10. Qu'arrive-t-il à votre répertoire de travail, à votre journal et à votre stage?

## Commandes utiles

- `git log --oneline`
- `git commit --amend`
- `git status`
- `git reset --soft`
- `git reset --mixed`
- `git reset --hard`
- `git revert`

## Plus d'explications

Ce qui suit est tiré de la section Recap de [https://git-scm.com/book/en/v2/Git-Tools-Reset-Demystified].
La commande reset écrase ces trois arborescences dans un ordre spécifique, s'arrêtant lorsque vous lui demandez:
1. Déplacez ce que pointe la branche HEAD (arrêtez-vous ici si --soft)
2. Faites ressembler la stage à HEAD (arrêtez ici à moins que --hard)
3. Faire ressembler le répertoire de travail à la stage
