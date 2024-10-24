# Cheatsheets Gitflow

## Commande initiale

|   Commandes   |                 rôles                  |
| :-----------: | :------------------------------------: |
| git flow init | lancer git flow dans un dépot existant |


## Partie fonctionnalité

|                    Commandes                     |                          rôles                           |
| :----------------------------------------------: | :------------------------------------------------------: |
|    git flow feature start "ma_fonctionalité"     |               commencer une fonctionnalité               |
|    git flow feature finish "ma_fonctionalité"    |               Terminer une fonctionnalité                |
|   git flow feature publish "ma_fonctionnalité"   |                Publier une fonctionnalité                |
| git flow feature pull origin "ma_fonctionnalité" |   récupérer une fonctionnalité d'un autre utilisateur    |
|    git flow feature track "ma_fonctionnalité"    | suivre l'état d'une fonctionalité sur le serveur distant |

## Partie livraison

|                Commandes                |                 rôles                 |
| :-------------------------------------: | :-----------------------------------: |
|  git flow release start "ma_livraison"  |      créer branche de livraison       |
| git flow release publish "ma_livraison" |     publier branche de livraison      |
|  git flow release track "ma_livraison"  | suivre l'état de la branche livraison |
| git flow release finish "ma_livraison"  |     terminer la branche livraison     |

## Partie hotfix

|              Commandes              |            rôles            |
| :---------------------------------: | :-------------------------: |
| git flow hotfix start "ma_version"  | commencer la branche hotfix |
| git flow hotfix finish "ma_version" |   terminer branche hotfix   |