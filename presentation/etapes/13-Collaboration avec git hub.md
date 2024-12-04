Voici un scénario d'exercice Git et GitHub conçu pour des débutants, avec une attention particulière à l'utilisation des commandes de base (add, commit, push, pull, clone) et à la gestion des conflits. L'exercice guidera les participants dans la création d'un dépôt, la gestion des versions avec Git, et la résolution d'un conflit de fusion.

### **Scénario de l'atelier Git et GitHub :**

**Contexte de l'exercice :**
Les participants vont travailler sur un projet simple en équipe. Chaque participant aura sa propre copie du projet sur GitHub et devra collaborer en modifiant des fichiers et en utilisant les commandes Git pour gérer les versions. À la fin de l'exercice, un conflit de fusion sera introduit afin d'illustrer la manière de le résoudre.

### **Objectifs :**
- Apprendre à créer un dépôt Git local et distant.
- Apprendre à ajouter, committer, pousser et récupérer des modifications avec Git.
- Résoudre un conflit de fusion Git.

### **Étapes de l'exercice :**

#### **1. Créer un dépôt GitHub :**
1. Allez sur [GitHub](https://github.com).
2. Créez un nouveau dépôt appelé **"atelier-git"** (ou tout autre nom au choix).
3. Ne cochez pas l'option d'initialiser le dépôt avec un `README` (les participants le feront eux-mêmes).

#### **2. Cloner le dépôt sur leur machine :**
Les participants devront cloner le dépôt créé sur GitHub pour commencer à travailler localement.

```bash
git clone https://github.com/votre-utilisateur/atelier-git.git
cd atelier-git
```

#### **3. Ajouter un fichier de projet :**
Les participants ajoutent un fichier `index.html` à leur dépôt local. Le contenu peut être simple, comme un titre ou un paragraphe de texte.

```html
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bienvenue à l'atelier Git</title>
</head>
<body>
    <h1>Bienvenue à l'atelier Git</h1>
    <p>Un exercice pour apprendre les bases de Git et GitHub.</p>
</body>
</html>
```

#### **4. Ajouter et committer le fichier :**
Les participants devront ajouter ce fichier à l'index Git, faire un commit, et pousser leurs modifications vers GitHub.

```bash
git add index.html
git commit -m "Ajout du fichier index.html"
git push origin main
```

#### **5. Demander aux participants de modifier le fichier :**
Les participants vont maintenant travailler sur leur propre branche ou sur le fichier principal, par exemple, en ajoutant un nouveau paragraphe au fichier `index.html`. Ils feront cela à la fois sur leur machine locale et sur GitHub.

```html
<p>Cette partie a été modifiée par [Nom du participant].</p>
```

#### **6. Simulation de la modification par un autre participant (en ajoutant du texte différent) :**
Simuler la situation où un autre participant modifie le même fichier sur GitHub avec un contenu différent :

```html
<p>Cette partie a été modifiée par [Autre participant].</p>
```

Ils devront modifier leur version localement, mais avant de pousser, ils feront un `git pull` pour récupérer les modifications de l'autre.

```bash
git pull origin main
```

Cela entraînera un **conflit de fusion**, car le fichier `index.html` a été modifié à la fois localement et sur GitHub par deux participants différents.

#### **7. Résoudre un conflit de fusion :**
- Git signalera un conflit dans le fichier `index.html`.
- Ouvrir le fichier dans un éditeur pour voir les conflits. Le fichier sera modifié pour montrer des délimitations comme suit :

```html
<p>Cette partie a été modifiée par [Nom du participant].</p>
<<<<<<< HEAD
<p>Cette partie a été modifiée par [Autre participant].</p>
=======
<p>Cette partie a été modifiée par [Nom du participant].</p>
>>>>>>> [commit hash]
```

- Les participants devront choisir comment résoudre le conflit (par exemple, choisir une version, combiner les deux, ou créer une version différente).

```html
<p>Cette partie a été modifiée par [Nom du participant].</p>
<p>Cette partie a également été modifiée par [Autre participant].</p>
```

#### **8. Ajouter, committer et pousser la résolution de conflit :**
Une fois le conflit résolu, ils devront ajouter le fichier modifié, faire un commit de la résolution et pousser les modifications vers GitHub.

```bash
git add index.html
git commit -m "Résolution du conflit dans index.html"
git push origin main
```

#### **9. Vérification sur GitHub :**
Les participants devront vérifier que leurs modifications apparaissent correctement sur GitHub. Le fichier `index.html` doit maintenant refléter la résolution du conflit.

### **Résumé des commandes Git utilisées :**

- **`git clone`** : Cloner un dépôt distant sur la machine locale.
- **`git add`** : Ajouter des fichiers à l'index Git.
- **`git commit`** : Enregistrer les modifications dans l'historique de Git.
- **`git push`** : Pousser les commits locaux vers le dépôt distant.
- **`git pull`** : Récupérer les modifications depuis le dépôt distant.
- **`git status`** : Vérifier l'état actuel du dépôt.
- **`git merge`** : Fusionner deux branches Git (généralement automatiquement, mais peut créer des conflits).
- **Résolution de conflit** : Modifier manuellement les fichiers en conflit pour résoudre les différences entre les versions locales et distantes.

### **Points clés à enseigner :**
1. **Collaboration et versionnage** : Travailler en équipe avec Git et GitHub pour gérer les versions et suivre les changements.
2. **Conflits de fusion** : Apprendre à identifier et résoudre les conflits lorsque deux développeurs modifient le même fichier.
3. **Bonnes pratiques** : Toujours faire un `git pull` avant de pousser pour éviter les conflits.

### **Conclusion :**
Cet atelier permettra aux participants d'apprendre les bases de Git et GitHub dans un environnement collaboratif et de se familiariser avec la résolution des conflits, une compétence essentielle pour tout développeur utilisant Git dans un cadre d'équipe.