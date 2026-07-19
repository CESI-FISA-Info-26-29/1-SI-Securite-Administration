# Fiche de Révision : Active Directory et Gestion des Identités

## Définitions

### Annuaire
Un **annuaire** est un système de stockage de données organisé de manière hiérarchique (contrairement aux SGBD relationnels).  
Avantages : 
- Consultation rapide des données.  
- Duplication facilitée.  
- Moindre espace de stockage requis.

#### LDAP
**LDAP** (Lightweight Directory Access Protocol) est le protocole utilisé pour interroger les annuaires.  
- Les entrées et attributs sont définis par un schéma.
- Organisation hiérarchique avec héritage des attributs entre types parents et enfants.

Exemple : Active Directory utilise LDAP pour stocker et interroger ses données.

---

### Active Directory (AD)
Un **Active Directory** est un service d'annuaire développé par Microsoft.  
- Stocke des informations sur les objets réseau (utilisateurs, groupes, imprimantes, etc.).  
- Propose des méthodes d’authentification (Kerberos, LDAP) et de contrôle d’accès.  
- Organisé en domaines, arbres et forêts.  

#### Domaines, arbres et forêts
- **Domaine** : Conteneur de gestion des objets réseau (utilisateurs, groupes, etc.).  
- **Arbre** : Collection de domaines partageant un espace de noms commun.  
- **Forêt** : Ensemble d’arbres partageant une structure de schéma et de configuration.

---

### Rôles FSMO (Flexible Single Master Operations)
1. **Schema Master** : Modifie la structure de la base AD (1 par forêt).  
2. **Domain Naming Master** : Attribue les noms de domaines (1 par forêt).  
3. **Relative ID Master (RID)** : Gère les blocs de SID pour chaque objet (1 par domaine).  
4. **Primary Domain Controller (PDC)** : Synchronise l’heure, gère les mots de passe et les stratégies (1 par domaine).  
5. **Infrastructure Master** : Gère la réplication des références d’objets (1 par domaine).

---

### GPO (Group Policy Objects)
Les **GPO** permettent de gérer les paramètres des ordinateurs et des utilisateurs dans un réseau via Active Directory.  
- Appliqués selon l’ordre LSDOU : **Local**, **Site**, **Domaine**, **Unité d’Organisation (OU)**.
- Fréquence d’actualisation :  
  - Toutes les 90 minutes sur les postes clients.  
  - Toutes les 5 minutes sur les contrôleurs de domaine.  
- Commandes utiles :  
  - `gpresult /r` pour vérifier l’application.  
  - `gpupdate /force` pour appliquer immédiatement les stratégies.

---

### Tiering
Le **tiering** est un modèle de sécurité pour séparer les comptes à privilèges en différentes couches (tiers).  
Objectif :  
- Restreindre l’usage des comptes dans leur périmètre d’origine.  
- Contenir les attaques (ex. : rançongiciel).

---

### IAM (Identity and Access Management)
La **Gestion des Identités et des Accès** vise à administrer les utilisateurs et leurs droits d'accès.  
#### Composantes principales :  
1. **Identification** : Création d’une identité utilisateur.  
2. **Authentification** : Vérification de l’identité.  
3. **Autorisation** : Attribution des droits d’accès.  
4. **Gestion des utilisateurs** : Création, modification, suppression.  
5. **Annuaire central** : Base des identités et des droits.

Exemples de solutions :  
- Okta, Microsoft Azure IAM, AWS IAM, Ping Identity, Keycloak.

---

### NTLM (New Technology LAN Manager)
**NTLM** est un protocole d’authentification utilisé dans les anciens systèmes Windows.  
- Basé sur un mécanisme de hachage.  
- Remplacé par **Kerberos**, mais toujours utilisé pour la compatibilité.

---

### Kerberos
**Kerberos** est un protocole d’authentification AAA :  
- Basé sur un système de tickets émis par un **KDC (Key Distribution Center)**.  
- Supporte le **Single Sign-On (SSO)** pour réduire le nombre de connexions.

---

