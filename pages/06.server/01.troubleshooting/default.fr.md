---
title: 'Dépannage du serveur'
---

##Le serveur ne démarre pas
**Symptôme** : le serveur ne s’allume pas quand on appuie sur le bouton.
- Vérifier que le connecteur d’alimentation est  correctement enfiché. Le débrancher et le rebrancher.
- Vérifier que la batterie est chargée
- Essayer avec le bloc d'alimentation fourni avec le serveur et le brancher sur le secteur 220V.
- S’il ne s’allume toujours pas, le serveur est matériellement défaillant et doit être retourné au constructeur pour réparation. Contacter le siège de BSF. 

## Le hotspot IdeasBox n'apparait pas
- Connecter un écran au serveur (à défaut, un vidéoprojecteur) et vérifier que l’interface graphique fonctionne. 
- Redémarrer le serveur une première fois et attendre quelques minutes, vérifier si le hotspot apparaît à nouveau.
- Contacter BSF pour une intervention à distance 

## J'ai perdu le mot de passe admin

* Brancher un clavier, une souris et un écran au serveur pour accéder à l'interface graphique.
* Une fois l'écran branché, rentrer le login : ```ideascube``` et le mot de passe que BSF vous a transmis
* Une fois connecté, cliquer en bas à gauche sur l'icône menu et sélectionnez "Outils système > LXTerminal"
* Dans le LXTerminal, taper : ```ideascube changepassword admin``` (```admin``` ou un autre utilisateur).

## J'ai perdu le chargeur

Ou son embout.

Le serveur encaisse une tension de 7V à 20V, il faut préférer le 12V.

Au bout du chargeur, le connecteur est détachable. Il peut arriver qu'on en perde l'embout. Celui-ci peut se trouver assez facilement dans le commerce.
Cependant il faudra faire attention à son format : il ressemble à un embout "classique" 2.5/5.5, mais tous les embouts 2.5/5.5 ne rentrent pas dedans.
Histoire de s'éviter des surprises, on prendra soin d'emmener le sreveur en magasin afin de tester le potentiel achat et s'assurer qu'il rentre bien dans la prise femelle.
