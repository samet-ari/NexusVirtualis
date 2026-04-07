# :satellite: Opération Nexus Virtualis  
### **Virtualisation avancée & Hyperviseurs Type 1 en environnement imbriqué**

> « La virtualisation est une technologie qui permet de créer des versions virtuelles de ressources physiques telles que des serveurs, des systèmes de stockage ou des réseaux. »

Ce projet a pour objectif d’explorer, installer et comparer **quatre hyperviseurs de type 1** (ESXi, Hyper-V, Proxmox VE, XCP-ng) au sein d’un environnement de virtualisation imbriquée basé sur **VMware Workstation Pro**.

Il constitue un **laboratoire complet**, documenté étape par étape, permettant d’apprendre les fondamentaux de la virtualisation professionnelle.

---

## :book: Sommaire

- :dart: Objectifs du projet
- :jigsaw: Architecture globale
- :desktop_computer: Hyperviseurs étudiés
- :gear: Préparation de l’environnement
- :satellite: Réseau VMware Workstation
- :cd: Téléchargement des ISOs
- :hammer_and_wrench: Installation des hyperviseurs
- :penguin: VM Debian embarquée
- :books: Ressources & Références

---

## :dart: Objectifs du projet

- Comprendre les **concepts fondamentaux** des hyperviseurs Type 1.  
- Installer et configurer **ESXi, Hyper-V, Proxmox VE et XCP-ng**.  
- Utiliser **VMware Workstation Pro** comme hyperviseur de type 2 (nested virtualization).  
- Déployer une **VM Debian** sur chaque hyperviseur.  
- Manipuler les réseaux NAT, Host-Only et Bridged.

---

## :jigsaw: Architecture globale

PC Hôte (Windows / Linux)
│
└── VMware Workstation Pro (Type 2)
      ├── VM ESXi 8.0
      │     └── VM Debian
      ├── VM Hyper-V (Windows Server 2022)
      │     └── VM Debian
      ├── VM Proxmox VE
      │     └── VM Debian
      └── VM XCP-ng
            └── VM Debian

---

## :desktop_computer: Hyperviseurs étudiés

- VMware ESXi 8.0  
- Microsoft Hyper-V  
- Proxmox VE  
- XCP-ng  

---

## :gear: Préparation de l’environnement

- Activation Intel VT-x / AMD-V  
- Activation Virtualize VT-x/EPT dans VMware  

---

## :satellite: Réseau VMware Workstation

- NAT  
- Host-Only  
- Bridged  

---

## :cd: ISOs

- ESXi  
- Windows Server 2022  
- Proxmox VE  
- XCP-ng  

---

## :hammer_and_wrench: Installation

- ESXi  
- Hyper-V  
- Proxmox  
- XCP-ng  

---

## :penguin: VM Debian

- 2 vCPU  
- 1 Go RAM  
- 8 Go disque  

---

## :books: Ressources

- Documentation officielle des hyperviseurs  
