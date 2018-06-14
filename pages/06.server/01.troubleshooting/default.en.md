---
title: Troubleshooting
---

# Troubleshooting the Server

##The server doesn't turn on
**Symptom**: the server doesn't turn on when you press the button 
- Verify that the power cord is correctly plugged in.  Unplug it and plug it back in.
- Vérify the battery is charged.
- Try with the power blog supplied with the server plugged into the 220v main power.
- If it still doesn't work, the servir is defective, and needs to be returned to the manufacturer for repairs.  Contage BSF headquarters. 

## The charger doesn't charge the battery
- First, make sure that the charger has a power supply.
- If it is connected to the power supply, verify the connections between the charger and the exterior IEC plug of the yellow module.
- Check the voltage with a voltmeter.  If it is at 0, verify the connection between the terminals of the charger and the battery.
- Make sure the terminals are in good shape (unscrew the bolts, sandpaper the connectors and the copper plate, unscrew and reconnect the connectors between the charger and the battery)
-  If it still doesn't work, take out the battery and recharge it with a current charger (automobile type)
-  If it turns out that the battery can't be recharged, replace it with a model available in your area (12V, 160Ah, ideally a gel battery, but a other models will do the job for a short time).
-  If the battery can recharge, recharge it quickly to avoid significant loss of charge.

## Le hotspot Ideasbox n'apparait pas
- Connecter un écran au serveur (à défaut, un video projecteur) et vérifier que l’interface graphique fonctionne. 
- Redémarrer le serveur une première fois et attendre quelques minutes, vérifier si le hotspot apparaît à nouveau.
- Contacter BSF pour une intervention à distance 

## J'ai perdu le mot de passe admin

* Brancher un clavier, une souris et un écran au serveur pour accéder à l'interface graphique.
* Une fois l'écran branché, rentrer le login : ideascube et le mot de passe que BSF vous a transmis
* Une fois connecté, cliquer en bas à gauche sur l'icône menu et sélectionnez "Outils système > LXTerminal"
* Dans le LXTerminal, tapez : ```ideascube changepassword admin``` (```admin``` ou un autre utilisateur).