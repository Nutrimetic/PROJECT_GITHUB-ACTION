﻿# PROJECT_GITHUB-ACTION

L'objectif de se projet est de permettre de synchroniser automatiquement des fichiers sur plusieurs repository tel que :
+ Fichiers utilitaires :
+ + .gitignore
+ + .dockerignore
+ + .editorconfig
+ + CODEOWNERS
+ Fichiers de workflow github :
+ + Automatisation
+ + + Création d'une PR pour pouvoir pousser du code du main vers release automatiquement
+ + CI
+ + + Build d'une image docker
+ + + Lancement des tests
+ + CD
+ + + Build d'une image docker

## Ajouter un nouveau repository à synchroniser
Pour ajouter un nouveau repository à synchroniser il faut modifier le fichier sync-files. Ce fichier est organisé
en section. Certains sections sont spécifiques à un language (par exemple, lancement d'une commande pour les tests python)

## Configuration du projet
Afin de pouvoir modifier d'autres repository, le secret GITHUB_TOKEN n'a pas les droits suffisant.
Il faut donc créer un nouveau token avec les droits <b>repo</b> et <b>workflow</b> et le renseigner dans les secrets du repository :

![Image des settings secret du repository github](img/Setting_github_secret.PNG)

## Documentations utile
Toute la documentation utile est accessible la : https://github.com/BetaHuhn/repo-file-sync-action
