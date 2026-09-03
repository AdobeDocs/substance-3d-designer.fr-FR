---
name: generate-node-documentation
description: ""
source-git-commit: 69f546a26d2e09127b1c79ef4003e235536289da
workflow-type: tm+mt
source-wordcount: '723'
ht-degree: 4%

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
mettre à jour `TOC.md` et la disposition du dossier ensemble (voir le dossier/la table des matières de CLAUDE.md
convention).

## Pages liminaires

Les pages de nœud utilisent le bloc **minimal** : uniquement `title` et un style de chemin de navigation
`description`. (Ce bloc est différent des documents CLAUDE.md hérités à 11 champs pour
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

Inclure uniquement s’il existe des exemples d’images/de GIFs. Utiliser un tableau de galerie de HTMLS ; un `<td>`
par image avec une légende facultative ; effectuez un retour à la ligne vers un nouveau `<tr>` après 3 images. Chemins d’accès aux médias
pointez dans le dossier `.resources` de la page.

```html
## Examples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="./<node-name>.resources/<file>.gif" /><br><i>Caption</i>
        </td>
        <td style="border: 0; background: transparent">
            <img src="./<node-name>.resources/<file2>.jpg" /><br><i>Another caption</i>
        </td>
    </tr>
</table>
```

Laisser les cellules de fin dans une dernière ligne partiellement remplie vides (`<td …></td>`) plutôt que
redistribution. Omettez les sous-titres si la source n’en a pas.

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
