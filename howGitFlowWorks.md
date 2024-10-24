# GitFlow

## Qu'est-ce que Git Flow ?

- Modèle de branching git alternatif pour structurer les workflows de développement.
- Fonctionnalité présente dans Git, mais parfois non installée par défaut.
  - Pour l'installer sous Linux, utilisez la commande :  
    `sudo apt-get install git-flow`
- GitFlow aide à organiser le développement, notamment dans les environnements d'équipe, en attribuant des rôles spécifiques à différentes branches et en définissant des règles d'interaction.
- Il est particulièrement utile pour les projets où plusieurs fonctionnalités ou corrections de bugs doivent être développées en parallèle.

## Comment fonctionne Git Flow ?

- Contrairement à un workflow standard où il n'y a qu'une branche principale, GitFlow introduit deux branches principales :
  - **main** : Branche qui contient le produit fini et prêt à être déployé (partie client).
  - **develop** : Branche où se concentre le développement actif et continu, une copie évolutive de `main`.

### Étapes de base :

1. **Initialisation du projet avec GitFlow** :

   - Pour créer les branches `develop` et initialiser GitFlow :
     ```bash
     git flow init
     ```
   - Si la branche `develop` n'existe pas encore, vous pouvez la créer manuellement :
     ```bash
     git branch develop
     git push -u origin develop
     ```

2. **Branches de features** :

   - Créées à partir de `develop`, elles servent à développer de nouvelles fonctionnalités.
   - Une fois la fonctionnalité terminée, elles sont fusionnées dans `develop`.
   - Exemple de création d'une branche de fonctionnalité :
     ```bash
     git flow feature start ma-feature
     ```
   - Après avoir terminé la fonctionnalité :
     ```bash
     git flow feature finish ma-feature
     ```

3. **Branches de release** :

   - Créées à partir de `develop` lorsque plusieurs fonctionnalités sont prêtes pour une nouvelle version.
   - Ces branches permettent de finaliser les préparations pour la mise en production, y compris les corrections de bugs mineurs et les tests.
   - Création d'une branche `release` :
     ```bash
     git flow release start v1.0.0
     ```
   - Une fois la version prête, la branche `release` est fusionnée dans `main` et dans `develop` :
     ```bash
     git flow release finish v1.0.0
     ```

4. **Branches Hotfix** :
   - Utilisées pour résoudre rapidement des bugs critiques survenus en production.
   - Créées à partir de `main`, elles permettent de corriger le problème et de le fusionner immédiatement dans `main` et `develop`.
   - Exemple de création d'une branche `hotfix` :
     ```bash
     git flow hotfix start v1.0.1
     ```
   - Après correction :
     ```bash
     git flow hotfix finish v1.0.1
     ```

## Avantages de GitFlow

- **Séparation claire des rôles** : Chaque branche a un rôle spécifique, ce qui clarifie le workflow.
- **Stabilité accrue** : Les branches `main` et `release` garantissent des versions stables avant déploiement.
- **Adaptabilité** : Il est possible de travailler sur plusieurs fonctionnalités, correctifs ou versions en parallèle, sans confusion.

## Inconvénients de GitFlow

- **Complexité** : Pour les petits projets ou les équipes réduites, ce workflow peut sembler trop structuré et lourd.
- **Multiplication des branches** : La gestion des nombreuses branches peut devenir difficile si l'équipe ne suit pas rigoureusement les pratiques.
