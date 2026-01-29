# VBS Overlay

Outil d’overlay système pour serveurs médias et machines de production audiovisuelle.

## ⬇️ Téléchargement
Les versions officielles sont disponibles ici :
👉 https://github.com/phalbig-VBS/VBS-Overlay/releases


## VBS Overlay — 📘 Manuel utilisateur

**VBS Overlay — User Manual / Manuel utilisateur**

**Version : VBS Overlay vX.Y.Z**  
**Publisher / Éditeur : Video Bridge Solutions**

**Table of Contents / Sommaire**

| **Français** | **English** |
| --- | --- |
| Présentation générale | General Overview |
| Prérequis et environnement recommandé | Requirements and Recommended Environment |
| Installation | Installation |
| Démarrage et principes de fonctionnement | Startup and Operating Principles |
| Menu Tray | Tray Menu |
| Dashboard | Dashboard |
| Fenêtre Manage | Manage Window |
| Machines | Machines |
| Link, Show Mode, Pattern, Desk Lock | Link, Show Mode, Pattern, Desk Lock |
| Flags & OSC | Flags & OSC |
| Bonnes pratiques d’exploitation | Operational Best Practices |
| Dépannage | Troubleshooting |
| Support, mises à jour et distribution | Support, Updates, and Distribution |

**Présentation générale / General Overview**

| **Français** | **English** |
| --- | --- |
| VBS Overlay est un outil de supervision système et réseau destiné aux machines de production audiovisuelle (media servers, régies, machines de backup). | VBS Overlay is a system and network monitoring tool designed for audiovisual production machines (media servers, control rooms, backup machines). |
| Il affiche un overlay non intrusif permettant une lecture immédiate de l’état réel de la machine. | It displays a non-intrusive overlay that provides an immediate view of the machine’s real status. |

**Informations affichées / Displayed information**

| **Français** | **English** |
| --- | --- |
| état général | overall system status |
| GPU et VRAM | GPU and VRAM |
| interfaces réseau | network interfaces |
| stockage | storage |
| machines du LAN | LAN machines |
| indicateurs d’état (Flags) | status indicators (Flags) |

**Objectif / Objective**

| **Français** | **English** |
| --- | --- |
| Savoir immédiatement si tout fonctionne correctement, sans perturber l’exploitation live. | Instantly know whether everything is working correctly, without disrupting live operations. |

**Prérequis et environnement recommandé / Requirements and Recommended Environment**

**Système / System**

| **Français** | **English** |
| --- | --- |
| Windows 10 ou Windows 11 (x64) | Windows 10 or Windows 11 (x64) |
| Droits administrateur requis pour l’installation | Administrator rights required for installation |

**Environnement cible / Target Environment**

| **Français** | **English** |
| --- | --- |
| Media Server (Resolume, etc.) | Media Server (Resolume, etc.) |
| GPU dédié (AMD ou NVIDIA) | Dedicated GPU (AMD or NVIDIA) |
| Réseau local actif (LAN) | Active local network (LAN) |

**Installation**

**Installation standard / Standard Installation**

| **Français** | **English** |
| --- | --- |
| Télécharger la dernière version depuis la section Releases | Download the latest version from the Releases section |
| Lancer VBSOverlay_Setup_vX.Y.Z.exe | Launch VBSOverlay_Setup_vX.Y.Z.exe |
| Suivre l’assistant d’installation | Follow the installation wizard |

**Installation silencieuse / Silent Installation (optional)**

| **Français** | **English** |
| --- | --- |
| VBSOverlay_Setup_vX.Y.Z.exe /SILENT | VBSOverlay_Setup_vX.Y.Z.exe /SILENT |

**Démarrage et principes de fonctionnement / Startup and Operating Principles**

**Lancement / Startup**

| **Français** | **English** |
| --- | --- |
| VBS Overlay démarre en tâche utilisateur | VBS Overlay runs as a user-level process |
| Une icône apparaît dans la zone de notification (Tray) | An icon appears in the system notification area (Tray) |

**Philosophie générale / General Philosophy**

