# Préparation

## Contenu

- **Introduction**
- **Prérequis**
- **Sujet**

---

## Introduction

Cette séquence de préparation vise à vous aider à installer l’environnement logiciel nécessaire pour travailler pendant les workshops, les corbeilles et sur votre projet. Vous aurez besoin d’un logiciel de virtualisation (un hyperviseur) pour utiliser des machines virtuelles sur votre PC, ainsi que de différents systèmes d’exploitation Microsoft et Linux.

## Prérequis

### Système & Réseau : CCNA1

Vous devez être capable de :
- Créer des réseaux LAN simples,
- Effectuer les configurations de base des routeurs et des commutateurs,
- Mettre en œuvre des schémas d'adressage IPv4,
- Comprendre le fonctionnement d’un serveur DNS et d’un serveur DHCP.

#### Vidéos de rappel des connaissances (IT-CONNECT)
- [Le DNS pour les débutants](https://www.youtube.com/watch?v=tyDxzzdKnsU) (10 mn)
- [Les adresses IP pour les débutants](https://www.youtube.com/watch?v=_JuY79L8_qA&t=1254s) (25 mn)
- [Le DHCP pour les débutants](https://www.youtube.com/watch?v=wo-DVmtfjPU&t=40s) (13 mn)

### Microsoft Windows & Linux Ubuntu

Vous devez connaître les commandes de base sous Linux et Windows.

- [Les commandes de base en console Linux](https://doc.ubuntu-fr.org/tutoriel/console_commandes_de_base)
- [Vi IMproved - Utilisation vim](https://doc.ubuntu-fr.org/vi)
- [Nano - Commandes de base](https://doc.ubuntu-fr.org/nano#commandes_de_base)
- [La ligne de commande Windows et les fichiers batch](https://windows.developpez.com/cours/ligne-commande/?page=page_4#LIV)

---

## Sujet

### Téléchargement

Pour cette préparation, vous devrez télécharger les systèmes d’exploitation et logiciels suivants.

#### Oracle VirtualBox (version adaptée à votre OS)
- [VirtualBox 7.0.20 platform packages](https://www.virtualbox.org/wiki/Downloads)
- VirtualBox 7.0.20 Oracle VirtualBox Extension Pack

**Pour les PC Windows :** assurez-vous d'avoir le runtime Microsoft Visual C++ installé  
  ([VC_redist.x64.exe](https://learn.microsoft.com/en-us/cpp/windows/latest-supported-vc-redist?view=msvc-170))

#### Windows Server 2022 et Windows 10
Connectez-vous sur Azure Éducation pour télécharger les fichiers `.iso` et récupérer les clés de licence.  
- Accédez via l’ENT ou [Azure Éducation](https://azureforeducation.microsoft.com)
  - **Windows Server 2022 Standard** (Français ou Anglais)
  - **Windows 10 Éducation 22H2** (Français ou Anglais)

**En cas d’indisponibilité d'Azure, utilisez les versions d’évaluation :**
- [Windows Server 2022](https://www.microsoft.com/fr-fr/evalcenter/download-windows-server-2022) (180 jours)
- [Windows 10 Entreprise 22H2](https://www.microsoft.com/fr-fr/evalcenter/evaluate-windows-10-enterprise) (90 jours)
- [Windows 11 Entreprise](https://www.microsoft.com/fr-fr/evalcenter/evaluate-windows-11-enterprise) (90 jours)

#### Ubuntu Server
- Téléchargez le fichier `.iso` : [Ubuntu Server 24.04.1 LTS](https://ubuntu.com/download/server)

---

# Énoncé

## Exercice : Installation et configuration de l'environnement de travail

### Architecture à mettre en place

L'objectif de cette séquence est de mettre en place l'architecture suivante :
1. **Installation de VirtualBox** sur votre PC Hôte.
2. **Création d'un réseau NAT Virtuel.**
3. **Installation de 3 machines virtuelles Invitées** :
   - Ubuntu Server
   - Windows Server 2022
   - Windows 10 Éducation

---

## Définitions

- **Virtualisation** : Technologie permettant de créer plusieurs environnements ou ressources à partir d'un seul système physique.
- **Machine virtuelle (VM)** : Environnement virtualisé fonctionnant sur une machine physique (votre PC), avec son propre système d’exploitation, CPU, mémoire RAM, disque dur et carte réseau.
- **Système d’exploitation (OS)** : Ensemble de programmes permettant l’utilisation des ressources de l’ordinateur (mémoire, disque dur, processeur), incluant un noyau, une interface utilisateur et un système de fichiers.
- **Hôtes et invités** : Le matériel physique avec un hyperviseur est appelé « hôte », tandis que les machines virtuelles utilisant ses ressources sont appelées « invités ».