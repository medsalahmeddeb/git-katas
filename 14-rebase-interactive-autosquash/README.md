# Git katas: rebase interactif avec l'option --autosquash
Vous avez travaillé sur une nouvelle fonctionnalité appelée Hello World.
Cette fonctionnalité finit par être complète avec la documentation et le test unitaire, mais il y a une faute de frappe dans la documentation.

Vous devez la réparer puis rebaser pour avoir une belle historique.

Heureusement, nous avons une tag de publication `v0.0` juste avant le démarrage de la fonctionnalité.

Il existe un moyen de le réparer facilement avec des options avancées pour `git commit` et` git rebase`.

## Installer:

1. Exécutez `. setup.sh` (ou `.\setup.ps1` dans PowerShell)

## Tâche

1. Explorez le dépôt et l'historique pour savoir quand le fichier de documentation a été ajouté.
2. Réparez le fichier `README.md` et ajoutez-le.
3. Ajoutez votre commit en utilisant `git commit --fixup=<commit id to be fixed>`.
4. Utilisez `git rebase --autosquash --interactive v0.0` pour afficher la recette de rebase générée automatiquement.
5. Utilisez `git log` pour afficher votre nouvelle belle historique.

### commandes utiles

- `ls -l` # fichiers de liste
- `tail -n +1 *` # affiche le contenu de tous les fichiers
- `git log --oneline` # affiche l'historique
- `git log --stat` # log quels fichiers ont changé
- `git log --patch` # log avec diff
- `git show <commit id>` # affiche les changements d'un commit
- `git add` # ajouter un fichier
- `git commit --fixup=<commit id>` # commit en générant automatiquement le message
- `git rebase -i <ref>` # exécuter le rebase interactif vers <ref> et réorganiser automatiquement les commits
