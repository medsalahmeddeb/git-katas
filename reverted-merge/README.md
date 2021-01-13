# Git Kata: fusion annulée

Dans ce kata, nous explorons les problèmes d'annulation d'un commit de fusion.

## L'historique

Votre équipe utilise cette  bibliothèque-1.2.3 pour son développement, qui est
maintenu par une autre équipe.

À un moment donné, votre équipe intègre une nouvelle version de la bibliothèque-1.2.4. Parce que vous êtes prudent, vous faites cela sur une branche `integrer-library-1.2.4`.

Malheureusement, vous découvrez après votre fusion que la bibliothèque a un bogue qui
doit être réparé par cette autre équipe. Pour éviter que le bogue ne soit diffusé dans
production, vous décidez d'annuler la validation de fusion.

## Installer

1. Exécutez `source setup.sh` (ou`.\setup.ps1` dans PowerShell)

## La tâche

1. Annulez la validation de fusion. Pour résoudre le conflit, vous devez déterminer
les fonctionnalités qui doivent être incluses dans `mymodule.txt`.
   * Vous pouvez dire si la fonctionnalité X doit être incluse ou non au moment où elle l'a été
     commitée.
   * Vous pouvez supposer que la fonctionnalité Y fonctionne également avec l'ancienne version de la bibliothèque.
2. Prenez le rôle de l'équipe de la bibliothèque et corrigez le bogue dans la bibliothèque sur
    la branche de l'intégration, par ex. changez `lib.txt`.
3. Ensuite, nous explorons comment vous pouvez obtenir les modifications de la branche dans le master
   encore. Essayez d'abord de fusionner pour voir ce qui se passe. Le fichier `lib.txt` change comme
       attendu, mais pas «mymodule.txt». Pour une discussion approfondie sur
       la raison consulter ce lien: [Rétablissement d'une fusion défectueuse] (https://github.com/git/git/blob/master/Documentation/howto/revert-a-faulty-merge.txt).
> annulation d'un commit de fusion également
> annule les _data_ que le commit a modifiées, mais il n' a
> aucun effet sur _historique_ que la fusion a eu.
>
> La fusion existera donc toujours, et elle sera toujours considérée comme
> les deux branches ensemble, et les futures fusions verront cette fusion comme
> le dernier état partagé

4. Annulez la fusion avec une réinitialisation --hard
5. Annulez la restauration et réessayez la fusion. Cette fois ça marche.

## Commandes utiles

* `git revert -m 1 <merge-sha1>`
* `git log --oneline --graph --all`
* `git add <nom-fichier>`
* `git revert --continue`
* `git checkout <branch-name>`
* `git merge <branch-name>`
* `git reset --hard <sha1>`
* `git revert <sha1>`
