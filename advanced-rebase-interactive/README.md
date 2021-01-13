# Rebase interactif avancé
Vous avez travaillé sur une nouvelle fonctionnalité appelée Hello World.
Cette fonctionnalité finit par être complète avec la documentation et le test unitaire, mais il y a quelques problèmes.
L'historique semble vraiment désordonnée, avec beaucoup de petites étapes à moitié, et il y a des choses incluses qui n'auraient jamais dû être là.

Vous devriez corriger cela pour que votre `git log` soit beau!

Pour ce faire, nous utiliserons notre bon ami `git rebase --interactive`

Heureusement, nous avons un tag de release `v0.0` juste avant le démarrage de la fonctionnalité.

Comme il s'agit d'un exercice avancé, il n'y a pas d'étapes spécifiques à suivre ni de solution unique.

## Installer:

1. Exécutez `source setup.sh` (ou`.\setup.ps1` dans PowerShell)

## Tâche

1. Explorez le repo et l'historique pour savoir ce qui s'est passé
2. Utilisez `git rebase --interactive v0.0` pour vous permettre d'éditer la "recette" du développement de la fonctionnalité.
3. Nettoyez l'historique de manière à ce qu'il ait un sens. Essayez d'utiliser autant de "fonctionnalités" de rebase (par exemple, reword, squash, fixup, drop) que possible. Vous décidez vous-même si vous voulez réécrire le tout en une seule fois, ou appliquer d'abord quelques changements, puis exécuter un nouveau `git rebase --interactive v0.0` pour continuer à nettoyer.

### commandes utiles

- `ls -l` # liste les fichiers
- `tail -n +1 *` # affiche le contenu de tous les fichiers
- `git log --oneline` # affiche l'historique
- `git log --stat` # log les fichiers qui ont été changé
- `git log --patch` # log avec diff
- `git rebase -i <ref>` # exécuter le rebase interactif vers <ref>
