### **Séance 3 : Gestion des Branches et Collaboration Avancée avec Git**  

#### **Objectifs pédagogiques :**  
- Comprendre et maîtriser l’utilisation des branches dans Git.  
- Apprendre à utiliser les Pull Requests pour la collaboration sur GitHub.  
- Mettre en pratique la gestion des branches et la révision collaborative du code.

---

### **Thèmes abordés :**

#### **1. Gestion des Branches (1h)**  

##### **1.1. Pourquoi utiliser des branches ?**  
Les branches sont essentielles pour le travail collaboratif et la gestion des différentes fonctionnalités d’un projet. Elles permettent de :  
- Développer des fonctionnalités ou des corrections sans perturber la branche principale (souvent `main` ou `master`).  
- Tester des modifications avant de les intégrer.  
- Collaborer sans conflits en isolant les travaux des autres membres de l’équipe.

##### **1.2. Créer une branche :**  
1. Pour créer une nouvelle branche, utilisez la commande `git branch` :  
   ```bash
   git branch ma-nouvelle-fonctionnalité
   ```  
2. Pour passer à cette branche, utilisez `git checkout` :  
   ```bash
   git checkout ma-nouvelle-fonctionnalité
   ```  
   Ou bien créez et passez à une branche en une seule commande :  
   ```bash
   git checkout -b ma-nouvelle-fonctionnalité
   ```  

##### **1.3. Travailler sur une branche :**  
Une fois sur la branche, vous pouvez ajouter, modifier et valider des fichiers de la même manière que sur la branche principale.  
1. Effectuez des changements (par exemple, dans un fichier `feature.md`) :  
   ```bash
   echo "Nouvelle fonctionnalité en développement" > feature.md
   git add feature.md
   git commit -m "Ajout de la nouvelle fonctionnalité"
   ```  

2. Pour voir les branches existantes :  
   ```bash
   git branch
   ```  

##### **1.4. Fusionner une branche avec la branche principale :**  
Une fois le travail terminé sur une branche, vous pouvez la fusionner avec la branche principale (`main` ou `master`).  
1. Passez à la branche principale :  
   ```bash
   git checkout main
   ```  
2. Fusionnez la branche de fonctionnalité dans `main` :  
   ```bash
   git merge ma-nouvelle-fonctionnalité
   ```  
   Si tout se passe bien, le travail sur `ma-nouvelle-fonctionnalité` sera fusionné dans `main`.

##### **1.5. Supprimer une branche :**  
Une fois la branche fusionnée, vous pouvez la supprimer localement :  
```bash
git branch -d ma-nouvelle-fonctionnalité
```

---

#### **2. Collaboration avec les Pull Requests (30 min)**  

##### **2.1. Introduction aux Pull Requests (PRs)**  
Les Pull Requests (PR) permettent de proposer des modifications à intégrer dans un dépôt partagé. Elles offrent un moyen formel de discuter des changements et de les réviser avant de les fusionner dans la branche principale.  

##### **2.2. Création d’une Pull Request :**  
1. **Pousser la branche de travail vers GitHub :**  
   Si vous avez créé une branche localement, vous devez la pousser vers GitHub :  
   ```bash
   git push origin ma-nouvelle-fonctionnalité
   ```  
2. **Créer la Pull Request (PR) sur GitHub :**  
   - Allez sur votre dépôt GitHub.
   - Cliquez sur "Compare & pull request" (Comparer et créer une Pull Request).
   - Ajoutez un titre et une description pour la PR.
   - Sélectionnez la branche cible (par exemple `main`) et la branche source (la branche que vous avez créée).
   - Cliquez sur "Create pull request" (Créer la Pull Request).

##### **2.3. Révision et fusion de la Pull Request :**  
1. Les autres membres de l’équipe (ou vous-même) peuvent maintenant réviser les changements proposés dans la PR.
2. Si tout est correct, cliquez sur **Merge pull request** pour fusionner les modifications dans la branche principale.  
3. Après avoir fusionné, vous pouvez supprimer la branche si elle n’est plus nécessaire.

---

#### **3. Exercice Pratique (1h)**  

**Objectif :** Pratiquer la gestion des branches et la collaboration avec les Pull Requests.  

1. **Création d’un projet GitHub partagé** :  
   Un membre de l’équipe crée un dépôt GitHub et invite les autres comme collaborateurs.  
2. **Création de branches et travail collaboratif** :  
   Chaque participant crée une branche pour une fonctionnalité ou une correction à apporter, effectue des modifications et les valide.  
3. **Poussée des modifications et création de Pull Requests** :  
   Chaque membre pousse sa branche sur GitHub et crée une Pull Request.  
4. **Révision et fusion des Pull Requests** :  
   L’équipe révisera les Pull Requests, discutera des changements, et les fusionnera dans la branche principale.

---

### **Récapitulatif : Commandes utilisées dans cette séance**  

| Commande            | Description                                 |  
|---------------------|---------------------------------------------|  
| `git branch`        | Liste ou crée une nouvelle branche.        |  
| `git checkout`      | Change de branche.                         |  
| `git merge`         | Fusionne une branche dans la branche actuelle. |  
| `git push origin`   | Pousse les modifications vers le dépôt distant. |  
| `git branch -d`     | Supprime une branche locale.               |  
| **GitHub**:         | **Créez une Pull Request sur la plateforme GitHub.** |  

---

### **Conclusion de la Séance 3**  
À la fin de cette séance, vous devriez être capable de créer et gérer des branches efficacement, ainsi que d’utiliser les Pull Requests pour collaborer sur des projets GitHub. Ces outils sont essentiels pour un développement logiciel organisé et collaboratif.

Souhaitez-vous un complément d’information ou un exemple détaillé sur un point particulier ? 😊