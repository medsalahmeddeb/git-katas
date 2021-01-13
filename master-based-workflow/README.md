# Flux de travail basé sur le master

Dans ce kata, nous allons pratiquer le workflow communément appelé "workflow basé sur le master". Il est parfois appelé flux de travail centralisé ou flux de travail simplifié. La collaboration fonctionne en poussant vers et en tirant de la branche master. Ce flux de travail convient aux projets simples ou aux projets solo.

Nous travaillerons avec un faux dépôt distant, qui sert de support à celui hébergé par un service comme GitHub ou Bitbucket.

## Installer

Exécutez `source setup.sh` (ou`.\setup.ps1` dans PowerShell) pour configurer l'exercice.

## Tâche

1. Obtenez une instance locale du remote en exécutant la commande `git clone fake-remote-repository local-repo`
2. Passez au référentiel local avec la commande `cd local-repo`
3. Ajoutez une ligne de texte à `README.md`
4. Validez le changement
5. Exécutez `git status` et notez comment votre branche master locale est liée à la branche master distante
6. Envoyez la modification à remote en utilisant la commande `git push`
7. Exécutez `git status` pour voir que vous êtes à jour
8. Ajoutez une autre ligne de texte à `README.md`
9. Validez le changement
10. Exécutez la commande `../ fitzgerald-pushes-before-we-do.sh` (ou` ..\fitzgerald-pushes-before-we-do.ps1` dans PowerShell) pour simuler un collaborateur apportant des modifications au fake-remote
11. Poussez votre changement. Notez qu'ils sont rejetés par remote
12. Exécutez la commande `git fetch` pour récupérer les modifications de fake-remote
13. Exécutez `git status` pour voir comment votre branche `master` et la branche distante `master` ont divergé
14. Exécutez `git merge origin/master` pour appliquer les modifications de fake-remote à votre branche master
15. Exécutez `git status` pour voir comment les branches master locales et distantes sont liées
16. Exécutez `git log --all --oneline --decorate --graph` pour voir le commit de fusion sur la branche master
17. Exécutez `git push` pour fournir vos modifications à fake-remote
18. Exécutez `git status` pour voir que votre branche `master` est à jour et n'a pas de modifications non livrées

## Commandes pertinentes

- `git push`
- `git fetch`
- `git merge`
- `git log --oneline --decorate --graph --all`
- `git clone`
