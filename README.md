# 🦷 Localisateur de Cabinet Orthodontiste

Outil d'aide à la décision pour identifier les meilleurs emplacements géographiques pour un cabinet d'orthodontie en Île-de-France.

## 🎯 Fonctionnalités

- **Visualisation interactive** : Carte avec zones IRIS colorées selon différents indicateurs
- **Analyse par rayon** : Sélectionnez un point et analysez les statistiques dans un rayon défini
- **Recherche d'emplacement optimal** : Algorithme intelligent pour trouver le meilleur emplacement
- **Filtrage avancé** : Par département et commune
- **Calcul de score** : Basé sur population enfants/ados, revenus, écoles et concurrence

## 📊 Données

L'application utilise des données socio-démographiques et géographiques sur :
- 5 260 zones IRIS en Île-de-France
- 222 cabinets orthodontistes existants
- 1 234 gares de transport
- Données INSEE sur revenus, population, éducation

## 🚀 Utilisation

1. Sélectionnez les départements et communes à analyser
2. Choisissez le rayon d'analyse (1-10 km)
3. Lancez la recherche pour trouver l'emplacement optimal
4. Explorez les résultats sur la carte interactive

## 🔧 Technique

- Frontend pur (HTML/CSS/JavaScript)
- Leaflet.js pour la cartographie
- Données intégrées (pas de serveur requis)
- Déploiement via GitHub Pages

## 📝 Score de localisation

Le score est calculé selon :
- 50% Population enfants/ados (6-17 ans)
- 30% Revenu médian de la zone
- 15% Nombre d'établissements scolaires
- 5% Population totale
- Pénalité selon la concurrence locale

---

**Développé pour l'aide à la décision d'implantation de cabinets dentaires**
