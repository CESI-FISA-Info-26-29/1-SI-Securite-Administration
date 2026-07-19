# PROJET ASSURANCESPLUS

Une agence du groupe ASSURANCESPLUS a récemment été victime d'une attaque par rançongiciel. Le préjudice est grave : toute activité sur le site est paralysée. Le siège du groupe a fait appel à l’ESN Numerica, dont vous faites partie. Après une première évaluation, Numerica a estimé à 10 jours le délai nécessaire pour remettre en service le système informatique de l’agence. Le DSI d’ASSURANCESPLUS souhaite éviter qu’un tel incident ne se reproduise, dans les 9 agences actuelles et dans les futures agences. ASSURANCESPLUS va bientôt s'agrandir.

Numerica confie à votre équipe plusieurs missions.

Vous devrez :

- Proposer un questionnaire de sécurité à destination des agences du groupe. Historiquement, chaque agence a son propre prestataire informatique qui gère son SI. L'objectif est de détecter les vulnérabilités et de proposer des mesures correctives basées sur des axes de remédiation.

- Travailler sur le déploiement de futures agences. Vous devrez élaborer une cartographie type du système d'information pour ces agences : vue administration, infrastructure logique et physique. Cette architecture devra respecter les bonnes pratiques en matière de sécurisation des systèmes d’information, garantir la continuité d’activité, la reprise après incident, ainsi que la traçabilité des événements. Le directeur du groupe souhaite un retour à la normale sous 4 heures pour les services critiques, et 24 heures pour les autres. Vous devez proposer un plan de sauvegarde.

## Voici les éléments à prendre en compte :

- Le siège du groupe héberge actuellement un domaine Active Directory nommé assurancesplus.fr.
- Il y a en moyenne 50 salariés par agence.

Chaque nouvelle agence sera structurée avec les services suivants :

- Service Client ;
- Service Conseil et Commerce ;
- Service Gestion des sinistres ;
- Service Juridique ;
- Direction de l’agence.

Chaque employé doit pouvoir se connecter à distance, soit en tant qu’itinérant (par exemple, les commerciaux), soit en télétravail.

Les besoins en partage de dossiers sont les suivants :

- Un dossier partagé par service, accessible uniquement au personnel du service concerné.
- Un dossier personnel pour chaque salarié avec un quota de stockage limité.
- Le personnel administratif doit pouvoir accéder en lecture aux données des services de location et de vente.
- La direction doit avoir accès aux dossiers de tous les services.

Tous les employés sont équipés de PC portables sous Windows Pro, et les utilisateurs ainsi que les ordinateurs sont authentifiés via Active Directory.

Chaque agence utilise :

- Un ERP ;
- Un copieur multifonction (impression, copie, numérisation) et une imprimante couleur ;
- Office 365, incluant la messagerie Outlook.

Chaque agence utilise un ERP (type Odoo), qui repose sur PostgreSQL en backend et suit une architecture à trois tiers :

- Un serveur de base de données PostgreSQL ;
- Un serveur d'applications (contenant les objets métiers, le moteur de workflow, le générateur d'états, etc.) ;
- Un serveur de présentation, qui permet aux utilisateurs de se connecter via n'importe quel navigateur web (Google Chrome, Firefox, etc.).

Dans chaque service, un correspondant informatique est désigné et doit pouvoir :

- Créer ou modifier les comptes utilisateurs de son service ;
- Gérer les droits d’accès ;
- Intégrer de nouveaux postes de travail au domaine.

Les données gérées par les agences ont été classées en trois catégories en fonction de leur criticité :

### Données Critiques :

- Base de données de l'ERP : Contient les informations sur les clients, les contrats, etc.
- Données partagées : Documents du service sinistres, juridique et de la direction.

### Données Importantes :

- Données partagées : Documents du service client, conseil et commerce.
- Emails professionnels : Correspondances internes et externes importantes.

### Données Moins Critiques :

- Dossiers personnels des employés.

Chaque agence est connectée au siège via une connexion Business VPN avec un débit garanti et un délai de rétablissement sous 4 heures, géré par le fournisseur d’accès internet d’ASSURANCESPLUS.

Chaque agence utilise historiquement son propre domaine Active Directory, indépendant de celui du siège, mais le déploiement des futures agences peut se faire différemment. Ceci fait partie de l'étude.

