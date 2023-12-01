---
layout: page
title: "Git - TP 1"
permalink: /git/tp/1

# Course related
course:
  name: Git
  sessions:
  - "2023-12-08"
  - "2023-12-15"
---

## Pré-requis

* Assurez-vous d'avoir un environnement dans lequel vous pouvez exécuter des commandes Git et Docker.
  - `git version`
  - `docker --version`
* Assurez-vous d'avoir un compte GitHub.
<br>Ne créez pas de compte avec votre adresse mail ORT ; ce compte pourra vous servir plus tard.

## 1. Mise en place du dépôt et de l'environnement local

### Création du dépôt

L'une des personnes du groupe va prendre la responsabilité du dépôt :

1. Création du dépôt "3olen-git-tp1" dans votre espace personnel.
<br>Cochez la case "Initialize this repository with: Add a README file".
2. 👥 Ajoutez l'étudiant 2 (et l'étudiant 3) comme collaborateur sur votre dépôt.
<br>Settings > Access > Collaborators
3. 🔒️ Protégez la branche `main` de votre dépôt.
<br>Settings > Branches > Branch protection rules > Add branch protection rule

Il existe plusieurs règles de protection, nous n'allons en sélectionner que quelques-unes, des règles considérées comme
"basiques" et qui aident à maintenir la collaboration sur un projet.

1. Branch name pattern: `main`
2. Protect matching branches:
  * Cochez "Require a pull request before merging" (1ère option).
  <br>Cette règle oblige les contributeurs à créer une branche et une pull request (PR) pour intégrer des commits sur
  la branche `main`.
    - Cochez la sous-option "Require approvals" (en spécifiant la valeur `1`).
    <br>Cette règle oblige une approbation de la PR par un autre contributeur, suite à sa revue/relecture de code,
    avant de pouvoir la merger.
    - Cochez la sous-option "Dismiss stale pull request approvals when new commits are pushed".
    <br>Cette règle réinitialise les approbations si de nouveaux changements sont intégrés à la PR.
  * Cochez "Require conversation resolution before merging" (3ème option).
  <br>Cette règle oblige la résolution des discussions/retours d'une PR avant de pouvoir la merger.

### Mise en place de l'environnement local

Dès lors que le dépôt est créé, chaque étudiant va pouvoir le cloner en local.

Vous allez ensuite vérifier que l'environnement local est correctement mis en place :

{% assign resource_script_assert_1 = site.static_files | where: "name", "assert-01-env" | first %}

1. Récupérez le fichier : [scripts/assert-01-env]({{ resource_script_assert_1.path | relative_url }}).
2. Déplacez-le dans le dossier `bin/assert` de votre dépôt.
3. Assurez-vous qu'il est bien exécutable avec les commandes appropriées.
4. Exécutez-le : `bin/assert/01-env`.
<br>Cela va de soi que votre terminal est positionné à la racine du dépôt.
