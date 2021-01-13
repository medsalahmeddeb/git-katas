# Git Kata: fichier d'attributs Git

Nous travaillerons un peu avec les [`.gitattributes`] (https://www.git-scm.com/docs/gitattributes)
fichier dans ce kata. Dans ce fichier, vous pouvez spécifier comment git gère les fichiers, par exemple s'ils sont des fichiers binaires ou texte. Par exemple, il est possible de décrire quel type de
fin de ligne à utiliser, ou si vous avez des fichiers binaires dans votre référentiel,
vous pouvez spécifier le programme à utiliser pour afficher le diff. Les exercices suivants
sont pour les plates-formes GNU/Linux et Mac.

## Installer:

1. Exécutez `source setup.sh` (ou`.\setup.ps1` dans PowerShell)

## La tâche

1. Créez un fichier `.gitattributes` avec le contenu suivant:

    `* .txt text = auto eol = lf working-tree-encoding = UTF-8`

2. Exécutez `git add file1.txt .gitattributes` et vous devriez voir

    `avertissement: CRLF sera remplacé par LF dans file1.txt.`

3. Essayez d'expérimenter en changeant «eol» en «auto» ou «crlf». Peux-tu expliquer
   pourquoi un seul d'entre eux modifie les fins de ligne du fichier, c'est-à-dire donne un
   avertissement similaire à celui ci-dessus.

4. Certains fichiers doivent avoir des fins de ligne DOS (CRLF) pour fonctionner. Un tel exemple
   is bat-files, par exemple, Jenkins requiert que les fins de ligne dans les bat-files soient CRLF avant
   être en mesure de les exécuter.

   `* .bat text = auto eol = crlf`

   Un problème similaire est présent avec les scripts Linux utilisant un shebang dans la première ligne pour pointer
   à un interprète. Les systèmes GNU/Linux auront un problème à les exécuter, par exemple, `bash\r` n'est pas
   reconnu comme interprète.

5. Git est principalement adapté aux fichiers texte, mais il peut également gérer les fichiers binaires
   et vous pouvez définir des programmes pour afficher le diff. Vous devez avoir installé exif (ou exiftool)
   pour que cela fonctionne. Si vous n'avez pas d'image png sur votre machine, vous pouvez utiliser:
   https://www.freepngimg.com/download/mario/20698-7-mario-transparent-background.png

    `* .png diff = exif`

6. Remplacez l'image, par exemple, en utilisant celle-ci qui est une version plus petite de l'image
  https://www.freepngimg.com/download/temp/20698-7-mario-transparent-background_400x400.png

  Maintenant, exécutez git diff, et vous pouvez voir quels attributs ont été modifiés.

7. Les fins de ligne peuvent également être contrôlées via
   [`git config`] (https://www.git-scm.com/book/en/v2/Customizing-Git-Git-Configuration):

    git config --global core.autocrlf entrée

   Cela garantira que le référentiel contient toujours des fins de ligne LF, comme line
   les fins sont converties en LF lors des poussées. La configuration peut également être définie sur «true»
   et «faux». Vous pouvez expérimenter un peu avec cela.

## Commandes utiles

- `file file1.txt` (sous GNU/Linux et Mac)
- `git add`
- `git status`
- `iconv` est utile pour la conversion entre différents encodages de caractères.

## Information additionnelle

Le `.gitattributes` a une autre alternative, si vous êtes simplement intéressé par
ayant les mêmes fins de ligne et encodages de caractères dans les fichiers de votre
dépôt. [editorconfig] (https://editorconfig.org/) peut gérer l'indentation
size (utile pour Python), s'il faut utiliser des tabulations ou des espaces, ajouter une dernière nouvelle ligne
etc.
