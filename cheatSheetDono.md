# Gitflow

## Qu'est-ce que Git Flow ?

- Modèle de branching git alternatif
- Environnement présent dans git
  - Sinon le télécharger si pas présent de base dans Linux.
  - Commande : > `sudo apt-get install git-flow`
- Permet d'organiser son travail, notamment dans des environnements d'équipe
- Assigne des rôles très spécifiques aux différentes branches et définit comment et quand elles doivent interagir.

## Comment fonctionne Git Flow ?

- Au lieu d'une seule branche main, deux branches principales : **main** et **develop**
- **main :** Le produit fini - La partie client
- **develop :** Le produit en cours de développement, dupliquée de la branche main.

1. Compléter la branche main avec une branche develop.
   1. `git branch develop`, `git push -u origin develop` **ou alors :** git flow init fait aussi l'affaire.
2.
