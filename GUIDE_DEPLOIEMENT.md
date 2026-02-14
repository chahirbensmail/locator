# Guide de Déploiement sur GitHub Pages

## 📋 Fichiers à déployer

Vous aurez besoin de ces 3 fichiers :
1. `index.html` (l'application principale)
2. `orthodontiste-data.js` (les données - 44 MB)
3. `README.md` (documentation)

---

## 🚀 Méthode 1 : Interface Web GitHub (RECOMMANDÉ - plus simple)

### Étape 1 : Créer un compte GitHub
1. Allez sur https://github.com
2. Cliquez sur "Sign up"
3. Créez votre compte gratuit

### Étape 2 : Créer un nouveau repository
1. Une fois connecté, cliquez sur le bouton vert "New" (en haut à gauche)
2. Remplissez :
   - **Repository name** : `orthodontiste-locator` (ou un autre nom)
   - **Description** : "Outil d'aide à la décision pour cabinets orthodontistes"
   - Sélectionnez **Public**
   - ✅ Cochez "Add a README file"
3. Cliquez sur "Create repository"

### Étape 3 : Uploader les fichiers

⚠️ **ATTENTION** : Le fichier `orthodontiste-data.js` fait 44 MB. GitHub a une limite de 25 MB par fichier via l'interface web.

**Solution pour le gros fichier :**

#### Option A : Compresser le fichier (RECOMMANDÉ)
1. Sur votre ordinateur, faites un clic droit sur `orthodontiste-data.js`
2. Choisissez "Compresser" ou "Envoyer vers → Dossier compressé"
3. Vous obtenez `orthodontiste-data.js.zip` (environ 5-10 MB)
4. Dans GitHub, cliquez sur "Add file" → "Upload files"
5. Uploadez `index.html`, `README.md` et `orthodontiste-data.js.zip`
6. ⚠️ Modifiez `index.html` ligne ~267 pour décompresser au chargement

#### Option B : Utiliser GitHub CLI (pour fichiers > 25 MB)
Voir Méthode 2 ci-dessous.

### Étape 4 : Activer GitHub Pages
1. Dans votre repository, cliquez sur "Settings" (en haut)
2. Dans le menu de gauche, cliquez sur "Pages"
3. Sous "Source", sélectionnez :
   - Branch : `main`
   - Folder : `/ (root)`
4. Cliquez sur "Save"
5. Attendez 1-2 minutes

### Étape 5 : Accéder à votre site
Votre site sera disponible à :
```
https://votre-username.github.io/orthodontiste-locator/
```

---

## 💻 Méthode 2 : Ligne de commande Git (pour fichiers > 25 MB)

### Prérequis
- Installer Git : https://git-scm.com/downloads
- Installer Git LFS : https://git-lfs.github.com/

### Étapes

1. **Créer le repository sur GitHub** (comme Méthode 1, Étape 2)

2. **Sur votre ordinateur, ouvrir un terminal** dans le dossier contenant les fichiers :

```bash
# Initialiser Git
git init
git add .gitattributes

# Configurer Git LFS pour les gros fichiers
git lfs install
git lfs track "orthodontiste-data.js"

# Ajouter tous les fichiers
git add .
git commit -m "Initial commit"

# Lier au repository GitHub (remplacez VOTRE-USERNAME et VOTRE-REPO)
git remote add origin https://github.com/VOTRE-USERNAME/VOTRE-REPO.git
git branch -M main

# Pousser vers GitHub
git push -u origin main
```

3. **Activer GitHub Pages** (comme Méthode 1, Étape 4)

---

## ⚠️ Limites de GitHub

- Maximum 100 MB par fichier avec Git LFS
- 1 GB d'espace de stockage gratuit
- Bande passante limitée (100 GB/mois gratuit)

---

## 🔧 Alternative : Hébergement du fichier de données ailleurs

Si le fichier est trop gros pour GitHub, vous pouvez :

1. **Héberger le JS sur Cloudflare R2 / AWS S3** (gratuit jusqu'à 10 GB)
2. **Modifier index.html** pour charger depuis l'URL externe :
   ```html
   <script src="https://votre-storage.com/orthodontiste-data.js"></script>
   ```

---

## 📞 Besoin d'aide ?

Si vous rencontrez des problèmes :
1. Vérifiez que tous les fichiers sont bien uploadés
2. Attendez 2-3 minutes après activation de Pages
3. Videz le cache de votre navigateur (Ctrl+F5)
4. Vérifiez l'onglet "Actions" sur GitHub pour voir les erreurs

---

## 🎉 Partager votre application

Une fois déployée, partagez simplement l'URL :
```
https://votre-username.github.io/orthodontiste-locator/
```

Les personnes qui visitent cette URL pourront utiliser l'application directement dans leur navigateur !
