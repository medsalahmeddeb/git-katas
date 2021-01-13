# Bisect

La branche master est cassée, maintenant je souhaite que nous utilisions l'intégration prétestée. Je suis parti quelques jours en vacances et maintenant, quand je suis de retour, je me rends compte que le master est brisé et qu'il est brisé depuis un moment. Toutes les demandes d'extraction ont fonctionné mais tout le monde a été trop occupé pour se rendre compte que la construction principale échoue.

J'aimerais savoir quel commit a introduit l'échec du test. Mais il semble que ce soit trop difficile à comprendre à la main, le test est compliqué et il y a tellement de commits à passer et personne n'a changé le script de test.

Essayons d'utiliser `git bisect` pour trouver quel commit a cassé la construction.

Heureusement, j'ai ajouté une balise `initial-commit` lorsque le projet a démarré que nous pouvons utiliser pour commencer à rechercher le bogue.

Pour obtenir de l'aide sur l'utilisation de bisect, je peux toujours lancer `git bisect --help`.

Pour exécuter les tests, je peux exécuter le script de test:
''
$ ./test.sh
''
## Installer:

1. Exécutez `source setup.sh` (ou`.\setup.ps1` dans PowerShell)

## Tâches

1. Utilisez `git bisect` pour localiser le mauvais commit

## Vérifier

Lorsque j'ai terminé, je peux tester la solution avec le script de vérification

`` bash
$ cd ..
$ ./verify.sh # ou.\verify.ps1` dans PowerShell
''

## Si je suis coincé

J'ai trouvé ce manuel que je peux utiliser si je suis bloqué:


''
$ git bisect start
$ git bisect mauvais
$ git bisect bon initial-commit
$ git bisect run './test.sh'
''
