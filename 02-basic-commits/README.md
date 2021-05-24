# Git Kata: Commits de base
Ce kata vous présentera les commandes `git add` et` git commit`.

Vous pouvez regarder au bas de ce fichier, si vous n'avez pas encore effectué la configuration de base de git.

## Installer:

1. Exécutez `source setup.sh` (ou`.\setup.ps1` dans PowerShell)

## La tâche

1. Utilisez `git status` pour voir dans quelle branche vous vous trouvez.
2. À quoi ressemble `git log`?
3. Créez un fichier
4. À quoi ressemble la sortie de `git status` maintenant?
5. `ajouter` le fichier à la zone de préparation (staging area)
6. À quoi ressemble `git status` maintenant?
7. `commit` le fichier dans le référentiel
8. À quoi ressemble `git status` maintenant?
9. Modifiez le contenu du fichier que vous avez créé précédemment
10. À quoi ressemble `git status` maintenant?
11. `ajouter` le changement de fichier
12. À quoi ressemble `git status` maintenant?
13. Modifiez à nouveau le fichier
14. Faites un `commit`
15. À quoi ressemble le «statut» maintenant? Le `journal`?
16. Ajouter et valider la dernière modification

## Commandes utiles
- `git add`
- `git commit`
- `git commit -m" Mon message de commit "`
- `git log`
- `git log -n 5`
- `git log --oneline`
- `git log --oneline --graph`
- `touch filename` pour créer un fichier (ou `sc filename ''` dans PowerShell)
- `echo content > file` pour écraser le fichier avec le contenu (ou `sc filename 'content'` dans PowerShell)
- `echo content >> file` pour ajouter le fichier avec le contenu (ou` ac filename 'content'` dans PowerShell)


## Configuration initiale de Git
1. `git config --global user.name" John Doe "`
1. `git config --global user.email" johndoe @ example.com`

Pour le vim effrayé:
- `git config --global core.editor nano`

Pour les fenêtres peeps:
- `git config --global core.editor notepad`

Autres options de l'éditeur:
- `git config --global core.editor" atom --wait "`
- `git config --global core.editor" code --wait "`
- `git config --global core.editor" 'C:/Program Files/Notepad ++/notepad ++. exe' -multiInst "`
