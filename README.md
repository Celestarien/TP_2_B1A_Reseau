# TP 2 RÉSEAU
## I) Exploration locale en solo

### 1) Affichage d'informations sur la pile TCP/IP locale

#### **Affichez les infos des cartes réseau de votre PC :**


* Pour l’interface Wi-Fi :
1)	Appuyez sur : ```(la touche Windows) + R```
2)	Tapez ```« cmd »``` et appuyez sur la touche ```« ENTRÉE »```
3)	Par la suite tapez ```« ipconfig -all »```
4)	Cherchez la ligne ```« Carte réseau sans fil Wi-Fi : »``` qui n’est d’autre que le nom de votre carte réseau sans fil
5)	Dans cette catégorie, cherchez la ligne ```« Adresse physique »``` qui correspond à votre adresse MAC (elle est unique)
6)	Ensuite si vous désirez trouver votre adresse IP, cherchez la ligne ```« Adresse IPv4 »```


###### Adresse de réseau = 10.33.0.0/22
###### Adresse de broadcast = 10.33.3.255


* Pour l’interface Ethernet :
1)	Appuyez sur : ```(la touche Windows) + R```
2)	Tapez ```« cmd »``` et appuyez sur la touche ```« ENTRÉE »```
3)	Par la suite tapez ```« ipconfig -all »```
4)	Cherchez la ligne ```« Carte Ethernet Ethernet : »``` qui n’est d’autre que le nom de votre carte réseau ethernet
5)	Dans cette catégorie, cherchez la ligne ```« Adresse physique »``` qui correspond à votre adresse MAC (elle est unique)
6)	Ensuite si vous désirez trouver votre adresse IP, cherchez la ligne ```« Adresse IPv4 »``` (vous pouvez la voir uniquement si votre PC est branché en Ethernet à votre routeur)
###### La carte Ethernet ne possède pas d’adresse IP donc il nous est impossible de calculer son adresse de réseau et donc aussi son adresse de broadcast.


#### **Affichez votre gateway :**

1)	Appuyez sur : ```(la touche Windows) + R```
2)	Tapez ```« cmd »``` et appuyez sur la touche ```« ENTRÉE »```
3)	Par la suite tapez ```« ipconfig -all »```
4)	Cherchez la ligne ```« Carte réseau sans fil Wi-Fi : »```
5)	Dans cette catégorie, cherchez la ligne ```« Passerelle par défaut »``` qui correspond à votre gateway



#### **Affichez les informations réseau avec un interface graphique :** 

1)	Allez dans vos paramètres
2)	Cliquez sur « Réseau et Internet »
3)	Cherchez « Modifier vos paramètres réseau » puis cliquez « Modifier les options d’adaptateur »
4)	Double-cliquez sur l’interface que vous souhaitez
5)	Et enfin, cliquez sur « Détails… »

À quoi sert la gateway dans le réseau d'Ingésup ?
Son but est de faire la liaison entre deux réseaux, afin de faire l'interface entre des protocoles réseau différents.

### 2) Modifications des informations

##### A. Modification d'adresse IP - pt. 1


###### 1ère IP du réseau = 10.33.0.1
###### Dernière IP du réseau = 10.33.3.254
* Pour modifier votre adresse IP avec une interface graphique :
1)	Allez dans vos paramètres
2)	Cliquez sur ```« Réseau et Internet »```
3)	Cherchez ```« Modifier vos paramètres réseau » puis cliquez « Modifier les options d’adaptateur »```
4)	Double-cliquez sur votre interface Wi-Fi
5)	Cliquez sur ```« Propriétés »```
6)	Cherchez et double-cliquez sur ```« Protocole Internet version 4(TCP/IPv4) »```
7)	Cochez la case ```« Utiliser l’adresse IP suivante : »```
8)	Remplissez dans ```« Adresse IP »``` votre adresse IP actuelle mais en changeant le dernier chiffre.
9)	Remplissez votre masque de sous-réseau par votre masque réseau actuelle
10)	Remplissez ```« Passerelle par défaut »``` par votre gateway/passerelle par défaut actuelle
11)	Pour finir, cliquez sur ```« Ok »```


##### B.Nmap


1)	Appuyez sur : ```(la touche Windows) + R```
2)	Tapez ```« cmd »```
3)	 Faites un clic droit dessus et cliquez sur ```« Ouvrir en tant qu’administrateur »```
4)	Tapez la commande : ```« cd\ »```
5)	Puis accédez à votre répertoire où se situe Nmap
6)	Par la suite tapez : ```« nmap -sn -PE <ADRESSE_DU_RESEAU_CIBLE> »```
7)	Cherchez un adresse IP libre


##### C. Modification d'adresse IP - pt. 2
1)	Allez dans vos paramètres
2)	Cliquez sur ```« Réseau et Internet »```
3)	Cherchez ```« Modifier vos paramètres réseau »``` puis cliquez ```« Modifier les options d’adaptateur »```
4)	Double-cliquez sur votre interface Wi-Fi
5)	Cliquez sur ```« Propriétés »```
6)	Cherchez et double-cliquez sur ```« Protocole Internet version 4(TCP/IPv4) »```
7)	Cochez la case ```« Utiliser l’adresse IP suivante : »```
8)	Remplissez dans ```« Adresse IP  »``` votre adresse IP actuelle mais en changeant le dernier chiffre.
9)	Remplissez votre masque de sous-réseau par votre masque réseau actuelle
10)	Remplissez ```« Passerelle par défaut »``` par une gateway aléatoire
11)	Pour finir, cliquez sur ```« Ok »```

