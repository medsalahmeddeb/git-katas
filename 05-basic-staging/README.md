# Git Kata: mise en stage de base

Ce kata examinera la zone de **staging** de git.

Dans git, nous travaillons avec trois domaines différents:
* Le répertoire de travail dans lequel vous effectuez vos modifications
* La zone de **staging** (préparation) où toutes les modifications que vous avez ajoutées via `git add` resteront
* Le **repositiory** (référentiel) où chaque commit est ajouté à votre historique. Pour mettre vos modifications le répo, lancez la commande `git commit`.

Un fichier peut avoir des modifications à la fois dans le répertoire de travail et dans la zone de préparation.
Ces changements ne doivent pas nécessairement être les mêmes.

Nous travaillerons également avec `git reset` pour réinitialiser les changements ajoutées d'un fichier et `git checkout` pour ramener un fichier à un état antérieur.

## Installer:

1. Exécutez `source setup.sh` (ou`.\setup.ps1` dans PowerShell)

## La tâche

Vous êtes dans votre propre référentiel. Il existe un fichier appelé `file.txt`.

1. Quel est le contenu de `file.txt`?
2. Remplacez le contenu dans `file.txt`: `echo 2 > file.txt` pour changer l'état de votre fichier dans le répertoire de travail (ou `sc file.txt '2'` dans PowerShell)
3. Que vous dit `git diff`?
4. Que vous dit `git diff --staged`? pourquoi est-ce vide?
5. Exécutez `git add file.txt` pour organiser vos modifications depuis le répertoire de travail.
6. Que vous dit `git diff`?
7. Que vous dit `git diff --staged`?
8. Écrasez le contenu dans `file.txt`: `echo 3 > file.txt` pour changer l'état de votre fichier dans le répertoire de travail (ou `sc file.txt '3'` dans PowerShell).
9. Que vous dit `git diff`?
10. Que vous dit `git diff --staged`?
11. Expliquez ce qui se passe
12. Exécutez `git status` et observez que `file.txt` est présent deux fois dans la sortie.
13. Exécutez `git reset HEAD file.txt` pour annuler la modification
14. Que vous dit `git status` maintenant?
15. Mettez le changement dans le **staging** et commitez
16. Qu'affiche le log?
17. Remplacez le contenu de `file.txt`: `echo 4 > file.txt` (ou `sc file.txt '4'` dans PowerShell)
18. Quel est le contenu de `file.txt`?
19. Que nous dit `git status`?
20. Exécutez `git checkout file.txt`
21. Quel est le contenu de `file.txt`?
22. Que nous dit `git status`?



## Commandes utiles

- `git add`
- `git commit`
- `git commit -m "Mon message de commit court paresseux"`
- `git reset`
- `git checkout`
- `git log`
- `git log -n 5`
- `git log --oneline`
- `git log --oneline --graph`
- `git reset HEAD`
- `git checkout`

## Alias

Vous pouvez configurer des alias tels que:
`git config --global alias.lol 'log --oneline --graph --all'`
Cela pourrait vous être utile.
