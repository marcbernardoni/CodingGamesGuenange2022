# Mise en place d'un projet simple en Node.js

## Description

Il s'agit d'un projet sans prétention qui permet de démarrer un projet en javaScript avec Node.js. Il ne dépend d'aucun framework mais permet la mise ne place rapide d'outils afin que notre code respecte certaines règles syntaxique et qu'il soit correctement formatté.

## Dépendances

Ce projet permet de passer à la vitesse supérieur notamment grâce à l'utilisation du **gestionnaire de paquet npm**

4 paquets et leurs dépendances sont utilisés ici :

- [ESLint](eslint.org) : ESLint est un outil permettant d'identifier et de signaler les motifs trouvés dans le code ECMAScript/JavaScript.
- [Prettier](prettier.io) : Prettier est un formatteur de code obstiné !
- [Husky](typicode.github.io/husky) : Husky améliore vos commits et plus 🐶 woof !
- [jsdom](github.com/jsdom/jsdom#readme) : jsdom est une implétention en pur javaScript des standarts du Web (notamment basé sur les travaux du WHATWG à propos des standarts HTML et DOM). Il est nécessaire pour faire fonctionner [Quokka.js](github.com/jsdom/jsdom#readme)

## Installation du projet

### Légende : 
- nomRepo : Le nom du dépôt github
- yourFolder : Le nom du dossier sur votre ordinateur

### Opérations:

Voici comment installer rapidement ce projet :
Créer un nouveau Dépôt github :
```
gh repo create nomRepo --public
```

Puis choisir l'option *importer depuis un dépot existant*. Dans le champ demandant l'url du dépôt enrez :
**https://github.com/marcbernardoni/nodejs-setup.git**

Enfin entrez les commandes suivantes:
```
git clone https://github.com/marcbernardoni/nomRepo.git yourFolder
cd yourFolder
npm install
```

Pour changer le nom du Repository, créer un nouveau dépôt git :
```
gh repo create nomRepo --public
```


## Instructions

### Dossier _src_

Un dossier source est présent. C'est le dossier dans lequel il est prévu de mettre tous vos fichiers en cours de développement.

### Les scripts inclus

Il y a 3 scripts prêt à l'emploi:

- start : permet de tester le bon fonctionnment de node en executant le ficher d'exemple _./src/index.js_
- lint : permet de detecter l'ensemble des erreurs de syntaxe et de mise en forme du code
- lint:fix : permet de détecter et de corriger (si possible) l'ensemble des erreurs de syntaxe et de mise ne forme du code

Pour executer un script, il faut utiliser la commande `npm run nomDuScript``

### Husky

Lors d'un commit git, Husky permet de lancer automatiquement des hooks. Seuls deux hooks sont présents:

- l'un permet de lancer automatiquement le script _lint_
- le second affiche un message si le commit s'est bien déroulé

## Guide de Style

Le guide de style est basé sur celui d'[airbnb](https://airbnb.io/javascript/react/).
Seuls deux exceptions dérogent aux règles précédentes :

- il faut utiliser des guillemets simples partout
- les point-virgules sont omis
