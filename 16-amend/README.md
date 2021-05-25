# Git kata: modification des commits
Lorsque nous travaillons, nous faisons beaucoup de commits.
Parfois, nous oublions quelque chose évidente que nous voudrions corriger rapidement.

`git commit --amend` nous permet de faire ça - bricoler avec le dernier commit que nous avons fait.

Vous pouvez utiliser `git log -p` ou` git show` pour inspecter le contenu des commits et des modifications de fichier qui ont été ajoutés aux commits.

## Installer:

1. Exécutez `source setup.sh` (ou`.\setup.ps1` dans PowerShell)

## La tâche

1. Que nous dit `git status`?
2. Que nous dit `git log -p`?
3. Ajouter bar.txt dans le stage
4. Exécutez `git commit --amend`
5. Que s'est-il passé? Que nous dit `git log -p`?
6. Que se passe-t-il si vous exécutez à nouveau `git commit --amend`?

## Commandes utiles

- `git add`
- `git log --oneline --graph`
- `git log -p`
- `git show`
- `git commit --amend`
