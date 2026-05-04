# Printemps du Livre de Montaigu 2026 — Recherche Auteurs

Site de recherche pour aider les visiteurs à trouver leurs auteurs favoris au festival.
Basé sur le programme officiel du **29 avril 2026**.

> 🚧 **Prototype** réalisé par **Paul Albert / Inside Events** comme démo de fan experience.

## ✨ Fonctionnalités

- 🔎 **Recherche instantanée** par nom (insensible aux accents et à la casse)
- 🏷️ **Filtres** par type d'auteur (Généraliste / Jeunesse / BD)
- 📅 **Filtres** par jour de présence (Ven 8 / Sam 9 / Dim 10)
- 📍 **Filtres** par source (Libraires / Maisons d'édition)
- 🔢 Tri alphabétique ou par numéro de stand
- 📱 Responsive (mobile, tablette, desktop)
- ⌨️ Raccourci clavier : appuie sur `/` pour aller à la recherche

## 🚀 Hébergement sur GitHub Pages

1. Crée un repo public sur GitHub (ex: `printemps-livre-2026`)
2. Pousse les fichiers `index.html` et `auteurs.js` à la racine
3. Va dans **Settings → Pages**
4. Choisis la branche `main` et le dossier `/ (root)`
5. GitHub te donne une URL du type :
   `https://<ton-username>.github.io/<nom-du-repo>/`

C'est tout. Pas de build, pas de dépendances, tout est statique.

## ✏️ Modifier les données

Ouvre `auteurs.js` dans un éditeur de texte. Le format d'une entrée :

```javascript
{
  name: "Olivier ADAM",
  cat: "generaliste",        // "generaliste" | "jeunesse" | "bd"
  source: "libraire",         // "libraire" | "edition"
  stand: "D",                 // Lettre (libraire) ou numéro (édition)
  v: false,                   // Vendredi (true = présent / false = absent)
  s: true,                    // Samedi
  d: true,                    // Dimanche
  highlight: "Lauréat..."     // (optionnel) Mention spéciale en rose
}
```

Pour mettre à jour la présence d'un auteur, modifie simplement les booléens `v`, `s`, `d`.

## 🎨 Design

- Couleurs reprises du programme officiel : jaune `#FFE600`, rose `#EC008C`
- Typographies : **Bricolage Grotesque** (titres), **DM Sans** (corps), **Caveat** (touches manuscrites)
- Toutes les données sont chargées côté client — aucun appel serveur

## 🔄 Si le programme change

L'organisation peut envoyer un programme actualisé jusqu'au dernier moment. Dans ce cas :
1. Mets à jour `auteurs.js` avec les nouvelles données
2. Modifie aussi le bandeau orange dans `index.html` (cherche "29 avril 2026") si la date change
3. Push sur GitHub — la mise à jour est instantanée

## 📞 Contact

**Paul Albert** — Fondateur Inside Events
paulalbert214@gmail.com — 07.50.24.21.47
