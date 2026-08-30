---
name: write-experience-league-markdown
description: ""
Source: https://experienceleague.adobe.com/fr/docs/contributor/contributor-guide/writing-essentials/markdown
source-git-commit: e44437dcecf30714ffe5274c91135d84a0360aa7
workflow-type: tm+mt
source-wordcount: '647'
ht-degree: 6%

---


# Rédaction de l’Experience League Markdown

Experience League rend Markdown parfumé GitHub via un pipeline personnalisé
avec ses propres extensions et bizarreries de rendu. La GFM standard fonctionne principalement, mais
les éléments ci-dessous sont spécifiques à l’Experience League : corrigez-les et ajoutez du contenu
échoue lors de la vérification de lien/point CI ou n’effectue pas le rendu correctement sur le site en ligne.

## Intitulés

* `#` à `#####` (niveaux 1 à 5). La page de garde `title` de la page est
niveau 0 ; le premier titre Markdown du corps doit être un
un seul titre `# Level 1` correspondant (ou correspondant étroitement) au titre de la page.
* N’ignorez pas les niveaux arbitrairement ; la mini-table des matières est générée à partir des intitulés.

## Formatage de texte

* `**bold**`, `*italic*`, `***bold and italic***`.
* Caractères spéciaux littéraux d&#39;échappement avec une barre oblique inverse (`\*`, `\_`, etc.).
* Les **esperluettes** dans les titres doivent être écrites (`and`) ou codées en tant que
  `&amp;` — un `&` brut dans un titre peut interrompre l&#39;analyse.
* Les **chevrons** utilisés comme texte (et non comme HTML réel) doivent être codés :
  `<placeholder>` → `&lt;placeholder&gt;`.
* Les **guillemets ouvrants/fermants** collés à partir de traitements de texte doivent être codés, et non pas laissés comme
caractères bouclés littéraux : double gauche `&#8220;`, double droite `&#8221;`,
apostrophe/single droite `&#8217;`.

## Listes

* Listes numérotées : commencez chaque élément par `1.` (ou `1)`) — GitHub/Experience
Numérotation automatique de la ligue indépendamment des chiffres littéraux saisis.
* Listes à puces : utilisez `*`, `-` ou `+`, mais **ne mélangez pas les puces
dans la même liste/le même document**.
* L&#39;imbrication de listes `TOC.md` utilise `+` de manière cohérente, en respectant les paramètres du fichier existant
style de puce plutôt que d’en introduire un autre.

## Liens

* Les références croisées internes doivent être des liens Markdown **relatifs** vers le
fichier `.md` cible : `[Overview](../../overview.md)`.
* Les références externes doivent être des URL **absolues**.
* Ancrages dans les en-têtes/plages d’une autre page : ajoutez `#anchor-id`, par exemple.
  `[Mesh](../../glossary/glossary.md#mesh)`.
* Les ancrages dans la page sont déclarés sous la forme d’un en-tête (signature automatique) ou d’un
expliciter `<span id="anchor-id"></span>` juste avant le terme —
voir `help/glossary/glossary.md` pour le modèle utilisé dans ce référentiel.
* Les ancrages de section `TOC.md` utilisent la syntaxe `{#section-id}` après un en-tête/une liste
libellé, par exemple `Getting started{#getting-started}`.

## Images

* `![Alt text](path/to/image.png "Optional hover title")`.
* Les paramètres de requête de dimensionnement/optimisation facultatifs sont pris en charge :
  `![Adobe logo](my-page.resources/logo.png?width=750&format=png&optimize=medium)`.
* **Le texte alternatif ne doit pas contenir de traits de soulignement**, car ils ne s&#39;affichent pas correctement ;
utilisez plutôt des tirets ou des espaces.
* Les images spécifiques à la page se trouvent dans un dossier frère `<page-name>.resources/`
en regard de `.md`, référencé relativement (par ex.
  `<page-name>.resources/image.png`). `help/assets/` est un ancien partage
  dossier — n&#39;y ajoutez pas de nouvelles images (voir CLAUDE.md).

