
---

## **Diapositive 1 : Introduction à Git**

### **Titre : Pourquoi utiliser Git ?**

- **Description** :
  - Gestion des versions pour suivre l'historique des fichiers.
  - Collaboration efficace dans une équipe.
  - Possibilité de revenir à des versions antérieures.
- **Illustration** :
  - Icône de fichiers empilés avec une flèche de retour en arrière.

---

## **Diapositive 2 : Différence entre Git et GitHub**

### **Titre : Git vs GitHub**

- **Description** :
  - **Git** : Outil local pour gérer les versions.
  - **GitHub** : Plateforme en ligne pour partager et collaborer.
- **Illustration** :
  - Icône d'une console pour Git et un nuage avec un logo GitHub pour GitHub.

---

## **Diapositive 3 : Installation et Configuration**

### **Titre : Installer et configurer Git**

- **Description** :
  - Téléchargement depuis [git-scm.com](https://git-scm.com).
  - Configuration de l’identité avec :
    ```bash
    git config --global user.name "Votre Nom"
    git config --global user.email "votre.email@example.com"
    ```
- **Illustration** :
  - Icône d'engrenages et d'ordinateur.

---

## **Diapositive 4 : Initialisation d’un Projet**

### **Titre : Commencer avec Git**

- **Description** :
  - Créer un dossier :
    ```bash
    mkdir mon_projet
    cd mon_projet
    ```
  - Initialiser un dépôt Git :
    ```bash
    git init
    ```
- **Illustration** :
  - Icône de dossier avec un symbole Git.

---

## **Diapositive 5 : Suivi des Fichiers**

### **Titre : Suivre les fichiers avec Git**

- **Description** :
  - Ajouter un fichier au suivi :
    ```bash
    git add fichier.txt
    ```
  - Valider les modifications :
    ```bash
    git commit -m "Message du commit"
    ```
  - Vérifier l’état :
    ```bash
    git status
    ```
- **Illustration** :
  - Icône de check-list ou fichier suivi par une flèche.

---

## **Diapositive 6 : Historique des Modifications**

### **Titre : Historique des Versions**

- **Description** :
  - Voir l’historique des commits :
    ```bash
    git log
    ```
  - Résultat : Identifiants des commits, auteurs, et messages associés.
- **Illustration** :
  - Ligne de temps avec des nœuds représentant les commits.

---

## **Diapositive 7 : Exercice Pratique**

### **Titre : Créez votre premier dépôt**

- **Étapes** :
  1. Créer un dossier :
     ```bash
     mkdir projet_demo
     cd projet_demo
     ```
  2. Initialiser Git :
     ```bash
     git init
     ```
  3. Créer un fichier `index.html` et ajouter du contenu :
     ```bash
     echo "<html><body>Hello Git!</body></html>" > index.html
     ```
  4. Ajouter et valider le fichier :
     ```bash
     git add index.html
     git commit -m "Ajout du fichier index.html"
     ```
- **Illustration** :
  - Capture d’écran simulée d’un terminal exécutant ces commandes.

---

## **Diapositive 8 : Récapitulatif des Commandes**

### **Titre : Commandes Essentielles de Git**

| **Commande**    | **Description**                           |
| --------------- | ----------------------------------------- |
| `git init`      | Initialise un dépôt.                      |
| `git add`       | Ajoute des fichiers au suivi.             |
| `git commit -m` | Valide les modifications avec un message. |
| `git status`    | Vérifie l’état des fichiers.              |
| `git log`       | Affiche l’historique des versions.        |

- **Illustration** :
  - Icônes pour chaque commande (par ex., horloge pour `git log`).

---

Avec ce plan, vous avez une base pour concevoir des diapositives engageantes. Souhaitez-vous des détails supplémentaires ou des suggestions pour un outil de création comme PowerPoint, Canva, ou Google Slides ?
