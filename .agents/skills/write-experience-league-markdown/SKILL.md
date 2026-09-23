---
name: write-experience-league-markdown
description: |
  Règles de syntaxe, extensions personnalisées et pièges pour l’écriture de contenu Markdown publié sur Adobe Experience League. Utilisez cette compétence lors de la création ou de la modification d’une page sous help/ dans ce référentiel (ou tout autre référentiel de contenu Experience League) : en-têtes, liens, images, tableaux, blocs de notes/d’alertes, balises UICONTROL/DNL, incorporations vidéo, ancres et pièges de rendu connus. Source : https://experienceleague.adobe.com/fr/docs/contributor/contributor-guide/writing-essentials/markdown
source-git-commit: ed17c57a1aa9669a602d4523bdef20cd7d82db75
workflow-type: tm+mt
source-wordcount: '1263'
ht-degree: 4%
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
expliciter `<span id="anchor-id"></span>` (HTML) / `{: #anchor-id}` (Markdown) immédiatement avant le terme —
voir `help/glossary/glossary.md` pour le modèle utilisé dans ce référentiel.
* Les ancrages de section `TOC.md` utilisent la syntaxe `{#section-id}` après un en-tête/une liste
libellé, par exemple `Getting started{#getting-started}`.

## Images

Utilisez la syntaxe d’image Markdown chaque fois que possible :

```markdown
![Alt text](path/to/image.png "Optional hover text")
```

* Le texte `![...]` doit être un texte optionnel accessible. Soyez concis et pratique
n’utilisez pas de tirets de soulignement ; utilisez plutôt des espaces ou des tirets.
* Le chemin d’accès à l’image peut être relatif au fichier Markdown ou relatif à la racine, par exemple
comme `/help/assets/shared-image.png`. Les images spécifiques à la page appartiennent au groupe
dossier `<page-name>.resources/` apparenté (par exemple,
  `<page-name>.resources/image.png`). `help/assets/` est un dossier partagé hérité ;
  n’ajoutez pas de nouvelles images spécifiques à cette page.
* Les paramètres de requête d&#39;image facultatifs peuvent contrôler le traitement CDN :
  `?width=750&format=png&optimize=medium`. Conserver ces paramètres sur l’image
  URL, avant tout bloc de propriété.
* Ajoutez les propriétés de l&#39;image immédiatement après la fermeture de `)` :
  `![Alt text](image.png "Hover text"){width="300" align="center"}`.
  `width` est une valeur en pixels ou un pourcentage de la zone d&#39;affichage ; les images sont mises à l&#39;échelle
proportionnellement. Les valeurs d&#39;alignement prises en charge sont `center` et `right`.
  `valign` n&#39;est pas pris en charge.
* Utilisez `modal="regular"` ou `zoomable="yes"` pour effectuer un clic pour zoomer sur une image :
  `![Alt text](image.png){width="100" zoomable="yes"}`. Ne pas combiner
  cliquez pour zoomer avec un lien vers une image ; le lien hypertexte est prioritaire.
* Pour créer un lien entre une image et une autre page, enchaînez l’image dans un lien Markdown :
  `[![Alt text](image.png)](../target/target.md)`.
* Pour les grandes images, fournissez au moins 640 pixels de largeur de source lorsque cela est possible.
utilisez au maximum environ 2 000 pixels, sauf en cas de besoin, et conservez les fichiers image sous
5 Mo si possible. Le pipeline accepte les fichiers jusqu’à 100 Mo, mais les fichiers plus
20 Mo de validation des échecs et les articles ne doivent généralement pas contenir plus de
100 images (certaines indications plus anciennes indiquent 200 ; utilisez la limite plus stricte).

Utilisez HTML uniquement lorsque Markdown ne peut pas exprimer la mise en page requise, telle qu&#39;une
un tableau spécial ou une présentation intégrée personnalisée. Formulaire d&#39;image de HTML pris en charge
est :

```html
<img src="image.png" alt="Alt text" />
```

* Fournissez toujours un attribut `alt` significatif et utilisez un attribut relatif ou
`src` relatif à la racine cohérent avec les images Markdown.
* Pour les images de HTML dans le HTML intégré conservé, ajoutez
  `data-preserve-html="true"` vers les balises qui les contiennent lorsque l&#39;option
  balisage environnant. Par exemple :

  ```html
  <div data-preserve-html="true" align="center">
    <img src="my-page.resources/preview.gif" alt="Preview" />
  </div>
  ```

* Pour activer le clic pour zoomer sur une image de HTML, utilisez
  `class="modal-image"` sur la balise `<img>`.
* N&#39;utilisez pas d&#39;attributs de HTML non pris en charge ou dépendez de `valign` ; préférez Markdown
propriétés de largeur et d’alignement.

