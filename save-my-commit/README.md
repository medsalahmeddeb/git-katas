# Git Kata: Sauvegarder mon commit

Dans ce dépôt, nous avions ajouté le Saint Grail dans `holygrail.txt`. Malheureusement, nous réinitialisons notre branche `master` au commit initial. Il est maintenant temps de se remettre de l'erreur.

## Installer

1. Exécutez `source setup.sh` (ou`.\setup.ps1` dans PowerShell)

## La tâche

Nous venons de réinitialiser la branche `master` au commit initial. Nous récupérerons le travail perdu.

1. Utilisez `git log` pour voir que l'historique est bref
2. Utilisez `ls` pour vérifier que` holygrail.txt` n'est pas dans l'espace de travail
3. Utilisez `git reflog` pour trouver le commit qui a ajouté` holygrail.txt`
4. Utilisez `git reset --hard` pour récupérer notre historique et notre travail
5. Utilisez `git log` et` ls` pour voir le travail récupéré
6. Annulez votre solution en exécutant `git reset --hard initial-commit`
7. Utilisez `git cherry-pick` pour restaurer` holygrail.txt`
8. Comparez l'historique et l'espace de travail à la solution à l'aide de la réinitialisation
9. Encore une fois, annulez votre solution en utilisant `git reset --hard initial-commit`
10. Forcer le Git garbage collector à s'exécuter avec `git gc`
11. Essayez de restaurer le Saint Grail en utilisant l'une des solutions précédentes

## Commandes git pertinentes
- `git reflog`
- `git cherry-pick`
- `git reset --hard`
- `git log`
