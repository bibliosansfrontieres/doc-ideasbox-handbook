---
title: 'Ubuntu Linux'
---


## Ubuntu

Ubuntu se définit comme une distribution conviviale, avec une interface « simple, intuitive, et sécurisée ».

Par défaut, le démarrage de l'ordinateur se fait sous Ubuntu.

### Installation

Les versions LTS (Long Term Support), qui sont supportées pendant 5 ans, sont préférées. La 14.04 a récemment fait place à la 16.04. La 18.04 présente actuellement quelques soucis concernant la session invité.

Par dessus Ubuntu, on installe le paquet [```edubuntu-desktop```](https://packages.ubuntu.com/xenial/edubuntu-desktop) qui lui-même tire une collection d'applications à but pédagogique.

L'ensemble de l'installation et de la configuration se fait au moyen d'un playbook ansible (un outil d'automatisation de la configuration et de la gestion), nommé `idbuntu` ([disponible sur Github](https://github.com/bibliosansfrontieres/idbuntu)). Sa lecture, bien que technique, documente la mise en oeuvre dans son intégralité.

## Les sessions

Il existe trois types de sessions utilisateurs.

### La session invité

**La session invité** est destinée aux utilisateurs.

Parmi ses caractéristiques, cette session est amnésique : à l'ouverture de session, c'est une session toute neuve qui est recréée d'après un modèle, et elle est effacée dès sa fermeture. Cela permet de ne pas avoir à se soucier des éventuelles informations laissées par chaque utilisateur (documents personnels, connexions aux comptes sur des sites web, ...).

### La session `ideasbox`

**La session `ideasbox`** est celle qui sert de modèle à la session `invité`.

Toutes les personnalisations qui y seront effectuées se verront répliquées dans la session `invité` : fond d'écran, raccourcis, etc.

Elle n'est donc pas à utiliser au quotidien.

Le login est `ideasbox`, le mot de passe est communiqué à la demande par BSF.

### Les sessions Admin

**La session `Local Admin`** sert à l'administration et l'entretien du système. C'est la seule session qui dispose des droits administrateurs, permettant ainsi d'ajouter ou supprimer des logiciels, intervenir sur la configuration réseau et toute autre composante du système.

La première fois qu'on ouvre une session avec ce compte, un changement de mot de passe est exigé. Le mot de passe initial est `ChooseAStrongPasswordPLZ` et nous vous invitons à utiliser un nouveau mot de passe relativement fort.

Le compte `bsfadmin` est destiné aux équipes de BSF, pour les opérations de maintenance et de support. Les clés SSH des techniciens BSF restent présentes dans le compte root ; si elles sont supprimées, aucun support ne peut alors être fourni.

### Voir aussi

  * [Script de création des comptes](https://github.com/bibliosansfrontieres/idbuntu/blob/master/roles/users/tasks/main.yml)
  * [Personnalisation de la session invité](https://help.ubuntu.com/community/CustomizeGuestSession) sur le wiki Ubuntu (en anglais)

## Les logiciels

La liste des logiciels généralement installés figure dans [le playbook](https://github.com/bibliosansfrontieres/idbuntu/blob/master/roles/software/tasks/main.yml).

Y figurent des logiciels de bureautique, création d'image, montage vidéo, retouche photo, édition musicale, programmation, découverte, mais aussi des jeux.

On y ajoute également le Tor browser (pour surfer anonymement sur le web), mais aussi Skype.

## Administration

Pour procéder à l'administration du système, il faudra tout d'abord se mettre en rapport avec BSF pour la mise en place d'un compte dédié. Ce compte n'est pas systématiquement créé car les besoins sont rares. Cependant, sur certains projets disposant des ressources nécessaires, un tel compte sera un plus.

Par défaut, Ubuntu télécharge et applique automatiquement les mises à jour de sécurité.

### Upgrades

#### Depuis Ubuntu 14.04

La version 14.04 d'Ubuntu est une LTS (Long Term Support), dont le support arrive à terme début 2019. Il convient d'upgrader au moins vers 16.04, en suivant [la procédure standard](https://tutorials.ubuntu.com/tutorial/tutorial-upgrading-ubuntu-desktop). Mais d'abord, il faut s'occuper de Skype.

Skype a disparu des dépôts partenaires, et une version 64bits est désormais disponible. On commence par désinstaller l'ancienne version 32bits :
```
sudo apt-get remove skype
sudo dpkg --remove-architecture i386
```
Puis on installe Skype de nouveau, depuis un PPA :
```
sudo add-apt-repository ppa:andykimpe/skype
sudo apt-get update
sudo apt-get install skype
```