### SSO (Single Sign-On)
Le **SSO** permet à un utilisateur d’accéder à plusieurs applications avec un seul identifiant.  
#### Avantages :  
- Simplifie la gestion des identifiants.  
- Réduit les risques d’hameçonnage.

#### Inconvénients :  
- En cas de compromission, l’accès à toutes les applications devient vulnérable.

---

### SID (Security Identifier)
Le **SID** est un identifiant unique attribué à chaque objet Active Directory.  
Format : `S-R-X-Y1-Y2-Yn-1-Yn`  
- **S** : Indique qu’il s’agit d’un SID.  
- **R** : Niveau de révision.  
- **X, Y** : Identificateurs et valeurs associées.

---

### AAA / DICP
- **AAA** : Authentification, Autorisation, Comptabilisation.  
- **DICP** : Disponibilité, Intégrité, Confidentialité, Preuve.  

---

### Relation d’approbation
Une **relation d’approbation** permet l’accès aux ressources entre deux domaines Active Directory.  
#### Types :  
1. **Unidirectionnelle** : Un domaine fait confiance à un autre.  
2. **Bidirectionnelle** : Les deux domaines se font confiance.  
3. **Transitive** : La confiance s’étend aux domaines liés.  
4. **Non transitive** : Limite la confiance à deux domaines spécifiés.

---

### AGDPL (Account, Global, Domain Local, Permission)
Méthode de gestion des droits dans Active Directory :  
1. **Account** : Ajouter les utilisateurs dans des groupes globaux.  
2. **Global** : Insérer les groupes globaux dans des groupes locaux.  
3. **Domain Local** : Attribuer les droits NTFS aux groupes locaux.  

---

### Niveau fonctionnel
Le **niveau fonctionnel** d’un domaine ou d’une forêt Active Directory détermine les fonctionnalités disponibles et les versions de Windows Server prises en charge.  

#### Exemples :  
- N.F. Windows Server 2012 R2 : Compatible avec Server 2025, 2022, 2019, 2016, 2012 R2.  
- N.F. Windows Server 2016 : Compatible avec Server 2025, 2022, 2019, 2016.

---

## Questions de Validation

#### **Compatibilité entre serveurs Windows**

1. **Un serveur Windows 2019 peut-il être intégré dans un domaine Windows Server 2016 ?**  
   - Oui.

2. **Un serveur Windows 2016 peut-il être intégré dans un domaine Windows Server 2019 ?**  
   - Oui, en tant que serveur membre.  
   - Pour héberger une copie de l’AD : cela dépend du niveau fonctionnel de la forêt (N.F. 2016 = oui, N.F. 2019 = non).

---

#### **Forêt et domaine**

3. **Quelle est la différence entre une forêt et un domaine ?**  
   - Une forêt contient plusieurs domaines. Les domaines d’une même forêt sont automatiquement approuvés, ce qui n'est pas le cas entre deux forêts distinctes.

---

#### **Relations d’approbation**

4. **Quels sont les prérequis pour approuver deux domaines ?**  
   - Connaître le nom des domaines.  
   - Posséder un compte administrateur.  
   - Configurer une redirection DNS.

5. **Que se passe-t-il lorsqu’un utilisateur d’un domaine approuvé se connecte à un autre domaine ?**  
   - Si l’utilisateur ouvre une session sur sa propre machine : il récupère ses accès.  
   - Si l’utilisateur ouvre une session sur une machine du domaine approuvé : il récupère les GPO du domaine en question.

---

#### **Limites Active Directory**

6. **Une base AD est-elle limitée en nombre d’OU ou de comptes utilisateurs ?**  
   - Non, elle peut contenir plusieurs milliards d’objets.

---

#### **Forêt et approbations complexes**

7. **Supposons une forêt A avec des domaines A1, A2, une forêt B avec B1, B2 et une forêt C avec C1, C2. Si toutes les forêts sont approuvées, un utilisateur de C2 peut-il ouvrir une session sur une machine de A1 ?**  
   - Oui, mais les performances peuvent être affectées en raison du nombre de liens d’approbation à traverser.

