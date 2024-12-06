# Exercice : Introduction à Git et GitHub pour débutants

---

## Contexte du projet : 
Vous travaillez sur un projet de site web simple avec vos coéquipiers. Le projet se compose d’un fichier `index.html` que vous devez modifier pour y ajouter du contenu.

---

## Étapes de l'exercice :

### 1. Préparation du dépôt local :  
1. Cloner le dépôt GitHub sur votre machine :  
   ```bash
   git clone https://github.com/<nom_utilisateur>/atelier-git.git
   cd atelier-git
   ```

2. Afficher l’état du dépôt :  
   ```bash
   git status
   ```

---

### 2. Travailler sur le projet :  
1. Ajouter du contenu au fichier `index.html` :  
   - Ouvrez le fichier `index.html` et ajoutez une ligne à l’intérieur de la balise `<body>`.  
     Exemple :  
     ```html
     <p>Bienvenue à l'atelier Git et GitHub !</p>
     ```

2. Ajouter les modifications au suivi de Git :  
   ```bash
   git add index.html
   ```

3. Créer un commit pour enregistrer les modifications localement :  
   ```bash
   git commit -m "Ajout d'un message de bienvenue"
   ```

4. Envoyer les modifications sur le dépôt distant :  
   ```bash
   git push origin main
   ```

---

### 3. Simuler un conflit :  
1. Un autre participant modifie également le fichier `index.html` et fait un `push`.  
2. Vous essayez maintenant de récupérer les modifications du dépôt distant :  
   ```bash
   git pull origin main
   ```

3. Résolution du conflit :  
   - Git vous avertit qu’il y a un conflit dans le fichier `index.html`.  
   - Ouvrez le fichier et vous verrez des marqueurs de conflit :  
     ```html
     <<<<<<< HEAD
     <p>Bienvenue à l'atelier Git et GitHub !</p>
     =======
     <p>Atelier Git : Découvrez les bases.</p>
     >>>>>>> [commit distant]
     ```
   - Résolvez le conflit en choisissant la version correcte ou en combinant les deux :  
     ```html
     <p>Bienvenue à l'atelier Git et GitHub ! Découvrez les bases.</p>
     ```
   - Une fois le conflit résolu, ajoutez à nouveau le fichier :  
     ```bash
     git add index.html
     ```

4. Créer un commit de résolution :  
   ```bash
   git commit -m "Résolution du conflit sur index.html"
   ```

5. Envoyer à nouveau les modifications :  
   ```bash
   git push origin main
   ```

---

### 4. Validation de l’exercice :  
- Vérifiez que toutes les modifications sont visibles sur GitHub.
- Félicitez les participants pour avoir réussi à gérer un conflit !