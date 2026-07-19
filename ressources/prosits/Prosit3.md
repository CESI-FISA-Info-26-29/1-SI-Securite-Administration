# Fiche de Révision : Concepts de Continuité et Sauvegarde Informatique

## Définitions

### RTO (Recovery Time Objective)

Le **RTO** correspond à la durée maximale d'interruption acceptable d'une ressource informatique.  
Exemple : Un RTO de 2 heures signifie que le système doit être opérationnel au plus tard 2 heures après l'incident.

---

### RPO (Recovery Point Objective)

Le **RPO** est la durée maximale d’enregistrement des données qu'il est acceptable de perdre en cas de panne.  
Exemple : Un RPO de 15 minutes impose des sauvegardes régulières pour limiter la perte de données.

---

### PRA (Plan de Reprise d'Activité)

Le **PRA** regroupe l'ensemble des procédures techniques et organisationnelles permettant la reconstruction et la remise en route des systèmes après un incident majeur.

---

### PCA (Plan de Continuité d'Activité)

Le **PCA** garantit une disponibilité élevée des systèmes critiques en cas de crise.  
Objectif : Maintenir l'accès aux applications essentielles même en cas de sinistre.

---

### PRI (Plan de Reprise Informatique)

Le **PRI** est équivalent au PRA, mais se concentre exclusivement sur les systèmes informatiques.

---

### PCI (Plan de Continuité Informatique)

Le **PCI** est le volet technologique du PCA. Il prévoit des mesures pour assurer la continuité des systèmes informatiques après un incident.

---

### Stockage

Le **stockage** correspond à l'enregistrement des données utilisées activement.  
Exemple : Documents sur un disque dur ou un espace serveur.

---

### Sauvegarde

La **sauvegarde** consiste à enregistrer des données pour les restaurer en cas de sinistre. Elle repose sur des stratégies telles que :

