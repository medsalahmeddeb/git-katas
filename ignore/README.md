# Git Kata: Ignore
Nous allons travailler un peu avec le fichier `.gitignore` dans ce kata.
Dans ce fichier, vous pouvez spécifier à la fois des extensions de fichier et des structures de dossiers que vous ne souhaitez pas que Git effectue le suivi.
Vous pouvez toujours les fichiers et dossiers `git add` qui sont ignorés dans le fichier` .gitignore`.

Nous travaillerons également avec `git rm`, qui est la commande Git remove. `git rm` fait exactement la même chose que de supprimer un fichier de votre répertoire de travail, puis de mettre ce changement dans le stage avec `git add filename` sur le fichier qui vient d'être supprimé.
Parfois, vous ajoutez un fichier par accident qui n'était pas destiné à Git, par exemple fichiers binaires, fichiers de classe, etc.

Si vous voulez signaler à Git qu'un fichier doit être supprimé de git, mais que vous le souhaitez toujours dans votre répertoire de travail, utilisez `git rm --cached` pour émettre une commande remove sur la zone de stage, mais pas dans votre repertoire de travail.


## Installer:

1. Exécutez `source setup.sh` (ou`. \ Setup.ps1` dans PowerShell)

## La tâche

1. Créez un fichier avec le nom «foo.s»
2. Quelle est la sortie de `git status`?
3. Créez un fichier `.gitignore` dans votre répertoire de travail contenant `*.s`
4. Quelle est la sortie de `git status`?
5. Validez le fichier `.gitignore`
6. Validez `file1.txt`
7. Ajoutez les fichiers `txt` à `.gitignore` en ajoutant une ligne contenant `*.txt`
8. Que nous dit `git status`?
9. Modifiez `file1.txt`
10. Que nous dit `git status`? Pourquoi le fichier a-t-il été suivi même si l'extension `txt` est dans le fichier ignoré?
11. Créez un autre fichier texte dans le référentiel, à quoi ressemble `git status` maintenant? Pourquoi n'est-il pas suivi?
12. Effectuez la suppression de `file1.txt` avec la commande` git rm --cached`
13. Que dit `git status`?
14. Ajoutez un nouveau fichier `file2.txt` et ajoutez `!file2.txt` à `.gitignore`.
15. Que dit `git status`? Pouvez-vous penser à un cas d'utilisation pour garder une trace d'un fichier bien que l'extension soit ignorée?

## Commandes utiles
- `git rm`
- `git add`
- `git commit`
- `git commit -m`
- `git rm --cached`


## Alias
Vous pouvez configurer des alias en tant que tels:
`git config --global alias.lol 'log --oneline --graph --all'`
Cela pourrait vous être utile.
