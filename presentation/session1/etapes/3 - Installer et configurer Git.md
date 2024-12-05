# 3 - Installer et configurer Git :

---

## Étape 1: Installer Git :

- Télécharger l’archive de Git sur le site officiel : [https://git-scm.com/download/win](https://git-scm.com/download/win)

- Extraire l’archive dans un dossier de votre choix.

## Étape 2: Vérifier que Git est installé :

```bash
git -v
```

## Étape 3: Configurer Git:

- Ouvrir le fichier `cmd`

- Exécuter la commande suivante :

  ```bash
  git config --global user.name "Votre nom"
  git config --global user.email "Votre adresse email"
  ```

## Étape 4: Vérifier la configuration :

```bash
git config --list
```