## Tableaux

Préférez les tableaux Markdown natifs au contenu tabulaire ordinaire :

```markdown
| Header | Another header | Yet another header |
|--- |--- |--- |
| row 1 | column 2 | column 3 |
| row 2 | row 2 column 2 | row 2 column 3 |
```

* Placez une ligne vide avant le tableau. Les tableaux Markdown nécessitent au moins un
ligne d’en-tête et une ligne de corps ; utilisez un tableau de HTML pour une ligne ou sans en-tête
table.
* Utilisez au moins trois tirets dans chaque cellule de séparateur d’en-tête et conservez les mêmes valeurs
nombre de caractères de barre verticale dans chaque ligne. Échapper un canal littéral comme `\|` ou
  `&vert;`.
* Utilisez les repères d’alignement dans la ligne de séparation si nécessaire :
  `|---|:---:|---:|` pour l&#39;alignement à gauche, au centre et à droite.
* Le HTML en ligne est pris en charge dans les cellules de tableau Markdown pour les sauts de paragraphe et
listes de base. Utilisez `<p>` pour des paragraphes distincts, `<br>` pour des sauts de ligne et
  `<ul>`/`<ol>` avec `<li>` éléments pour les listes. Addition
  `data-preserve-html="true"` pour intégrer des éléments de HTML lorsque requis par le
  balisage du référentiel environnant.

  ```markdown
  | Header | Details |
  |---|---|
  | Text | First paragraph.<p>Second paragraph.<br>New line.<ul><li>Item</li></ul> |
  ```

* Evitez les tableaux très larges et très hauts, difficiles à naviguer.
Soyez prudent avec le code en ligne dans les tableaux, car le code long peut forcer
largeurs de colonnes disproportionnées.
* Pour choisir la disposition d’un tableau Markdown, ajoutez la propriété après la propriété
tableau, séparé par une ligne vierge :

  ```markdown
  {style="table-layout:fixed"}
  ```

  Utilisez `table-layout:auto` (valeur par défaut) lorsque du texte ou du code long doit être flexible
  largeur des colonnes. Utiliser `fixed` pour les colonnes équilibrées, telles que les tableaux contenant
  images de taille similaire.

Utilisez un tableau de HTML lorsque Markdown ne peut pas exprimer la structure requise, telle que
omission d’en-têtes, combinaison de cellules avec des plages, équilibrage de colonnes ou alignement
contenu dans les cellules :

```html
<table style="table-layout:fixed">
  <tr>
    <th>Property</th>
    <th>Value</th>
  </tr>
  <tr>
    <td align="center">Example</td>
    <td>Details</td>
  </tr>
</table>
```

* Les éléments de tableau pris en charge sont les suivants : `<table>`, `<tbody>`, `<thead>`, `<tfoot>`
  `<tr>`, `<th>`, `<td>`, `<col>` et `<colgroup>`, ainsi que pris en charge
éléments en ligne tels que `<p>`, `<br>`, `<b>`, `<i>`, `<ul>`, `<ol>` et
  `<li>`.
* N&#39;utilisez pas la syntaxe Markdown dans une table de HTML. Par exemple, Markdown
le rendu des notes, des images et des liens peut être littéral ; utilisez plutôt la syntaxe de HTML.
  Les balises de localisation `UICONTROL` et `DNL` sont des exceptions.
* Utilisez `align="left"`, `align="center"` ou `align="right"` sur une cellule lorsque
nécessaire. Les tableaux de HTML ne peuvent pas contenir de tableaux imbriqués.
* Définissez la disposition du tableau de HTML sur la balise d’ouverture :
  `<table style="table-layout:auto">` ou
  `<table style="table-layout:fixed">`.
* Pour un tableau de HTML sans bordure d’une ligne, utilisez
  `<tr style="border: 0;">`.

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

Experience League ne prend pas en charge les intégrations vidéo MP4 ou YouTube dans `[!VIDEO]` blocs. Si vous avez besoin d’un aperçu animé, utilisez plutôt un GIF dans le dossier frère `.resources` de la page et centrez-le avec le HTML intégré si nécessaire.

```markdown
<div data-preserve-html="true" align="center">
  <img src="my-page.resources/my-preview.gif" alt="My preview" />
</div>
```

N&#39;utilisez pas `[!VIDEO]` pour les fichiers MP4 locaux, les fichiers MP4 distants ou les URL YouTube, car le pipeline de publication les rejette et l&#39;interface utilisateur échoue.

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

Voir la section « Page front matter » de AGENTS.md pour le bloc exact utilisé par
pages de contenu standard dans ce référentiel et `metadata.md` au niveau du référentiel
champs hérités.