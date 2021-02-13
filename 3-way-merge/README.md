# Git Kata: Fusion à 3 voies

## Installer

1. Exécutez `source setup.sh` (ou`.\setup.ps1` dans PowerShell)

## La tâche
Vous êtes à nouveau dans votre propre branche, cette fois nous allons faire un peu de jonglage avec les branches, pour montrer à quel point les branches sont légères dans git.

1. Créez une branche appelée greeting et vérifiez-la

2. Modifiez le message de greeting.txt pour qu'il contienne votre message d'accueil préféré

3. Ajoutez les fichiers greeting.txt à la zone de préparation (index)

4. Commitez

5. Revenez à la branche master

6. Créez un fichier README.md avec des informations sur ce référentiel

7. Ajoutez le fichier README.md à l'index et commitez

8. Quelle est la sortie de `git log --oneline --graph --all`?

9. Diff les branches

10. Fusionner la branche greeting dans master

## Commandes utiles
- `git branch`
- `git branch <branch-name>`
- `git branch -d <branch-name>`
- `git checkout <branch-name>`
- `git checkout -b <branch-name>`
- `git branch -v`
- `git add`
- `git commit`
- `git commit -m`
- `git merge <branchA> <branchB>`
- `git diff <branchA> <branchB>`
- `git log --oneline --graph --all`
