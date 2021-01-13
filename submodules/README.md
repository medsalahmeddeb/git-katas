# Git Katas: sous-modules

Les sous-modules sont un moyen d'incorporer d'autres dépôts git dans le vôtre, en conservant un pointeur vers son `origine`.
Cela vous permet de récupérer directement les changements de source, ainsi que de les pusher.

## Installer

1. Exécutez `source setup.sh` (ou`.\setup.ps1` dans PowerShell)

> REMARQUE: si vous exécutez setup.sh sous Windows, vous pouvez rencontrer des problèmes en recherchant le script de configuration. À la place, exécutez `./setup.sh`, et les dossiers seront créés correctement.

## La tâche

Après avoir exécuté le script d'installation, il vous restera trois référentiels dans le dossier `exercice`.

* Un référentiel `component` cloné depuis` remote`.
* Un référentiel `product`.
* Un référentiel `remote`. Il s'agit du référentiel "distant" qui existe sur votre hôte de référentiel Git préféré, par exemple github.com.

Accédez au référentiel `product`.

1. Ajoutez un composant en tant que sous-module de produit en exécutant `git submodule add ../remote include`.
2. À quoi ressemble votre répertoire de travail?
3. Est-ce que `git status` ressemble à ce que vous attendez?
4. Et si vous cd vers "include"?
5. Exécutez `git diff --cached` dans` product`. Où pouvez-vous trouver l'ID de commit affiché dans la ligne `+Subproject commit ...`?
6. Validez les modifications sur le référentiel `product`.

Accédez au référentiel `component`.

7. Sait-il qu'il est utilisé comme sous-module?
8. Modifiez le dépôt `component` puis `git commit` et `git push`.

Accédez au référentiel `product`.

9. Est-ce que `git status` ou` git submodule foreach 'git status'` vous dit quelque chose sur ce nouveau commit?
10. Allez dans le répertoire `include` et faites `git pull` de la dernière version.
11. Vérifiez que la modification du référentiel `component` est disponible dans `include`.
12. Allez dans le répertoire `product`. Quel est le statut actuellement dans votre référentiel de `product`? Examinez également avec `git diff`.
13. Accédez à votre dossier «include». Faites un changement et pusher-le à son origine.

Allez dans le répertoire `exercice`. Nous allons faire un clone de produit pour illustrer comment les sous-modules d'un clone doivent être initialisés.

14. Exécutez `git clone product product_alpha`.
15. Allez dans le répertoire `product_alpha`, à quoi ressemble votre répertoire de travail, que dit le journal et que contient le répertoire` include`?
16. Lancez `git submodule init`, à quoi ressemble votre répertoire` include`?
17. Lancez `git submodule update`, à quoi ressemble votre répertoire` include` maintenant?
18. La dernière modification de «composant» est-elle disponible dans include?

Accédez au référentiel `product`.

19. Validez les modifications sur le référentiel `product`.

Accédez au référentiel `product_alpha`. Nous nous assurerons que nous avons les dernières modifications du produit.

20. Exécutez `git submodule update`.
19. La dernière modification de `component` est-elle disponible dans` include`?
20. Examinez la sortie de `git submodule status`. Comparez l'ID de validation avec le référentiel `component`.
21. Exécutez `git submodule update --remote`.
19. La dernière modification par rapport à «composant» est-elle disponible dans include?
20. Examinez la sortie de `git submodule status`. Comparez l'ID de validation avec le référentiel `component`.

Dessinez tout cet exercice!
