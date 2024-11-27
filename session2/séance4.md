### **Séance 4 : Bonnes Pratiques et Exercice de Synthèse**  

#### **Objectifs pédagogiques :**  
- Appliquer les bonnes pratiques Git et GitHub pour un développement structuré.  
- Travailler sur un projet complet incluant l'utilisation des branches, la gestion des conflits, et les Pull Requests.  

---

### **Thèmes abordés :**

#### **1. Bonnes Pratiques Git (1h)**  

##### **1.1. Convention de messages de commit**  
Un bon message de commit doit être clair, précis et descriptif.  
- Format recommandé :  
  ```text
  Résumé du changement (50 caractères max)  

  Description détaillée (72 caractères max par ligne, optionnelle).  
  Expliquez pourquoi le changement a été effectué et ce qu'il implique.
  ```  
- Exemples :  
  - **Correct** :  
    ```text
    Ajout de la page d'accueil  

    Création d'une page d'accueil simple avec une barre de navigation.
    ```  
  - **Incorrect** :  
    ```text
    Update files  
    ```  

##### **1.2. Organisation des dépôts**  
1. **Fichiers essentiels à inclure** :  
   - **README.md** : Décrit le projet, son objectif, et comment le configurer.  
   - **LICENSE** : Définit les droits d’utilisation (facultatif).  
   - **CONTRIBUTING.md** : Fournit des instructions pour contribuer au projet (optionnel).  

2. **Utilisation de `.gitignore`** :  
   - Ajoutez un fichier `.gitignore` pour exclure les fichiers non nécessaires du suivi Git (par ex. fichiers de configuration locaux, logs, etc.).  
   - Exemple d’un `.gitignore` typique :  
     ```text
     # Fichiers générés
     *.log
     *.tmp
     /node_modules
     /dist

     # Fichiers secrets
     .env
     ```

##### **1.3. Gestion des branches**  
- **Stratégie de branches** :  
  - **main** : Branche stable contenant le code prêt pour la production.  
  - **feature/nom_fonctionnalité** : Branche pour développer une nouvelle fonctionnalité.  
  - **hotfix/nom_correction** : Branche pour corriger rapidement un bug en production.  

---

#### **2. Exercice de Synthèse (1h30)**  

**Objectif :** Mettre en œuvre toutes les notions apprises dans un projet fictif.  

##### **Scénario : Création d’un site web collaboratif**  
1. **Mise en place du projet :**  
   - Créez un nouveau dépôt GitHub nommé `site_collaboratif`.  
   - Ajoutez les fichiers essentiels (`README.md`, `.gitignore`).  

2. **Création de branches :**  
   - Un membre de l’équipe configure la branche principale (`main`).  
   - Chaque participant crée une branche dédiée pour une fonctionnalité spécifique :  
     - `feature/header` : Développement de l’en-tête du site.  
     - `feature/footer` : Développement du pied de page.  
     - `feature/content` : Ajout du contenu principal.  

3. **Développement :**  
   - Chaque membre développe sa fonctionnalité sur sa branche respective.  
   - Validez les modifications avec des messages de commit clairs.

4. **Fusion et gestion des conflits :**  
   - Les branches sont fusionnées dans la branche principale (`main`) via des Pull Requests.  
   - En cas de conflit :  
     - Identifiez le fichier en conflit.  
     - Résolvez le conflit directement dans le fichier (utilisez les marqueurs Git).  
     - Validez les modifications corrigées :  
       ```bash
       git add fichier_conflit
       git commit -m "Résolution des conflits sur fichier_conflit"
       ```  

5. **Finalisation :**  
   - Une fois toutes les fonctionnalités fusionnées, assurez-vous que le projet est prêt pour une mise en production (vérification collective du dépôt).

---

### **Récapitulatif des Commandes Clés Utilisées dans cette Séance**  

| Commande              | Description                                   |  
|-----------------------|-----------------------------------------------|  
| `git commit -m`       | Ajoute un message clair pour un commit.      |  
| `git branch`          | Crée ou affiche les branches existantes.     |  
| `git checkout`        | Passe d'une branche à une autre.             |  
| `git merge`           | Fusionne une branche dans la branche actuelle. |  
| `git pull`            | Récupère les modifications du dépôt distant. |  
| `git add`             | Ajoute des fichiers au suivi ou après une résolution de conflit. |  

---

### **Conclusion de la Séance 4**  

Cette séance clôt le cycle de formation en consolidant toutes les notions abordées :  
- Utilisation efficace des branches.  
- Application des bonnes pratiques de collaboration.  
- Résolution de conflits et gestion de Pull Requests.  

Souhaitez-vous un complément sur une partie spécifique ou un tutoriel détaillé pour l'exercice pratique ? 😊