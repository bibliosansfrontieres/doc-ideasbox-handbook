# Dépannage du serveur

##Le serveur ne démarre pas
**Symptôme** : le serveur ne s’allume pas quand on appuie sur le bouton.
- Vérifier que le connecteur d’alimentation est  correctement enfiché. Le débrancher et le rebrancher.
- Vérifier que la batterie est chargée
- Essayer avec le bloc d'alimentation fourni avec le serveur et le brancher sur le secteur 220v.
- S’il ne s’allume toujours pas, le serveur est matériellement défaillant et doit être retourné au constructeur pour réparation. Contacter le siège de BSF. 

## Le chargeur ne charge pas la batterie
Il faut vérifier en premier lieu son alimentation électrique. Si elle est fonctionnelle, vérifier les connexions entre le chargeur et la prise IEC extérieure au module jaune. Si ces connexions sont bonnes, examiner les tensions à l'aide d'un voltmètre : s’il reste à 0, vérifier la connexion entre les bornes de sortie du chargeur et les bornes de la batterie. Si elles sont correctes (dévisser les boulons, passer au papier de verre les connecteurs et la plaque de cuivre, dévisser/revisser les connexions entre le chargeur et la batterie), sortir la batterie et la recharger en utilisant un chargeur courant (type automobile). 
S’il s’avère que la batterie ne peut être rechargée, la remplacer par un modèle disponible sur le terrain (12v 160 ah idéalement au gel, mais un modèle type démarrage, à électrolyte liquide, fera l’affaire pour quelques temps). 
Si la batterie peut être rechargée, la recharger au plus vite pour éviter les décharges profondes. 

## Le hotspot IdeasBox n'apparait pas
- Connecter un écran au serveur (à défaut, un vidéoprojecteur) et vérifier que l’interface graphique fonctionne. 
- Redémarrer le serveur une première fois et attendre quelques minutes, vérifier si le hotspot apparaît à nouveau.
- Contacter BSF pour une intervention à distance 

## J'ai perdu le mot de passe admin

* Brancher un clavier, une souris et un écran au serveur pour accéder à l'interface graphique.
* Une fois l'écran branché, rentrer le login : ```ideascube``` et le mot de passe que BSF vous a transmis
* Une fois connecté, cliquer en bas à gauche sur l'icône menu et sélectionnez "Outils système > LXTerminal"
* Dans le LXTerminal, tapez : ```ideascube changepassword admin``` (```admin``` ou un autre utilisateur).
