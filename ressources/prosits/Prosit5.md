# Fiche de Révision : Sécurité Réseau et Concepts Associés

## Définitions

### Pare-feu (Firewall)

Un **pare-feu** est un dispositif de sécurité (logiciel ou matériel) qui surveille et contrôle le trafic réseau entrant et sortant selon des règles prédéfinies.  
Objectif : Protéger le réseau interne des menaces externes.

#### Types de pare-feu :

1. **Stateless Firewall (sans état)** :

   - Filtrage simple des paquets basé sur l’adresse IP, les ports, et le protocole.
   - Ne tient pas compte de l’état des connexions.

2. **Stateful Firewall (avec état)** :

   - Suit l’état des connexions dans des tables internes.
   - Permet une analyse plus approfondie du trafic pour détecter les anomalies.

3. **Pare-feu Nouvelle Génération (NGFW)** :

   - Combine les fonctionnalités des pare-feu classiques avec des outils avancés (inspection approfondie, IPS, antivirus, etc.).

4. **UTM (Unified Threat Management)** :
   - Solution tout-en-un regroupant pare-feu, antivirus, anti-spam, filtrage de contenu, etc.
   - Idéal pour les entreprises pour simplifier la gestion et renforcer la sécurité.

---

### DMZ (Demilitarized Zone)

La **DMZ** est un sous-réseau isolé du LAN et d’Internet par un pare-feu.  
Utilisation : Héberger des services accessibles publiquement (serveurs web, DNS, FTP) tout en protégeant le LAN des attaques.  
Avantages :

- Contrôle d’accès renforcé.
- Isolation des serveurs compromis.

---

### Sécurité Périmétrique et en Profondeur

- **Sécurité périmétrique** : Protection basique basée sur un pare-feu pour isoler le réseau interne.  
  _Limite : Insuffisante face aux connexions externes et aux applications cloud._

- **Sécurité en profondeur** : Approche multi-niveaux avec segmentation et plans de secours.  
  Inclut :
  - IPS, Proxy, WAF.
  - Plans de reprise d’activité (PRA).

---

### ACL (Access Control List)

Les **ACL** sont des listes de règles appliquées aux équipements réseau pour autoriser ou bloquer le trafic.

#### Types :

1. **ACL standard** : Filtrage basé sur l’adresse source uniquement.
2. **ACL étendue** : Filtrage sur plusieurs critères (adresse, protocole, ports).
3. **ACL réflexive** : Intègre l’état des connexions.
4. **ACL temporisée** : Active selon des plages horaires définies.
5. **ACL CBAC** : Filtrage avancé incluant des protocoles de la couche application.

---

### SIEM (Security Information and Event Management)

Le **SIEM** combine la gestion des informations de sécurité (SIM) et des événements de sécurité (SEM).  
Rôle :

- Agréger les données des équipements (pare-feu, IPS, serveurs).
- Détecter les anomalies pour réagir rapidement.

Exemples :

- **Splunk** : Monitoring et détection des menaces.
- **IBM QRadar** : Déploiement cloud ou sur site.
- **LogRhythm** : Adapté aux petites entreprises.

---

### Proxy

Un **proxy** est un intermédiaire entre l’utilisateur et Internet.  
Utilisation :

- Contrôle d’accès (ex. : usage d’Internet par les employés).
- Sécurité et anonymisation.
- Mise en cache pour économiser la bande passante.

---

### IPS/IDS (Intrusion Prevention/Detection System)

- **IDS (Intrusion Detection System)** : Détecte les activités suspectes et alerte.
- **IPS (Intrusion Prevention System)** : Détecte et bloque les menaces en temps réel.

---

### Vecteurs d’attaques

Les **vecteurs d’attaques** sont les moyens utilisés par un attaquant pour infiltrer un SI.

#### Types :

1. **Humain** : Exploitation d’erreurs ou imprudences des employés.
2. **Physique** : Attaque sur des équipements matériels.
3. **Logiciel** : Exploitation de failles dans les logiciels.
4. **Réseau** : Failles dans les configurations réseau.

---

### Malwares

Les **malwares** sont des logiciels malveillants conçus pour nuire ou voler des données.

#### Types :

- **Spyware** : Espionne les activités de l’utilisateur.
- **Virus** : Détruit ou vole des données (nécessite une action humaine).
- **Worms** : Se réplique automatiquement dans le réseau.
- **Trojan** : Permet un accès distant à l’attaquant.
- **Ransomware** : Crypte les fichiers et demande une rançon.

---

### SOC (Security Operations Center)

Le **SOC** est une unité de surveillance de la sécurité d’une entreprise.  
Rôle : Prévention, détection, et réponse aux incidents grâce à des outils comme SIEM, IPS, pare-feu, etc.

---

### PSSI (Politique de Sécurité des Systèmes d’Information)

La **PSSI** est un document stratégique définissant les règles et procédures de sécurité pour protéger les systèmes d’information.

---

### DDOS (Distributed Denial of Service)

Une **attaque DDoS** submerge un système avec un trafic malveillant pour perturber ou bloquer un service.  
Types :

- Attaques de couche application.
- Attaques volumétriques.

---

### Ports

