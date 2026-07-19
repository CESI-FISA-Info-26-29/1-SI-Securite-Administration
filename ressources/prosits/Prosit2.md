# Fiche de Révision : Virtualisation et Conteneurisation

## Définitions

### Help Desk

Un **Help Desk** est un centre d’assistance utilisateur, offrant un point de contact unique entre un client et une entreprise. Accessible via e-mail, téléphone ou portail en ligne, il aide à résoudre des problèmes techniques.

---

### Ticketing

Un outil de **ticketing** est un logiciel de gestion des demandes clients, centralisant les communications issues de divers canaux.

---

### GLPI

**GLPI** (Gestion Libre de Parc Informatique) est un logiciel ITSM open source pour la gestion des services informatiques.

#### Caractéristiques :

- Inventaire des ressources.
- Gestion des tâches administratives et financières.
- Fonctionnalités conformes au guide ITIL v2 pour la gestion des incidents, demandes et changements.

---

### ITSM (IT Service Management)

L’**ITSM** englobe les processus et activités nécessaires à la conception, la prestation et le support des services informatiques.

#### Objectifs :

- Répondre aux besoins des utilisateurs et des entreprises.
- Automatiser les services avec des outils ITSM.

---

### ITIL

**ITIL** (_Information Technology Infrastructure Library_) est un cadre de bonnes pratiques pour l’ITSM.

- **Version ITIL 4** : 5 volumes couvrant 34 pratiques ITSM.

---

### Data Center

Un **Data Center** regroupe les équipements d’un système d’information pour sécuriser, gérer et maintenir les données.

---

### Virtualisation

La **virtualisation** consiste à créer une version virtuelle de ressources physiques (OS, serveurs, réseaux, stockage).

#### Types :

- **Virtualisation de serveurs** : Plusieurs environnements sur une machine.
- **Virtualisation réseau** : Division en canaux pour affectation flexible.
- **Virtualisation du stockage** : Regroupement en un dispositif unique.
- **Virtualisation des postes (VDI)** : Environnement bureautique sur serveur distant.

---

### Conteneurisation

La **conteneurisation** exécute des applications dans des environnements isolés au niveau de l’OS, sans hyperviseur.

#### Avantages :

- Légèreté.
- Portabilité.
- Évolutivité.

#### Limites :

- Nécessite un OS hôte unique.
- Moins d’isolation qu’une VM.

---

### Hyperviseurs

#### Type 1

Directement installé sur le matériel (ex. : VMware ESXi, Microsoft Hyper-V).

#### Type 2

Fonctionne au-dessus d’un OS hôte (ex. : Oracle VirtualBox, VMware Workstation).

## Questions de Validation

#### **Hyperviseurs**

1. **Dans quels cas choisit-on tel ou tel type de virtualisation ?**
   - **Conteneurs** : Idéal pour le développement Agile, DevOps, les microservices et les environnements multi-cloud.
   - **Serveur virtuel** : Préféré pour les applications lourdes, spécialisées ou nécessitant une isolation accrue.

2. **Peut-on tout virtualiser avec la virtualisation de serveurs ?**
   - Oui, la plupart des applications courantes (serveurs Web, BDD) peuvent être virtualisées. Cependant, certaines applications très spécifiques ou dépendantes du matériel peuvent rencontrer des limitations.

3. **Quels sont les principaux acteurs ?**
   - **Hyperviseurs Type 1** : VMware ESXi, Microsoft Hyper-V, Xen, KVM.
   - **Hyperviseurs Type 2** : Oracle VirtualBox, VMware Workstation, VMware Fusion.

4. **Comparatif des solutions :**
   - **Type 1** : Haute performance, accès direct au matériel, meilleure isolation.
   - **Type 2** : Facilité d’installation, idéal pour des environnements de test ou des usages non intensifs.

5. **Peut-on virtualiser tous les OS avec ces produits ?**
   - Non. Par exemple, macOS ne peut être virtualisé légalement que sur du matériel Apple.

6. **Quelles limites, contraintes et impacts du type 1 & 2 ?**
   - **Type 1** : Plus performant, mais nécessite un matériel dédié.
   - **Type 2** : Moins performant, dépend de l’OS hôte, moins adapté à la production.

---

#### **Virtualisation d’applications**

1. **Quels sont les avantages de la virtualisation d'application ?**
   - Réduction des coûts.
   - Meilleure portabilité.
   - Simplification des mises à jour et déploiements.

2. **Quels sont les acteurs principaux ?**
   - VMware, Citrix, Microsoft.

3. **Quelles architectures peut-on définir ?**
   - Virtualisation centralisée (applications sur serveur).
   - Applications isolées (streaming sur poste local).
   - Infrastructure complète (VDI).

4. **Quelles limites, contraintes et impacts ?**
   - Dépendance à une bonne connectivité réseau.
   - Coûts élevés pour les infrastructures complexes.
   - Performance limitée pour des applications intensives.

---

#### **Technologies de conteneurs**

1. **Faut-il toujours s’orienter vers une technologie de conteneurs ?**
   - Non, les conteneurs sont idéaux pour les microservices et environnements légers. Pour des applications nécessitant un accès direct au matériel ou une isolation forte, les VM sont préférables.

2. **Quel est le rôle du cluster ?**
   - Fournir redondance, haute disponibilité, et reprise rapide en cas de panne.

3. **Quel est l’intérêt de la mise en cluster des hyperviseurs ?**
   - Améliore la continuité de service avec un faible coût de redondance.

---

#### **Comparatif Docker / Kubernetes**

1. **Quel est le service concurrent de Kubernetes proposé par Docker ?**
   - Docker Swarm.

2. **Quelle est la différence entre Docker Compose et Kubernetes/Swarm ?**
   - **Docker Compose** : Orchestration pour un seul hébergeur.
   - **Kubernetes/Swarm** : Gestion multi-hébergeurs avec orchestration avancée.

---

#### **Virtualisation**

1. **Quelle est la différence entre la virtualisation Type 1 et Type 2 ?**
   - **Type 1** : Installé directement sur le matériel, performant et isolé.
   - **Type 2** : Fonctionne sur un OS, plus accessible mais moins performant.

2. **Quel est l’hyperviseur de VMware ?**
   - VMware ESXi.

3. **Quels sont les concurrents d’ESXi ?**
   - Hyper-V, KVM, Xen, Proxmox VE, Citrix Hypervisor.

4. **Quels sont les concurrents d’Oracle VirtualBox ?**
   - VMware Workstation, VMware Fusion.

---

#### **Docker**

1. **Pourquoi utiliser des volumes Docker ?**
   - Pour stocker des données de manière persistante et partager entre plusieurs conteneurs, indépendamment de leur cycle de vie.

---

#### **OS Virtualisation**

1. **Peut-on virtualiser tous les OS ?**
   - Non. Par exemple, macOS ne peut être virtualisé légalement que sur du matériel Apple.

---

#### **Virtualisation Imbriquée**

1. **Qu’est-ce que la virtualisation imbriquée ?**
   - Permet d’exécuter des machines virtuelles dans d’autres machines virtuelles. Utile pour tester ou déployer des environnements complexes.