## Tableaux

* Délimité par des barres verticales, avec un tiret en-tête/ligne de séparation :

  ```markdown
  | Header | Another header | Yet another header |
  |--- |--- |--- |
  | row 1 | column 2 | column 3 |
  | row 2 | row 2 column 2 | row 2 column 3 |
  ```

* Une ligne vide doit précéder le tableau, sinon il ne s’affichera pas sous forme de tableau.
* Les tableaux ne peuvent pas contenir correctement du contenu de bloc complexe ou à plusieurs paragraphes dans un
cellule : ce référentiel nécessite des images/listes à l&#39;intérieur d&#39;une cellule de tableau (par ex.
tables de comparaison dans `overview.md`), le HTML en ligne est rétabli
(`<div>`, `<b>`, `<ul>`/`<li>`) avec `data-preserve-html="true"` sur chaque
afin que le pipeline ne le supprime pas. Suivre plutôt ce modèle existant
que d&#39;inventer un nouveau HTML intégré, sauf en cas de nécessité.

## Code

* Code intégré : backticks simples.
* Blocs clôturés : triple backticks, avec un langage facultatif pour la syntaxe
mise en surbrillance (` `&#x200B;``python `, ` ``&#x200B;`javascript `, etc.).

## Blocs de note/d’alerte

Syntaxe de blockquote personnalisée, un type par bloc, ligne de blockquote vide entre
l’étiquette et le corps :

```markdown
>[!NOTE]
>
>This is a standard NOTE block.

>[!TIP]
>
>This is a standard TIP.

>[!IMPORTANT]
>
>This is an IMPORTANT note.
```

Types pris en charge : `NOTE`, `TIP`, `IMPORTANT`, `CAUTION`, `WARNING`,
`ADMINISTRATION`, `AVAILABILITY`, `PREREQUISITES`, `ERROR`, `INFO`, `SUCCESS`.

## Intégrer des vidéos

```markdown
>[!VIDEO](https://video.tv.adobe.com/v/29770/?quality=12)
```

## Balise UICONTROL

Enchaîne les noms d’éléments de l’interface utilisateur (libellés de bouton, éléments de menu, noms de champ) de manière intégrée.
le pipeline de localisation sait qu&#39;il doit rechercher une chaîne translatée et tombe
Revenir à l’étiquette anglaise s’il n’en existe aucune :

```markdown
Click [!UICONTROL Save] to apply changes.
Go to [!UICONTROL Tools] > [!UICONTROL Settings].
```

Utilisez-le pour chaque étiquette d’interface utilisateur littérale référencée dans le texte didactique (menu
éléments, noms des boutons, titres des boîtes de dialogue, noms des panneaux).

## Balise DNL (« Ne pas localiser »)

Enchaîne les noms de produit, les noms de fonctionnalités tierces ou toute expression qui doit
ne jamais être translaté par une machine :

```markdown
Use [!DNL Adobe Analytics] to track metrics.
The [!DNL Target] implementation requires configuration.
```

Dans ce référentiel, utilisez-le pour les noms de produits tels que `[!DNL Substance 3D Designer]`,
`[!DNL Substance 3D Sampler]`, etc., sur les premières mentions/mentions importantes par page,
cohérent avec les pages existantes.

## HTML intégré

Le HTML brut est autorisé (le référentiel `markdownlint_custom.json` désactive MD033
spécifiquement pour cette raison), mais n&#39;est préservé de manière fiable que par le biais du
pipeline lorsque les balises portent `data-preserve-html="true"`. Réserver le HTML intégré
pour les cas où Markdown ne peut pas exprimer (images/listes dans les cellules du tableau,
`<span id="...">` ancrages) plutôt que comme substitut général de Markdown.

## Pages liminaires

Voir la section « Page front matter » de CLAUDE.md pour le bloc exact utilisé par
pages de contenu standard dans ce référentiel et `metadata.md` au niveau du référentiel
champs hérités.