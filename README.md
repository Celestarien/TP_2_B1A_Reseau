# TP 2 RÉSEAU
## I) Exploration locale en solo

### 1) Affichage d'informations sur la pile TCP/IP locale

#### **Affichez les infos des cartes réseau de votre PC :**


* Pour l’interface Wi-Fi :
1)	Appuyez sur ```(la touche Windows) + R```
2)	Tapez ```« cmd »``` et appuyez sur la touche ```« ENTRÉE »```
3)	Par la suite tapez ```« ipconfig -all »```
4)	Cherchez la ligne ```« Carte réseau sans fil Wi-Fi : »``` qui n’est autre que le nom de votre carte réseau sans fil
5)	Dans cette catégorie, cherchez la ligne ```« Adresse physique »``` qui correspond à votre adresse MAC (elle est unique)
6)	Ensuite si vous désirez trouver votre adresse IP, cherchez la ligne ```« Adresse IPv4 »```


###### Adresse de réseau = 10.33.0.0/22
###### Adresse de broadcast = 10.33.3.255


* Pour l’interface Ethernet :
1)	Appuyez sur ```(la touche Windows) + R```
2)	Tapez ```« cmd »``` et appuyez sur la touche ```« ENTRÉE »```
3)	Par la suite tapez ```« ipconfig -all »```
4)	Cherchez la ligne ```« Carte Ethernet Ethernet : »``` qui n’est autre que le nom de votre carte réseau éthernet
5)	Dans cette catégorie, cherchez la ligne ```« Adresse physique »``` qui correspond à votre adresse MAC (elle est unique)
6)	Ensuite si vous désirez trouver votre adresse IP, cherchez la ligne ```« Adresse IPv4 »``` (vous pouvez la voir uniquement si votre PC est branché en Ethernet à votre routeur)
###### La carte Ethernet ne possède pas d’adresse IP donc il nous est impossible de calculer son adresse de réseau et donc aussi son adresse de broadcast.


#### **Affichez votre gateway :**

1)	Appuyez sur ```(la touche Windows) + R```
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
Son but est de réaliser la liaison entre deux réseaux, afin de faire l'interface entre des protocoles réseau différents.

![Image pour TP 2](https://user-images.githubusercontent.com/43401854/50291529-24fdbb00-046f-11e9-8b12-5da1f33bc328.png)

### 2) Modifications des informations

##### **A. Modification d'adresse IP - pt. 1**


###### 1ère IP du réseau = 10.33.0.1
###### Dernière IP du réseau = 10.33.3.254
#### **Pour modifier votre adresse IP avec une interface graphique :**
1)	Allez dans vos paramètres
2)	Cliquez sur ```« Réseau et Internet »```
3)	Cherchez ```« Modifier vos paramètres réseau »``` puis cliquez ```« Modifier les options d’adaptateur »```
4)	Double-cliquez sur votre interface Wi-Fi
5)	Cliquez sur ```« Propriétés »```
6)	Cherchez et double-cliquez sur ```« Protocole Internet version 4(TCP/IPv4) »```
7)	Cochez la case ```« Utiliser l’adresse IP suivante : »```
8)	Remplissez dans ```« Adresse IP »``` votre adresse IP actuelle mais en changeant le dernier chiffre.
9)	Remplissez votre masque de sous-réseau par votre masque réseau actuel
10)	Remplissez ```« Passerelle par défaut »``` par votre gateway/passerelle par défaut actuelle
11)	Pour finir, cliquez sur ```« Ok »```


##### **B.Nmap**


1)	Appuyez sur ```(la touche Windows) + R```
2)	Tapez ```« cmd »```
3)	 Faites un clic droit dessus et cliquez sur ```« Ouvrir en tant qu’administrateur »```
4)	Tapez la commande : ```« cd\ »```
5)	Puis accédez à votre répertoire où se situe Nmap
6)	Par la suite tapez : ```« nmap -sn -PE <ADRESSE_DU_RESEAU_CIBLE> »```
7)	Cherchez une adresse IP libre


##### **C. Modification d'adresse IP - pt. 2**
1)	Allez dans vos paramètres
2)	Cliquez sur ```« Réseau et Internet »```
3)	Cherchez ```« Modifier vos paramètres réseau »``` puis cliquez ```« Modifier les options d’adaptateur »```
4)	Double-cliquez sur votre interface Wi-Fi
5)	Cliquez sur ```« Propriétés »```
6)	Cherchez et double-cliquez sur ```« Protocole Internet version 4(TCP/IPv4) »```
7)	Cochez la case ```« Utiliser l’adresse IP suivante : »```
8)	Remplissez dans ```« Adresse IP  »``` votre adresse IP actuelle mais en changeant le dernier chiffre.
9)	Remplissez votre masque de sous-réseau par votre masque réseau actuel
10)	Remplissez ```« Passerelle par défaut »``` par une gateway aléatoire
11)	Pour finir, cliquez sur ```« Ok »```


## II) Exploration locale en duo

### 1) Prérequis
* Deux Pcs avec ports RJ45
* Un câble RJ45
* **Firewalls désativés** sur les deux PCs

