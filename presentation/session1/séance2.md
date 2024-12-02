
---

### **Diapositive 1 : Titre de la présentation**

**Titre :**
**Session 2 : Collaboration avec GitHub**

**Description :**

- Comprendre l’interaction entre un dépôt local et distant.
- Découvrir les outils pour collaborer efficacement.
- Apprendre à résoudre les conflits.

**Visuel :**

- Icône GitHub (logo)
- Illustration montrant un dépôt local et un dépôt distant connectés.

---

### **Diapositive 2 : Création d’un dépôt GitHub**

**Titre :**
**1. Création d’un Dépôt sur GitHub**

**Étapes clés :**

1. Connectez-vous à GitHub et cliquez sur **New Repository**.
2. Remplissez les détails : nom, options (privé/public), initialisation avec `README.md` (facultatif).
3. Cliquez sur **Create Repository**.

**Visuel :**

- Capture d’écran d’un formulaire GitHub avec les zones importantes mises en surbrillance.

---

### **Diapositive 3 : Liaison d’un projet local à GitHub**

**Titre :**
**2. Connecter un Projet Local à GitHub**

**Commandes clés :**

1. **Ajoutez un dépôt distant** :
   ```bash
   git remote add origin <URL_DU_DEPOT>
   ```
2. **Poussez le projet vers GitHub** :
   ```bash
   git push -u origin main
   ```

**Astuce :** Configurez une clé SSH pour simplifier la connexion.

**Visuel :**

- Illustration montrant un terminal avec les commandes.
- Icône de connexion représentant le lien local-distant.

---

### **Diapositive 4 : Gestion des modifications**

**Titre :**
**3. Synchronisation des Modifications**

**Commandes utiles :**

- **Récupérer les mises à jour du dépôt distant** :
  ```bash
  git pull origin main
  ```
- **Pousser vos modifications locales vers GitHub** :
  ```bash
  git push origin main
  ```

**Concepts :**

- Toujours synchroniser avant de travailler.
- Gérer les conflits pour intégrer les modifications.

**Visuel :**

- Schéma : deux flèches illustrant le flux "push/pull" entre un dépôt local et distant.

---

### **Diapositive 5 : Résolution des conflits**

**Titre :**
**4. Résolution des Conflits**

**Étapes clés :**

1. Identifiez les conflits :
   ```bash
   git pull origin main
   ```
   Git vous alerte des conflits.
2. Ouvrez le fichier concerné pour examiner les marqueurs de conflit :
   ```
   <<<<<<< HEAD
   Votre modification locale
   =======
   Modification distante
   >>>>>>> origin/main
   ```
3. Modifiez, sauvegardez, puis validez :
   ```bash
   git add fichier
   git commit -m "Résolution des conflits"
   ```

**Visuel :**

- Capture d’un fichier avec des marqueurs de conflit.
- Icône "warning" pour indiquer un conflit.

---

### **Diapositive 6 : Clés SSH pour GitHub**

**Titre :**
**5. Configuration des Clés SSH**

**Étapes :**

1. Générez une clé SSH :
   ```bash
   ssh-keygen -t rsa -b 4096 -C "votre.email@example.com"
   ```
2. Ajoutez la clé publique à GitHub :
   - Copiez la clé avec :
     ```bash
     cat ~/.ssh/id_rsa.pub
     ```
   - Collez-la dans **GitHub > Settings > SSH and GPG keys**.

**Avantage :** Plus besoin de saisir vos identifiants à chaque `push` ou `pull`.

**Visuel :**

- Icône clé pour représenter la sécurité.
- Capture de l’interface GitHub pour ajouter une clé SSH.

---

### **Diapositive 7 : Exercice Pratique**

**Titre :**
**6. Exercice Pratique : Collaboration avec GitHub**

**Objectif :** Collaborer en équipe sur un projet partagé et résoudre des conflits.

**Étapes :**

1. Cloner un dépôt partagé :
   ```bash
   git clone <URL_DU_DEPOT>
   ```
2. Modifier un fichier, ajouter et pousser les modifications.
3. Résoudre un conflit en cas de `git pull` avec des modifications incompatibles.

**Visuel :**

- Illustration d’une collaboration en équipe (personnes travaillant sur un même projet).
- Icône représentant un conflit avec une solution.

---

### **Diapositive 8 : Résumé**

**Titre :**
**Résumé de la Séance 2**

**Commandes importantes :**

- `git remote add`, `git push`, `git pull` : synchronisation.
- Résolution de conflits : marqueurs `<<<<<<<` et `>>>>>>>`.
- Utilisation de clés SSH pour simplifier les interactions.

**Prochaines étapes :**

- Gérer les branches et apprendre les Pull Requests.

**Visuel :**

- Icône GitHub avec des flèches représentant le flux de collaboration.

---

Souhaitez-vous les diapositives sous un format particulier ou des précisions sur une section ? 😊
