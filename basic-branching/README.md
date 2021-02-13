# Git Kata: branchement de base
## Installer:

1. Exécutez `source setup.sh` (ou`.\setup.ps1` dans PowerShell)

## La tâche
Vous êtes à nouveau dans votre propre branche, cette fois nous allons faire un peu de jonglage avec les branches, pour montrer à quel point les branches sont légères dans git.
Astuce: `git checkout` vous fera passer d'une branche à une autre.

1. Utilisez `git branch` pour voir les deux branches de base de cet exercice

2. Dans quelle branche êtes-vous?

3. Utilisez `git branch mybranch` pour créer une nouvelle branche appelée _mybranch_

4. Utilisez à nouveau `git branch` pour voir la nouvelle branche créée.

5. Utilisez `git checkout mybranch` pour passer à votre nouvelle branche.

6. Comment la sortie de `git status` change-t-elle lorsque vous basculez entre _master_ et la nouvelle branche que vous avez créée?

7. Comment l'espace de travail change-t-il lorsque vous passez d'une branche à l'autre?

8. Assurez-vous que vous êtes sur votre branche _mybranch_ avant de continuer.

9. Créez un fichier appelé `file1.txt` avec votre nom.

10. `add` le fichier et `commit` ce changement.

11. Utilisez `git log --oneline --graph` pour voir votre branche pointant vers le nouveau commit.

12. Revenez à la branche appelée _master_.

13. Utilisez `git log --oneline --graph` et remarquez comment le commit que vous avez fait sur la branche _mybranch_ est manquant dans la branche _master_.

14. Créez un nouveau fichier appelé `file2.txt` et commitez ce fichier.

15. Utilisez `git log --oneline --graph --all` pour voir votre branche pointant vers le nouveau commit, et que les deux branches ont maintenant des commits différents sur elles.

16. Basculez vers votre branche _mybranch_.

17. Qu'est-il arrivé à votre répertoire de travail? Pouvez-vous voir votre `file2.txt`?

18. Utilisez `git diff mybranch master` pour voir la différence entre les deux branches.

## Commandes utiles
- `git checkout`
- `git checkout -b`
- `git log --oneline --graph`
- `git branch`
- `git diff`
