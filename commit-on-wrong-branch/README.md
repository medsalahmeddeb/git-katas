# Commit sur mauvaise branche
## Installer:

1. Exécutez `source setup.sh` (ou`.\setup.ps1` dans PowerShell)

## Kata 5: Commit sur une mauvaise branche

Vous travaillez très dur sur la branche master.
Une partie de votre travail est déjà commitée. C'est alors que votre patron arrive avec une demande urgente.

Vous sauvegardez un commit et démarrez une nouvelle branche nommée 'quickfix'. Vous faites ce que votre patron veut et vous commitez les changements dans cette nouvelle branche.

C'est là que vous réalisez que vous avez créé un petit désordre avec vos branches.

Actuellement, vos commits ressemblent à ceci
```
         master
           |
           v
   A <---- B
   ^ \
   |  \--- C
remote     ^
           |
        quickfix
```
Mais vous voulez que cela ressemble à ceci:
```
         remote
           |
           v
   A <---- C <---- B
                   ^
                   |
                  HEAD
```


Allez-y!

Remarque: puisque le B dans la structure courante et dans la structure cible n'a pas le même parent, il ne peut pas être littéralement le même commit.

## La tâche

1. Utilisez `git log --oneline --graph --all` pour afficher toutes les branches et leurs commits.
2. Copiez C sur le master avant B en rebasant quickfix sur le master.
3. Faites une nouvelle branche **changes-including-B** de notre master afin que nous puissions continuer à travailler sur B.
4. Réinitialisez HEAD du master sur C.
5. Supprimez la branche quickfix.
6. ~~Push master~~. Vous ne pouvez pas faire cela dans l'exercice d'entraînement.
7. Vous pouvez fusionner la branche **changes-including-B** dans master et supprimer **changes-including-B** ou simplement checkout **changes-including-B** et y travailler.

## Commandes utiles
- `git log --oneline --graph --all`
- `git checkout <branch-name>`
- `git rebase <branch-name>`
- `git branch <branch-name>`
- `git reset --soft HEAD ~`
- `git branch -d <branch-name>`
- `git merge <branch-name>`
