# Git Kata: balisage des commits
## Installer:

1. Exécutez `source setup.sh` (ou`.\setup.ps1` dans PowerShell)

## Motivation

Les [Tags] (https://git-scm.com/book/en/v2/Git-Basics-Tagging) sont pratiques pour
garder une trace des commits référants un numéro de version. Une façon de les utiliser est
avec les branches, où nous pouvons marquer les commits dans une branche s'ils changent le
numéro de version, par exemple, une branche appelée `version/1.1` peut avoir les tags `1.1.1`,
`1.1.2` etc. Les tags peuvent également être utilisées sans branches.

Il existe deux types de tags, les tags annotées et les tags non annotées. tags annotées
peuvent contenir des informations supplémentaires, c'est-à-dire que vous pouvez ajouter un message de journal, en plus du nom. Outre les tags annotées, vous pouvez créer des tags non annotées
qui ont juste le nom. Dans certains cas, les tags sans annotations fonctionnent bien,
car le nom de la tag et les modifications du commit contiennent les informations nécessaires.

## La tâche

Pour plus de simplicité, nous travaillerons simplement avec la branche master. Un couple
des tags sont déjà créées.

1. Vérifiez les tags créées.
2. Effectuez un nouveau commit et introduisez une nouvelle tag annotée.
3. Nous avons fait quelques commits. Pouvez-vous ajouter une tag à un commit arbitraire?
4. Le référentiel d'exercices contient une tag annotée. Quel est le message?
5. Peut-être que toutes les tags ne sont pas nécessaires. Supprimez certains d'entre eux.

## Commandes utiles
- `git tag`
- `git tag -d <tag>`
- `git tag --list <modèle>`
- `git push --tags <branch>`
- `git rev-parse <tag>`
- `git show`
