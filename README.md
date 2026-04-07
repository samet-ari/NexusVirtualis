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
- Utiliser **VMware Workstation Pro** comme hyperviseur de type 2 pour exécuter des hyperviseurs de type 1 (nested virtualization).  
- Déployer une **VM Debian** sur chaque hyperviseur pour valider leur fonctionnement.  
- Manipuler les réseaux NAT, Host-Only et Bridged.

---

## :jigsaw: Architecture globale

---

## :desktop_computer: Hyperviseurs étudiés

| Hyperviseur | Type | Licence | Notes |
|------------|------|---------|-------|
| VMware ESXi 8.0 | Type 1 | Free/Commercial | Référence datacenter |
| Microsoft Hyper-V | Type 1 | Inclus Windows Server | Intégration AD/Windows |
| Proxmox VE 8.x | Type 1 | Open Source | KVM + LXC, très pédagogique |
| XCP-ng 8.3 | Type 1 | Open Source | Basé sur XenServer |

---

## :gear: Préparation de l’environnement

### Activation de la virtualisation imbriquée

- Activer **Intel VT-x / AMD-V** dans le BIOS/UEFI.
- Dans VMware Workstation :  
  - Activer **Virtualize Intel VT-x/EPT**  
  - Activer **IOMMU** si disponible.

---

## :satellite: Réseau VMware Workstation

| Mode | Internet | Accès hôte | Usage |
|------|----------|------------|--------|
| NAT | Oui | Non | Téléchargements, mises à jour |
| Host-Only | Non | Oui | Réseau isolé |
| Bridged | Oui | Oui | Cluster Proxmox (bonus) |

---

## :cd: Téléchargement des ISOs

- ESXi 8.0 → Broadcom  
- Windows Server 2022 → Microsoft Evaluation Center  
- Proxmox VE → Téléchargement libre  
- XCP-ng → Téléchargement libre  

---

## :hammer_and_wrench: Installation des hyperviseurs

### ✔️ ESXi 8.0  
- 12 Go RAM  
- 40 Go disque  
- 2 NIC (NAT + Host-Only)

### ✔️ Hyper-V  
- Windows Server 2022  
- Secure Boot désactivé pour Debian  

### ✔️ Proxmox VE  
- 8 Go RAM  
- 60 Go disque  

### ✔️ XCP-ng  
- 8 Go RAM  
- 60 Go disque  

---

## :penguin: VM Debian embarquée

| Paramètre | Valeur |
|----------|--------|
| vCPU | 2 |
| RAM | 1 Go |
| Disque | 8 Go |
| ISO | Debian netinst |
| Secure Boot | Off |

---

## :books: Ressources & Références

- Documentation officielle VMware, Microsoft, Proxmox, XCP-ng  
- Extraits du document *Opération Nexus Virtualis*  
