# Git Kata: cherry-pick

Dans cette tâche, nous voulons avoir deux branches, master et feature. Nous avons travaillé et progressé sur les deux branches séparément. Cependant, il y a quelques changements sur la branche de feature que nous voulons prendre et ajouter à la branche master. Sans obtenir l'intégralité de l'ensemble de modifications de la branche de feature.

Git a des fonctionnalités pour "prendre-juste-ces-changements" et cela s'appelle "cherry-pick".
Vous indiquez à Git quels commits vous souhaitez sélectionner et Git ajoutera ces commits à l'historique des commits de votre branche.

Git peut choisir un seul commit ou une plage de commits dans une branche.

## Installer:

1. Exécutez `source setup.sh` (ou`.\setup.ps1` dans PowerShell)

## La tâche


Nous avons actuellement cet historique git dans notre repo exercice:

    A - B - C - D           master
          \
            E - F - G - H   feature

Comme vous pouvez le voir, la branche `feature` et la branche `master` ont progressé avec des commits différents. Nous voulons sélectionner les commits F et G et les ajouter à la branche master, de sorte que notre historique Git ressemble à ceci:

    A - B - C - D - F - G master
          \
            E - F - G - H feature

1. Utilisez `git log --decorate --oneline --graph --all` pour consulter l'historique
2. Utilisez `cat` pour afficher le contenu de `names.txt`. Ce fichier est modifié dans le commit F
3. Utilisez `cat` pour afficher le contenu de `sentence.txt`. Ce fichier est modifié dans le commit G
4. Utilisez `git cherry-pick <commit_hash_F>` pour sélectionner uniquement le commit F sur votre branche
5. Utilisez `git log --decorate --oneline` pour voir la modification de l'historique et ce commit F devrait maintenant être le dernier commit sur la branche master
6. Utilisez `cat` pour voir le contenu de `names.txt` regardez comment il a maintenant changé!
7. Utilisez `git reset --hard HEAD^` pour supprimer cette cherry-pick de l'historique afin que nous puissions maintenant réessayer et choisir une plage de commits
8. Utilisez `git log --decorate --oneline --graph --onelinecoda` pour vérifier que le commit cherry pick est maintenant supprimé de la branche
9. Nous sommes maintenant essentiellement revenus à notre point de départ, utilisez maintenant `git cherry-pick <commit_hash_F> ^ .. <commit_hash_G>` pour sélectionner la plage de commits de F à G (les deux commits). Faites très attention et n'oubliez pas le symbole `^` après le premier hash de commit (voir la section *Remarque utile* ci-dessous pour comprendre pourquoi cela est nécessaire)
10. Utilisez `git log --decorate --oneline --graph --oneline` pour afficher l'historique
11. Utilisez `cat` pour voir le contenu de `names.txt` et `sentence.txt` voir comment ils ont changé!
12. Combien de commits ont été ajoutés en raison du cherry-pick?

## Remarque utile

Lors de l'utilisation d'une plage de commmits avec la commande cherry pick, le premier hash de commit spécifié pour le plus ancien (côté gauche de la plage) n'est pas réellement inclus dans le choix de cherry-pick, ce commit est exclu mais tous les autres entre et y compris le dernier commit sont inclus.

Donc, pour contourner ce problème, il est utile d'utiliser le signe `^` après le premier hash de commit pour dire à Git que vous voulez le commit AVANT ce commit, donc l'inclure dans le processus de sélection de cerise.

Par exemple

    git cherry-pick ABCD..EFGH

n'inclurait pas le commit ABCD, à la place vous devriez ajouter un symbole caret à la fin de l'ABCD pour dire à git de l'inclure, comme ceci:

    git cherry-pick ABCD^..EFGH

Référence: https://www.tollmanz.com/git-cherry-pick-range/
Référence: https://git-scm.com/docs/git-cherry-pick

## Commandes utiles
- `git cherry-pick <ref>`
- `git reset --hard <ref>`
- `git log --decorate --oneline --graph --all`