Une présentation de l'infrastructure prévue pour les nouvelles agences du groupe ASSURANCESPLUS est fixée pour la semaine 50. Cette présentation devra être accompagnée d'une maquette qui attestera de la viabilité et de la sécurité du nouveau système d'information. En complément de la présentation, une démonstration des scripts prévus pour le déploiement sera également attendue.

## Ressources pour les étudiants

- Cartographie du système d’information : https://cyber.gouv.fr/publications/cartographie-du-systeme-dinformation
- Vidéo sur la cartographie du SI : https://www.youtube.com/watch?v=VSsmnnl6-T8&t=72s
- MinumEco « EcoDiag » EcoInfo / CNRS : https://ecoresponsable.numerique.gouv.fr/publications/boite-outils/fiches/ecodiag/
- Ecoinfo « Ecodiag » : https://ecoinfo.cnrs.fr/ecodiag-calcul/
- France Num « My Impact : une calculatrice pour évaluer son empreinte environnementale numérique professionnelle » : https://www.francenum.gouv.fr/guides-et-conseils/pilotage-de-lentreprise/numerique-durable/my-impact-une-calculatrice-pour

## Livrables attendus

### Livrable 1 : Cartographie

- Document de cartographie du SI type proposé pour les nouvelles agences. Ce document devra présenter :
  - Une vue de l’administration (Zone d'administration, service d'annuaire d'administration, Forêt AD/arbre LDAP, Domaine AD/LDAP...)
  - Une vue des infrastructures logiques (Réseaux, sous-réseaux, passerelles, interconnexions, équipement de sécurité, Serveurs DHCP, DNS, Rôles...)
  - Une vue des infrastructures physiques (équipements physiques qui composent le système d’information ou qui sont utilisés par celui-ci)
- Politique de sauvegarde : Une proposition de plan de sauvegarde et une proposition de topologie de sauvegarde.
- Plusieurs outils gratuits peuvent être utilisés pour dessiner des diagrammes, par exemple LucidChart ou draw.io.

La présentation du livrable devra être claire et professionnelle.

### Livrable 2 : Sécurité du S.I.

- Questionnaire de Sécurité : Un questionnaire de sécurité pour les agences existantes, qui permettra d’identifier les vulnérabilités et de mesurer le niveau de sécurité des infrastructures, des données et des processus, ainsi que le respect des normes.
  - Pour chaque point abordé dans le questionnaire, indiquez des axes de remédiation et/ou les bonnes pratiques.
- Politique de filtrage : La politique de filtrage à déployer sur le ou les pare-feu (dont les règles de pare-feu).
- Scripts : Des scripts de déploiement et d’administration commentés.

### Livrable 3 : Maquette du S.I.

- Évaluation de la maquette du Système d'Information proposé pour les nouvelles agences.
- Une présentation de l'infrastructure prévue pour les nouvelles agences du groupe ASSURANCESPLUS est fixée pour la semaine 50. Cette présentation devra être accompagnée d'une maquette attestant de la viabilité du nouveau système d'information. En complément de la présentation, une démonstration des scripts prévus pour le déploiement sera également attendue.

Une partie de votre maquette peut être présentée à l'aide de Packet Tracer.

### Évaluation de la soutenance : Argumentation sur les stratégies de gestion du S.I.

- Vous devrez expliquer et justifier l'infrastructure logique et physique retenue (serveurs, réseau, postes de travail, etc.). Vous présenterez les éléments complémentaire à la maquette, ou que vous ne pouviez pas maquetter. Le scenario de présentation de votre maquette sera évalué.
- Vous expliquerez comment l'administration du système garantira la confidentialité, l'intégrité, la disponibilité des données et des services, ainsi que la traçabilité des actions effectuées sur le système.
- Vous devrez enfin présenter et commenter une évaluation du bilan carbone de votre solution technique, y compris les postes utilisateurs. Pour cela, vous pouvez utiliser des outils disponibles sur les sites des constructeurs, ou encore des outils disponibles dans les ressources.

La présentation de l’attestation de réussite du MOOC SecNumacadémie par chaque membre du groupe projet sera considérée comme un point bonus lors de l’évaluation individuelle de la soutenance et des questions/réponses.

La durée de la présentation est de 30 à 35 minutes + 10 à 15 minutes de questions réponses.

Taille des groupes projet préconisée : 3-4 élèves
