---
name: generate-node-documentation
description: |
  Comment créer une page de référence de nœud Substance 3D Designer afin qu’elle corresponde à la mise en page standard utilisée dans help/compositing-graphes/nodes-reference-for-com/node-library/. Utilisez cette compétence lors de la création ou de la modification d'une page de nœud (description, entrées, sorties, paramètres ou exemples d'un nœud) sous cette arborescence de la bibliothèque de nœuds, ou des pages de référence de fonction/nœud atomique équivalentes. Couvre la convention du dossier/de la table des matières, la page de garde minimale, le tableau des icônes/descriptions, les tableaux des entrées/sorties/paramètres ancrés et la galerie d’exemples. Pour les règles générales Adobe Experience League Markdown (légendes, liens, UICONTROL/DNL, images), utilisez la compétence write-experience-league-markdown ; cette compétence ne couvre que la structure nœud-page. Exemple canonique : help/compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.md
source-git-commit: ed17c57a1aa9669a602d4523bdef20cd7d82db75
workflow-type: tm+mt
source-wordcount: '976'
ht-degree: 3%
---

# Génération de la documentation du nœud

Chaque page de référence de nœud feuille de ce référentiel suit une structure cohérente. Ceci
la compétence est la spécification de cette structure. L&#39;exemple canonique et parfaitement travaillé est
`.../node-library/texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.md` —
en cas de doute, ouvrez-le et mettez-le en miroir.

Cette compétence ne couvre que la *structure* de la page des nœuds. Pour l’Experience League de base Markdown
(blocs de notes/d’alertes, liens relatifs par rapport aux liens absolus, UICONTROL/DNL, paramètres de requête d’image,
lint gotchas) suivez la compétence `write-experience-league-markdown`.

## Emplacement d’une page de nœud (convention de dossier/table des matières)

* Un dossier par nœud, sous le chemin de catégorie/sous-catégorie correspondant, par ex.
  `.../node-library/<category>/<subcategory>/<node-name>/<node-name>.md`.
