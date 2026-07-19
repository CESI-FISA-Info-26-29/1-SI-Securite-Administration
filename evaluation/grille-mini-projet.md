# Grille d’évaluation pour le mini-projet

| **Critères**                       | **Description**                                                                                       | **Points** |
|------------------------------------|-------------------------------------------------------------------------------------------------------|------------|
| **1. Questionnaire de sécurité**   |                                                                                                       | **/4**     |
| - Pertinence des questions         | Les questions identifient efficacement les vulnérabilités potentielles.                              | 2          |
| - Propositions de remédiation      | Chaque question est accompagnée d’axes d’amélioration ou de bonnes pratiques.                        | 2          |
|                                    |                                                                                                       |            |
| **2. Simulation de l’infrastructure numérique** |                                                                                       | **/10**    |
| - Schéma d’architecture            | Le schéma représente clairement l’architecture physique et logique du système.                       | 2          |
| - Configuration du serveur         | Active Directory est configuré avec des groupes d’utilisateurs et des droits d’accès adaptés.        | 2          |
| - Segmentation réseau              | Les VLANs sont correctement configurés et respectent les exigences (isolement élèves/enseignants).   | 2          |
| - Partage de fichiers              | Les dossiers sont configurés avec les permissions adéquates (personnels, partagés, sensibles).       | 2          |
| - VPN                              | Le VPN est fonctionnel et permet un accès distant sécurisé.                                          | 2          |
|                                    |                                                                                                       |            |
| **3. Tests et validation**         |                                                                                                       | **/3**     |
| - Droits d’accès                   | Les tests démontrent que seuls les utilisateurs autorisés accèdent aux ressources sensibles.         | 2          |
| - Fonctionnalité globale           | Les configurations globales fonctionnent sans failles majeures.                                      | 1          |
|                                    |                                                                                                       |            |
| **4. Documentation**               |                                                                                                       | **/3**     |
| - Structure et clarté              | La documentation est bien organisée, avec une introduction, des étapes détaillées, et une conclusion. | 1          |
| - Explications des configurations  | Les configurations (Active Directory, VLANs, VPN, partage) sont bien expliquées dans un langage clair. | 1.5        |
| - Preuves des tests                | Des captures d’écran pertinentes illustrent les tests et valident les configurations.                | 0.5        |
|                                    |                                                                                                       |            |
| **Total**                          |                                                                                                       | **/20**    |

---

### Précisions sur les attentes pour la documentation :

1. **Structure et clarté :**
   - La documentation doit être organisée avec une table des matières, une introduction, les étapes détaillées, et une conclusion.  
   - Elle doit être rédigée dans un langage clair et accessible, sans jargon inutile.  

2. **Explications des configurations :**
   - Chaque élément configuré doit être expliqué brièvement, avec des détails sur les choix réalisés (ex. pourquoi telle plage d’adresses IP ou telle segmentation VLAN).  
   - Les configurations importantes (Active Directory, VLANs, VPN, partage de fichiers) doivent être décrites étape par étape.  

3. **Captures d’écran :**
   - Intégrez des captures pour illustrer les tests réalisés, comme :  
     - Une connexion réussie d’un utilisateur au domaine.  
     - L’isolation des VLANs (par exemple, en testant qu’un élève ne peut pas accéder aux dossiers enseignants).  
     - Une capture de la sauvegarde/restauration ou de la connexion VPN fonctionnelle.  