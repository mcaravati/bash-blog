# Projet Système Blogue
## Par Simon TALBI et Matteo CARAVATI, S1A

### Le script est un simple utilitaire de gestion de blogue par ligne de commande.
#### Il permet :
 - de créer et d'éditer des pages en format markdown, en utilisant divers éditeurs
 - de lister les pages rédigées
 - de supprimer des pages rédigées
 - de générer un ensemble de pages HTML ainsi qu'un fichier PDF à partir des pages rédigées

### Syntaxe d'appel du script :
 ```bash
Usage ./blogue.sh COMMANDE [PARAMETRE]
La liste des commandes est editer, supprimer, lister, construire
  - Éditer un document : ./blogue editer [PAGE]
  - Supprimer un document : ./blogue supprimer [PAGE]
  - Lister les documents : ./blogue lister
  - Générer les fichiers PDF/HTML : ./blogue construire
  - Visualiser le site : ./blogue visualiser [pdf]
```

### Traces d'exécution :
#### Pour l'édition :
```
~/systeme/blog-systeme > ./blogue.sh editer
Fichier à éditer : 
lama
```
```
~/systeme/blog-systeme > ./blogue.sh editer lama
```
#### Pour lister les pages :
```
~/systeme/blog-systeme > ./blogue.sh lister
index.md  lama.md  pommes.md  soleil.md
```
#### Pour supprimer des pages :
```
~/systeme/blog-systeme > ./blogue.sh supprimer
Fichier à supprimer : 
lama
Voulez-vous supprimer la page markdown/lama.md ? (yes/no)?
yes
```
```
~/systeme/blog-systeme > ./blogue.sh supprimer lama
Voulez-vous supprimer la page markdown/lama.md ? (yes/no)?
yes
```
#### Pour construire le blogue : 
```
~/systeme/blog-systeme > ./blogue.sh construire
```
#### Pour visualiser le blogue :
```
~/systeme/blog-systeme > ./blogue.sh visualiser pdf
```
```
~/systeme/blog-systeme > ./blogue.sh visualiser
```

## Difficultés rencontrées lors du projet :
Aucune difficulté majeure n'a été rencontrée durant la réalisation de ce projet.
Un problème qui a cependant été un frein à notre progression est l'action à effectuer pour vérifier que le dossier markdown/ existe et n'est pas vide.

## Travail réalisé :
Tout le travail demandé a été réalisé.
Nous avons ajouté l'erreur générée si une extension est spécifiée, et nous avons aussi fait en sorte que le programme fonctionne, même avec des fichiers avec des noms à espaces.

## Améliorations apportées :
Nous avons ajouté des tests vérifiant que les paquets texlive et pandoc sont bien installés, pour la génération du site statique HTML et du PDF.
Si les paquets ne sont pas installés, le script retourne une erreur.