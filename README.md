# EKO Mini — Note technique

Site statique — un seul fichier `index.html`, sans build. Langues FR / EN / NL / ES et thème clair / sombre intégrés ; bouton **⎙ PDF** pour imprimer la page courante en PDF (Ctrl/Cmd + P fonctionne aussi).

## Mise en ligne (une fois)

1. **GitHub** — créer un dépôt privé `eko-mini-techdoc` (github.com → New repository, sans README).
2. Depuis ce dossier :
   ```
   git remote add origin git@github.com:<organisation>/eko-mini-techdoc.git
   git push -u origin main
   ```
3. **Vercel** — vercel.com → Add New… → Project → Import `eko-mini-techdoc` → Framework preset : *Other* → Deploy. Aucune commande de build, aucun répertoire de sortie.
4. Le site est en ligne sur `eko-mini-techdoc.vercel.app`. Domaine personnalisé : Settings → Domains.

## Mise à jour

Modifier `index.html` (ou déposer un nouveau PDF dans `pdf/`), puis :
```
git add -A && git commit -m "…" && git push
```
Vercel redéploie automatiquement à chaque push sur `main`. Chaque déploiement garde son URL propre : l'historique des versions est dans Vercel → Deployments.

## Paramètres d'URL

`?lang=en` `?lang=nl` `?lang=es` `?theme=dark` — utiles pour un lien direct dans un e-mail.
