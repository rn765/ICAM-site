# ICAM Conciergerie — Site web

Site one-page pour ICAM Conciergerie, agence de gestion de locations courte durée à Bruxelles.

## Stack technique

- **[Astro 5+](https://astro.build)** — Framework statique, composants `.astro` uniquement
- **[Tailwind CSS v4](https://tailwindcss.com)** — Via `@tailwindcss/vite`, sans `tailwind.config.js`
- **Déploiement** — Cloudflare Pages (HTML statique)

## Commandes

| Commande | Description |
|---|---|
| `npm install` | Installe les dépendances |
| `npm run dev` | Lance le serveur de dev sur `http://localhost:4321` |
| `npm run build` | Build de production dans `./dist/` |
| `npm run preview` | Prévisualise le build de production |

## Structure du projet

```
src/
├── layouts/Layout.astro        # Layout principal (head, meta, scripts, WhatsApp float)
├── pages/index.astro           # Page unique
├── components/
│   ├── Nav.astro               # Navigation sticky + hamburger mobile
│   ├── Hero.astro              # Hero pleine hauteur avec CTA
│   ├── PourQui.astro           # 3 colonnes profil client
│   ├── Methode.astro           # Timeline 01→04
│   ├── PourquoiNous.astro      # 4 cards différenciants
│   ├── CadreLegal.astro        # Fond bleu nuit, 3 obligations légales
│   ├── Tarif.astro             # Grille pricing 4 cards (20%→30%)
│   ├── FAQ.astro               # Accordéon 10 questions (vanilla JS)
│   ├── CTAFinal.astro          # CTA final fond bleu nuit
│   ├── Footer.astro            # Pied de page 3 colonnes
│   └── WhatsAppFloat.astro     # Bouton flottant WhatsApp
└── styles/global.css           # Design system + animations

```

## Modifier le contenu

- **Tarifs** → array `tarifs` dans `src/components/Tarif.astro`
- **FAQ** → array `faqs` dans `src/components/FAQ.astro`
- **Méthode** → array `steps` dans `src/components/Methode.astro`
- **Coordonnées** → chercher `+32471596624` et `contact@icam-conciergerie.com`
- **Couleurs** → variables CSS dans `src/styles/global.css`
- **Meta Pixel** → chercher `META_PIXEL_PLACEHOLDER` dans `src/layouts/Layout.astro`

## Déploiement Cloudflare Pages

1. Push sur GitHub
2. Connecter sur [pages.cloudflare.com](https://pages.cloudflare.com/)
3. Build command : `npm run build`
4. Output directory : `dist`
5. Node version : 18+

---

© 2026 ICAM GROUP SRL — Tous droits réservés
