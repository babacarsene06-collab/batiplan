# BatiPlan — Générateur de devis

Application web **hors ligne** pour créer et gérer des devis d’architecture / plans (2D–3D), adaptée au contexte sénégalais (FCFA, Wave, Orange Money).

## Fichiers

| Fichier | Rôle |
|---------|------|
| `index.html` | Application complète (interface + logique) |
| `manifest.webmanifest` | Installation type « application » sur mobile |
| `sw.js` | Service worker (cache hors ligne) |
| `README.md` | Ce fichier |

## Hébergement sur GitHub Pages

1. Crée un dépôt GitHub (ex. `batiplan`).
2. Envoie ces fichiers à la **racine** du dépôt (branche `main`).
3. Dans le dépôt : **Settings → Pages → Source** : branche `main`, dossier `/ (root)`.
4. L’URL sera du type :  
   `https://TON_COMPTE.github.io/batiplan/`

### En ligne de commande

```bash
git init
git add index.html manifest.webmanifest sw.js README.md
git commit -m "BatiPlan — générateur de devis"
git branch -M main
git remote add origin https://github.com/TON_COMPTE/batiplan.git
git push -u origin main
```

Puis active GitHub Pages comme indiqué ci-dessus.

## Utilisation locale

Ouvre simplement `index.html` dans **Chrome** ou **Edge** (double-clic).  
Le service worker ne s’active qu’en `http://` ou `https://` (donc sur GitHub Pages ou un petit serveur local).

Serveur local rapide :

```bash
npx serve .
# ou
python3 -m http.server 8080
```

## Données

Tout est stocké dans le **navigateur** (localStorage) : devis, clients, signature, modèles.  
Pense à **Exporter mes données** régulièrement (menu) pour une sauvegarde fichier.

## Fonctionnalités principales

- Devis multi-lignes, unités, calculateur tarifaire  
- Multi-devis (onglets), variantes, avenants  
- PDF / impression, WhatsApp, e-mail  
- Relances, historique par devis  
- Wave / Orange Money sur le document  
- Signature pro + acceptation client  
- Carnet clients, modèles de prestations  

---

Prototype de travail — vérifie prix, mentions légales et obligations fiscales avant envoi au client.