---

#### **Rôles FSMO**

8. **Quels sont les rôles FSMO, leurs fonctions et leur répartition ?**  
   - **Schema Master** (1 par forêt) : Gère la structure de la base AD.  
   - **Domain Naming Master** (1 par forêt) : Attribue et renomme les noms de domaines.  
   - **Relative ID Master (RID)** (1 par domaine) : Gère l’unicité des SID dans chaque domaine.  
   - **Primary Domain Controller (PDC)** (1 par domaine) : Synchronise l’heure, gère les stratégies et les changements de mots de passe.  
   - **Infrastructure Master** (1 par domaine) : Gère la réplication des références d’objets entre domaines.

---

#### **Scénario de déconnexion de filiale**

9. **Si une filiale partage un domaine AD avec la maison mère et que le lien est coupé : quels problèmes surviennent ?**  
   - **Pas de DHCP local** : Problème d’attribution d’adresses.  
   - **DC local présent** : Les utilisateurs peuvent ouvrir une session, mais les modifications (mots de passe, etc.) ne seront pas répercutées.  
   - **DNS local présent** : Pas de problème pour l'accès Internet si la filiale a son propre accès.

---

#### **Kerberos**

10. **Quels sont les inconvénients de Kerberos ?**  
    - Nécessite des services compatibles avec Kerberos.  
    - Synchronisation horaire obligatoire entre les machines.  
    - Point unique de défaillance (KDC).  
    - Si le KDC est compromis, l'ensemble des services devient vulnérable.  
    - Ne chiffre que l’authentification, pas les données transmises.

---

#### **Compatibilité de niveaux fonctionnels**

11. **Quels systèmes d’exploitation peuvent être utilisés comme contrôleurs de domaine avec un niveau fonctionnel de forêt et domaine Windows Server 2012 R2 ?**  
    - Windows Server 2025 (préversion).  
    - Windows Server 2022.  
    - Windows Server 2019.  
    - Windows Server 2016.  
    - Windows Server 2012 R2.

---

#### **Types de relations d’approbation Active Directory**

12. **Quels sont les différents types de relations d’approbation disponibles ?**  
    - **Trust unidirectionnel** : Un domaine fait confiance à un autre sans réciprocité.  
    - **Trust bidirectionnel** : Confiance mutuelle entre deux domaines.  
    - **Trust transitif** : La confiance s’étend aux domaines liés.  
    - **Trust non transitif** : La confiance est limitée aux deux domaines spécifiés.

---

#### **AAA et IAM**

13. **Est-ce que AAA est la même chose qu’IAM ?**  
    - Non.  
      - **AAA** : Authentification, Autorisation, Comptabilisation.  
      - **IAM** : Gestion complète des identités et des accès sur l’ensemble du cycle de vie.

---

#### **SSO**

14. **Quels sont les risques du SSO ?**  
    - En cas de compromission des informations d’identification, toutes les applications connectées deviennent vulnérables.  
    - Dépendance au service SSO : si le SSO tombe, les utilisateurs ne peuvent plus se connecter.  
    - Recommandation : Coupler SSO avec l’authentification à deux facteurs (2FA).

---

#### **NTFS**

15. **Pourquoi ne pas accorder de droits NTFS à des utilisateurs spécifiques ?**  
    - Gestion complexe et risques d’erreurs lors des changements de rôle ou des départs.  
    - Difficulté à appliquer des politiques de sécurité uniformes.  
    - Dépannage plus compliqué.

---

#### **Sécurité des mots de passe**

16. **Qu’est-ce que l’entropie d’un mot de passe ?**  
    - L’imprévisibilité ou complexité d’un mot de passe, mesurée en bits. Plus l’entropie est élevée, plus le mot de passe est difficile à casser.

---

#### **Stratégies de groupe (GPO)**

17. **Comment vérifier l’application d’une stratégie de groupe ?**  
    - Utiliser la commande `gpresult /r` pour voir les stratégies appliquées.  
    - Utiliser `gpupdate /force` pour appliquer immédiatement les stratégies.

