Voici un scénario pratique pour apprendre à résoudre un conflit Git sans utiliser les branches. Ce scénario est adapté aux débutants et montre comment gérer un conflit sur le même fichier par un seul utilisateur.

---

### **Scénario pratique : Résolution d’un conflit dans Git**
**Contexte** :  
Un utilisateur modifie accidentellement deux fois un fichier avec des changements différents, sans effectuer un `git pull` entre les deux modifications.

---

#### **Étapes du scénario :**

1. **Création du projet et initialisation de Git :**  
   - Créer un répertoire :  
     ```bash
     mkdir atelier-conflit
     cd atelier-conflit
     ```
   - Initialiser Git :  
     ```bash
     git init
     ```
   - Créer un fichier :  
     ```bash
     echo "Ceci est la première version du fichier." > fichier.txt
     git add fichier.txt
     git commit -m "Ajout initial du fichier."
     ```

2. **Ajout d’un premier changement :**  
   - Modifier le fichier :  
     ```bash
     echo "Ligne ajoutée par erreur lors de la première modification." >> fichier.txt
     git add fichier.txt
     git commit -m "Ajout d'une ligne au fichier."
     ```

3. **Simuler un conflit (deuxième modification sans `git pull`) :**  
   - Modifier directement le fichier :  
     ```bash
     echo "Ligne différente ajoutée lors de la deuxième modification." >> fichier.txt
     ```
   - Tenter de committer :  
     ```bash
     git add fichier.txt
     git commit -m "Ajout d'une autre ligne différente."
     ```
   - Git va détecter une différence entre les deux versions.

4. **Tentative de fusion des modifications :**  
   - Git signale un conflit. Identifier le conflit avec :  
     ```bash
     git status
     ```

5. **Résolution du conflit :**  
   - Ouvrir le fichier concerné (`fichier.txt`) dans un éditeur de texte. Les parties conflictuelles sont entourées de :  
     ```
     <<<<<<< HEAD
     Ligne ajoutée par erreur lors de la première modification.
     =======
     Ligne différente ajoutée lors de la deuxième modification.
     >>>>>>> Commit message ou ID
     ```
   - Décider de quelle ligne garder ou fusionner les deux :
     ```
     Ligne ajoutée par erreur lors de la première modification.
     Ligne différente ajoutée lors de la deuxième modification.
     ```
   - Enregistrer les modifications et quitter l’éditeur.

6. **Finalisation :**  
   - Indiquer que le conflit est résolu :  
     ```bash
     git add fichier.txt
     ```
   - Confirmer avec un commit de fusion :  
     ```bash
     git commit -m "Résolution du conflit sur fichier.txt."
     ```

7. **Vérification :**  
   - Vérifier que tout est correct et propre avec :  
     ```bash
     git log
     git status
     ```

---

### **Résultat attendu :**
À la fin de ce scénario, l'utilisateur apprend :  
- À détecter un conflit.  
- À lire et interpréter les délimitations de conflit dans un fichier.  
- À résoudre un conflit manuellement et finaliser les modifications.  

Ce scénario simple met l'accent sur l'identification et la résolution directe, sans concepts complexes comme les branches.