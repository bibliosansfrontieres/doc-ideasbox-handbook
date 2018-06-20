---
title: 'Installation et configuration des tablettes'
---

Les tablettes sont pré-paramétrées dans les IdeasBox. Cependant il se peut que des besoins de dernières minutes soient exprimés directement sur le terrain.

Il faudra donc être réactif ! 

**Il est très fortement conseillé d'utiliser un ordinateur sous Linux pour toutes les opérations décrites ci-dessous.**

##Stratégie d'installation 
Vous avez le choix entre deux stratégies d'installation des nouvelles applications sur les tablettes.  

** Vous décidez d'activer le Google Play store sur toutes les tablettes**
  * Cela nécessite de créer un compte Google 
  * De passer sur chaque tablette pour configurer le compte Google
  * De sélectionner chaque application à installer 
  * De vérifier et repasser éventuellement sur certaines tablettes pour relancer les tablettes qui n'auraient pas pu télécharger toutes les applications

**Vous décidez de ne pas passer par le Google play store et d'installer en masse via un Ordinateur vos applications**
  * Cela nécessite que vous ayez toutes les applications avec vous, si ce n'est pas le cas vous serez certainement obligé de passer par l'étape décrite ci-dessus, mais vous le ferez uniquement sur une tablette
  * D'utiliser un ordinateur sous linux (car l'installation de l'utilitaire est très simple)
  * De disposer du script permettant les installation en masse 
  * D'être conscient qu'il faudra brancher chaque tablette à l'ordinateur

###Avantage et inconvénient des 2 solutions 

