# AR1G — Compo d'équipe

Petite application web statique (un seul fichier `index.html`, sans build ni backend) pour préparer la composition d'une équipe de volley :

- **Disponibilités** : marquer chaque joueur·euse *disponible* ou *absent·e*.
- **Rôles** : attribuer un rôle à chacun·e — Passeur·euse (Pa), Central·e (C), Réceptionneur·euse (R4), Pointu·e (Po), Libéro (L), ou Coach (Co).
- **Terrain / Banc** : répartir l'effectif entre le terrain et le banc.
- **Compo terrain validée** : 1 passeur·euse, 2 central·es, 2 R4, 1 pointu·e, 1 libéro (7 actif·ves), plus 1 ou 2 coachs. Un bandeau indique ce qui manque ou est en surnombre.
- **Composer auto** : remplit automatiquement le terrain à partir des rôles disponibles.

La sélection est mémorisée dans le navigateur (localStorage).

## Lancer en local

```powershell
python -m http.server 8778
# puis ouvrir http://localhost:8778/
```

## Déploiement

Hébergé via **GitHub Pages** (branche `main`, racine) — dépôt public, site public.

## Sécurité

- En-tête `Content-Security-Policy` restrictif (`default-src 'none'`), aucune ressource externe.
- `referrer` désactivé.
- Fichier `_headers` fourni pour les hébergeurs qui le supportent (Cloudflare Pages / Netlify). GitHub Pages ne l'applique pas.

Aucune donnée n'est envoyée à un serveur : tout reste dans le navigateur.
