# git-merge-driver

Ce référentiel contient un outil de fusion, sous la forme d'un script shell, qui peut gérer la fusion de fichiers `.tst` en conflit.
Il contient également une branche de fonctionnalités avec des modifications conflictuelles apportées à un fichier `.tst`.
Dans cet exercice, nous allons configurer le référentiel git pour toujours résoudre les conflits de fusion dans les fichiers `.tst` via le script` merge-tst-files.sh`.
Nous le ferons en configurant `merge-tst-files.sh` comme _merge driver_ pour les fichiers` .tst`.

## Installer:

1. Exécutez `source setup.sh` (ou`.\setup.ps1` dans PowerShell)

## La tâche

1. Définissez le script `merge-tst-files.sh` comme pilote de fusion dans` .git/config`
2. Définissez le pilote de fusion à utiliser pour les fichiers `.tst` dans` .gitattributes`
3. Ajoutez le script `merge-tst-files.sh` à PATH
4. Fusionner dans la branche `feature/1`
5. Vérifiez la sortie pour vérifier que le script `merge-tst-files.sh` a été utilisé pour résoudre le conflit.
6. Pouvez-vous valider/pousser la configuration de votre pilote de fusion? Sinon, comment le distribueriez-vous autrement?
