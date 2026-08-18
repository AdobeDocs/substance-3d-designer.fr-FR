---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/getting-started/overview.html"
breadcrumb-title: ''
description: Découvrez Substance 3D Designer et ses fonctionnalités de création de matières et de textures procédurales.
helpx_creative_field: ""
helpx_description: Designer > Getting started > Overview
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Vue d’ensemble
user-guide-description: ''
user-guide-title: ''
source-git-commit: f320cf6842ff56ac24912ceda264f30c28317c05
workflow-type: tm+mt
source-wordcount: '970'
ht-degree: 2%

---


# Vue d’ensemble

[Substance 3D Designer](https://www.adobe.com/fr/products/substance3d-designer.html) est une application destinée à la création de textures, matériaux et filtres 2D dans une interface basée sur les nœuds, avec un accent particulier sur la génération procédurale, la paramétrisation et les workflows non destructifs. Il s’agit de l’application la plus longue à fonctionner dans l’écosystème Substance 3D et les ressources qui en découlent sont les plus polyvalentes et les plus dynamiques possibles.

Voici comment il se compare aux autres applications :

|  | <div><img alt="Icône Substance 3D Sampler" class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell_position-par_dx_table_row-r0-column-c1_position_position-par_image_713298714" src="../../assets/sa-appicon-noshadow-256.png" title="Icône Substance 3D Sampler" width="64px"/></div>  Substance 3D Sampler | <div><img alt="Icône Substance 3D Painter" class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell_position-par_dx_table_row-r0-column-c2_position_position-par_image" src="../../assets/pt-appicon-noshadow-256.png" width="64px"/></div>  Substance 3D Painter | <div><img alt="Icône Substance 3D Designer" class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell_position-par_dx_table_row-r0-column-c3_position_position-par_image" src="../../assets/ds-appicon-noshadow-256.png" title="Icône Substance 3D Designer" width="64px"/></div>  Substance 3D Designer |
| --- | --- | --- | --- |
| <b>Courbe d&#39;apprentissage</b> | Faible | Moyen | Élevée |
| <b>Création de documents</b> | Oui | Oui | Oui |
| <b>Création de modèles 3D</b> | Non | Limité\* | Limité\* |
| <b>Création de filtres, de motifs et d’effets</b> | Non | Limité | Oui |
| <b>Exporter le contenu paramétrique</b> | Non | Non | Oui |

\* : Displacement uniquement, voir la fonctionnalité <b>Exportation de scène</b> dans la section [Vue 3D](../../interface/3d-view/3d-view.md).

En bref, Substance 3D Designer doit être considéré comme l’application de texturation la plus technique et la plus avancée disponible.

Cela vous permet de créer du contenu pour presque tous les cas d’utilisation ou scénarios. Cela signifie que vous n’êtes pas limité à un seul type de sortie, tel qu’un matériau/ensemble de textures unique pour un filet mappé UV, mais que vous pouvez créer du contenu pour un ensemble d’utilisations beaucoup plus étendu.

Par exemple, la plupart des contenus intelligents de procédure dans Painter et Sampler ont été créés et exportés depuis Designer. Des éléments tels que les Alpha de pinceau, les générateurs, les filtres et les Matériaux de base peuvent tous être créés dans Designer.

## Workflow

Substance 3D Designer est un éditeur basé sur des nœuds qui vous permet de créer du contenu de nombreuses manières différentes avec différentes complexités. [Le workflow est expliqué plus en détail sur les pages dédiées](../../getting-started/workflow-overview/workflow-overview.md), mais les avantages suivants sont liés à l&#39;utilisation du logiciel :

<b>[Non linéaire](../../compositing-graphs/substance-compositing-graphs.md) </b> : vous pouvez créer une multitude de sorties de texture à la fois. Modifiez un masque ou un curseur, et automatiquement toute sortie connectée est recalculée. Plus besoin de créer séparément des mappages tels que Couleur de base, Rugosité, Normal, etc.

<b> [Non destructif](../../compositing-graphs/compositing-graph-key-con/substance-compositing-graph-key-concepts.md) </b> : vous pouvez annuler n&#39;importe quelle action *sans* perdre votre travail. Il devient beaucoup plus rapide d’itérer et d’expérimenter, trouvant des workflows encore plus efficaces.

<b> [Integrated Baking](../../bakers/bakers.md) </b> : accédez à des outils de cuisson de filet avancés et ultra-rapides directement dans le logiciel. Vous n’avez plus besoin d’effectuer la cuisson dans un logiciel séparé et d’effectuer de longs processus d’importation et d’exportation.

<b> [Parametric](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md) </b> : vous pouvez configurer pour contrôler presque tous les aspects d&#39;une texture à l&#39;aide d&#39;un seul curseur ou d&#39;une seule liste déroulante. Cela vous permet d’ajouter un contrôle et une variation sans fin à une seule ressource.

## Filetypes

L’application et son écosystème utilisent 4 types de fichiers différents. Soyons clairs : il s&#39;agit de types de fichiers <b>exportés depuis Substance 3D Designer</b> et qui peuvent être importés dans certaines applications Substance 3D ou dans toutes les autres.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../assets/ds-sbs-48.png)

### Fichier Substance 3D

*(\*.SBS)*

Les fichiers de Substance de données sont les **fichiers source principaux** pour Designer. Lorsque vous ouvrez un fichier de Substance de données, vous pouvez **afficher et modifier tous les nœuds d&#39;un graphique**. Ils sont représentés comme des packages, qui peuvent contenir un nombre quelconque de ressources telles que des graphiques, des fonctions, des bitmaps, des maillages, etc... Ils sont plus difficiles à partager et moins rapides à calculer. Ils ne peuvent être ouverts que dans Substance 3D Designer et la Substance Player.

</td>
<td style="border: 0;" valign="top">

![](../../assets/sbsar-48.png)

### Ressource Substance 3D

*(\*.SBSAR)*

Les archives de Substances sont <b> compilées, optimisées</b> fichiers de Substances. Ils sont beaucoup plus rapides à calculer et peuvent facilement être partagés sans problèmes de référence. Les paramètres peuvent encore être modifiés, mais la modification du graphique est <b>verrouillée</b>. Les archives de Substances peuvent être utilisées dans toutes les applications Substance 3D et toute application disposant d&#39;une [intégration Substance 3D](https://experienceleague.adobe.com/en/docs/substance-3d/ecosystem/home) (certaines avec un plug-in externe), telle qu&#39;Autodesk 3DS Max &amp; Maya, Unreal Engine ou Unity Engine.

</td>
<td style="border: 0;" valign="top">

![](../../assets/bmp-96.png){width="48px"}

### Fichiers statiques

*(\*.TGA, \*.BMP, \*.PNG, \*.FBX, \*.OBJ, etc...)*

Substance 3D Designer prend toujours en charge l’exportation vers des types de fichiers statiques. Une image 2D peut être exportée vers un fichier bitmap, un modèle 3D peut être exporté vers des types de fichiers 3D courants. Lors de l&#39;exportation vers des fichiers statiques, **toutes les fonctionnalités dynamiques sont perdues**. Les images sont verrouillées en résolution, les modèles 3D sont verrouillés en polycount.

</td>
</tr>
</table>

Cela signifie généralement que vous conservez votre travail au format SBS lorsque vous travaillez dans Designer, que vous l’exporterez vers SBSAR si la cible le prend en charge (Painter par exemple), ou que vous utiliserez des fichiers bitmap statiques si SBSAR n’est pas nécessaire ou n’est pas pris en charge.

## Types de ressources

Les fichiers Substance 3D peuvent contenir une grande variété de ressources à des fins différentes. Certaines ressources ne peuvent être créées qu’à l’intérieur de Designer, d’autres proviennent d’applications externes.

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

[![](../../assets/graph-5.png){width="150px"}](../../compositing-graphs/substance-compositing-graphs.md)

</td>
<td width="100.00%" style="border: 0;" valign="top">

### Graphes Substance

Les graphiques à Substances vous permettent de générer et de traiter *des données d&#39;image 2D*, puis de les exporter vers une ou plusieurs textures. Dans de nombreux cas, un projet s’articule autour d’un ou plusieurs graphiques de Substance.

[Accédez à la section dédiée aux graphiques de Substance.](../../compositing-graphs/substance-compositing-graphs.md)

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

[![](../../assets/function-1.png){width="150px"}](../../function-graphs/function-graphs.md)

</td>
<td width="100.00%" style="border: 0;" valign="top">

### graphiques de fonction de Substance

Les <b>fonctions</b> offrent un niveau supérieur d&#39;abstraction et de complexité : plutôt que de traiter des données d&#39;image (ensembles de valeurs de pixels), vous *traitez des valeurs uniques* (entiers, flottants, vecteurs). Les fonctions sont utilisées pour effectuer des opérations plus complexes ou pour affiner des comportements spécifiques. Les fonctions ne fonctionnent généralement pas de manière autonome et ne sont pas utilisées en dehors du cadre des graphiques de Substances.

[Accédez à la section dédiée aux graphiques de fonction de Substance.](../../function-graphs/function-graphs.md)

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

[![](../../assets/folder-4.png){width="150px"}](../../resources/importing-linking-and-new/importing-linking-and-new-resources.md)

</td>
<td width="100.00%" style="border: 0;" valign="top">

### Ressources non graphiques

Les ressources non graphiques peuvent provenir d&#39;applications externes (telles que Photoshop ou Autodesk Maya), tandis que certaines peuvent également être *créées dans Designer*. La principale différence est qu&#39;il ne s&#39;agit pas de graphiques basés sur les nœuds ; la plupart d&#39;entre eux sont des éléments à utiliser à l&#39;intérieur ou à côté des types de graphiques mentionnés précédemment.

Les types de ressources suivants existent :

* [Bitmaps](../../resources/bitmap-resource/bitmap-resource.md)
* [Images vectorielles (SVG)](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md)
* [Maillage 3D et scène](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/3d-mesh-resource-200574577.html)
* [Police](../../resources/font-resource/font-resource.md)
* [AxF](../../resources/axf-appearance-exchange/axf-appearance-exchange-format.md)

</td>
</tr>
</table>