- **Complète** : Copie intégrale.
- **Différentielle** : Données modifiées depuis la dernière sauvegarde complète.
- **Incrémentielle** : Données modifiées depuis la dernière sauvegarde (quelle qu'elle soit).

---

### Archivage

L'**archivage** est l'enregistrement de données pour des fins légales ou historiques. Ces données ne sont pas destinées à être réutilisées sauf dans des cas spécifiques.  
Différence avec la sauvegarde : L’archivage n’est pas conçu pour une récupération immédiate en cas d’incident.

---

### Disponibilité

La **disponibilité**, ou _High Availability (HA)_, désigne la capacité d’un système ou service à rester accessible en permanence.  
Exemples de solutions :

- RAID 1 ou 5, clusters de serveurs, routage.

---

### Intégrité

L’**intégrité des données** garantit que les données ne subissent aucune altération accidentelle ou volontaire.  
Éléments constitutifs :

- Complétude, précision, authenticité, validité.  
  Exemples : Contrôle de Redondance Cyclique (CRC), Frame Check Sequence.

---

### Criticité de la donnée

La **criticité** représente l’importance d’une donnée pour l’entreprise, influençant sa gestion et sa politique de sauvegarde.

---

### Résilience

La **résilience** désigne la capacité d’un système à résister et à se rétablir après une défaillance ou une attaque.

---

### Souveraineté des données

Concept selon lequel les données numériques doivent être soumises à la législation du pays où elles sont stockées.  
Exemple : RGPD, ISO 27001.

---

### Cloud

Le **cloud** désigne les serveurs accessibles via Internet et les logiciels qui y fonctionnent.

#### Modèles de services :

1. **Cloud privé** : Serveur dédié à une organisation.
2. **Cloud public** : Serveurs partagés entre plusieurs organisations.
3. **Cloud hybride** : Association de clouds publics et privés.
4. **Multicloud** : Utilisation de plusieurs clouds publics.

---

### SLA (Service Level Agreement)

Un **SLA** est un contrat définissant les niveaux de service attendus, leurs performances, et les mesures prises en cas de non-respect.

---

### Règle 3-2-1

Une stratégie de sauvegarde recommandée :

1. **3 copies** des données.
2. **2 types de supports** de stockage.
3. **1 copie hors site**.

---

### Sauvegardes : Complète, Différentielle, Incrémentielle

- **Sauvegarde complète** : Copie de l'intégralité des données.
- **Sauvegarde différentielle** : Copie des modifications depuis la dernière sauvegarde complète.
- **Sauvegarde incrémentielle** : Copie des modifications depuis la dernière sauvegarde, quelle qu'elle soit.

---

### RAID

Le **RAID** (Redundant Array of Independent Disks) répartit les données sur plusieurs disques pour améliorer :

- La performance.
- La sécurité.
- La tolérance aux pannes.

---

### NAS (Network Attached Storage)

Le **NAS** est un dispositif de stockage en réseau offrant un accès centralisé aux données.  
Avantage : Redondance grâce à la technologie RAID.

---

### SAN (Storage Area Network)

Le **SAN** est un réseau dédié au stockage de données, séparé du réseau principal.

---

### Backup as a Service (BaaS)

Le **BaaS** est un service de sauvegarde externalisé, généralement basé sur le cloud.

---

### Disaster Recovery as a Service (DRaaS)

Le **DRaaS** est un service de reprise après sinistre externalisé, permettant de restaurer rapidement les systèmes après un incident.

---

### Backup on-premises

La **sauvegarde sur site** consiste à stocker les données localement, sur des serveurs ou des supports physiques.

---

## Questions de Validation

#### **Résilience**

1. **La résilience fait-elle partie des piliers de la sécurité du SI ?**
   - Non, la résilience n'est pas un pilier en soi, mais elle est un objectif visé par les piliers (disponibilité, intégrité, confidentialité).

---

#### **Stockage et sauvegarde**

2. **Le stockage et la sauvegarde, est-ce pareil ?**
   - Non.
     - **Stockage** : Enregistrement des données à utiliser activement.
     - **Sauvegarde** : Protection temporaire pour restauration en cas de sinistre.

---

#### **PRA vs PCA**

3. **Quel élément est le moins coûteux à mettre en œuvre, le PRA ou le PCA ?**
   - Le **PRA** est moins coûteux.
     - Le **PCA** nécessite des solutions techniques complexes pour assurer une continuité immédiate et transparente.

---

#### **Archivage et sauvegarde**

4. **Archiver revient-il à sauvegarder ?**
   - Non.
     - **Archivage** : Conservation à long terme, souvent pour des raisons légales.
     - **Sauvegarde** : Récupération rapide des données en cas d’incident.

---

#### **PCC (Plan de Communication de Crise)**

5. **Pouvez-vous expliquer ce qu’est un PCC ?**
   - Le **PCC** est une composante du PCA. Il vise à informer les collaborateurs, sous-traitants et autorités des procédures à suivre en cas de crise.

---

#### **PCA et PCI**

6. **Est-ce que le PCA fait partie du PCI ?**
   - Non.
     - **PCI** : Volet technologique du PCA, centré sur les systèmes informatiques.
     - **PCA** : Plus global, englobe les aspects organisationnels et techniques.

---

#### **Sauvegardes**

7. **Quelle stratégie nécessite le plus de temps de sauvegarde : incrémentielle ou différentielle ?**

   - La sauvegarde **différentielle** nécessite plus de temps, car elle copie toutes les modifications depuis la dernière sauvegarde complète.

8. **Quelle stratégie de sauvegarde nécessite le moins d’espace de stockage ?**
   - La sauvegarde **incrémentielle** nécessite le moins d’espace.

---

#### **RAID**

9. **Est-ce que le RAID est une solution de sauvegarde ?**
   - Non. Le **RAID** améliore les performances et la tolérance aux pannes, mais ne protège pas contre les suppressions accidentelles ou les corruptions de données.

---

#### **RTO**

10. **Pourquoi le RTO est-il important ?**
    - Il définit le temps maximal acceptable d’interruption d’un service. Cela permet d’équilibrer les coûts et les impacts liés à la reprise d’activité.

---

#### **SLA (Service Level Agreement)**

11. **Quelles sont les principales composantes du SLA ?**
    - Périmètre de service couvert.
    - Plage de service garanti (ex. : 24/7).
    - Taux de disponibilité (ex. : 99%).
    - Garantie de Temps d’Intervention (GTI).
    - Garantie de Temps de Rétablissement (GTR).

---

#### **Continuité d’activité informatique**

12. **Que peut-on mettre en place pour garantir un niveau de continuité ?**
    - Définir un **PCI**.
    - Répliquer les données sur un autre site distant.
    - Mettre en place une redondance matérielle (serveurs, réseaux, alimentation).
    - Virtualisation pour flexibilité et rapidité de reprise.
    - Surveillance proactive, gestion des incidents, tests réguliers.

---
