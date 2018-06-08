---
title: 'Communiquer avec les Autres'
---

Les réseaux de communications et Internet ont rendu les communications
avec les autres plus aisées que jamais, mais ont répandu la surveillance
d’une manière que l’histoire de l’humanité n’a jamais connu. Sans
prendre de mesures supplémentaires afin de protéger votre intimité,
chaque appel téléphonique, message de texte, e-mail, message
instantanée, appel vocal IP, vidéo, chat et message au moyen des médias sociaux peut être vulnérable
pour les espions.

Souvent, la manière la plus sûre de communiquer avec les autres est de
le faire en personne, sans ordinateurs ni implication quelconque de
téléphones. Ce n’est pas toujours possible, la meilleure des choses à
faire est donc d'utiliser le chiffrement global
si vous communiquez sur un réseau et avez besoin de protéger le contenu
de vos communications.


# Comment fonctionne le chiffrement Global !

Lorsque deux personnes souhaitent communiquer de manière sécurisée (par
exemple, Akiko et Boris), elles doivent générer des crypto clés. Avant
qu’Akiko n’envoie un message à Boris, elle devra le chiffrer grâce au
code de Boris afin que seul ce dernier puisse le déchiffrer puis, elle envoie le message déjà chiffré sur Internet. Si quelqu’un
espionne Akiko et Boris—et même s’il a accès au service utilisé par
Akiko afin d’envoyer ce message (comme son compte e-mail) —il ne pourra
visualiser que les données chiffrées et ne pourra pas lire le message.
Lorsque Boris le reçoit, il doit utiliser son code afin de de le
déchiffrer et de rendre le message lisible.

