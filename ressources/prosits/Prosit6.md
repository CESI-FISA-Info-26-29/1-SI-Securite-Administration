# Fiche de Révision : VPN et Concepts Associés

## Définitions

#### **VPN**
Un **Virtual Private Network** est un réseau privé virtuel utilisant des protocoles de tunnelisation pour établir un canal de communication sécurisé sur un réseau public non sécurisé. Il est souvent utilisé par les entreprises pour connecter différents sites ou pour permettre aux utilisateurs nomades de sécuriser leurs échanges de données.

---

#### **Site-to-site VPN**
Un **site-to-site VPN** connecte les ressources de différents sites via des connexions sécurisées sur un réseau public comme Internet. Il existe deux types :
1. **Basé sur Intranet** : Accessible uniquement en interne.  
2. **Basé sur Extranet** : Partiellement accessible aux entités externes autorisées.

---

#### **Intranet**
Un **Intranet** est un réseau interne, généralement réservé aux employés d'une organisation, non accessible depuis l'extérieur.

---

#### **Extranet**
Un **Extranet** est une extension d'un Intranet, permettant un accès limité à des parties externes autorisées, généralement à travers une connexion sécurisée.

---

#### **VPN Client**
Un logiciel utilisé par des entités distantes pour établir un tunnel VPN sécurisé avec un serveur.

---

#### **IPsec**
**Internet Protocol Security** est une suite de protocoles sécurisant les communications IP en garantissant la confidentialité, l'intégrité et l'authenticité des données échangées via un tunnel sécurisé.

---

#### **MPLS**
**Multiprotocol Label Switching** est une technologie réseau qui combine le routage IP (niveau 3) et la commutation (niveau 2) pour optimiser le trafic réseau et améliorer la rapidité des échanges.

---

#### **PPTP**
**Point-to-Point Tunneling Protocol** est un protocole réseau permettant de créer des VPN via une méthode de tunnellisation point à point.

---

#### **L2TP**
**Layer 2 Tunneling Protocol** est une extension de PPTP, fonctionnant au niveau 2 du modèle OSI pour établir des connexions VPN.

---

#### **AAA**
L'acronyme pour **Authentication, Authorization, Accounting** désigne des protocoles qui gèrent :  
- L'identité des utilisateurs (authentification).  
- Les autorisations d'accès (autorisation).  
- La traçabilité des actions (accounting).

---

#### **GRE**
**Generic Routing Encapsulation** est une méthode de création de connexions point à point privées, utilisée notamment pour les VPN.

---

#### **RSA**
Un système cryptographique asymétrique basé sur le chiffrement avec clés publique et privée. Il repose sur la difficulté de factoriser de grands nombres entiers pour garantir la sécurité des communications.

---

#### **OpenSSL**
Une boîte à outils de chiffrement implémentant les protocoles SSL et TLS, permettant la génération de certificats numériques, de clés cryptographiques et la gestion des communications sécurisées.

---

#### **SSL**
**Secure Socket Layer** est un protocole permettant de sécuriser les communications entre deux ordinateurs en garantissant la confidentialité, l'intégrité et l'authentification des données échangées.

---

#### **TLS**
**Transport Layer Security** est le successeur de SSL. Il est plus sécurisé et plus rapide, offrant des garanties similaires en matière de confidentialité, d'intégrité et d'authentification.

---

#### **Certificat**
Un fichier signé par une autorité de certification, garantissant l'authenticité de son propriétaire et permettant des actions comme la signature, le chiffrement ou l'authentification.

---

#### **PKI**
**Public Key Infrastructure** est une infrastructure permettant la gestion complète du cycle de vie des certificats numériques (création, signature, validation et révocation).

---

#### **X.509**
Une norme pour les certificats numériques contenant des informations sur la clé publique, l'identité de son propriétaire et l'autorité de certification qui l'a émis.

---

#### **Format PEM**
Un format de fichier utilisé pour stocker des certificats, des clés cryptographiques et d'autres données liées à la sécurité, encodées en Base64.

---

#### **Heartbleed**
Une vulnérabilité dans la bibliothèque **OpenSSL** découverte en 2014, permettant à un attaquant de lire la mémoire d'un serveur ou d'un client pour voler des données sensibles.

---

#### **Kerberos**
Un protocole d'authentification réseau basé sur le chiffrement symétrique et l'utilisation de tickets, évitant ainsi l'envoi de mots de passe en clair sur le réseau.

---

#### **OAuth**
Un protocole de délégation d'autorisation permettant à une application tierce d'accéder à une API sécurisée au nom d'un utilisateur, sans partager ses identifiants.

---

#### **SSO**
**Single Sign-On** permet à un utilisateur d'accéder à plusieurs applications avec une seule authentification, simplifiant la gestion des identités.

---

#### **PGP**
**Pretty Good Privacy** est un logiciel hybride de cryptographie combinant cryptage asymétrique et symétrique, souvent utilisé pour sécuriser les emails et fichiers.

---

#### **OpenVPN**
Un protocole et un logiciel VPN basé sur OpenSSL, utilisant des algorithmes de chiffrement robustes comme AES-256 pour sécuriser les communications.

---

#### **LDAPs**
Une version sécurisée du protocole LDAP, utilisant SSL/TLS pour chiffrer les communications et garantir leur confidentialité.

---

#### **Certificat numérique**
Un certificat signé électroniquement garantissant l'authenticité et la sécurité des communications numériques.

