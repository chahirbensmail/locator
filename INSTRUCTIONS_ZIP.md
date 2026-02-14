# Instructions après upload sur GitHub

## ✅ Vérification du nom du fichier .zip

Le code recherche le fichier : `orthodontiste-data.js.zip`

Si vous avez nommé votre fichier différemment (par exemple `orthodontiste-data.zip`), vous devez :

1. Soit **renommer le fichier** sur GitHub :
   - Cliquez sur le fichier .zip dans votre repository
   - Cliquez sur l'icône crayon (Edit)
   - Renommez-le en `orthodontiste-data.js.zip`
   - Commitez le changement

2. Soit **modifier index.html** ligne 267 :
   ```javascript
   const response = await fetch('VOTRE-NOM-DE-FICHIER.zip');
   ```

## 📝 Structure du fichier .zip

Le .zip DOIT contenir directement le fichier `orthodontiste-data.js` (pas dans un sous-dossier).

Pour vérifier :
- Décompressez votre .zip localement
- Vous devez voir directement `orthodontiste-data.js` (pas `dossier/orthodontiste-data.js`)

Si le fichier est dans un sous-dossier, recréez le .zip correctement :
1. Clic droit sur `orthodontiste-data.js` uniquement
2. Compresser → Créer une archive
3. Nommez-la `orthodontiste-data.js.zip`

## 🔍 Débogage

Si la page ne charge pas :
1. Ouvrez la console du navigateur (F12)
2. Regardez les erreurs
3. Vérifiez que le fichier .zip est bien téléchargé (onglet Network)

## 🎉 Test final

Une fois déployé, votre application sera accessible à :
```
https://votre-username.github.io/votre-repo-name/
```

Le premier chargement prendra 10-30 secondes (téléchargement du fichier de 44 MB).
