# HEAD détaché

Lorsqu'un utilisateur se retrouve dans un état de "Detached HEAD", c'est une situation effrayante, mais comme nous le savons, Git ne fait pas peur.

## Installer:

1. Exécutez `source setup.sh` (ou`.\setup.ps1` dans PowerShell)

## La tâche

1. Exécutez `git status` et` git log --oneline --graph --all` pour voir ce qui se passe.
2. Restaurez l'état normal dans ce référentiel en passant à `master`

Notez que cette tâche peut sembler plus déroutante si vous n'avez pas exécuté `setup.sh` dans votre terminal.

Nous voulons avoir une branche appelée «the-begin» qui est faite à partir du premier commit avec le message «A».

3. Pouvez-vous faire cela en provoquant d'abord un Detached HEAD?

## Commandes utiles

- `git status`
- `git log --oneline --graph --all`
- `git checkout <ref>`
