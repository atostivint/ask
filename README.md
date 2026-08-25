# ask.alexandre.tostivint.bzh

Page portfolio d'Alexandre Tostivint, architecte cloud senior.
Concept : une page façon « fiche produit de modèle IA » où les visiteurs
peuvent poser leurs questions techniques en direct via le chat Crisp.

**En ligne sur** : https://ask.alexandre.tostivint.bzh

## Contenu du dépôt

| Fichier | Rôle |
|---|---|
| `index.html` | La page complète : HTML + CSS + JS, zéro framework, zéro tracker |
| `CNAME` | Domaine custom GitHub Pages (`ask.alexandre.tostivint.bzh`) |

Le widget de chat est fourni par [Crisp](https://crisp.chat) (plan gratuit).
L'identifiant du widget (`CRISP_WEBSITE_ID`) est dans `index.html`.

## Déploiement

Statique : tout push sur `main` est servi directement par GitHub Pages.
Aucun build, aucun workflow CI.

DNS géré par Terraform dans le dépôt homelab (`stacks/cloud/dns_tostivint_bzh.tf`,
Cloudflare, enregistrement CNAME vers `atostivint.github.io`, non proxifié
pour laisser GitHub gérer le certificat TLS).
