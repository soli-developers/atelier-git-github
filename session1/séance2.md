### **Séance 2 : Collaboration avec GitHub et Gestion des Modifications**  

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
   - Nom du dépôt : *par exemple `projet_demo`*.  
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

| Commande            | Description                                 |  
|---------------------|---------------------------------------------|  
| `git remote add`    | Ajoute un dépôt distant.                   |  
| `git push`          | Pousse les modifications vers le dépôt distant. |  
| `git pull`          | Récupère les modifications du dépôt distant. |  
| `ssh-keygen`        | Génère une clé SSH pour GitHub.            |  
| `git clone`         | Clone un dépôt distant en local.           |  

---