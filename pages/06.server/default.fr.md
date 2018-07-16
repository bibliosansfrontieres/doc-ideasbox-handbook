---
title: 'Le serveur'
---

## Principe de fonctionnement

L'IdeasBox intègre un serveur diffusant un réseau wifi dans son environnement proche. Les utilisateurs connectés à ce dernier accèdent à des ressources numériques \(films, ressources pédagogiques, sites Internet\) installées sur le disque du serveur, ces données sont présentés par le logiciel IdeasCube.

Il est possible de raccorder le serveur de l'IdeasBox à Internet \(via sa seconde antenne wifi ou via un câble réseau\).

Cette fonctionnalité permet 2 choses:

* Le partage de la connexion Internet à tous les utilisateurs connectés au hotspot wifi du serveur de l'IdeasBox
* La mise à jour du serveur et de son contenu

Le logiciel IdeasCube est un portail de contenus proposant des ressources documentaires numériques \(livres, fichiers multimédia, vidéos\), des sites \(Wikipedia, le projet Gutenberg, Wikisource\) et des outils de formation initiale et continue \(Moocs\) consultables hors ligne.

[Parcourir le manuel utilisateur et administrateur d'IdeasCube](http://ideascube.doc.bibliosansfrontieres.org)

## Installation

L'installation du serveur est automatisé grâce à un outil de déploiement appelé Ansible. Nous utilisons cet outil afin d'installer et paramétrer automatiquement tous les composants nécessaires au bon fonctionnement du serveur. Un descriptif des actions réalisées est disponible sur [GitHub](http://ansiblecube.doc.bibliosansfrontieres.org).

Note : le serveur n'est pas destiné à être branché sur la télé. Pour afficher sur la télé un contenu présent sur le serveur, il faut brancher un des laptops à la télé ; c'est depuis cet ordinateur qu'on affichera l'interface Ideascube.
