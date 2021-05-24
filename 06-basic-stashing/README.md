# Git Kata: stockage basique

## Installer:

1. Exécutez `source setup.sh` (ou`.\setup.ps1` dans PowerShell)

## La tâche

Vous travaillez sur votre projet. Vous avez mis en stage des travaux mais il-y-a des travaux non mis également.
Soudainement, vous êtes informé qu'un bug est arrivé en production. Vous allez cacher votre travail, corriger le bogue et revenir à votre travail d'origine.

1. Explorez le repo
   1. Quel travail avez-vous dans le répertoire de travail?
   2. Quel travail avez-vous mis en stage?
   3. À quoi ressemble le journal de commits?
   > * Notez que file.txt a des changements dans le stage (changements dans l'index) et des changements pas dans le stage (changements dans le répertoire de travail) *
2. Utilisez `git stash` pour cacher votre travail actuel.
   1. Maintenant, quel travail avez-vous dans le répertoire de travail?
   2. Quel travail avez-vous mis en stage?
   3. À quoi ressemble le journal des commits?
   4. À quoi ressemble la liste de stash?
3. Corrigez les fautes de frappe dans bug.txt sur master et validez vos modifications.
4. Maintenant, pour revenir à votre travail, appliquez le stash à master.
   1. Quel travail avez-vous dans le répertoire de travail?
   2. Quel travail avez-vous mis en stage?
   > * Oups. Tous nos changements ne sont pas mis en stage maintenant. Cela peut être indésirable et inattendu *
5. Annulez vos modifications avec `git reset --hard HEAD`. Il s'agit d'une commande non sécurisée car elle supprimera définitivement les fichiers de votre index et de votre répertoire de travail, mais nos modifications sont stockées en toute sécurité, donc tout va bien. Consultez le kata [reset] (reset/README.md) si vous n'êtes pas sûr de ce qui se passe ici.
6. Appliquez le stash à master avec l'option `--index`.
   1. Quel travail avez-vous dans le répertoire de travail?
   2. Quel travail avez-vous mis en stage?
   > * Ok, revenons là où nous étions! *
7. Nous n'aurons plus besoin du stash. Supprimez le.
   1. À quoi ressemble la liste des réserves?
   2. À quoi ressemble le journal de validation?



## Commandes utiles

- `git status`
- `git status -s`
- `git diff`
- `git diff master`
- `git stash`
- `git stash list`
- `git stash apply`
- `git stash apply --index`
- `git stash drop`
- `git log --oneline --all --graph`
- `git commit`
- `git add`
