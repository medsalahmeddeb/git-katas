# Kata : réorganiser l'historique
Les commits ici ont évidemment été faits par un homme fou.
Malheureusement, ils contiennent en fait des informations utiles - c'est juste que l'historique est étrange.
Vous devriez corriger cela pour que notre `git log` soit superbe!

## Installer

1. Exécutez `source setup.sh` (ou`.\setup.ps1` dans PowerShell)

## Tâche

Réorganisez l'historique de manière à ce que cela ait du sens - ajoutez les fichiers dans l'ordre qui correspond à leur nom.

1. Utilisez `git log --oneline --graph` pour afficher les commits
2. Essayez également `git reflog` pour afficher les commits. `git reflog` est par défaut `git reflog show` et c'est un alias pour `git log -g --abbrev-commit --pretty = oneline`
3. Utilisez `git rebase -i <after-this-commit>` pour réorganiser les commits. Il y a des commentaires dans le fichier que vous éditez qui expliquent les commandes disponibles.
4. Utilisez `git log --oneline --graph` pour afficher le résultat

### commandes utiles

- `git rebase -i <after-this-commit>`
- `git log --oneline --graph`
- `git reflog`
