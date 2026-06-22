# Site IFCAR Solutions

Site vitrine corporate (HTML / CSS / JavaScript — sans framework, sans build).
Cabinet de conseil RH : **Recrutement · Formation · Conseil · Accompagnement**.

## Structure

```
ifcar_site/
├── index.html            Accueil
├── a-propos.html         À propos de nous
├── recrutement.html      Recrutement (privé / public / ONG · IFCARJOB)
├── formation.html        Formation (ingénierie · catalogues · sessions · IFCARFORMATION)
├── conseil.html          Conseil
├── accompagnement.html   Accompagnement individuel
├── contact.html          Contact (formulaire + carte)
├── 404.html
├── assets/
│   ├── css/style.css     Design system complet
│   ├── js/main.js        Navigation, accordéons, animations, formulaires
│   └── img/              Logo, favicons et photos optimisées (web)
├── robots.txt · sitemap.xml · site.webmanifest
```

## Charte graphique

| Couleur | HEX | Usage |
|---------|-----|-------|
| Vert | `#95ce0a` | accents, CTA principaux |
| Bleu | `#0081bf` | couleur institutionnelle |
| Navy  | `#0b2233` | sections sombres, footer |
| Gris clair | `#f5f8fb` | sections alternées |

Typographies : **Plus Jakarta Sans** (titres) + **Inter** (texte), via Google Fonts.

## Mise en ligne

Site 100 % statique : déposez le dossier sur n'importe quel hébergement
(O2switch, OVH, Netlify, Vercel, GitHub Pages…). Aucune compilation nécessaire.

## À personnaliser avant la production

Ces valeurs sont des **placeholders** à remplacer :

- **Téléphone / Fax** : `+212 5 22 00 00 00` (présent dans le header de chaque page et le footer)
- **Email** : `contact@ifcarsolutions.com`
- **Adresse** et **ICE** (`00000000000000`) — page `contact.html`
- **Carte Google Maps** — `contact.html` : remplacer la `src` de l'`<iframe>` par l'adresse exacte
- **Réseaux sociaux** — liens `href="#"` dans le footer (LinkedIn, Facebook, Instagram, YouTube)
- **Chiffres clés** (accueil) — `data-count` à ajuster aux valeurs réelles
- **Logos / témoignages / références** clients — remplacer les libellés génériques par les vrais
- **Fiche / brochures à télécharger** — boutons « Télécharger notre fiche » (`href="#"`)

## Formulaires (CRM / Leads)

Les formulaires affichent une confirmation côté client (démo). Pour alimenter
automatiquement une base prospects, connectez l'envoi à un backend ou à un
service comme **Formspree**, **Web3Forms** ou un webhook CRM :

1. Dans `index.html` et `contact.html`, retirer l'attribut `data-demo` du `<form>`.
2. Ajouter `action="https://formspree.io/f/VOTRE_ID"` et `method="POST"`.

Le handler de démonstration se trouve dans `assets/js/main.js` (`form[data-demo]`).

## Évolutions prévues (Phase 2)

Paiement en ligne, catalogue dynamique de formations, e-learning, extranet
clients, espace formateurs, tableau de bord commercial.
