---
title: 'Wireless/Radio Internet Connection (Ubiquiti)'
---

Ubiquiti WiFi antennas allow you to establish wireless connections.
They support 3 operation modes:

- Station
- Acces point
- AP-Repeater

In our context, we use WiFi antennas in the **Access Point** and **Station** modes, in order to create a WiFi connection between two antennas that can distrbute the internet across a large area.

>>>>>**Before any deployment, it is absolutely necessary to conduct a feasibility study to have a quick overview of what the hardware will be able to do.**

The key is to base your study on photos taken between point A and point B to determine if a direct link can be established.  This is certainly the most important step!

Next, it is [possible to calculate the loss in dB](https://www.pasternack.com/t-calculator-fspl.aspx) between two antennas if you know the antenna gain, the distance between two points and the frequency used.  For example, a tree situated between the two antennas will decrease the signal power by 5dB.

[Use AirLin](https://airlink.ubnt.com/), an online too distributed by Ubiquiti in order to verify the distance between point A and point B.  The software will also give you an indication of the elevation of the terrain and the height necessary for the mast supporting the antenna.
You can also check with [GeoPortail](http://www.geoportail.gouv.fr). If the Ideas Box will be deployed in France, you will have access to the altitude of your installation site.  It is always good to cross-check the information.  If not, use Google Maps or Open Street Maps to get an idea of buildings which could be located between the antennas.

In order to function well, the antennas need to "see eachother."  It is thus essential to place them at a good height.  If a building is located between the antennas, it is very possible that the connection will not be able to be established.

If you cannot visit the location yourself, discuss the site with your partners to get as much information about it as possible, such as:
- GPS coordinates of point A and point B
- Altitude of the two points
- Nature of the buildings around point A and B (local, house, appartment building, number of floors, can you attach the antenna somewhere, can you mount the antenna, etc...)
- Are there tall buildings between point A and point B?
- Can the antenna be placed higher than these buildings?


![Type of antenna used](serveimage.jpeg)

##Technical specifications
* Model: [Nanostation M5](http://www.ldlc.com/fiche/PB00142273.html) 
* Guid price: 99 €
* Power: 0.5 A @24V (power supplied)
* Max power consumption: 8W  
* Gain: 16 dBi
* Temperatures at which antenna can function: -30 à 75°C  
* Frequencies at which antenna can function: 5170 - 5875 Hz
* Beamwidth: 43° (H-pol) / 41° (V-pol) / 15° (Elevation)

The diagrams below give the vertical and horizontal angles covered by the WiFi antenna.  For example, you can see that the "Vertical Elevation" has an angle that permits it to send the waves towards the ground rather than into the air.

![](nsm5.png)


---


## Generalizations about the Radio

*A radiocommunication is a telecommunication performed in the air using electromagnetic waves.  These waves constitute a transmission of energy that manifest itself in the form of an electric field couples with a magnetic field.  The information is transported thanks to constant modulation of the properties of the wave (its amplitude, frequency, phase, or wavelength among other things)  See [wikipedia](https://fr.wikipedia.org/wiki/Radiocommunication) for more information.*

**Units**
* Frequency: hertz
* Bandwidth: hertz
* Power: watt

The WiFi network functions on the following frequencies: 2.4 ghz or 5 ghz

It is possible to calculate the range of a WiFi network with the following formula:

$$ D = G x P $$
 - D: distance
 - G: Gain de l'antenne en dBi
 - P: Puissance en watt
 
## Configuration et mise en oeuvre

### Matériel à prévoir 
* Acheter plusieurs adaptateurs passifs - 
* Ajouter un multimètre (dans la valise à moustaches normalement)
* ajouter du colson dans la boite (à ajouter dans la valise à moustaches)
* Amener **PLEINS** de câbles Ethernet

### Première connexion
Suivez le plan de montage disponible dans la boite de l'antenne. Deux câbles réseaux seront nécessaire au montage.

Au premier lancement l'antenne est acessible à l'adresse [http://192.168.1.20](http://192.168.1.20), vérifiez avant le démarrage de l'antenne que cette adresse IP n'est pas attribué à une autre machine, si cela le cas, cela engendrera un conflit d'adresse IP et votre antenne ne sera pas accessible.

Une fois connecté au site web, entrez les identifiants par défaut (à changer après la première connexion)

**Login: **ubnt   
**Mot de passe: **ubnt

désactiver https pour l'accès à la console d' admin

-----
**Note sur le protocole AirMax:**  
*airMAX is Ubiquiti’s proprietary Time Division Multiple 
Access ( TDMA) polling technology. airMAX improves 
overall performance in Point-to-Point (PtP) and 
Point-to-MultiPoint (PtMP) installations and noisy 
environments because it reduces latency, increases 
throughput, and offers better tolerance against 
interference.*  
Ce protocole étant propriétaire nous préférons le laissez désactivé dans la mesure du possible 

**Note sur airView: **  
*Use the airView Spectrum Analyzer to analyze the noise 
environment of the radio spectrum and intelligently select 
the optimal frequency to install a PtP airMAX link. *


> A chaque changement de configuration, n'oubliez pas de cliquer sur **Apply** pour prendre en compte vos modifications



## 1ere antenne 
Il s'agit de l'antenne qui va délivrer l'accès Internet et qui sera donc connecté au réseau des réseaux.

### Premier onglet
- Décocher l'option airMax

### Onglet WIRELESS
La Consommation est d'environ 3 à 4 watts

- **Wireless mode**: Access-Point
- **Activer WDS**
- **SSID**: Sélectionner un SSID, celui-ci devra être le même pour les 2 antennes
- **Country Code**: Chaque pays dispose de sa propre régulation au niveau des normes de radiocommunication. Sélectionnez le pays dans lequel vous déployez cet équiement 
- **Channel Width** : Séléctionnez `20 Mhz`. Plus ce chiffre est élevé plus la vitesse de transmission des données est élevés. Cependant cette fréquence est également compatible avec le standard wifi utilisé par les appareils mobiles. Enfin il est également possible d'utiliser le paramètre `Auto 20/40Mhz`
- **EIRP Limit** : Cocher cette case, cela permet de de contraindre l'appareil à suivre les régles définis par le **country code**. Cependant, si vous constater un problème de liaison entre les 2 antennes, décochez le `EIRP Limit` et mettre  à fond le curseur de `output power`, sachez cependant que votre équipement ne respectera plus la loi du pays et que vous exposez vous ou votre partenaires à des poursuites.
- **Wireless security** : Sélectionnez WPA2 et choisir un mot de passe
- **Frequency** : choisir 5180. Quand on utilise des antenne en mode relais : choisir 2 fréquences éloignées pour éviter les collusions entre les fréquences

### Onglet NETWORK
- **Network Mode**: Bridge
- **Management Network Settings**: 
  - Static
  - IP Address : Choisissez une adresse IP disponible sur le réseau et si possible bloquer cette adresse IP dans le serveur DHCP afin qu'elle ne soit pas attribué à une autre machine.     
**Attention: ** Les 2 bornes wifi devront être sur le même réseau local pour pouvoir communiquer.

### Onglet ADVANCED
- Instal EIRP Control: Cochez cette case

## 2nd antenne 

### Onglet WIRELESS
La Consommation est d'environ 3 à 4 watts

- **Wireless mode**: Station
- **Activer WDS**
- **SSID**: Sélectionner un SSID, celui-ci devra être le même pour les 2 antennes
- **Country Code**: Chaque pays dispose de sa propre régulation au niveau des normes de radiocommunication. Sélectionnez le pays dans lequel vous déployez cet équiement 
- **Channel Width** : Séléctionnez `20 Mhz`. Plus ce chiffre est élevé plus la vitesse de transmission des données est élevés. Cependant cette fréquence est également compatible avec le standard wifi utilisé par les appareils mobiles. Enfin il est également possible d'utiliser le paramètre `Auto 20/40Mhz`
- **EIRP Limit** : Cocher cette case, cela permet de de contraindre l'appareil à suivre les régles définis par le **country code**. Cependant, si vous constater un problème de liaison entre les 2 antennes, décochez le `EIRP Limit` et mettre  à fond le curseur de `output power`, sachez cependant que votre équipement ne respectera plus la loi du pays et que vous exposez vous ou votre partenaires à des poursuites.
- **Wireless security** : Sélectionnez WPA2 et choisir un mot de passe
- **Frequency** : choisir une fréquence éloigné de 5180. Quand on utilise des antenne en mode relais : choisir 2 fréquences éloignées pour éviter les collusions entre les fréquences

### Onglet NETWORK
- **Network Mode**: Bridge
- **Management Network Settings**: 
  - Static
  - IP Address : Choisissez une adresse IP disponible sur le réseau et si possible bloquer cette adresse IP dans le serveur DHCP afin qu'elle ne soit pas attribué à une autre machine.     
**Attention: ** Les 2 bornes wifi devront être sur le même réseau local pour pouvoir communiquer.

## Dépannage et conseils
**Chan IRC** : `#tetaneutral` sur freenode ou `#lqdn`
guerby    
**Pour débuguer** : tcpdump ou wiresharkœ + ping

## Documents de références : 
- [Wikipedia](https://en.wikipedia.org/wiki/Ubiquiti_Networks)
- [Page du produit](https://www.ubnt.com/airmax/nanostationm/)
- [Quick start guide](https://dl.ubnt.com/guides/NanoStation_M/NanoStation_M_Loco_M_QSG.pdf)
- [AirOS Guide](https://dl.ubnt.com/guides/airOS/airOS_UG.pdf)
- [Data Sheet](https://dl.ubnt.com/datasheets/nanostationm/nsm_ds_web.pdf)