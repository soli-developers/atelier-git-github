# **Plan de Formation : Git et GitHub**


## **Session 1 : Introduction et Bases de Git**  
**Objectifs pédagogiques** :
- Comprendre les principes de base de Git.  
- Manipuler Git en ligne de commande pour le suivi des versions.  
- Configurer un projet local et interagir avec un dépôt distant.  

**Séance 1 (2h30)** :  
**Thèmes abordés** :  
1. Introduction à Git et à la gestion de version (30 min) :
   - Problématique résolue par Git.
   - Différence entre Git et GitHub.
   - Installation et configuration initiale (éditeur, identité, etc.).

2. Premiers pas avec Git (1h) :  
   - Initialisation d’un répertoire avec `git init`.
   - Ajout et suivi des fichiers : commandes `git add`, `git status`, et `git commit`.
   - Historique des versions avec `git log`.

3. Exercice pratique (1h) :  
   - Création d'un répertoire local.
   - Ajout et modification de fichiers, suivi et validation des modifications.

**Séance 2 (2h30)** :  
**Thèmes abordés** :
1. Collaboration avec GitHub (1h) :
   - Création d’un dépôt GitHub.
   - Liaison d’un projet local à GitHub : `git remote` et `git push`.
   - Gestion des clés SSH (introduction rapide).

2. Gestion des modifications et résolution de problèmes (30 min) :
   - Récupération des modifications avec `git pull`.
   - Résolution des conflits (concepts et exemples simples).

3. QCM (1h) :
   - Validation des acquis de la session 1.
   - Accès à la session 2 uniquement après validation (score minimal requis : 70%).

---

## **Session 2 : Collaboration avancée et bonnes pratiques**  
**Objectifs pédagogiques** :  
- Maîtriser les branches pour travailler en équipe.  
- Appliquer les bonnes pratiques Git et GitHub.  

**Séance 3 (2h30)** :  
**Thèmes abordés** :  
1. Gestion des branches (1h) :  
   - Concepts de branche et d’intégration continue.
   - Création, changement et fusion de branches : `git branch`, `git checkout`, `git merge`.

2. Collaboration avec les Pull Requests (30 min) :
   - Introduction aux Pull Requests sur GitHub.
   - Révision de code et validation collaborative.

3. Exercice pratique (1h) :  
   - Travail à plusieurs sur un projet exemple.
   - Création de branches, gestion des modifications et fusion des changements.

**Séance 4 (2h30)** :
**Thèmes abordés** :
1. Bonnes pratiques Git (1h) :  
   - Convention de messages de commit.
   - Organisation des dépôts (README, fichiers `.gitignore`, etc.).

2. Exercice de synthèse (1h30) :
   - Gestion d’un projet complet incluant branches, conflits, et Pull Requests.

---

## **Exercice d’Introduction : Ligne de Commande**

**Objectif** : Apprendre à naviguer et gérer des fichiers dans un terminal, base essentielle pour comprendre les commandes Git.

**Durée** : 1 heure.

### **Scénario** :
Un nouveau projet est en cours de création, mais l’organisation des fichiers doit être faite via la ligne de commande.

**Activités** :
1. **Navigation dans le terminal** (15 min) :
   - Commandes de base : `pwd`, `ls`, `cd`.
   - Création de dossiers : `mkdir projet_git`.

2. **Gestion des fichiers** (20 min) :
   - Création de fichiers : `touch README.md`.
   - Modification d’un fichier avec un éditeur (par ex. `nano`, `vim`, ou autre).
   - Copie, déplacement, suppression : `cp`, `mv`, `rm`.

3. **Exercice guidé** (25 min) :
   - Scénario : Créer une structure de répertoire pour un projet fictif :
     - **Arborescence demandée** :
       ```
       projet_git/
       ├── src/
       │   └── main.js
       ├── docs/
       │   └── README.md
       └── assets/
           └── logo.png
       ```
   - Réaliser les manipulations uniquement via la ligne de commande.