| **Français** | **English** |
| --- | --- |
| Aucun focus pris sur les applications de show | No focus is taken from show applications |
| Overlay transparent et non cliquable | Transparent and non-clickable overlay |
| Impact négligeable sur les performances système | Negligible impact on system performance |

**Menu Tray / Tray Menu**

| **Français** | **English** |
| --- | --- |
| Le Menu Tray est le point d’accès principal à VBS Overlay. | The Tray Menu is the main access point to VBS Overlay. |
| Il permet de piloter l’application sans ouvrir de fenêtre intrusive. | It allows you to control the application without opening any intrusive window. |

**Fonctions disponibles / Available Functions**

| **Français** | **English** |
| --- | --- |
| Ouvrir le Dashboard | Open the Dashboard |
| Ouvrir la fenêtre Manage | Open the Manage window |
| Afficher / masquer l’Overlay | Show / hide the Overlay |
| Quitter l’application (arrêt propre) | Quit the application (clean shutdown) |

**Dashboard**

| **Français** | **English** |
| --- | --- |
| Le Dashboard est l’interface de supervision en temps réel. | The Dashboard is the real-time monitoring interface. |
| Il sert à observer, pas à configurer. | It is designed for observation, not configuration. |

**Informations générales / General Information**

| **Français** | **English** |
| --- | --- |
| Nom de la machine | Machine name |
| Version de VBS Overlay | VBS Overlay version |
| État global | Global status |

**GPU**

| **Français** | **English** |
| --- | --- |
| Liste complète des GPU détectés | Complete list of detected GPUs |
| Utilisation GPU | GPU usage |
| VRAM utilisée / disponible | VRAM used / available |
| Support multi-GPU | Multi-GPU support |

**Fenêtre Manage / Manage Window**

| **Français** | **English** |
| --- | --- |
| La fenêtre Manage est le centre de configuration de VBS Overlay. | The Manage window is the configuration center of VBS Overlay. |
| Toute modification doit être effectuée hors exploitation live. | Any modification must be performed outside of live operation. |

**Sections principales / Main Sections**

| **Français** | **English** |
| --- | --- |
| Machines | Machines |
| Link | Link |
| Options associées | Associated options |

**Flags & OSC**

**Définition / Definition**

| **Français** | **English** |
| --- | --- |
| Un Flag est un indicateur visuel d’état. | A Flag is a visual status indicator. |
| Il n’exécute aucune action et ne déclenche aucun automatisme. | It performs no action and triggers no automation. |

**Principe du heartbeat / Heartbeat Principle**

| **Français** | **English** |
| --- | --- |
| Messages reçus régulièrement → Flag ON | Messages received regularly → Flag ON |
| Arrêt des messages → timeout → Flag OFF | Messages stop → timeout → Flag OFF |

**Structure OSC recommandée / Recommended OSC Structure**

| **Français** | **English** |
| --- | --- |
| /vbs/flag/&lt;nom_du_flag&gt; | /vbs/flag/&lt;flag_name&gt; |

**Bonnes pratiques d’exploitation / Operational Best Practices**

| **Français** | **English** |
| --- | --- |
| Vérifier le Dashboard avant le show | Check the Dashboard before the show |
| Activer Show Mode avant public | Enable Show Mode before the audience |
| Tester Pattern hors exploitation | Test Pattern outside live operation |
| Utiliser les flags comme indicateurs, jamais comme commandes | Use flags as indicators only, never as controls |

**Dépannage / Troubleshooting**

**Overlay absent / Overlay Not Visible**

| **Français** | **English** |
| --- | --- |
| Vérifier l’icône Tray | Check the Tray icon |
| Vérifier l’écran cible | Check the target display |
| Vérifier les droits utilisateur | Check user permissions |

**Support, mises à jour et distribution / Support, Updates, and Distribution**

| **Français** | **English** |
| --- | --- |
| Les mises à jour sont disponibles via GitHub Releases | Updates are available via GitHub Releases |
| Toujours vérifier la cohérence version application ↔ version manuel | Always verify application version ↔ manual version consistency |

**Le code source n’est pas public.**  
**The source code is not public.**

© Video Bridge Solutions — VBS Overlay