* Le dossier porte le nom de nœud kebab-case ; il contient le fichier **one** `.md`
nommé de la même manière.
* Tous les médias incorporés de la page (icône, exemples d&#39;images, GIFs) résident dans un frère **&#x200B;  `<node-name>.resources/` dossier &#x200B;** en regard de `.md` et sont référencés par un
  chemin relatif (par exemple `<node-name>.resources/<file>.png`). Ne pas pointer les pages de nœud sur
  le dossier partagé `help/assets/`, c&#39;est-à-dire un modèle hérité en cours de suppression progressive ; nouveau et
  les pages modifiées utilisent leur propre dossier `.resources`.
* Chaque page a une entrée correspondante dans `help/guide/TOC.md`. Lors de l’ajout ou du déplacement d’un
mettre à jour `TOC.md` et la disposition du dossier ensemble (voir Dossier/Table des matières d&#39;AGENTS.md
convention).

## Pages liminaires

Les pages de nœud utilisent le bloc **minimal** : uniquement `title` et un style de chemin de navigation
`description`. (Ceci est différent des 11 champs du bloc existant AGENTS.md documents pour
pages de contenu standard.)

```yaml
---
title: "Shape splatter v2"
description: "Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Generator > Pattern > Shape splatter v2"
---
```

## Structure du corps

De haut en bas, tout ce qui se trouve en dessous de la page de garde :

### &#x200B;1. Titre H1

Un seul `# <Node title>` : exactement un H1 par page.

### &#x200B;2. Icône/tableau de description

Un tableau de HTML, une ligne, deux cellules. La cellule de gauche (`33.33%`) contient l&#39;icône, puis la
Chemin de navigation `In:` ; la cellule de droite (`100.00%`) contient `## Description` et la prose.

```html
<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![<Node title> icon](<node-name>.resources/<node-name>.png "<Node title>")

<b>In:</b> <Category> &gt; <Subcategory>

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

<Description prose.>

</td>
</tr>
</table>
```

Conventions de la prose des cellules de description :
* Séparez les paragraphes par `<br><br>` (les lignes vides brutes à l&#39;intérieur de la cellule ne sont pas fiables).
* L&#39;accentuation intégrée est `<b>…</b>` / `<i>…</i>`.
* Les parties d&#39;entrée utilisent `<i>Note:</i>` / `<i>Tip:</i>` au début de la phrase.
* Utilisez `&gt;` pour `>` sur la ligne `In:` (elle se trouve dans le HTML). Choisir la catégorie /
les noms de sous-catégories du nœud lui-même ; ne les inventez pas.
* Pour les nœuds avec plusieurs versions (par exemple, couleur/niveaux de gris/valeur ou variantes numérotées)
comme les Cellules 1 / Cellules 2), ajouter un dernier paragraphe de description qui fait référence à l&#39;autre
les versions avec des liens relatifs, séparés par un seul saut de ligne. Exemple : &grave;See also: [&#128279;](../input-grayscale/input-grayscale.md)Input
grayscale, [Input value](../input-value/input-value.md)&grave;.

### &#x200B;3. Légendes facultatives

`>[!INFO]`, `>[!TIP]`, `>[!NOTE]`, etc. accédez **après** le tableau icône/description (et non
dans la cellule). Syntaxe selon la compétence `write-experience-league-markdown`.

### &#x200B;4. Entrées

Inclure uniquement si le nœud a des épingles d&#39;entrée. Faites précéder le titre d’un point d’ancrage.

```markdown
<a name="inputs"></a>

## Inputs

|  |  |
|:---|:---|
| <b>Background height</b> <i>Grayscale</i> | The base height map in which shapes are scattered.<br><br>The contribution is controlled by the <b>Background input opacity</b> parameter. |
```

* Deux colonnes, ligne d&#39;en-tête vide, alignement `|:---|:---|`.
* Une ligne par entrée : cellule gauche `<b>Name</b> <i>Type</i>`, cellule droite la description.
* Le marqueur de type est en italique de HTML — `<i>Type</i>` — et non en markdown `*Type*`.

### &#x200B;5. Sorties

Même forme que les entrées, avec `<a name="outputs"></a>` + `## Outputs`. Inclure uniquement si
nœud documente les sorties distinctes (de nombreux nœuds ont une seule sortie implicite et l&#39;omettent
section — n&#39;en inventez pas une).

Pour les sorties multicanaux compressées, séparez les canaux par `<br>` et créez un retrait
sous-points avec `&nbsp;` (voir les lignes « Splatter UVW » / « Splatter data » dans le
référence) :

```markdown
| <b>Splatter UVW</b> | <b>R</b> - U component of the shapes' UVs.<br><b>G</b> - V component of the shapes' UVs.<br><b>B</b> - The shapes' height. (W)<br><b>A</b> - Packed data:<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- <i>Integer part:</i> The shapes' unique identifier. |
```

### &#x200B;6. Paramètres

Même forme de tableau, avec `<a name="parameters"></a>` + `## Parameters`. Ignorer l’ensemble
si le nœud n&#39;a pas de paramètres (n&#39;émettez jamais une table vide ou un « Aucun paramètre ».
ligne).

* **Paramètres groupés** : émettez une ligne d&#39;étiquette étendue avec une cellule de droite vide avant la
lignes du groupe :

  ```markdown
  | <b>Positioning</b> |  |
  | <b>Project Input</b> <i>UV Position, World Space Position</i> | Choose whether the projection position is set in 2D/UV or in 3D/World space. |
  ```

* **Valeurs d&#39;énumération/options multiples** : répertorie les options dans la cellule de description sous la forme d&#39;une
  Liste de tirets séparés par `<br>` :

  ```markdown
  | <b>Position distribution mode</b> <i>Integer</i> | The method of distributing the shapes:<br><br>- <b>2D grid:</b> A simple uniform grid.<br>- <b>Poisson disc:</b> Randomly offsets grid cells to prevent overlaps.<br>- <b>Uniform:</b> An even distribution of a set number of shapes. |
  ```

### &#x200B;7. Exemples

Inclure uniquement s’il existe des exemples d’images/de GIFs. Utilisation d’un HTML sans bordure à mise en page fixe
table de la galerie ; un `<td>` par image ; retour à la ligne vers un nouveau `<tr>` après 3 images. Chemins d’accès aux médias
pointez dans le dossier `.resources` de la page. Utiliser un élément de HTML `<img>` pour chaque
par exemple, avec `class="modal-image"` pour que l&#39;image publiée s&#39;ouvre dans la norme
visionneuse d’images. Fournissez un texte `alt` significatif qui identifie le nœud et l&#39;exemple
nombre. N’utilisez pas la syntaxe d’image Markdown dans cette galerie.

```html
## Examples

<table style="table-layout:fixed">
    <tr style="border: 0;">
        <td style="border: 0;">
            <img src="<node-name>.resources/<file>.gif" class="modal-image" alt="<Node title> - Example 1" />
        </td>
        <td style="border: 0;">
            <img src="<node-name>.resources/<file2>.jpg" class="modal-image" alt="<Node title> - Example 2" />
        </td>
    </tr>
</table>
```

Conserver le `style="table-layout:fixed"` de la table et le `style="border: 0;"`
attributs tels qu’ils apparaissent ; n’ajoutez pas de bordures, de marges ni de styles d’arrière-plan.
Laisser les cellules de fin dans une dernière ligne partiellement remplie vides
(`<td style="border: 0;"></td>`) plutôt que de redistribuer. Utiliser l’image existante
ordre et noms de fichiers. Si une page comporte des légendes, conservez-les plutôt en tant que texte `alt`
plutôt que d’ajouter une annotation de légende visible. Omettre toute la section lorsque la page n’a pas
exemple de média.

## Valeurs de type canonique

Réutilisez le libellé de type du nœud ; valeurs standard : `Grayscale`, `Color`, `Integer`,
`Float`, `Float2`, `Float3`, `Float4`, `Integer2`, `Boolean`, `Grayscale Input`,
`Color Input`, `(Color value)`, `(Grayscale value)`. Ne pas inventer ou normaliser un texte
le nœud n&#39;utilise pas réellement.

## Règles de cellule de tableau

* Aucune ligne brute à l&#39;intérieur d&#39;une cellule de tableau — joignez les lignes avec `<br>` (et `<br><br>` entre
paragraphes).
* L&#39;accentuation à l&#39;intérieur des cellules est `<b>`/`<i>` et le marqueur de type est toujours `<i>Type</i>`.
* Retrait des sous-points imbriqués avec `&nbsp;` séquences.

## Règles / ne pas

* **Ne pas fabriquer** d&#39;entrées, de sorties ou de paramètres que le nœud n&#39;a pas ; omettez le
à la place. Ne reformulez pas, ne résumez pas et ne supprimez pas le contenu technique existant, mais uniquement
reformatez-le.
* **Conserver les liens relatifs** aux autres pages `.md` ; liens externes absolus.
* **Déposer la dérive héritée** lors de la modification d’une ancienne page dans ce format : balises de difficulté
(`**Simple**` / `**Intermediate**` / `**Complex**`), redondant `## <Title>`
sous-titre à l’intérieur de la cellule d’icône, des phrases de stub comme « Il n’y a aucune image jointe à
this page. », ainsi que les tables de navigation/wrapper vides restantes lors des migrations précédentes.
* **Un H1** par page ; les sections utilisent `##` et les ancres Entrées/Sorties/Paramètres
(`inputs` / `outputs` / `parameters`) doivent précéder leurs en-têtes afin de passer d’une page à l’autre
  Les liens `#inputs` se résolvent.
* **Gardez `TOC.md` synchronisé** lorsque vous ajoutez, renommez ou déplacez une page.
