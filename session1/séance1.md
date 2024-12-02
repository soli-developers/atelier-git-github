### **Chapitre : Premiers Pas avec Git**  

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
| Commande            | Description                                 |  
|---------------------|---------------------------------------------|  
| `git init`          | Initialise un dépôt Git dans un dossier.   |  
| `git status`        | Affiche l’état des fichiers.               |  
| `git add`           | Ajoute des fichiers au suivi.              |  
| `git commit -m`     | Valide les modifications avec un message.  |  
| `git log`           | Affiche l’historique des commits.          |  
| `git diff`          | Montre les différences non validées.       |  