**La solution Google Play Store** peut être pratique si votre partenaire souhaite avoir une certaine indépendance et projette d'installer de nouvelles applications régulièrement. Cependant dans des contextes où le débit de la connexion Internet est faible, ce n'est pas la stratégie à prévoir, car les applications doivent être téléchargés sur chaque tablette ! (Une application peut peser jusqu'à 150Mo). Néanmoins cela peut être rassurant pour un partenaires disposant de compétences techniques faibles. Il faut savoir enfin que vous rentrez ensuite dans le  monde de Google à vos risque et périls, mais c'est pratiquement inévitable si vous souhaitez utiliser des applications payantes.  


**La solution sans Google Play Store** est très intéressante mais nécessite quelques compétences techniques et un transfert de compétences au partenaire à ce niveau là. Par ailleurs, vu qu'il s'agit de script bash avec l'utilitaire ADB, nous pouvons également en profiter pour supprimer des applications jugées inutiles ou ne fonctionnant pas. Les applications dans ce cas ne sont téléchargés qu'une seule fois ce qui peut convenir pour une connexion Internet disposant d'un faible débit. Soit vous disposez déjà des applications sur votre ordinateur, soit vous pouvez les télécharger directement avec l'utilitaire [Google Play Downloader](http://codingteam.net/pro ject/googleplaydownloader), il vous faudra configurer un compte Google valide dans les "settings" afin de télécharger les applications.

## Utilisation de Google Play Downloader
Ce logiciel permet de télécharger directement les applications Android  depuis le Play Store, sachez cependant que certaines applications ne sont pas visibles à travers cet outil, même si elles existent bel et bien sur le Play Store... Si vous réussisez à trouver toutes vos applications, je vous conseille très fortement de rester sur cette méthode et de ne pas passer par la méthode ci-dessous beaucoup plus fastidieuse... Sautez directement à la section **Installation et suppression d'applications en masses**

## Activation du Play Store et téléchargement

L'idée est donc de procéder de la sorte pour installer des applications en dernière minute.
1. Créer un compte Google pour accéder au Google Play
2. Configurer les Google Apps de la tablette avec le compte créé précédemment 
  3. Il se peut que l'icon du Google Play store soit caché sur les tablettes Danew, donc 
    4. Menu des applications
    5. Cliquez sur **Paramètres** -> **Applications** -> onglet **Toutes**
    6. Sélectionnez l'application **Google play store**
    7. Puis cliquez sur **Lancer** en milieu/fin de page
    8. Une nouvelle fenêtre s'ouvrira pour vous demander votre login / mot de passe Google
9. Un fois enregistré, téléchargez les applications souhaitées 
10. Télécharger également l'application [**File Expert**](https://play.google.com/store/apps/details?noprocess&id=xcxin.filexpert) pour faire un backup de vos applications téléchargées. 

A ce stade, vous avez téléchargé vos applications gratuites et payantes. Il faut maintenant réaliser un backup de vos nouvelles applications pour les déployer sur toutes vos tablettes.

**ATTENTION** Cette application ne sauvegarde QUE les applications et ne **sauvegarde pas les données**. Cela signifie que certaines applications sauvegardées puis restaurées sur une autre tablette ne fonctionneront pas. Pour sauvegarder les données il faut que la tablette soit ROOTÉE !

1. Lancez **File Expert**
2. Ouvrez le menu de gauche, Icon (=)
3. Descendez jusqu'à **Catégories** et cliquez sur **Applications**
4. Sélectionnez **Applications installées**
5. Dans le panneau qui vient de s’ouvrir, sélectionnez (par un appui long) les applications que vous souhaitez sauvegarder.
6. Une fois effectué, cliquez sur l'icône en haut à droite, en forme de cercle avec un point au milieu, ceci lancera la sauvegarde de toutes vos applications précédemment sélectionnées
7. Une fois le backup effectué, ouvrez le menu de gauche à nouveau et sélectionnez **Stockage interne**, cliquez sur **backup_apps**, vous devriez retrouver toutes vos applications sauvegardées.
8. Enfin pour les récupérer sur votre poste, connectez la tablette à votre ordinateur grâce au cordon USB 
9. Lorsque la fenêtre s'ouvrira, sélectionnez **Stockage interne** et copiez toutes les applications sauvegardées sur votre ordinateur.

Vous êtes maintenant en possession de toutes les applications que vous avez téléchargées et êtes maintenant prêt à les installer sur vos tablettes.

## Installation et suppression d'applications en masses

### Pour les tablettes Danew 
Si c'est la première fois que vous connectez une tablette Danew à votre ordinateur, il se peut que ce dernier ne sache pas communiquer correctement avec les tablettes de modèle Danew. Il faut donc exécuter cette commande dans un terminal  
`echo "0x0e8d" > ~/.android/adb_usb.ini`  
Et ajouter cette ligne `SUBSYSTEM=="usb", ATTR{idVendor}=="0e8d", MODE="0666", GROUP="plugdev"` dans le fichier `/etc/udev/rules.d/51-android.rules`

### L'utilitaire ADB

Un utilitaire appelé `ADB` disponible sous Linux permet grâce à une ligne de commande d'installer une collection de fichier **.apk** (application Android) sur un appareil Android. 

> Si l'utilitaire ADB n'est pas installé sous votre PC, voici la commande à exécuter pour l'installer sous un système Linux 
`sudo apt-get install android-tools-adb`

Par défaut il n'est pas possible d'installer directement des applications depuis la ligne de commande. Si le pack google play n'est pas installé  sur l'appareil, le seul moyen d'installer des applications est via l'utilitaire en ligne de commande ABD. 

**[Il faut donc dans un premier temps autoriser l'installation d'applications tierces dans les paramètres d'Android.](http://www.frandroid.com/comment-faire/lemultimedia/231266_autoriserlessourcesinconnues)**

###Désintallation d'applications
Vouz aurez peut être la mauvaise surprise de devoir désintaller certaines applications pour en installer d'autres (problème d'espace mémoire).  

Pour ce faire, vous devrez repérer le nom de l'application. 

Ex : [Helium - App Sync and Backup](https://play.google.com/store/apps/details?noprocess&id=com.koushikdutta.backup&hl=fr)  
La barre d'URL contient le nom complet de l'application : 
https://play.google.com/store/apps/details?id=com.koushikdutta.backup&hl=fr  
Le nom est juste après **id=** soit **com.koushikdutta.backup**

Repérez et notez toutes les applications que vous désirez supprimer dans un fichier `app_a_supprimer.csv`  

###Rapatriement des APK
Si vos applications se trouvaient sur une tablette rapatriez les sur votre ordinateur dans un dossier nomée `apk`


Créez un dossier `android_app` quelque part sur votre ordinateur (ex :  `/home/jeanmichel`)
 - Déplacez le fichier `app_a_supprimer.csv` et le dossier `apk` dans votre nouveau dossier `android_app`
 - Créez un fichier `delete_install_android_app.sh` et collez le contenu ci-dessous  
 ```#!/bin/bash
while IFS='' read -r line || [[ -n "$line" ]]; do
	    adb uninstall $line
done < "app_a_supprimer.csv"  
find apk/ -name '*.apk' -exec adb install -r {} \;```
 - Ouvrez un terminal
 - Déplacez vous dans votre dossier de travail, ex `cd /home/jeanmichel/android_app`
 - Rendez le fichier `delete_install_android_app.sh` exécutable avec `chmod +x delete_install_android_app.sh`
 - Lancez le script de suppression et d'installation des application `./delete_install_android_app.sh`
 - Le script ci-dessus aura pour effet de supprimer les applications listé dans le fichier CSV puis d'installer toutes les applications disponibles dans le dossier APK. 
 - Vous aurez enfin à placer manuellement les icônes des nouvelles applications sur le bureau.
