# Cours de GIT

## Introduction

Git est un logiciel qui permet de faire du versionning avec collaboration via des serveurs web dédiés comme GitHub ou GitLab.

## Instalation

Pour pouvoir utiliser GIT il faut installer le logiciel sur nos machines.

```bash
apt install get

# control d'action
git --version
```

## Initialisation du travail

Sur la VM
```bash
cd Documents # On rentre dans documents

mkdir cours #creer un dossier

cd cours # On rentre dans cours

git init # initialise le depot git en dossier cacher

ls -a # affiche tous les fichiers et dossiers meme chaches
```

Toujours sur la VM !
Creer un "new repository" avec le même nom que nôtre dépôt local.
Pour le moment, on ne crée pas le fichier.
gitignore ni le readme. ON LES CR2ERA PLUS TARD;

### Création de la connexion avec le débot

```bash
git remote add origin https://github.com/GozikizoG/cours1.git

#login de connextion
git config user.name "GozikizoG"

#email de connexion
git config user.email "cypriencosta77@mail.com"

```
On évite de créer une connexion globale pour pouvoir changer de compte git au besoin

# Créer un fichier et le pousser vers le dépot distant

```bash 
nano text.txt
```


Il y a trois étapes pour pousser du contenu vers github

1. ajouter les fichiers que l'on souhaite suivre en versionning
```bash
git add test.txt
```

2. préparer l'envoie en regroupant les fichiers et en donnant un message explicatif sur le contenu
```bash
git commit -m "mon premier commit"
```

3. envoyer effectivements les informations vers github
```bash
git push - u origin master
# le mot de passe login pour l'autorisation est le token
```

Il vous faudra votre login **github** et un TOKEN (à créer sur github).
``Compte > settings > developper settings > token classic > generate``
Donner les droits puis valider et surtout noter le token
