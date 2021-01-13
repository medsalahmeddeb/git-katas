

# Vue d'ensemble des exercices Git Kata

## Installer

1. [configure-git] (configure-git/README.md) - Si git n'est pas configuré, quelques étapes de configuration de base

## Git Katas de base dans l'ordre suggéré

1. [basic-commits] (basic-commits/README.md) - Création basique de commits.
2. [basic-staging] (basic-staging/README.md) - Interagir avec le stage (index).
3. [basic-branching] (basic-branching/README.md) - Le premier pas vers le **branching**.
4. [ff-merge] (ff-merge/README.md) - Une visite guidée des **merges**.
5. [3-way-merge] (3-way-merge/README.md) - Une **merge** de base, impliquant plusieurs branches divergentes.
6. [merge-conflict] (merge-conflict/README.md) - Une **merge** de base entre des branches divergentes avec des changesets incompatibles.
7. [merge-mergesort] (merge-mergesort/README.md) - Un conflit de **merge** avec le code réel.
8. [rebase-branch] (rebase-branch/README.md) - Utilisation de **rebase** comme alternative à la **merge**.
9. [basic-revert] (basic-revert/README.md) - Utilisez **revert** pour annuler une modification
10. [reset] (reset/README.md) - **Reset** est une commande puissante et légèrement dangereuse : les trois modes de **reseting**.
11. [basic-cleaning] (basic-cleaning/README.md) - Nettoyage de l'espace de travail.
12. [modifier] (modifier/README.md) - Modifier les **commits** précédents.
13. [réorganiser-l'historique] (réorganiser-l'historique/README.md) - Nous pourrions avoir créé nos commits dans un ordre plus optimal : corriger ce scénario.
14. [squashing] (squashing/README.md) - Beaucoup de petits commits sont bons lorsque vous travaillez localement, mais pour partager votre code, il peut être plus avantageux de fournir vos modifications de code dans de grands ensembles.
15. [advanced-rebase-interactive] (advanced-rebase-interactive/README.md) - Entraînez-vous à utiliser les commandes de **rebase** interactives.
16. [basic-stashing] (basic-stashing/README.md) - Le premier pas vers le **stashing** (stockage).
17. [ignore] (ignore/README.md) - Les bases de l'utilisation du fichier `.gitignore`. Et en utilisant `git rm`.
18. [submodules] (submodules/README.md) - Les sous-modules sont détestés
19. [git-tag] (git-tag // README.md) - Les **tags** sont pratiques pour garder une trace des commits qui référencent un numéro de version.

## Katas qui résolvent des problèmes standards

1. [commit-on-wrong-branch] (commit-on-wrong-branch/README.md) - Si nous mettons accidentellement des commits unpushed sur la mauvaise branche, comment pouvons-nous les _move_ efficacement vers une autre branche avant de travailler là-dessus branche.
2. [commit-on-wrong-branch-2] (commit-on-wrong-branch-2/README.md) - Un autre exercice sur ce qu'il faut faire si vous avez commis accidentellement sur la mauvaise branche.
3. [reverted-merge] (reverted-merge/README.md) - Nous annulons une **merge**, mais, une fois les correctifs ajoutés à la branche **merge**née, nous voulons les changements de la **merge** et les nouveaux correctifs.
4. [save-my-commit] (save-my-commit/README.md) - Si vous supprimez accidentellement ou volontairement un commit, allez ici pour essayer de le sauvegarder. Vous utiliserez le reflog.
5. [Detached HEAD] (detached-head/README.md) - git se plaint que vous êtes dans un "état "Detached HEAD "". Que faire?

## Fonctionnalités avancées GIT

1. [git-attributes] (git-attributes/README.md) - Le fichier .gitattributes vous permet de spécifier la façon dont git gère les fichiers, comme les fins de ligne dans les fichiers texte ou comment diffèrent un fichier binaire.
2. [Bad-commit] (bad-commit/README.md) - Utiliser `git bisect` pour trouver un mauvais commit.
3. [bisect] (bisect/README.md) - Un autre kata utilisant `git bisect`.
4. [pre-push] (pre-push/README.md) - Un exercice rapide d'utilisation des hooks Git.
5. [Investigation] (investigation/README.md) - Découvrez ce qui se passe dans un dépôt Git, voyez à quoi il ressemble sous le capot.
6. [Objects] (objects/README.md) - Un petit exercice sur les internes de Git.
7. [merge-driver] (merge-driver/README.md) - Définition d'un pilote de **merge** personnalisé.
8. [rebase-exec] (rebase-exec/README.md) - Exécute des tests sur chaque commit en utilisant `git rebase --exec`
