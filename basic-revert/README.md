# Git Kata: retour de base
## Installer:

1. Exécutez `source setup.sh` (ou`.\setup.ps1` dans PowerShell)

## La tâche

Dans cette tâche, quelques changements se sont introduits, que nous aimerions éliminer. Notre historique est publique, nous ne pouvons donc pas simplement la changer. Nous devons plutôt utiliser revert pour supprimer les modifications indésirables de manière sûre.

1. Utilisez `git log --decorate --oneline` pour consulter l'historique
2. Utilisez `cat` pour afficher le contenu de `greetings.txt`
3. Utilisez `git revert` sur le dernier commit, pour supprimer les changements du dernier commit ajouté
4. Utilisez `git log --decorate --oneline` pour afficher l'historique
5. La commande revert a-t-elle ajouté ou supprimé un commit?
6. Utilisez `cat` pour afficher le contenu de `greetings.txt`
7. Utilisez `ls` pour voir le contenu de l'espace de travail
8. Utilisez `git log --decorate --oneline` pour trouver le SHA du commit qui ajoute les informations d'identification au référentiel
9. Utilisez `git revert` pour annuler la validation qui a ajouté les informations d'identification
10. Utilisez `git log --decorate --oneline` pour afficher l'historique
11. Utilisez `ls` pour voir le contenu de l'espace de travail
12. Combien de commits ont été ajoutés ou modifiés lors du dernier retour?
13. Utilisez `git show` avec le SHA du commit que vous avez rétabli pour voir que le fichier d'identifiants est toujours dans l'historique


## Commandes utiles
- `git revert <ref>`
- `git log --decorate --oneline`
- `git show <ref>`