---

#### **Autorité de Certification (CA)**
Un organisme délivrant des certificats numériques pour valider l’identité des entités et sécuriser les échanges.

---

#### **Certificat auto-signé**
Un certificat signé par son propre émetteur, généralement utilisé à des fins internes et considéré comme moins sécurisé pour les usages publics.

---

#### **Certificat racine**
Le certificat de base d'une chaîne de confiance, appartenant à une autorité de certification et utilisé pour valider les certificats dérivés.

---

#### **bcrypt**
Un algorithme de hachage sécurisé, utilisé pour protéger les mots de passe en générant un hachage unique à l’aide d’un processus de salage.

---

#### **Wildcard**
Un certificat SSL permettant de sécuriser un domaine et ses sous-domaines grâce à une seule configuration.  

## Questions de Validation

#### **Quels sont les mécanismes garantissant la sécurisation des données d'IPSec ?**
- **ESP** (Encapsulated Security Payload) : Garantit la confidentialité, l'intégrité et l'authenticité des données.  
- **AH** (Authentication Header) : Garantit l'intégrité et l'authenticité des données, mais pas leur confidentialité.

---

#### **Citez les deux modes de fonctionnement d'IPSec :**
1. **Mode Tunnel** : Protège l'intégralité du paquet IP (en-tête et données).  
2. **Mode Transport** : Protège uniquement les données (la charge utile) du paquet IP.

---

#### **Quels sont les deux buts principaux des VPNs ?**
1. **Sécuriser les communications** sur des réseaux publics ou non sécurisés.  
2. **Permettre l’utilisation d’adresses et de protocoles privés** au-dessus de réseaux publics (comme Internet).

---

#### **Lorsque j'utilise la clé privée pour chiffrer, qu'est-ce que j'assure ?**
Cela assure **l'authenticité** du message, car seule la clé publique correspondante peut déchiffrer le message, prouvant qu'il provient du propriétaire de la clé privée.

---

#### **Lorsque j'utilise la clé publique pour chiffrer, qu'est-ce que j'assure ?**
Cela assure la **confidentialité** du message, car seule la personne possédant la clé privée correspondante peut le déchiffrer.

---

#### **Qu'assure le SSL/TLS ?**
- **Confidentialité** : Les données sont chiffrées pour empêcher leur interception.  
- **Authentification** : Vérifie l'identité des parties communicantes.  
- **Intégrité** : Assure que les données échangées n'ont pas été altérées.

---

#### **Qu'est-ce qu'une autorité de certification (CA) ?**
Une autorité de certification est une organisation de confiance qui :  
- Valide l'identité des entités (personnes, entreprises, serveurs).  
- Délivre des certificats numériques pour garantir l'authenticité et la sécurité des communications.  
Exemples : Verisign, DigiCert, Let’s Encrypt.

---

#### **Quelle est la différence entre l'identification et l'authentification ?**
- **Identification** : Répond à la question *"Qui êtes-vous ?"*.  
- **Authentification** : Répond à la question *"Pouvez-vous le prouver ?"*, par un mot de passe, une clé, ou un certificat.

---

#### **Quels sont les différents types de connexions VPN ?**

| **Nom**                      | **Type**        | **Méthode**                             | **Usage**                                                                 |
|-------------------------------|-----------------|-----------------------------------------|---------------------------------------------------------------------------|
| VPN d'accès à distance        | Accueil         | SSL/TLS                                 | Pour les utilisateurs distants accédant aux ressources d'entreprise.     |
| VPN site à site               | Privé           | Connexion entre réseaux via LAN/WAN     | Relier plusieurs réseaux internes géographiquement éloignés.             |
| Applications VPN              | Mobile          | Application VPN sur appareil mobile     | Pour les utilisateurs mobiles souhaitant un accès sécurisé en déplacement.|

---

#### **Comment une Autorité de Certification émet-elle un certificat SSL ?**
1. Le demandeur génère une **CSR** (Certificate Signing Request) contenant une clé publique.  
2. L’AC vérifie l’identité du demandeur via une autorité d’enregistrement.  
3. Si valide, l’AC signe le certificat avec sa clé privée et délivre le certificat électronique.  
4. Le certificat est installé sur le serveur.

---

#### **Quelles sont les autorités de certification connues ?**
- Symantec  
- DigiCert  
- Comodo  
- GlobalSign  
- Let’s Encrypt  

---

#### **Quelle est la différence entre TLS et SSL ?**
- **SSL** : Protocole plus ancien avec des failles de sécurité connues.  
- **TLS** : Successeur de SSL, plus sécurisé, plus rapide et norme actuelle.  
Bien que le terme **SSL** soit encore utilisé couramment, **TLS** est désormais la norme.

---

#### **Chiffrement vs hachage vs encodage – Quelle est la différence ?**
- **Chiffrement** : Rend les données illisibles sans la clé appropriée, réversible.  
- **Hachage** : Produit une empreinte digitale unique et non réversible à partir des données.  
- **Encodage** : Convertit les données pour les rendre compatibles avec d'autres systèmes, facilement réversible.

---

#### **Comment sécuriser un serveur via HTTPS ?**
1. Configurer un certificat SSL/TLS signé par une autorité de certification reconnue.  
2. Restreindre l'accès au serveur via un VPN si possible.  
3. Placer le serveur en **DMZ** pour isoler le réseau interne.  
4. Configurer un proxy web pour limiter l’exposition.

---
