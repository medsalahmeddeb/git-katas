# Git Kata: changer d'auteur

## Installer:

1. Exécutez `source setup.sh` (ou`.\setup.ps1` dans PowerShell)


## La tâche

Vous vous êtes enfin convaincu que vous devriez commencer avec l'idée de projet open source que vous chérissez depuis si longtemps.
Mais hélas, vous vous êtes rendu compte après les premiers commits que vous avez oublié de configurer votre nom d'utilisateur et votre adresse e-mail.

Votre entreprise est assez aimable pour vous permettre d'utiliser votre ordinateur de travail pour contribuer à des projets open source, mais cela signifie également que votre nouveau référentiel git a utilisé la configuration globale sur votre machine, c'est-à-dire votre nom de travail et votre adresse e-mail.
En plus de tout cela, vous avez déjà poussé les premiers commits vers votre référentiel distant.

Pas de soucis, vous vous souvenez de quelque chose sur [la configuration des configurations] (https://git-scm.com/book/en/v2/Customizing-Git-Git-Configuration), [rebasing] (https: // git-scm. com/book/en/v2/Git-Tools-Rewriting-History).

Vous vous souvenez également que changer la configuration ne changera que le `committer` d'un commit mais pas son` author`, donc vous devrez également [set] (https://git-scm.com/docs/git-commit # Documentation/git-commit.txt --- authorltauthorgt) ou [reset] (https://git-scm.com/docs/git-commit#Documentation/git-commit.txt---reset-author) l'auteur .
Vous savez que vous devez rebaser complètement à partir de la [racine commit] (https://git-scm.com/docs/git-rebase#Documentation/git-rebase.txt---root).

Heureusement, vous venez de démarrer le projet afin que vous puissiez toujours [forcer la poussée] (https://git-scm.com/docs/git-push#Documentation/git-push.txt--f) sans craindre de gâcher ([Le Perils of Rebasing] (https://git-scm.com/book/en/v2/Git-Branching-Rebasing)) quelqu'un d'autre repo local.

## Commandes utiles
- `git config --local user.name" mon nom "`
- `git config --local user.email" myemail@home.com "`
- `git rebase -i --root`
- `git commit --amend --author =" mon nom <myemail@home.com> "--no-edit`
- `git commit --amend --reset-author --no-edit`
- `git rebase --continue`
- `git push --force`
