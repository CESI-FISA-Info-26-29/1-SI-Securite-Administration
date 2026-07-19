# Mini-Projet : Simulation d'une infrastructure numérique sécurisée

L’école fictive **CESI Éducation** (Centre d’Études en Sécurité Informatique) cherche à moderniser et sécuriser son système d’information suite à un incident impliquant la gestion des dossiers de synthèse des élèves. Lors d’une réunion de fin d’année, un enseignant a constaté qu’un dossier contenant des informations sensibles (notes, appréciations, données personnelles) était accessible sans restriction par des élèves.  

Face à cette situation, la direction de CESI Éducation souhaite :  

1. Sécuriser l’accès aux données sensibles.  
2. Optimiser les ressources pédagogiques pour les enseignants et les élèves.  
3. Préparer une architecture technique applicable aux futures écoles affiliées.  

Votre mission est de proposer une simulation d’une infrastructure numérique sécurisée qui répond aux besoins actuels tout en assurant une évolutivité pour les futures écoles.

---

## Objectifs du projet  

1. **Sécuriser les données sensibles :**  
   - Limiter l’accès aux dossiers critiques (dossiers de synthèse) aux enseignants et administrateurs.  
   - Garantir une gestion des droits d’accès rigoureuse.  

2. **Organiser les ressources pédagogiques :**  
   - Mettre en place des espaces de partage sécurisés pour les enseignants.  
   - Fournir à chaque élève un dossier personnel avec un accès restreint.  

3. **Segmenter les accès réseau :**  
   - Séparer les réseaux Wi-Fi des enseignants et des élèves pour garantir la sécurité et éviter les intrusions.  

4. **Préparer les futures écoles affiliées :**  
   - Proposer une infrastructure standardisée et évolutive, facile à déployer.  

---

## Cartographie définie  

#### Architecture physique

| **Élément**                | **Description**                                                                 | **Quantité** |
|-----------------------------|---------------------------------------------------------------------------------|--------------|
| **Serveur physique local**   | Serveur principal gérant Active Directory et les partages de fichiers.           | 1            |
| **Postes fixes**             | 5 postes fixes dans la salle informatique connectés au domaine.                 | 5            |
| **Points d'accès Wi-Fi**     | Deux points d’accès Wi-Fi séparés : un pour les étudiants, un pour les enseignants. | 2            |

---

#### Architecture logicielle

| **Logiciel/Service**       | **Usage**                                                                   | **Type**         |
|-----------------------------|----------------------------------------------------------------------------|------------------|
| **Active Directory**        | Gestion des comptes enseignants et élèves.                                | Serveur local    |
| **Microsoft 365**           | Outils bureautiques et classes virtuelles pour enseignants.               | Cloud            |
| **ERP pédagogique**         | Gestion des absences et des notes.                                        | Cloud SaaS       |
| **Partage de fichiers**     | Stockage des ressources pédagogiques et des dossiers sensibles.           | Serveur local    |

---

### Livrable 2 : Questionnaire de sécurité  

Proposez un questionnaire (10 questions maximum) pour identifier les failles dans la sécurité actuelle. 

#### Exemple

- Les mots de passe des enseignants sont-ils renouvelés régulièrement ?  
- Les sauvegardes des données critiques sont-elles effectuées et testées ?  
- Existe-t-il une procédure pour désactiver les comptes des utilisateurs inactifs ?  

Pour chaque question, proposez des recommandations ou des axes d'amélioration.

---

### Livrable 3 : Simulation de l’infrastructure numérique  

#### Objectif

Créer une simulation de l’architecture numérique définie ci-dessus en utilisant des outils tels que VirtualBox, GNS3, ou Packet Tracer. Cette simulation doit démontrer la faisabilité technique et l’efficacité des solutions proposées.

#### Éléments à inclure

1. **Serveur Active Directory :**  
   - Gestion centralisée des utilisateurs (élèves, enseignants, administrateurs).  
   - Mise en place de groupes et de politiques de droits d'accès.  

2. **Partage des ressources :**  
   - Dossiers pédagogiques accessibles uniquement aux enseignants.  
   - Dossiers personnels pour chaque élève avec quotas de stockage.  
   - Accès restreint aux dossiers sensibles pour les enseignants et l’administration.  

3. **Segmentation réseau :**  
   - Réseaux distincts pour élèves et enseignants via des VLANs.  
   - Deux points d’accès Wi-Fi :  
     - **SSID Étudiants** : Accès limité aux ressources pédagogiques.  
     - **SSID Enseignants** : Accès sécurisé avec priorisation.  

4. **Sauvegarde et VPN :**  
   - Automatisation des sauvegardes des données sensibles avec test de restauration.  
   - Configuration d’un VPN pour les enseignants et administrateurs accédant à distance.  

#### Tests à effectuer

- Vérifiez les droits d’accès (enseignants/élèves) sur les ressources pédagogiques.  
- Testez la segmentation réseau pour éviter tout accès non autorisé.  
- Simulez une sauvegarde/restauration des données critiques.  
- Validez l’utilisation du VPN pour un accès distant sécurisé.

---

### Évaluation

Votre travail sera évalué sur :

- **Clarté et pertinence du questionnaire de sécurité** (livrable 2).  
- **Réalisation et documentation de la simulation** (livrable 3) :  
  - Schéma visuel de l’infrastructure simulée.  
  - Captures d’écran des tests effectués.  
  - Description des problèmes rencontrés et des solutions apportées. 