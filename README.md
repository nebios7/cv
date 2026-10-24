# 📄 Générateur de CV + lettre de motivation

Application web **100 % locale** pour créer un CV et une lettre de motivation, avec aperçu en direct et export PDF. Un seul fichier HTML, sans framework, sans serveur, sans compte.

**Démo :** https://nebios7.github.io/cv/ *(après activation de GitHub Pages, voir plus bas)*

## ✨ Fonctionnalités

### CV
- Identité, titre, contacts, profil, photo (zoom et position réglables)
- Compétences, langues, centres d'intérêt
- Sections : expériences, projets, contributions, formations, certifications, ressources, liens (GitHub, LinkedIn…)
- 4 palettes de couleurs, 3 densités (compact, normal, aéré)
- Choix des sections à afficher

### Lettre de motivation
- Destinataire, poste visé, objet, date automatique
- 3 types : réponse à une annonce, candidature spontanée, stage / alternance
- 3 tons : formel, dynamique, sobre
- Génération automatique à partir des données du CV, puis texte modifiable

### Export
- **Imprimer** (mise en page A4 prête à l'impression)
- **Télécharger PDF**
- **Sauvegarder / Charger** ses données en `.json`

## 🚀 Utilisation

### En local
1. Télécharger `index.html`
2. Double-cliquer dessus : il s'ouvre dans le navigateur

### En ligne (GitHub Pages)
1. Nommer le fichier **`index.html`** à la racine du dépôt
2. Aller dans **Settings → Pages**
3. *Source* : `Deploy from a branch` → branche `main` → dossier `/ (root)` → **Save**
4. Après environ une minute, le site est disponible sur `https://nebios7.github.io/cv/`

## 🔒 Données et confidentialité

- Tout fonctionne dans le navigateur : **aucune donnée n'est envoyée à un serveur**.
- Les informations sont conservées dans le `localStorage` du navigateur et peuvent être exportées en `.json`.
- La lettre est générée par des modèles de phrases (pas d'IA) : relire et adapter avant envoi.

## 🧱 Technique

| Élément | Détail |
|---|---|
| Structure | HTML, CSS, JavaScript natif dans un seul fichier |
| Style | Inspiré de [gitingest.com](https://gitingest.com) (bordures noires, ombres décalées) |
| PDF | [html2pdf.js](https://github.com/eKoopmans/html2pdf.js) chargé depuis cdnjs |
| Stockage | `localStorage` + export / import JSON |

> Sans connexion Internet, l'application fonctionne ; seul le bouton « Télécharger PDF » nécessite la bibliothèque externe. Le bouton « Imprimer » (puis « Enregistrer au format PDF ») reste utilisable hors ligne.

## 📁 Structure du dépôt

```
cv/
├── index.html   # l'application complète
└── README.md
```

## 🛠️ Personnalisation

- **Couleurs** : variables CSS `--peach`, `--orange`, `--green`, `--blue` au début du `<style>`, ou objet `PAL` dans le JavaScript.
- **Phrases de la lettre** : fonction `genBody()` dans le JavaScript.
- **Sections du CV** : objet `LISTS` et fonction `drawCv()`.

## 📜 Licence

À définir par l'auteur (ex. MIT).

---

Fait avec ❤️ par [@nebios7](https://github.com/nebios7)
