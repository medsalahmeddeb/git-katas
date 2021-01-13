# Git kata: Alias

En travaillant, nous avons tendance à écrire beaucoup de commandes. Cela peut devenir fastidieux, surtout lorsque les commandes sont assez longues. Git vous permet de créer un alias pour les commandes, ce qui réduit considérablement le temps passé à les saisir et réduit le risque de faire des fautes de frappe.

Les alias sont stockés dans votre git config et peuvent donc être système, globaux ou locaux. La configuration système est valide pour chaque utilisateur sur la machine, la configuration globale est liée à votre utilisateur, tandis que la configuration locale vit dans un référentiel spécifique.

## Installer

1. Exécutez `source setup.sh` (ou`.\setup.ps1` dans PowerShell)

## La tâche

1. Affichez votre configuration en exécutant `git config --list`
2. Ajoutez un nouvel alias global \
 `git config --global alias.lol 'log --oneline --graph --all'` \
 Cela vous permet d'appeler `git lol` comme alternative à` git log --oneline --graph --all`
3. Exécutez votre alias `git lol`
4. Exécutez la commande complète `git log --oneline --graph --all` \
Y a-t-il une différence dans la sortie?
5. Créez un autre alias, cette fois local, qui répertorie les commits dont vous êtes l'auteur \
`git config --local alias.lome "log --author=\"$(git config --get user.name)\" "`
6. Exécutez votre alias `git lome` \
 Que montre-t-il?
7. Affichez votre configuration git et ses origines en exécutant `git config --list --show-origin` \
 Pouvez-vous trouver vos configurations d'alias?
8. Essayez d'exécuter `git lome` dans un autre dépôt git \
 Est-ce que ça marche?
9. Supprimez votre alias `git lol` en exécutant` git config --global --unset alias.lol`

## Commandes utiles

- `git config --list`
- `git config --list --show-origin`
- `git config get <configuration>`
- `git config --unset <configuration>`
