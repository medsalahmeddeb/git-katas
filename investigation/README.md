# Git Kata: objets Git

Les objets sont stockés dans `<repository>/.git/objects` dans des sous-dossiers correspondant aux deux premiers caractères du SHA.
`fc1da6e8f` est donc le fichier:` .git/objects/fc/1da6e8f`.

`git cat-file` montre le contenu de tout _ref_ que vous lui passez.
`-p` demande à` cat-file` de bien imprimer le contenu d'un objet.

`git ls-tree master .` liste le contenu d'un dossier.

## Installer:

1. Exécutez `source setup.sh` (ou`.\setup.ps1` dans PowerShell)

## Tâche

1. En utilisant `git ls-tree` et` git cat-file`, dessinez toute la structure de données Git.
- Quels objets d'arbre et de blob avez-vous et vers quoi pointent-ils?
- Qu'est-ce que les commits pointent à l'intérieur de ce graphique et où?
