# Git Kata: fusion rapide
## Installer:

Exécutez `source setup.sh` (ou`.\setup.ps1` dans PowerShell)


## La tâche

Vous êtes à nouveau dans votre propre branche, cette fois nous allons faire un peu de jonglage avec les branches, pour montrer à quel point les branches sont légères dans git.

1. Créez une branche feature appelée FEATURE en majuscule

2. Découvrez la branche

3. Quelle est la sortie de `git status`?

4. Modifiez le message de greeting.txt pour qu'il contienne un message d'accueil en majuscules

5. Ajoutez les fichiers greeting.txt à la zone de staging et validez

6. Quelle est la sortie de `git branch`?

7. Quelle est la sortie de `git log --oneline --graph --all`

* N'oubliez pas: vous voulez insérer le commit sur la branche FEATURE dans master. La commande 'git merge [nom de la branche]' prend la branche, qui contient les commits, comme argument. Les commits sont appliqués à la branche pointée par HEAD (branche actuelle). *

8. Allez dans la branche «master»

9. Utilisez `cat` pour voir le contenu de greeting.txt

10. Diff des branches

11. Fusionner les branches

12. Utilisez `cat` pour voir le contenu de greeting.txt

13. Supprimez la branche en majuscule


## Commandes utiles
- `git branch`
- `git branch <branch-name>`
- `git branch -d <branch-name>`
- `git checkout`
- `git branch -v`
- `git add`
- `git commit`
- `git commit -m`
- `git merge <branch>`
- `git diff <branchA> <branchB>`
- `git log --oneline --graph --all`