Le chiffrement global implique un certain effort, mais il s’agit de la
seule manière grâce à laquelle les utilisateurs peuvent vérifier la
sécurité de leurs communications sans devoir faire confiance à la
plate-forme qu’ils utilisent. Certains services, tels que Skype, ont
[prétendu](https://support.skype.com/en/faq/fa10983/what-are-p2p-communications)
offrir un chiffrement global, il n’en est rien. Afin que le chiffrement
global soit sécurisé, les utilisateurs doivent pouvoir vérifier que la
crypto clé grâce à laquelle ils chiffrent les messages appartient à la
personne à laquelle ils croient qu’elle doive appartenir. Si le logiciel
de communication ne dispose pas de cette capacité intégrée, tout
chiffrement utilisé peut être intercepté par le prestataire du service lui-même, par
exemple, si un gouvernement l’y oblige.

Vous pouvez lire le livre blanc sur la Liberté d’Expression de la
Fondation, [Travaux de
Chiffrement](https://pressfreedomfoundation.org/encryption-works) afin
d’obtenir des instructions détaillées sur la manière d’utiliser le
chiffrement global pour protéger les messages instantanés et les
e-mails. Assurez-vous de consulter également les modules suivants
d’Autoprotection Digitale contre la Surveillance :

-   [Introduction à la Cryptographie à Clé Publique et
    PGP](/en/module/introduction-public-key-cryptography-and-pgp)
-   [Instructions d’utilisation d’OTR pour
    Windows](/en/module/how-use-otr-windows)
-   [Instructions d’utilisation d’OTR pour
    Mac](/en/module/how-use-otr-mac)


Appels Vocaux
-------------

Lorsque vous réalisez un appel d’un téléphone fixe ou portable, votre
appel n’est pas chiffré dans son intégralité. Si vous utilisez un
téléphone portable, votre appel peut être (faiblement) chiffré entre le
combiné et les antennes-relais. Cependant, si votre conversation voyage
sur le réseau téléphonique, elle est vulnérable à toute interception par
votre prestataire de téléphonie et, en conséquence, aux gouvernements et
organisations qui contrôlent votre compagnie téléphonique. La manière la
plus facile d’assurer que vos conversations vocales sont globalement
chiffrées est d’utiliser VoIP.

Méfiez-vous! Les prestataires les plus célèbres de VoIP, tels que Skype
et Google Hangouts, offrent le chiffrement du
transport afin que les espions ne puissent pas écouter, mais *les prestataires
sont toujours à même de le faire*. En fonction de votre modèle de
menace, ceci peut constituer ou non un problème.

Certains services qui offrent des appels VoIP globalement chiffrés
comprennent :

-   [Ostel](https://ostel.co/)
-   [RedPhone](/en/module/how-use-redphone-android)
-   [Silent Phone](https://silentcircle.com/services#mobile)
-   [Signal pour
    iPhone](/en/module/how-use-signal-%E2%80%93-private-messenger)
-   [Signal pour Android](https://ssd.eff.org/fr/node/93)

Afin de maintenir des conversations VoIP globalement chiffrées, les deux
parties doivent utiliser le même logiciel (ou un logiciel compatible).


Messages de Texte
-----------------

Les SMS n'offrent pas un chiffrement de bout en bout. Si vous voulez envoyer des SMS chiffrés sur votre
téléphone, il vous faudra utiliser une application de messagerie
instantanée chiffré au lieu du SMS.

Quelques applications de messagerie instantanée chiffrées utilisent leur propre protocole. 
 - Les utilisateurs de [Signal](https://ssd.eff.org/fr/node/61/) sur Androïde et iOS peuvent parler de manière sécurisé avec les autres utilisateurs du programme.
 -  [ChatSecure](https://ssd.eff.org/fr/node/51) est une application qui chiffre vos conversations avec OTR sur tous types de réseaux utilisant XMMP, ce qui veut dire que vous pouvez choisir un grand nombre de services de messagerie indépendants.

Messages Instantanés
--------------------

- Off-the-Record (OTR) est un protocole de chiffrement pour les conversations via texte en temps réel, qui peut être utilisé
avec de nombreux services.

Certains outils qui incorporent OTR à la messagerie instantanée
comprennent :

-   [Pidgin](https://ssd.eff.org/fr/module/instructions-utiliser-otr-pour-windows) (pour Windows ou Linux)
-   [Adium](https://ssd.eff.org/fr/node/40/) (pour OS X)
-   [ChatSecure](https://ssd.eff.org/fr/node/51/) (pour iPhone et Android)


E-mails
-------

La plupart des prestataires de services de courrier vous permet d’avoir accès à vos e-mails en utilisant un navigateur Web, comme Firefox ou Chrome. La grande majorité de ces prestataires fournit
un support pour HTTPS ou chiffrement de la couche de transport.  
Vous pouvez savoir si votre prestataire de services de courrier admet
HTTPS si vous vous connectez à votre messagerie Web et l’URL en haut de votre navigateur commence par les lettres HTTPS au lieu de HTTP (par exemple : <https://mail.google.com>).

Si votre prestataire de services de courrier admet HTTPS, mais pas par
défaut, tâchez de remplacer HTTP par HTTPS dans l’URL et actualisez la
page. Si vous souhaitez vous assurer que vous utilisez toujours HTTPS
sur les sites où il est disponible, téléchargez [l’accessoire pour
navigateur HTTPS Everywhere](https://www.eff.org/https-everywhere) pour Firefox ou Chrome.

Certains prestataires de messagerie Web utilisant HTTPS par défaut,
comprennent :

-   GMail
-   Riseup
-   Yahoo

Certains prestataires de messagerie Web vous offrent l’option d’utiliser HTTPS par défaut en le sélectionnant dans vos paramètres. Le service le plus célèbre offrant toujours cette option est Hotmail.

Quelles sont les conséquences du chiffrement de la couche de transport
et pourquoi seriez-vous susceptible d’en avoir besoin ? HTTPS, également dénommé SSL (Couche de Connexion Sécurisée) ou TLS (Sécurité de la Couche de Transport), chiffre vos communications de manière à ce que
personne d’autre ne puisse les lire sur votre réseau. Ceci peut faire
référence aux autres personnes utilisant le même Wi-Fi dans un aéroport ou café, les autres personnes dans votre bureau ou école, les
administrateurs de votre Prestataire de Services Internet, les pirates
informatiques malveillants, les gouvernements ou les agents du maintien de l’ordre. Les communications envoyées sur votre navigateur Web, y compris les pages Web que vous visitez et le contenu de vos e-mails, les publications sur les blogs et les messages, en utilisant HTTP au lieu de  HTTPS sont futiles aux yeux d’un attaquant au moment d’être interceptées et lues.

HTTPS est le niveau le plus basique de chiffrement de navigation Web que nous vous recommandons. Aussi élémentaire que
mettre votre ceinture de sécurité lorsque vous conduisez.

Mais HTTPS ne peut pas tout faire. Lorsque vous envoyez des e-mails en
utilisant HTTPS, votre prestataire de services de courrier obtient
toujours une copie non chiffrée de votre communication. Les
gouvernements et les agences du maintien de l’ordre peuvent avoir accès
à ces données grâce à un mandat. Aux États-Unis, la plupart des
prestataires de services de courrier possède une politique conformément
à laquelle ils doivent porter à votre connaissance toute requête de vos
données d’utilisateur provenant du gouvernement, étant donné qu’ils y
sont légalement autorisés, mais ces politiques sont strictement
volontaires et, dans bon nombre de cas, les prestataires sont légalement
empêchés d’informer les utilisateurs de cette requête de données.
Certains prestataires, comme Google, Yahoo et Microsoft, publient des
comptes rendus sur la transparence, en y détaillant le nombre de
requêtes de données des utilisateurs qu'ils reçoivent en provenance du
gouvernement, quels pays présentent ces requêtes et la fréquence avec
laquelle la compagnie a respecté ces requêtes en remettant ces données.

Si votre modèle de menace comprend un gouvernement ou une agence du maintien de l’ordre, ou que vous ayez d’autres raisons de vous assurer que votre prestataire ne peut pas remettre les contenus de vos communications par e-mail à un tiers, vous pouvez envisager d’utiliser le chiffrement global pour vos communications par e-mail.

PGP (Pretty Good Privacy/Confidentialité Plutôt Bonne) est le standard de chiffrement global de votre courrier. Correctement utilisé, il  offre un protection très forte à vos communications. Afin d’obtenir des instructions détaillées sur la manière d’installer et d’utiliser le chiffrement PGP de votre courrier, cf. :

-   [Instructions d’utilisation de PGP pour Mac OS
    X](/en/module/how-use-pgp-mac-os-x)
-   [Instructions d’utilisation de PGP pour
    Windows](/en/module/how-use-pgp-windows-pc)
-   [Instructions d’utilisation de PGP pour
    Linux](/en/module/how-use-pgp-linux)


## Ce que le chiffrement global ne peut pas faire


Le chiffrement global protège exclusivement le contenu de vos
communications, non les communications en elles-mêmes. Il ne protége pas vos méta-données —c’est-à-dire tout le reste, y compris l’objet de votre e-mail, ou la personne avec qui vous communiquez et quand.

Les métadonnées peuvent fournir des informations extrêmement
révélatrices vous concernant, même lorsque le contenu de vos
communications demeure secret.

Les métadonnées relatives à vos appels téléphoniques peuvent divulguer
certaines informations très intimes et sensibles. Par exemple :

-   Elles savent que vous appelé un service de sexe par téléphone à 2
    heures 24 et parlé pendant 18 minutes, mais elles ne savent pas de
    quoi vous avez parlé.
-   Elles savent que vous appelé la ligne directe pour la prévention des
    suicides du haut du Golden Gate Bridge, mais le sujet de votre appel
    demeure secret.
-   Elles savent que vous avez parlé avec un service de test VIH, puis à
    votre médecin, et enfin à votre compagnie d'assurance santé la même
    heure, mais elles ne savent pas de quoi vous avez discuté.
-   Elles savent que vous avez reçu un appel du bureau local de
    l’Association Nationale des Fusils lorsqu’elle menait une champagne
    contre la législation anti-pistolets, puis qu’elle a appelé les
    sénateurs et les représentants au congrès immédiatement après, mais
    le contenu de ces appels demeure sécurisé contre l’intrusion
    du gouvernement.
-   Elles savent que vous appelé un gynécologue, parlé pendant une
    demi-heure, puis appelé la Planification Familiale plus tard dans la
    journée, mais personne ne sait ce dont vous avez parlé.

Si vous appelez d’un téléphone portable, *les informations concernant
votre position consistent en des métadonnées*. En 2009, Malte Spitz,
politicien du Parti Écologiste, attaqua Deutsche Telekom en justice afin
de la forcer à remettre six mois de données stockés sur son téléphone,
qu’elle avait rendu disponibles à un journal allemand. La visualisation
[en
résultant](http://www.zeit.de/datenschutz/malte-spitz-data-retention/)
démontra un historique détaillé des mouvements de Spitz.

Protéger vos métadonnées requerra d’utiliser d’autres outils, comme
[Tor](/en/module/how-use-tor-windows#overlay=en/node/57/), avec le
chiffrement global.

Afin de visualiser un exemple de la manière dont Tor et HTTPS travaillent ensemble à la protection du contenu de vos communications et métadonnées contre de nombreux attaquants potentiels, vous pouvez
consulter [cette explication](https://www.eff.org/pages/tor-and-https).

Texte original publié sur https://ssd.eff.org/fr/playlist/souhaitez-vous-un-pack-de-s%C3%A9curit%C3%A9-pour-d%C3%A9butants#communiquer-avec-les-autres sous licence CC by.
