# Squash s'engage

Dans ce kata, je voudrais nettoyer un peu mon historique.

Les cinq derniers commits tous bricolent avec file.txt qui contient évidemment ma fonctionnalité.

Je voudrais que ces commits soient écrasés en un seul commit!

Pendant que vous y êtes, on voudrai vraiment que les caractères `\n` dans` file.txt` soient supprimés de l'historique.

## Installer

1. Exécutez `source setup.sh` (ou`.\setup.ps1` dans PowerShell)

## La tâche

1. _Squash_ les cinq commits pertinents en un seul et faire un bon message de commit (voir plus d'informations).
2. À quoi ressemble `git log` maintenant?
3. Nettoyez les caractères `\n` dans` file.txt` sans ajouter à l'historique des commits.

## Commandes utiles

- `git rebase -i <ref>`
- `git add`
- `git commit --amend`

## Plus d'informations

### Les sept règles d'un excellent message de commit Git

Depuis [Comment écrire un message de validation Git] (https://chris.beams.io/posts/git-commit/)

1. Séparez le sujet du corps par une ligne vierge
2. Limitez la ligne d'objet à 50 caractères
3. Mettez en majuscule la ligne d'objet
4. Ne terminez pas la ligne d'objet par un point
5. Utilisez l'impératif dans la ligne d'objet
6. Retourner à la ligne à 72 caractères dans le corps
7. Utilisez le corps pour expliquer quoi et pourquoi et comment

Exemple
''
Résumez les changements en environ 50 caractères ou moins

Texte explicatif plus détaillé, si nécessaire. Enveloppez-le à environ 72
caractères ou plus. Dans certains contextes, la première ligne est traitée comme
sujet du commit et le reste du texte comme corps. le
une ligne vide séparant le résumé du corps est critique (sauf si
vous omettez entièrement le corps); divers outils comme `log`,` shortlog`
et `rebase` peut devenir confus si vous exécutez les deux ensemble.

Expliquez le problème que ce commit résout. Concentrez-vous sur pourquoi vous
avez fait ce changement plutôt que comment (le code l'explique).
Y'a-t-il des effets secondaires ou d'autres conséquences non intuitives au
changement? Voici l'endroit pour les expliquer.

D'autres paragraphes viennent après des lignes vierges.

 - Les points à puces sont bien aussi

 - En règle générale, un trait d'union ou un astérisque est utilisé pour la puce, précédé
   par un seul espace, avec des lignes vides entre les deux, mais les conventions
   varient ici

Si vous utilisez un outil de suivi de tickets, mettez-y des références en bas,
comme ça:

Résout: #123
Voir aussi: #456, #789
''
