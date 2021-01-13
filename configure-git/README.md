
# Git Kata: Configurer Git

Ce kata n'a pas de script `setup.sh`. Lisez et suivez.

## Téléchargement et installation sous Windows

* Téléchargez sur [https://git-scm.com/download/win[https://git-scm.com/download/win) (ou utilisez [Chocolatey] (https://chocolatey.org/))
* Installer en utilisant les paramètres par défaut présélectionnés
* Après l'installation, ouvrez Git Bash pour les étapes de configuration suivantes

## Configuration initiale de Git

Git veut savoir qui il doit écrire en tant que commettant des changements, etc.
Pour ce faire, configurez le nom d'utilisateur et l'adresse e-mail de l'utilisateur vers Git avec les commandes suivantes:

1. `git config --global user.name" John Doe "`
2. `git config --global user.email" johndoe @ example.com`

### Configuration de l'éditeur

Parfois, Git a besoin que vous modifiiez un fichier qu'il crée, par exemple le message d'un commit que vous créez.
Par défaut, Git est configuré avec VIM, vous pouvez utiliser un autre outil qui vous plaît:

Si vous souhaitez utiliser l'éditeur nano basé sur cli:
- `git config --global core.editor nano`

Pour les peeps Windows:
- `git config --global core.editor notepad`

Ou bien d'autres outils que vous connaissez déjà:

- `git config --global core.editor" 'C:/Program Files/Notepad ++/notepad ++. exe' -multiInst -notabbar -nosession -noPlugin "`
- `git config --global core.editor" atom --wait "`
- `git config --global core.editor" code --wait "`

### Alias

Vous pouvez configurer des alias :
* `git config --global alias.lol 'log --oneline --graph --all'`

Cela peut vous être utile lorsque vous regardez le graphique Git.
Collez-le dans votre terminal et essayez-le avec `git lol`.

Plus d'informations sur les alias peuvent être trouvées dans le kata **alias**  .

### Authentification SSH

- Voir https://help.github.com/articles/generating-an-ssh-key pour plus de détails sur l'authentification par rapport aux référentiels SSH
- Ou exécutez `ssh-keygen` pour générer une paire de clés SSH dans`%USERPROFILE%/.ssh/`:

  `ssh-keygen -t rsa -b 4096 -C "johndoe@example.com"`

  Cela génère des clés publiques/privées nommées `id_rsa.pub`/` id_rsa`, respectivement)
- La clé publique `id_rsa.pub` doit être téléchargée sur votre serveur de dépôt:
- Pour GitHub, c'est dans _Settings_ -> _SSH et GPG keys_
- Pour le serveur BitBucket, c'est dans _Gérer le compte_ -> _SSH Keys_
