# gitkatas

## Mauvaise validation

Un des commits sur `master` a introduit un mauvais fichier.
Trouvez le commit et annulez-le en utilisant la **bisect**.

## Installer:

1. Exécutez `source setup.sh` (ou`.\setup.ps1` dans PowerShell)

## La tâche

Utilisez `git bisect` pour trouver le" mauvais "commit, puis utilisez `git revert` pour le restaurer. Lors de l'exécution de `git bisect`, vous indiquez si le "state" est "good" ou "bad" jusqu'à ce qu'il trouve le commit qui a introduit le changement.

Pour cet exercice, la version est mauvaise si «badfile» existe.

1. Démarrez `git bisect`.
2. Habituellement, le HEAD est "bad", comme c'est le cas dans cet exercice. Utilisez `git bisect bad` pour l'indiquer.
3. Habituellement, une ancienne version sera bonne. Dans cet exercice, la version de démarrage l'est. Utilisez `git bisect good <commit-ish>` pour l'indiquer.
4. `git bisect` vérifiera ensuite divers commits pour trouver le mauvais commit. Continuez à indiquer l'état jusqu'à ce qu'il vous indique le premier mauvais commit. Gardez une trace de ce commit.
5. Exécutez `git bisect reset` pour que nous puissions travailler sur le référentiel.
6. Utilisez `git diff` pour vous assurer que le mauvais commit n'a introduit que` badfile`.
7. Utilisez `git revert` dessus.

Si vous avez un script qui peut dire si le code source actuel est bon ou mauvais, vous pouvez couper en deux en lançant `git bisect run`.

## Commandes utiles

- `git bisect start`
- `git bisect bad`
- `git bisect good <commit-ish>`
- `git bisect good`
- `git bisect reset`
- `git diff <commit-ish-1> <commit-ish-2>`
- `git revert <commit-ish>`
- `git bisect run <cmd>`
- `test !-f badfile` (ou `gci. badfile` dans PowerShell) pour tester l'existence d'un fichier
- `test !-f badfile; echo $?`pour afficher le résultat du test sur la console
