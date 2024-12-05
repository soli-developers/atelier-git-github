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

# séance 1 : Premiers Pas avec Git

#### **Objectifs pédagogiques :**

- Comprendre les bases de Git et son utilité.
- Configurer Git pour un projet local.
- Apprendre à suivre et gérer les versions des fichiers avec Git.

---

### **1. Introduction à Git et à la gestion de version (30 min)**

#### **1.1. Pourquoi utiliser Git ?**

Imaginez un projet où plusieurs personnes modifient un même fichier en même temps. Comment savoir qui a changé quoi, et à quel moment ? Git permet :

- De suivre l'historique des modifications.
- De collaborer efficacement avec une équipe.
- De revenir à une version précédente en cas d'erreur.

#### **1.2. Différence entre Git et GitHub :**

- **Git** : un outil installé sur votre ordinateur pour gérer les versions de vos fichiers.
- **GitHub** : une plateforme en ligne pour partager et collaborer sur les projets utilisant Git.

#### **1.3. Installation et configuration de Git :**

- **Installation** : téléchargez et installez Git depuis le site officiel : [git-scm.com](https://git-scm.com).
- **Configuration initiale** :
  Ouvrez un terminal et exécutez :
  ```bash
  git config --global user.name "Votre Nom"
  git config --global user.email "votre.email@example.com"
  ```
  Ces commandes définissent votre identité pour les commits.

---

### **2. Premiers pas avec Git (1h)**

#### **2.1. Initialisation d’un projet :**

1. Ouvrez un terminal.
2. Créez un dossier pour votre projet :
   ```bash
   mkdir mon_projet
   cd mon_projet
   ```
3. Initialisez un dépôt Git dans ce dossier :
   ```bash
   git init
   ```
   Résultat : Git commence à surveiller les fichiers de ce dossier.

#### **2.2. Suivi des fichiers :**

1. **Créer un fichier à suivre** :
   Par exemple, créez un fichier `README.md` :

   ```bash
   echo "Mon premier projet Git" > README.md
   ```

2. **Vérifier l’état des modifications** :

   ```bash
   git status
   ```

   Vous verrez que Git a détecté le fichier non suivi `README.md`.

3. **Ajouter le fichier au suivi** :

   ```bash
   git add README.md
   ```

4. **Valider les modifications** :

   ```bash
   git commit -m "Ajout du fichier README.md"
   ```

   Cela enregistre un "snapshot" de l'état actuel du fichier.

5. **Consulter l’historique des versions** :
   ```bash
   git log
   ```
   Vous verrez un historique détaillé de vos commits.

---

### **3. Exercice Pratique : Création d’un Dépôt Local (1h)**

#### **Étape 1 : Créez un projet local**

1. Créez un dossier nommé `projet_demo`.

   ```bash
   mkdir projet_demo
   cd projet_demo
   ```

2. Initialisez Git :
   ```bash
   git init
   ```

#### **Étape 2 : Ajoutez des fichiers et suivez-les avec Git**

1. Créez un fichier `index.html` :

   ```bash
   echo "<!DOCTYPE html><html><head><title>Demo</title></head><body>Bienvenue!</body></html>" > index.html
   ```

2. Vérifiez l’état avec `git status`, ajoutez-le avec `git add`, puis validez avec `git commit`:
   ```bash
   git status
   git add index.html
   git commit -m "Ajout du fichier index.html"
   ```

#### **Étape 3 : Faites des modifications et observez l’historique**

1. Modifiez `index.html` :

   ```bash
   echo "<footer>© 2024</footer>" >> index.html
   ```

2. Vérifiez les modifications détectées :

   ```bash
   git status
   git diff
   ```

3. Ajoutez et validez les changements :

   ```bash
   git add index.html
   git commit -m "Ajout d'un pied de page"
   ```

4. Consultez l’historique :
   ```bash
   git log --oneline
   ```

---

### **Récapitulatif : Commandes utilisées**

| Commande        | Description                               |
| --------------- | ----------------------------------------- |
| `git init`      | Initialise un dépôt Git dans un dossier.  |
| `git status`    | Affiche l’état des fichiers.              |
| `git add`       | Ajoute des fichiers au suivi.             |
| `git commit -m` | Valide les modifications avec un message. |
| `git log`       | Affiche l’historique des commits.         |
| `git diff`      | Montre les différences non validées.      |

Ce chapitre permet de maîtriser les bases et de se familiariser avec les commandes essentielles de Git. Souhaitez-vous approfondir un aspect particulier ? 😊

# **Séance 2 : Collaboration avec GitHub et Gestion des Modifications**

#### **Objectifs pédagogiques :**

- Découvrir comment collaborer en utilisant GitHub.
- Comprendre les mécanismes de synchronisation entre un dépôt local et un dépôt distant.
- Gérer les modifications et résoudre les conflits de manière pratique.

---

### **Thèmes abordés :**

#### **1. Collaboration avec GitHub (1h)**

##### **1.1. Création d’un dépôt sur GitHub**

1. Rendez-vous sur [GitHub](https://github.com) et connectez-vous à votre compte.
2. Cliquez sur **New Repository** (Nouveau dépôt).
3. Remplissez les informations :
   - Nom du dépôt : _par exemple `projet_demo`_.
   - Définissez les options (privé/public) et ajoutez un fichier `README.md` si souhaité.
4. Cliquez sur **Create Repository**.

##### **1.2. Liaison d’un projet local à GitHub**

1. Dans le terminal, placez-vous dans le dossier de votre projet local :

   ```bash
   cd chemin/vers/votre_projet
   ```

2. Ajoutez le dépôt distant (URL fournie par GitHub) :

   ```bash
   git remote add origin https://github.com/votre-utilisateur/projet_demo.git
   ```

3. Poussez votre dépôt local vers GitHub :
   ```bash
   git push -u origin main
   ```
   Cela synchronise le dépôt local avec GitHub.

##### **1.3. Gestion des clés SSH (Introduction rapide)**

Pour éviter de saisir votre mot de passe à chaque opération :

1. **Générez une clé SSH** :

   ```bash
   ssh-keygen -t rsa -b 4096 -C "votre.email@example.com"
   ```

2. **Ajoutez la clé SSH à votre compte GitHub** :
   - Copiez la clé publique :
     ```bash
     cat ~/.ssh/id_rsa.pub
     ```
   - Collez-la dans **Settings > SSH and GPG keys > New SSH Key** sur GitHub.

---

#### **2. Gestion des modifications et résolution de problèmes (30 min)**

##### **2.1. Récupération des modifications depuis GitHub**

- Utilisez la commande `git pull` pour récupérer les mises à jour du dépôt distant :
  ```bash
  git pull origin main
  ```

##### **2.2. Résolution des conflits**

1. **Quand les conflits apparaissent** :
   Un conflit survient lorsque deux utilisateurs modifient le même fichier à des endroits incompatibles.

2. **Résolution des conflits** :
   - Git vous alertera et ajoutera des marqueurs dans le fichier concerné :
     ```text
     <<<<<<< HEAD
     Votre modification locale
     =======
     Modification distante
     >>>>>>> origin/main
     ```
   - Modifiez le fichier pour conserver la bonne version.
   - Une fois corrigé, ajoutez le fichier corrigé :
     ```bash
     git add fichier_conflit
     git commit -m "Résolution de conflit"
     ```

---

#### **3. QCM (1h)**

##### **Validation des acquis de la session 1 :**

Le QCM couvre les notions suivantes :

- Commandes de base : `git init`, `git add`, `git commit`.
- Historique des versions : `git log`.
- Synchronisation avec GitHub : `git push`, `git pull`.
- Résolution des conflits : compréhension des marqueurs de conflit.

**Score minimal requis : 70% pour accéder à la Session 2.**

---

### **Exercice Pratique : Collaboration avec GitHub**

**Objectif :**
Collaborer sur un projet partagé et résoudre des conflits.

**Durée :** 1h30

**Étapes :**

1. **Création du dépôt partagé** :

   - Un participant crée un dépôt sur GitHub et ajoute les autres comme collaborateurs.

2. **Clonage du dépôt** :

   - Les collaborateurs clonent le dépôt sur leurs machines :
     ```bash
     git clone https://github.com/votre-utilisateur/projet_demo.git
     cd projet_demo
     ```

3. **Modifications simultanées** :

   - Chaque participant modifie un fichier (par ex. `README.md`) et pousse les modifications :
     ```bash
     git add README.md
     git commit -m "Modification par utilisateur A"
     git push origin main
     ```

4. **Gestion des conflits** :
   - Lorsque plusieurs utilisateurs modifient le même fichier, des conflits peuvent apparaître lors d’un `git pull`.
   - Les participants doivent résoudre les conflits et valider les corrections.

---

### **Récapitulatif : Commandes utilisées dans cette séance**

| Commande         | Description                                     |
| ---------------- | ----------------------------------------------- |
| `git remote add` | Ajoute un dépôt distant.                        |
| `git push`       | Pousse les modifications vers le dépôt distant. |
| `git pull`       | Récupère les modifications du dépôt distant.    |
| `ssh-keygen`     | Génère une clé SSH pour GitHub.                 |
| `git clone`      | Clone un dépôt distant en local.                |

---

# Contexte :

donner un exemple de qcm pour la seance 2 avec niveaux de langue debutant et intermédiaire