Les **ports** sont des points d’accès pour les services réseau.  
Exemples courants :

- Port 80 : HTTP.
- Port 443 : HTTPS.
- Port 22 : SSH.

---

### Règles de Filtrage

Les **règles de filtrage** définissent comment un pare-feu contrôle le trafic.  
Critères :

- **Source/Destination** : Adresse IP, port.
- **Contenu** : Données dans les paquets.
- **Protocole** : TCP, UDP, ICMP.

---

## Questions de Validation

#### **Que représente une DMZ ?**

Une DMZ (Demilitarized Zone) est un sous-réseau séparé du LAN et d'Internet via un pare-feu. Elle héberge les services accessibles publiquement (comme les serveurs web, FTP, DNS) tout en isolant le réseau interne des menaces potentielles.

---

#### **Quels sont les différents types d'ACL que vous connaissez ?**

1. **Standard ACL** : Filtrage basé uniquement sur l’adresse source.
2. **Étendue ACL** : Filtrage sur plusieurs critères, comme l'adresse IP, les ports, et le protocole.
3. **Turbo ACL** : ACL optimisée pour un traitement rapide par le routeur.
4. **Temporisée ACL** : Active ou inactive selon des plages horaires.
5. **Réflexive ACL** : Filtrage basé sur l'état des connexions.
6. **CBAC ACL** : ACL avancée incluant des protocoles de la couche application.

---

#### **Pourquoi les pare-feu sont-ils utilisés pour bloquer certains ports ?**

Les ports ouverts sont des points d'entrée pour des attaques potentielles. Les pare-feu bloquent les ports inutilisés pour limiter les risques d'exploitation par des attaquants, comme les attaques via le port 3389 (RDP) souvent ciblé pour des ransomwares.

---

#### **Quelle est la différence entre ACL et règles de filtrage ?**

- **ACL** : Appliquée au niveau des équipements réseau comme les routeurs et switches.
- **Règles de filtrage** : Appliquées au niveau des pare-feu pour contrôler le trafic selon des critères complexes (source, destination, contenu, protocole).

---

#### **Quels sont les différents malwares que vous connaissez, avec leur fonctionnement ?**

1. **Spyware** : Espionne l'utilisateur et collecte des informations.
2. **Virus** : Endommage ou vole des données, nécessite une action humaine pour se propager.
3. **Worms** : Se réplique automatiquement sur le réseau.
4. **Trojan** : Fournit un accès distant à l'attaquant.
5. **Dialers** : Établit des connexions non autorisées à des modems.
6. **Rootkits** : Permet des privilèges élevés à l'attaquant.
7. **Botnets** : Machine compromise attendant les instructions de l'attaquant.
8. **Ransomware** : Crypte les fichiers et demande une rançon pour la clé de décryptage.

---

#### **Quels sont les types de firewalls et les solutions disponibles sur le marché ?**

- **Types de Firewalls** :

  1. Stateless (sans état)
  2. Stateful (avec état)
  3. Nouvelle Génération (NGFW)
  4. Proxy Firewall
  5. Identifiant Firewall

- **Solutions disponibles** :
  - Fortinet FortiGate
  - Cisco ASA
  - pfSense
  - Sophos XG
  - Palo Alto Networks
  - Kerio Control
  - Barracuda CloudGen Firewall
  - Juniper SRX

---

#### **Un proxy est-il un IDPS ?**

Non, un proxy n'est pas un IDPS. Le proxy gère le contrôle d'accès et la confidentialité, tandis que l'IDPS détecte et prévient les menaces en temps réel. Ils peuvent être combinés dans une architecture de sécurité globale.

---

#### **Un pare-feu est-il un IDS ou un IPS ?**

Un pare-feu nouvelle génération (NGFW) peut inclure des fonctionnalités IDS/IPS. Cependant, un pare-feu classique filtre principalement le trafic, tandis que l'IDS/IPS se concentre sur la détection et la prévention des menaces.

---

#### **Que peut détecter un IDS ?**

Un IDS peut détecter :

- Exploits connus (par signature).
- Comportements malveillants.
- Techniques d'évasion comme la fragmentation TCP/IP ou le rembourrage HTML.

---

#### **Un IPS peut-il empêcher les DDoS ?**

Un IPS peut prévenir certaines attaques DDoS d'application, mais pour les attaques DDoS volumétriques, des solutions spécialisées sont nécessaires.

---

#### **Comment se défendre contre les attaques DDoS ?**

- Utiliser des solutions spécialisées pour détecter et bloquer le trafic malveillant.
- Mettre en place des contre-mesures comme des pare-feu adaptés, des IPS, et des services de mitigation DDoS.

---

#### **VPN ou proxy : lequel est meilleur ?**

- **Proxy** : Contrôle d'accès et anonymisation de la connexion.
- **VPN** : Anonymisation et chiffrement des communications.  
  _Utilisation complémentaire possible selon les besoins._

---

#### **Quels sont les risques d’un port mal configuré ?**

Un port mal configuré ou laissé ouvert peut être exploité par des attaquants pour :

- Injecter des malwares.
- Lancer des attaques DDoS.
- Accéder à des données sensibles.
