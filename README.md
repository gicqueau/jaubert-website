# Cabinet Jaubert — Site marketing (STAGING)

Site vitrine pour le cabinet de **Me Didier Jaubert**, avocat au Barreau de Paris, dédié à la
**réparation du préjudice corporel** et au **droit de la santé**. 100 % en français.

> **STAGING / DÉMONSTRATION.** Toutes les pages portent `noindex,nofollow`. Plusieurs valeurs
> sont des **placeholders** à remplacer avant toute mise en production (voir checklist plus bas).
> Le contenu doit en outre être **soumis à l'Ordre des avocats de Paris** avant publication.

## Contenu

| Fichier | Rôle |
|---|---|
| `index.html` | Page d'accueil — 15 sections (hero, situations, différenciateurs, bio, bandeau Mediator, processus, prise en charge, Dintilhac, domaines, exemples, actualités, témoignages, formulaire, footer). |
| `mentions-legales.html` | Mentions légales (LCEN) — éditeur, hébergeur, profession. |
| `politique-confidentialite.html` | RGPD — finalités, base légale, durées, droits, cookies, secret professionnel. |
| `styles.css` | Design system bleu + vert, responsive, accessibilité RGAA/WCAG AA. |
| `CNAME` | Domaine GitHub Pages : `jaubert-website.ushaia.com`. |

## Design system

- Palette : Bleu Conseil `#1B3A5B`, Bleu Confiance `#2E6CA4`, Vert Apaisé `#3A8E7C`,
  Vert AA `#2F7567`, Vert Clair `#E8F2EE`, Ardoise `#21303A`, Gris `#5C6B73`, Brume `#F5F7F8`.
- Typographie : titres serif **Cormorant Garamond**, corps sans **Inter** (min 18px).
- Accessibilité : HTML5 sémantique, skip-link, focus visible 3px, navigation clavier,
  cibles ≥44px, `prefers-reduced-motion`, responsive sans scroll horizontal à 360px.

## Déploiement (GitHub Pages)

1. Créer un dépôt GitHub et y pousser le contenu de ce dossier (branche `master` ou `main`).
2. Repo **Settings → Pages** → Source : la branche, dossier `/ (root)`.
3. Le fichier `CNAME` configure le domaine personnalisé `jaubert-website.ushaia.com` :
   ajouter chez le DNS d'`ushaia.com` un enregistrement **CNAME** `jaubert-website` →
   `<utilisateur>.github.io`.
4. Activer **Enforce HTTPS** une fois le certificat émis.

Test local : ouvrir `index.html` dans un navigateur, ou
`python3 -m http.server` puis http://localhost:8000.

## ⚠️ PLACEHOLDERS À REMPLACER AVANT PRODUCTION

- [ ] **Numéro de téléphone** — partout `01 XX XX XX XX` / `tel:+3300000000000`
      (barre utilitaire, nav, bloc contact, footer).
- [ ] **Email du cabinet** — `contact@example-jaubert.fr` (bloc contact + footer) et
      adresses DPO/contact dans les pages légales.
- [ ] **Action du formulaire** — `index.html` pointe vers
      `https://formspree.io/f/REMPLACER_PAR_VOTRE_ID`. GitHub Pages n'a **pas de backend** :
      brancher un service (Formspree, Basin, etc.) ou une fonction serverless.
- [ ] **Portrait de Me Jaubert** — placeholders monogramme « DJ » (hero + bio) à remplacer
      par une photographie réelle (prévoir l'attribut `alt`).
- [ ] **Mentions légales** — SIREN/SIRET, TVA, téléphone, email (`À COMPLÉTER`).
- [ ] **Politique de confidentialité** — email/DPO, sous-traitant du formulaire, date de mise à
      jour, réévaluation cookies si analytics ajouté.
- [ ] **Chiffre Mediator (478)** — vérifier via l'article primaire France Inter avant prod.
- [ ] **Mot « spécialiste »** — NON utilisé (formulation « dédié à / intervient en »). À activer
      uniquement si le **certificat de spécialisation CNB** est confirmé.
- [ ] **Articles « Actualités »** — 3 cartes placeholder à remplacer par de vrais articles.
- [ ] **Témoignages** — exemples anonymisés ; à remplacer par des témoignages réels (initiales
      uniquement, avec accord écrit). Jamais de nom complet.
- [ ] **`noindex,nofollow`** — à retirer des pages lors du passage en production.
- [ ] **Validation Ordre des avocats de Paris** du contenu avant mise en ligne.

## Garde-fous de conformité (CNB / RIN)

Termes **interdits** et absents du site : *meilleur, n°1, leader, excellence, spécialiste/
spécialisé* (sauf certificat), toute *garantie de résultat*, « a gagné le procès Mediator »,
témoignages nominatifs, « consultation gratuite » tapageuse, « jamais les assureurs ».
Formulation retenue : **« du côté des victimes / à vos côtés »** ; **« premier échange / sans
engagement »**. Les exemples de dossiers portent la mention
« Chaque dossier est unique. Ces exemples ne constituent pas une garantie de résultat. »

---

Réalisé par [USHAIA](https://ushaia.com).
