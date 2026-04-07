# Opération Nexus Virtualis  
## ?? Virtualisation avancée & Hyperviseurs Type 1 en environnement imbriqué

> « La virtualisation permet de créer des versions virtuelles de ressources physiques telles que des serveurs, du stockage ou des réseaux. »

Ce projet explore quatre hyperviseurs de type 1 (ESXi, Hyper-V, Proxmox VE, XCP-ng) exécutés en virtualisation imbriquée via VMware Workstation Pro.  
Il constitue un laboratoire complet pour comprendre la virtualisation professionnelle.

---

## ?? Sommaire

- ?? Objectifs du projet  
- ?? Architecture globale  
- ??? Hyperviseurs étudiés  
- ?? Préparation de l’environnement  
- ?? Réseau VMware Workstation  
- ?? Téléchargement des ISOs  
- ??? Installation des hyperviseurs  
- ?? VM Debian embarquée  
- ?? Ressources & Références  

---

## ?? Objectifs du projet

- Comprendre les concepts fondamentaux des hyperviseurs Type 1  
- Installer et configurer ESXi, Hyper-V, Proxmox VE et XCP-ng  
- Utiliser VMware Workstation Pro pour exécuter des hyperviseurs Type 1 (nested virtualization)  
- Déployer une VM Debian sur chaque hyperviseur  
- Manipuler les réseaux NAT, Host-Only et Bridged  

---

## ?? Architecture globale

\\\
PC Hôte (Windows / Linux)
¦
+-- VMware Workstation Pro (Type 2)
      +-- VM ESXi 8.0
      ¦     +-- VM Debian
      +-- VM Hyper-V (Windows Server 2022)
      ¦     +-- VM Debian
      +-- VM Proxmox VE
      ¦     +-- VM Debian
      +-- VM XCP-ng
            +-- VM Debian
\\\

---

## ??? Hyperviseurs étudiés

| Hyperviseur | Type | Licence | Notes |
|------------|------|---------|-------|
| VMware ESXi 8.0 | Type 1 | Free/Commercial | Référence datacenter |
| Microsoft Hyper-V | Type 1 | Inclus Windows Server | Intégration AD/Windows |
| Proxmox VE 8.x | Type 1 | Open Source | KVM + LXC |
| XCP-ng 8.3 | Type 1 | Open Source | Basé sur XenServer |

---

## ?? Préparation de l’environnement

### Activation de la virtualisation imbriquée

- Activer Intel VT-x / AMD-V dans le BIOS/UEFI  
- Dans VMware Workstation :  
  - Activer « Virtualize Intel VT-x/EPT »  
  - Activer IOMMU si disponible  

---

## ?? Réseau VMware Workstation

| Mode | Internet | Accès hôte | Usage |
|------|----------|------------|--------|
| NAT | Oui | Non | Téléchargements, mises à jour |
| Host-Only | Non | Oui | Réseau isolé |
| Bridged | Oui | Oui | Cluster Proxmox (bonus) |

---

## ?? Téléchargement des ISOs

- ESXi 8.0 ? Broadcom  
- Windows Server 2022 ? Microsoft Evaluation Center  
- Proxmox VE ? Téléchargement libre  
- XCP-ng ? Téléchargement libre  

---

## ??? Installation des hyperviseurs

### ESXi 8.0  
- 12 Go RAM  
- 40 Go disque  
- 2 NIC (NAT + Host-Only)

### Hyper-V  
- Windows Server 2022  
- Secure Boot désactivé pour Debian  

### Proxmox VE  
- 8 Go RAM  
- 60 Go disque  

### XCP-ng  
- 8 Go RAM  
- 60 Go disque  

---

## ?? VM Debian embarquée

| Paramètre | Valeur |
|----------|--------|
| vCPU | 2 |
| RAM | 1 Go |
| Disque | 8 Go |
| ISO | Debian netinst |
| Secure Boot | Off |

---

## ?? Ressources & Références

- Documentation officielle VMware, Microsoft, Proxmox, XCP-ng  
- Extraits du document « Opération Nexus Virtualis »  
