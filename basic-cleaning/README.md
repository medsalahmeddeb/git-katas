# Git Kata: nettoyage de base

## Installer:

1. Exécutez `source setup.sh` (ou`.\setup.ps1` dans PowerShell)

## La tâche
Vous travaillez sur un projet qui implique des fichiers générés. Supposons que vous compiliez des fichiers C en fichiers objets. Avant de checkout une nouvelle branche, vous souhaitez nettoyer.

1. Explorez le répertoire avec `ls -R`. Il se trouve beaucoup de choses. Fichiers de code, fichiers temporaires, fichiers objets, .. Nettoyons!
2. Juste pour être sûr, faites un essai à sec et exécutez la commande clean avec l'option `-n`
3. Oh non! il y a un fichier `.c` qui aurait été supprimé!
4. Ajoutez `src/mylib.c` à la zone de préparation. ne le commitez pas.
5. Exécutez la commande clean avec l'option `-n`. Notez que mylib.c ne sera pas supprimé. Notez également que les fichiers du répertoire obj ne sont pas répertoriés
6. Exécutez la commande clean avec l'option `-n -d`.
7. Ça a l'air bien! nettoyer le dépôt `-f -d`

## Commandes utiles
- `git clean -n`
- `git add`
- `git clean -n -d`
- `git clean -f -d`
