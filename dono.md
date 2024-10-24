# Gitflow
- présent dans git
- pensé dans un principe qui va nous cadrer
- deux branches : main et development
- la branche principale esst development, à travers et à partir.
- master sert à cadrer livraison en production
- On voit l'état en cours de development grâce la branche devlopment
- bug sur main -> hotfixes branch et la merger sur main
-mais vu qu'on ne veut pas perdre les fonctionnalités, on la merge aussi sur development

- installer git flow sur linux : 
	- apt-get install git-flow

### commandes utiles
- git flow
- git flow init
> Permet d'initialiser les branches de travail
- git flow feature
> Permet de créer une nouvelle branche pour les features
- git branch
> Checker les branches de travail
- git flow feature start [nom-de-la-feature]
> Crée une branche annexée à feature
- git flow feature finish [ma-feature]
> Termine le travail sur la branche et la merge avec development
- git flow release
> 
- git flow release start 1.0.0
> crée la release
- git flow release finish 1.0.0
