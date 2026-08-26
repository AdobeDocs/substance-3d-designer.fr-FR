---
source-git-commit: ec58342925d3e608b0180b67a1e20ffaeb1f306a
workflow-type: tm+mt
source-wordcount: '527'
ht-degree: 0%

---
# CLAUDE.md

Ce fichier fournit des conseils à Claude Code (claude.ai/code) lors de l’utilisation du code dans ce référentiel.

&#x200B;# Documentation Substance 3D Designer

Ce référentiel contient la documentation de Substance 3D Designer. Il n&#39;y a pas de code d&#39;application, d&#39;étape de génération ou de suite de tests : le référentiel *est* le contenu, écrit dans Markdown et publié sur [Adobe Experience League](https://experienceleague.adobe.com/docs/substance3d-designer.html?lang=en).

&#x200B;# Structure du référentiel

* `help/` — tout le contenu de la documentation, organisé pour refléter la table des matières.
* `help/guide/TOC.md` — table des matières. Chaque entrée est un lien relatif (ancré à `/help/...`) vers le fichier Markdown d&#39;une page. `TOC.md` contient également des métadonnées d&#39;arborescence de page (`user-guide-title`, `breadcrumb-title`, `nudge`, des ancrages de section comme `{#section-id}`).
* `help/assets/` — images partagées et non spécifiques à une page (par exemple, icônes d&#39;application réutilisées sur plusieurs pages).
* `help/glossary/glossary.md` : une seule grande page de glossaire, organisée par ordre alphabétique avec des plages d&#39;ancrage (`<span id="term"></span>`) utilisées pour la réticulation via des fragments `#term`.
* `metadata.md` — page de garde au niveau du référentiel (ID de cloud/solution/produit, `git-repo`, etc.) qui est hérité par tous les `TOC.md`. Ne modifiez cette option que pour les modifications de métadonnées à l’échelle du référentiel ; les métadonnées spécifiques à la page appartiennent à la page de garde.
* `redirects.csv`, `linkcheckexclude.json`, `markdownlint_custom.json`, `pipeline.opts` — configuration du pipeline de publication (redirections, exceptions de vérification de lien, remplacements de règles de liaison, options de pipeline).
* `fix-image-names.py` — Utilitaire unique qui renomme les images `help/assets` avec des suffixes entre parenthèses (par exemple `foo(1).png` → `foo_1.png`) et réécrit chaque référence Markdown pour qu&#39;elle corresponde. Ne fait partie d’aucun workflow normal ; à exécuter manuellement uniquement lorsque ces noms de fichiers réapparaissent.

## Convention de dossier/table des matières

Pour chaque entrée dans `help/guide/TOC.md` :
* Il existe un dossier correspondant sous `help/`, suivant la même imbrication que la table des matières.
* Ce dossier contient un fichier Markdown, nommé version kebab-case du titre de la page.
* Si la page contient des médias sur mesure (images, GIFs, vidéos), elle se trouve dans un sous-dossier frère nommé `<md-file-name>.resources`.

Lors de l&#39;ajout ou du déplacement d&#39;une page, mettez à jour `TOC.md` et la mise en page du dossier ensemble, ils doivent rester synchronisés.

## Pages liminaires

Les pages de contenu standard utilisent un bloc de garde comme :

```yaml
---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/<section>/<page>.html"
breadcrumb-title: ""
description: <one/two sentence SEO description>
helpx_creative_field: ""
helpx_description: Designer > <Section> > <Page>
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: <Page title>
user-guide-description: ""
user-guide-title: ""
---
```

Assurez-vous que `description` est précis et concis. Il est utilisé pour le référencement/la recherche de fragments de code.

&#x200B;# Règles de création de contenu

* L&#39;anglais est la source de la vérité ; toutes les autres langues en sont traduites.
* Tous les liens vers d&#39;autres pages de documentation doivent être des liens **relatifs** ; tous les liens vers des ressources externes doivent être des liens **absolus**.
* Le contenu est écrit dans un Markdown parfumé GitHub avec des extensions/gotchas personnalisées de l&#39;Experience League, documenté [ici](https://experienceleague.adobe.com/fr/docs/contributor/contributor-guide/writing-essentials/markdown). Utilisez la compétence `write-experience-league-markdown` (le cas échéant) pour les détails.
* Chaque modification soumise est soumise à des vérifications automatiques de liaison et à une validation de liaison dans CI (voir ci-dessous) — vérifiez `markdownlint_custom.json` et `linkcheckexclude.json` avant de supposer qu&#39;une règle s&#39;applique ou qu&#39;un lien doit être corrigé.

&#x200B;# Validation / CI

* `.github/workflows/validate-articles.yml` s&#39;exécute sur les RP et envoie à `main` (et via un commentaire RP `retest`), appelant le workflow réutilisable partagé `Adobe-Enterprise-Docs/workflows` pour pointer Markdown et valider les liens. Il n&#39;y a pas de script local équivalent dans ce référentiel — CI est la source de vérité pour réussite/échec.
* `.github/workflows/mirror.yml` reflète `main` dans le référentiel public sur push. Il s&#39;agit d&#39;une infrastructure, et non d&#39;un élément que les modifications de contenu doivent modifier.
* `markdownlint_custom.json` étend le jeu de règles `markdownlint.json` partagé et désactive plusieurs règles (MD005, MD007, MD018, MD032, MD033, MD034, MD037, MD040) qui entrent en conflit avec les extensions Markdown personnalisées de l&#39;Experience League (par exemple, HTML en ligne, accentuation non standard). Ne « corrigez » pas le contenu pour respecter ces règles désactivées.
* `linkcheckexclude.json` autorise les modèles de liens (actuellement `example.com`/`example-end.com`) que le vérificateur de liens doit ignorer.

&#x200B;# Conventions de travail

* Il s’agit d’une documentation riche en notes de mise à jour : les notes de mise à jour sont disponibles sous `help/release-notes/`, un dossier par version (par exemple `version-16-0`), plus `all-changes` et `old-versions` pages d’agrégation. Suivez le dossier de la version existante comme modèle lors de l’ajout d’une nouvelle version.