### 2) Câblage
Prenez un câble (RJ45) et branchez-le des deux côtés.

### 3) Modification d'adresse IP

###### Pour réaliser les actions suivantes, il faut relier vos 2 PCs avec un câble RJ45 !

#### **Modifiez l'IP de 2 machines afin qu'elles soient dans un même réseau :**

1)	Allez dans vos paramètres
2)	Cliquez sur ```« Réseau et Internet »```
3)	Cherchez ```« Modifier vos paramètres réseau »``` puis cliquez ```« Modifier les options d’adaptateur »```
4)	Double-cliquez sur votre interface Wi-Fi
5)	Cliquez sur ```« Propriétés »```
6)	Cherchez et double-cliquez sur ```« Protocole Internet version 4(TCP/IPv4) »```
7)	Cochez la case ```« Utiliser l’adresse IP suivante : »```
8)	Remplissez dans ```« Adresse IP  »``` l'adresse IP que vous souhaitez.
###### :a: **TTENTION** : Les 3 premiers chiffres de l'adresse IP doivent être identiques sur les 2 PCs !
9)	Remplissez votre masque de sous-réseau par ```« 255.255.255.0 »```

#### **Vérification des changements :**

1)	Appuyez sur ```(la touche Windows) + R```
2)	Tapez ```« cmd »``` et appuyez sur la touche ```« ENTRÉE »```
3)	Par la suite tapez ```« ipconfig -all »```
4) Cherchez la ligne ```« Adresse IPv4 »``` et regardez si l'adresse IP correspond à celle que vous avez entré

#### **Testez la connectivité entre les 2 machines :**
1)	Appuyez sur ```(la touche Windows) + R```
2)	Tapez ```« cmd »``` et appuyez sur la touche ```« ENTRÉE »```
3) Tapez la commande ```« ping <L'adresse IP de la seconde machine> »```

### 4) Utilisation d'un des deux ordinateurs comme gateway

#### **Utilisez Internet grâce à un second PC :**

1) Désactivez l'interface WiFi sur l'un des deux postes
2) S'assurer de la bonne connectivité entre les deux PCs à travers le câble RJ45

3) Sur le PC qui n'a plus internet, définir comme passerelle l'adresse IP de l'autre PC sur la carte Ethernet

4) Sur le PC qui a toujours internet :

* Tapez dans votre barre de recherche ```« Paramètres »```

* Cliquez sur ```« Réseau et Internet »```

* Cherchez ```« Modifier vos paramètres réseau »``` puis cliquez ```« Modifier les options d’adaptateur »```

* Double-cliquez sur votre interface Wi-Fi

* Cliquez sur ```« Propriétés »```

* Puis cliquez sur ```« Partage »```

* Cochez ```« Autoriser d'autres utilisateurs du réseau à se connecter via la connexion Internet de cet ordinateur »```

* Et pour finir, cliquez sur ```« Ok »```

#### **Testez la connectivité :**

1)	Appuyez sur ```(la touche Windows) + R```
2)	Tapez ```« cmd »``` et appuyez sur la touche ```« ENTRÉE »```
3) Tapez la commande ```« ping <L'adresse IP de la seconde machine> »```

### 5) Petit "chat" privé ?

#### prérequis :

* Installation de netcat
* 2 PCs (un client et un serveur)

#### Utilisation de netcat :

##### Le PC client :

* Exécutez la commande ```« nc.exe <IP du serveur> <port d'écoute> »```

##### Le PC serveur :

* Exécutez la commande ```« nc.exe -l -p <port d'écoute> »```


## III) Manipulations d'autres outils/protocoles côté client

### 1) DHCP

#### Afficher le DHCP :

* Allez dans vos paramètres
* Puis allez dans ```« Réseau et Internet »```
* Cliquez sur ```« Modfier les options d'adaptateur »```
* Ensuite, cliquez 2 fois sur votre réseau
* Allez dans ```« Détails... »```
* Et cherchez la ligne ```« Serveur DHCP IPv4 »```

#### Date d'expiration du bail :

* Allez dans vos paramètres
* Puis allez dans ```« Réseau et Internet »```
* Cliquez sur ```« Modfier les options d'adaptateur »```
* Ensuite, cliquez 2 fois sur votre réseau
* Allez dans ```« Détails... »```
* Et cherchez la ligne ```« Bail expirant »```

#### Changer d'IP :

1)	Appuyez sur ```(la touche Windows) + R```
2)	Tapez ```« cmd »``` et appuyez sur la touche ```« ENTRÉE »```
3) Tapez la commande ```« ipconfig /release »```

### 2) DNS

#### Afficher le DNS :

* Allez dans vos paramètres
* Puis allez dans ```« Réseau et Internet »```
* Cliquez sur ```« Modfier les options d'adaptateur »```
* Ensuite, cliquez 2 fois sur votre réseau
* Allez dans ```« Détails... »```
* Et cherchez la ligne ```« Serveur DNS IPv4 »```

#### Lookup

###### Le ```lookup``` nous permet de savoir l'IP d'un domaine à partir de son nom.

#### Reverse lookup

###### Le ```reverse lookup``` quant à lui nous permet de connaitre le nom de domaine à partir d'une IP.


