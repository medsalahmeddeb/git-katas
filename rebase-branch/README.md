# Git Kata: rebase de la branche

## Installer:
1. Exécutez `source setup.sh` (ou`.\setup.ps1` dans PowerShell)


## La tâche
Vous êtes à nouveau dans votre propre branche, cette fois nous allons faire un peu de jonglage avec les branches, pour montrer à quel point les branches sont légères dans git.

1. Quelles branches existent?
2. Consultez le journal de la branche master
3. Découvrez la branche uppercase
4. Comparez le journal avec journal de la branche master?
5. Rebase votre branche uppercase avec le master (`git rebase master`)
6. Qu'est-ce qui vient de se passer? Dessine le!
7. Maintenant, vérifiez la branche master
8. Fusionner les uppercases dans le master
9. À quoi ressemble le journal maintenant?

## Commandes utiles
- `git checkout <branch-name>`
- `git rebase <branch-name>`
- `git log --oneline --graph --all`
- `git merge <branch-name>`
