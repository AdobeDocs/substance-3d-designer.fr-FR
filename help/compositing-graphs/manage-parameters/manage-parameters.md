---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/manage-parameters.html"
breadcrumb-title: ''
description: Découvrez comment gérer et organiser les paramètres dans les graphiques de composition de Substances pour une meilleure organisation du workflow.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Manage parameters
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Gérer les paramètres
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '709'
ht-degree: 3%

---


# Gérer les paramètres

Lorsque vous devez contrôler des paramètres autrement que directement, Designer propose plusieurs actions utiles pour :

* [Copier et coller](#copy-paste-parameters) les valeurs de tous les paramètres d&#39;un nœud
* Enregistrez les valeurs ou tous les paramètres d&#39;un nœud dans un [fichier de paramètres prédéfinis](../../compositing-graphs/manage-parameters/parameter-presets/parameter-presets.md), afin de les réutiliser ultérieurement
* [Exposez les paramètres](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md) des nœuds pour les rendre accessibles et les lier entre eux
* [Masquer ou afficher les paramètres](../../compositing-graphs/visible-control-vis/visible-if-control-visibility-of-inputs-outputs-and-parameters.md) en fonction des valeurs des autres paramètres
* Utilisez un graphique de fonction de [Substance](../../function-graphs/function-graphs.md) pour calculer la valeur d&#39;un paramètre

## Actions de paramètre

Les outils disponibles pour gérer les paramètres sont disponibles aux emplacements suivants :

### Actions globales

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Lorsque les propriétés d&#39;un nœud sont affichées dans le dock Propriétés, les paramètres du nœud peuvent être gérés globalement à l&#39;aide du menu « <b>Gérer les paramètres</b> » dans l&#39;en-tête de section suivant :

* Pour [nœuds atomiques](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/atomic-nodes.md) : paramètres spécifiques
* Pour [nœuds d&#39;instance](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md) : paramètres d&#39;instance

</td>
<td width="33.33%" style="border: 0;" valign="top">

![Menu global « Gérer les paramètres » dans Propriétés](../../assets/manage-parameters-menu-global.png "Menu global « Gérer les paramètres » dans Propriétés"){zoomable="yes"}

</td>
</tr>
</table>

Les actions de ce menu auront un impact sur *tous* les paramètres répertoriés dans cette section :

* <b>Exposer les paramètres :</b> ouvre la boîte de dialogue « Exposer les paramètres par lots ». Pour chaque paramètre exposé, l’action crée une nouvelle entrée de graphique et définit automatiquement une fonction à l’aide de cette entrée. En savoir plus sur l&#39;exposition des paramètres dans [cette page dédiée](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md).
* <b>Copier les paramètres :</b> Voir la section [Copier et coller les paramètres](#copy-paste-parameters) ci-dessous.
* <b>Coller les paramètres :</b> Voir la section [Copier et coller les paramètres](../../compositing-graphs/manage-parameters/manage-parameters.md) ci-dessous.
* <b>Enregistrer les paramètres dans un fichier de paramètres prédéfinis :</b> Pour en savoir plus sur les paramètres prédéfinis, consultez [cette page dédiée](../../compositing-graphs/manage-parameters/parameter-presets/parameter-presets.md).
* <b>Appliquer les paramètres d&#39;un fichier de paramètres prédéfinis :</b> Pour en savoir plus sur les paramètres prédéfinis, consultez [cette page dédiée](../../compositing-graphs/manage-parameters/parameter-presets/parameter-presets.md).
* <b>Tout réinitialiser :</b> réinitialise tous les paramètres à leurs valeurs et plages par défaut. Si une fonction a été appliquée à un paramètre, elle est rejetée.

>[!NOTE]
>
> Certaines actions ne sont pas disponibles pour certains nœuds atomiques. Voir [Limitations des nœuds atomiques](#atomic-nodes-limitations) ci-dessous.

### Actions à paramètre unique

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Si vous souhaitez gérer un paramètre *unique*, utilisez le menu « <b>Gérer la fonction</b> » à l&#39;opposé de l&#39;étiquette de paramètre.

</td>
<td width="33.33%" style="border: 0;" valign="top">

![Menu local « Gérer les paramètres » dans Propriétés](../../assets/manage-parameters-menu.png "Menu local « Gérer les paramètres » dans Propriétés"){zoomable="yes"}

</td>
</tr>
</table>

Vous pouvez appliquer un graphique de fonction de [Substance](../../function-graphs/the-function-graph/the-function-graph.md) à ce paramètre de trois façons :

* <b>Exposer comme nouvelle entrée de graphique :</b> qui crée une nouvelle entrée de graphique et définit automatiquement une fonction à l&#39;aide de cette entrée de graphique. En savoir plus sur l&#39;exposition des paramètres dans [cette page dédiée](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md).
* <b>Fonction vide :</b> créez une fonction à partir de zéro.
* <b>Valeur constante :</b> modifiez une fonction à partir d&#39;un [nœud de valeur constante](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/constant-nodes/constant-nodes.md) défini sur la valeur actuelle du paramètre.
* <b>Réinitialiser :</b> réinitialise le paramètre à sa valeur et sa plage par défaut. Si une fonction a été appliquée au paramètre, elle est rejetée.

>[!NOTE]
>
> Les actions de copier/coller et de fichier prédéfini sont globales pour tous les paramètres et ne sont donc pas disponibles pour des paramètres uniques.

### Menu contextuel du nœud

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Certaines actions de paramètre du menu *global* répertorié ci-dessus sont disponibles dans le menu contextuel du nœud. Cliquez sur RMB sur un nœud et accédez à « Gérer les paramètres » pour y accéder.

Notez que les actions de copier/coller ne sont pas disponibles dans ce menu. Vous les trouverez peut-être dans les propriétés du nœud comme expliqué ci-dessus.

Les mêmes limitations répertoriées ci-dessous pour les nœuds atomiques s’appliquent à ce menu.

</td>
<td width="50.00%" style="border: 0;" valign="top">

Menu ![&#39;Gérer les paramètres&#39; dans le menu contextuel du nœud](../../assets/manage-parameters-node-menu.png "&#39;Gérer les paramètres&#39; dans le menu contextuel du nœud"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Copier et coller des paramètres

Il est possible de copier toutes les valeurs de paramètres d&#39;un nœud source et de les coller sur un nœud cible. Les paramètres des nœuds source et cible sont <b>mis en correspondance en fonction de leurs identificateurs et de leurs types</b>.

Par exemple, un paramètre « Scale » dont l&#39;identificateur est « scale » et le type est « Float » peut être copié et collé sur un autre paramètre « Shape Scale » lorsque son identificateur est également « scale » et son type est également « Float ».

Cette fonctionnalité fonctionne de la même manière que l&#39;utilisation d&#39;un fichier de paramètre prédéfini [paramètre](../../compositing-graphs/manage-parameters/parameter-presets/parameter-presets.md). En effet, les données copiées dans le Presse-papiers sont les mêmes que celles stockées dans les fichiers de paramètres prédéfinis SBSPRS et peuvent être collées dans n’importe quel éditeur de texte pour être révisées et modifiées.

</td>
<td style="border: 0;" valign="top">

![Copier et coller des paramètres](../../assets/copy-paste-parameters.gif "Copier et coller des paramètres"){zoomable="yes"}

</td>
</tr>
</table>

## Limitations des nœuds atomiques

Certaines fonctionnalités ne sont pas disponibles pour certains [nœuds atomiques](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/atomic-nodes.md), en raison de leur implémentation et de leurs contrôles spécifiques.

Ces actions...

* [Copier/coller les paramètres](#copy-paste-parameters)
* [Enregistrer/Appliquer le fichier de paramètres prédéfinis](../../compositing-graphs/manage-parameters/parameter-presets/parameter-presets.md)

...ne sont pas disponibles pour ces nœuds atomiques :

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

[Bitmap](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md)

[Courbe](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/curve/curve.md)

[Distance](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/distance/distance.md)

[FX-Map](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md)

[Dégradé (dynamique)](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/gradient-dynamic/gradient-dynamic.md)

</td>
<td style="border: 0;" valign="top">

[Map de dégradé](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/gradient-map/gradient-map.md)

[Couleur en entrée](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md)

[Niveaux de gris en entrée](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md)

[Valeur d&#39;entrée](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md)

[Sortie](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)

</td>
<td style="border: 0;" valign="top">

[Processeur de pixels](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md)

[SVG](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/svg/svg.md)

[Texte](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md)

[Couleur uniforme](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/uniform-color/uniform-color.md)

[Processeur de valeurs](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/value-processor/value-processor.md)

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
