# Fiche de Révision : Supervision et Concepts Associés

## Définitions

#### **Supervision**

La **supervision** vérifie l'état d'un hôte ou d'un service et remonte une alerte en cas de comportement anormal (ex. : temps de réponse trop long, statut NOK). Une alerte signifie que le service est inutilisable (**Critical**) ou qu'il risque de l'être (**Warning**). Elle vise à garantir la disponibilité des services, à prévenir les défaillances et à minimiser les durées d'intervention.

---

#### **Monitoring**

Le **monitoring** est une combinaison de la supervision et de la métrologie. Il désigne les outils et processus permettant de suivre la vie de l'infrastructure informatique en temps réel.

---

#### **Métrologie**

La **métrologie** consiste à historiser les données, les traiter et les présenter sous forme de graphiques ou de rapports. Elle aide à optimiser les services en identifiant les améliorations nécessaires et en gérant efficacement les ressources.

---

#### **SNMP (Simple Network Management Protocol)**

Un protocole de gestion de réseau qui permet aux administrateurs de surveiller, gérer et diagnostiquer des problèmes réseau et matériels. Utilise les ports UDP 161 pour les requêtes et 162 pour les traps SNMP. Les versions SNMP v1 et v2c sont moins sécurisées, tandis que SNMP v3 offre un meilleur chiffrement.

---

#### **SNMP Traps**

Des messages d’alerte envoyés par un équipement supervisé à un serveur lorsque des événements spécifiques surviennent (ex. : dépassement d’un seuil).

---

#### **MIB (Management Information Base)**

Une **MIB** est une base de données hiérarchique contenant des informations sur les entités réseau (ex. : routeurs, serveurs). Chaque information est identifiée par un **OID** (Object Identifier), une suite unique de chiffres. Ex. : `1.3.6.1.2.1.2.2.1.2` correspond à `ifDescr`, qui décrit une interface réseau.

---

#### **Syslog**

Un protocole permettant la centralisation des journaux d’événements émis par des équipements réseau. Utilise le port UDP 514 pour collecter les informations et les consigner dans des fichiers journaux.

---

#### **Plugins / Sondes**

Scripts ou programmes utilisés par des outils comme Nagios/Centreon pour surveiller des services spécifiques. Ils renvoient des codes d’état :

- **0 (OK)** : Tout est normal.
- **1 (Warning)** : Alerte modérée.
- **2 (Critical)** : Alerte critique.
- **3 (Unknown)** : Problème dans l'exécution du plugin.

---

#### **Hôte**

Un équipement ou une machine à superviser (ex. : serveur, routeur).

---

#### **Service**

Un composant ou une fonctionnalité spécifique d’un hôte à surveiller (ex. : espace disque d’un serveur, trafic sur une interface réseau).

---

#### **Escalade**

Un processus pour transférer un incident à un niveau de support supérieur, soit par manque de compétences au niveau actuel, soit par dépassement d’un délai prédéfini.

---

#### **Capacity Planning**

La gestion des capacités garantit que l'infrastructure informatique répond aux besoins des utilisateurs en termes de ressources, de coût et de qualité de service.

---

#### **SaaS (Software as a Service)**

Un modèle où les applications sont accessibles via un navigateur, hébergées par un fournisseur et facturées à l’usage. Les mises à jour sont automatiques.

---

#### **On-Premise**

Un modèle où les infrastructures sont installées sur site, offrant plus de contrôle et répondant à des contraintes juridiques ou opérationnelles spécifiques.

---

#### **Environnement Cloud Privé**

Un environnement informatique dédié à une entreprise, permettant une gestion sécurisée des données sensibles dans un environnement contrôlé.

---

### Questions de validation

#### **Qu'est-ce que la supervision ? Quelle est la différence entre monitoring, supervision et métrologie ?**

- **Supervision** : Vérifie l'état des services et alerte en cas de problème.
- **Métrologie** : Historise et analyse les données pour optimisation.
- **Monitoring** : Combine supervision et métrologie pour un suivi global de l’infrastructure.

---

#### **Connaissez-vous des outils de supervision ?**

- Nagios, Centreon, Zabbix, Prometheus, PRTG, SolarWinds.

---

#### **Connaissez-vous le protocole SNMP ?**

Un protocole permettant de surveiller et gérer des équipements réseau. Il fonctionne principalement avec les ports UDP 161 (requêtes) et 162 (traps).

---

#### **Que veut dire proactif ?**

Être proactif signifie anticiper les problèmes ou opportunités au lieu de simplement réagir.

---

#### **En quoi la supervision permet la proactivité ?**

Elle détecte les anomalies et émet des alertes avant que les problèmes n'affectent les services (ex. : espace disque proche de la saturation).

---

#### **Commande pour afficher les informations d’un périphérique en parcourant la MIB :**

```bash
snmpwalk -v1 -c private 192.168.0.232
```

- **-v1** : Version du protocole.
- **-c private** : Nom de la communauté.
- **192.168.0.232** : Adresse IP du périphérique.

---

#### **Commande pour afficher une information précise dans la MIB :**

```bash
snmpget -v1 -c private 192.168.0.232 IF-MIB::ifOperStatus.122
```

---

#### **Connaissez-vous Nagios ?**

Nagios est une solution populaire de supervision qui permet de surveiller les hôtes et services. Bien que son usage ait diminué, des forks comme Centreon continuent de l’améliorer.

---

#### **Qu'est-ce qu'une escalade ?**

Une escalade transfère un incident à un niveau de support supérieur par manque de compétences ou dépassement d’un délai.

---
