# 🌌 M-CORE (Mobile-first Continuity & Offline Rendering Engine)

**Infrastructure de publication technique résiliente : L'excellence du Docs-as-Code, du mobile au Desktop.** *Idéale pour la Production, la Validation, le Stockage et la Diffusion d'informations en conditions extrêmes.*

![M-CORE Status](https://img.shields.io/badge/Status-Industrial_Beta-blue)
![License](https://img.shields.io/badge/License-Apache_2.0-orange)
![Arch](https://img.shields.io/badge/Arch-ARM64_%7C_x86_64-success)

-----

## 📌 Vision Industrielle

**M-CORE** est une infrastructure hybride conçue pour garantir la continuité de production technique en environnements dégradés. Il fournit un écosystème **Offline-First** capable de briser la dépendance aux infrastructures fixes.

L'objectif est de permettre aux ingénieurs et étudiants de maintenir un flux de production de haute qualité (**Docs-as-Code**) malgré l'instabilité énergétique (ENEO), les ruptures de connectivité ou les contraintes de mobilité. M-CORE unifie les flux de travail entre terminaux mobiles (Android/iOS) et stations de travail (Windows/Linux/macOS), transformant le Markdown brut en livrables certifiés (Web/PDF) sans accès Internet requis.

## 🏗️ Architecture de l'Écosystème

Le projet est orchestré selon un modèle de **Meta-Sourcing** via `git submodules`, garantissant une gestion granulaire des droits et une maintenance modulaire.

| Couche | Composant | Stack | Rôle Stratégique |
| :--- | :--- | :--- | :--- |
| **Orchestration** | [`m-core`](https://github.com/M-Core-Engineering/m-core.git) | Go-Task / CI-CD | Automatisation multi-OS et pipelines GitHub Actions. |
| **Kernel** | [`engine`](https://github.com/M-Core-Engineering/engine.git) | Rust / Go | Moteur propriétaire de transformation haute performance. |
| **Governance** | [`spec`](https://github.com/M-Core-Engineering/spec.git) | Vale / YAML | Standards de validation et conformité sémantique métier. |
| **Design** | [`templates`](https://github.com/M-Core-Engineering/templates.git) | Typst / Zola | Bibliothèque de composants UI et layouts industriels. |
| **Distribution** | [`showcase`](https://github.com/M-Core-Engineering/showcase.git) | HTMX / Alpine | Interface de diffusion Web optimisée pour l'Edge Computing. |
| **Bridge** | [`mobile`](https://github.com/M-Core-Engineering/mobile.git) | Tauri / Rust | Client natif Android/iOS et accès au système de fichiers. |

## 🚀 Le Workflow "M-Flow" (Cross-Platform)

M-CORE agit comme une **IaaS** portable synchronisant la rigueur du Desktop avec la flexibilité du Mobile :

1. **Authoring** : Rédaction fluide sur IDE (VS Code, Obsidian) ou terminaux mobiles (Termux).
2. **Linting & Policy** : Validation automatique immédiate selon les standards `spec`.
3. **Local Build** : Génération instantanée des artefacts (HTML5/PDF) en local (100% Offline).
4. **Cloud Sync & Deploy** : Dès reconnexion, déploiement sécurisé vers Cloudflare Pages via GitHub Actions.

## 🛠️ Démarrage Rapide

L'initialisation est automatisée via **Go-Task** pour garantir la cohérence de l'environnement sur tous les systèmes d'exploitation.

### 1\. Pré-requis (Gestionnaires de paquets)

* **Windows** : [Scoop](https://scoop.sh/) (Recommandé) ou Winget.
* **Android** : [Termux](https://termux.dev/).
* **Linux/macOS** : Apt, Brew ou Nix.

### 2\. Clonage et Initialisation

```bash
# Clonage récursif incluant tous les modules
git clone --recursive https://github.com/M-Core-Engineering/m-core.git
cd m-core

# Initialisation de l'environnement (Nécessite Go-Task)
task setup

# Vérification de l'intégrité
task lint
```

> **Note :** Si vous avez déjà cloné le dépôt sans l'option `--recursive`, exécutez :
> `git submodule update --init --recursive`

## 🛠️ Déploiement & Industrialisation

M-CORE utilise l'abstraction de tâches pour garantir la reproductibilité des builds en tout lieu.

```bash
# Cycle de validation et rendu local
task build:local

# Préparation au déploiement (Vérification CI/CD)
task deploy:check
```

## ⚖️ Philosophie & Principes d'Ingénierie (ROI)

* **Indépendance Infrastructurelle** : Réduction drastique des temps d'arrêt liés aux pannes réseau ou électriques.
* **Souveraineté des Données** : Versionnage intégral sous Git, assurant la traçabilité et l'auditabilité.
* **Frugal Engineering** : Priorité aux outils à binaire unique (Rust/Go) pour minimiser l'empreinte thermique et mémoire.
* **Qualité par Design** : Chaque document est traité comme un actif logiciel (versionné, testé, validé).
* **Indépendance Système** : Expérience utilisateur identique sur smartphone et station de travail.

-----

## 📊 Roadmap du MVP

* [x] Définition des standards d'édition (syntaxe **M-Spec**).
* [ ] Finalisation du moteur de rendu binaire multiplateforme.
* [ ] Automatisation complète du déploiement Edge.
* [ ] Interface de gestion de projet Mobile-First (Tauri).

-----

**Mainteneur Principal** : [Nguetsa Lorein Du Perron](https://github.com/lorein-duperron)
**Licence** : [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0) — *Garantissant la liberté d'usage et la protection des contributions.*
