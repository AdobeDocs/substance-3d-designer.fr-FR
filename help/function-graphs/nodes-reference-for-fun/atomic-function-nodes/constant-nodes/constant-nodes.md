---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/atomic-function-nodes/constant-nodes.html"
breadcrumb-title: ''
description: Accédez à des nœuds constants dans les graphes de fonction Substance 3D Designer pour définir des valeurs et des paramètres constants.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Constant
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Constante
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '662'
ht-degree: 0%

---


# Constante

Les nœuds constants permettent de créer une valeur statique utilisable dans les graphes de fonction de Substance. Contrairement aux [variables](../../../../function-graphs/variables/variables.md), elles ne peuvent pas être modifiées en externe.

En outre, cette page fournit des informations supplémentaires pour chaque type de données et cas d’utilisation courants.

## Entiers

Les entiers constants génèrent des nombres entiers et ont un pas de 1.

[Ils peuvent être convertis en Flottant](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/cast-nodes/cast-nodes.md), ce qui est recommandé lors de toute opération plus complexe que les ajouts, les soustractions et les comparaisons simples.

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![icône de type d&#39;Entier](../../../../assets/fn-constant-integer.png "icône de type d&#39;Entier")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Entier</b>

Un entier a un seul composant. Il est utile comme index pour effectuer des sélections, par exemple :

* sélection d&#39;une option présentée à l&#39;utilisateur sous forme de menu déroulant (voir « Liste déroulante » dans [cette page](../../../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)).
* sélection de l&#39;entrée d&#39;un nœud [commutateur multiple](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blending/multi-switch/multi-switch.md).<b></b>

>[!IMPORTANT]
>
> <b>Les entiers négatifs</b> dans les fonctions de paramètre ne sont *pas pris en charge*. Voir [cette page](../../../../technical-issues/parameters-not-working/parameters-not-working-as-expected.md) dans la section « Problèmes techniques » pour une solution.

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

Icône de type ![Entier 2](../../../../assets/fn-constant-integer2.png "Entier 2")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Entier 2</b>

Un nœud Entier 2 génère un vecteur d’entier statique à 2 composantes avec des composantes (X, Y).

Entier 2 n&#39;est pas courant, mais il est utilisé par exemple pour définir les répétitions 2D X et Y dans un [Tile Generator](../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md).

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

Icône de type ![Entier 3](../../../../assets/fn-constant-integer3.png "Entier 3")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Entier 3</b>

Un nœud Entier 3 génère un vecteur d’entier statique à 3 composants avec des composants (X, Y, Z).

L&#39;Entier 3 n&#39;est pas courant et est peu susceptible d&#39;être rencontré beaucoup.<b>\
</b>

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

Icône de type ![Entier 4](../../../../assets/fn-constant-integer4.png "Entier 4")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Entier 4</b>

Un nœud Entier 4 génère un vecteur d’entier statique à 4 composantes avec des composantes (X, Y, Z, W).

L&#39;Entier 4 n&#39;est pas courant et est peu susceptible d&#39;être rencontré beaucoup.<b>\
</b>

</td>
</tr>
</table>

## Flottants

Les Flottants constants génèrent des nombres à fractions et non des nombres entiers. Par conséquent, ils auront toujours des valeurs après le signe décimal et peuvent entrer ou diminuer par pas inférieurs à 1 (0,01 par défaut).

[Les Flottants peuvent être convertis en Entiers](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/cast-nodes/cast-nodes.md), mais ils seront arrondis à l&#39;Entier supérieur ou inférieur le plus proche, ce qui signifie que les données et l&#39;exactitude sont perdues.

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

Icône ![Type de Flottant](../../../../assets/fn-constant-float.png "Icône Type de Flottant")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Flottant</b>

Un Flottant, a un seul composant, le (1) est omis du nom par souci de brièveté. Le flottant est très courant et utilisé pour toute valeur nécessitant un contrôle précis sous la forme d’un curseur ou d’un angle. Vous pouvez le trouver dans presque tous les paramètres de Node. Il s&#39;agit également du type de données préféré pour une valeur en niveaux de gris !<b></b>

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

Icône de type ![Flottant 2](../../../../assets/fn-constant-float2.png "Flottant 2")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Flottant 2</b>

Un nœud Flottant 2 génère un vecteur de Flottant statique à 2 composants. Les composants sont nommés X, Y. Flottant 2 est assez courant et est utilisé pour [échantillonner les coordonnées](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md) et pour les [décalages de transformation](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/transforms.md)

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

Icône de type ![Flottant 3](../../../../assets/fn-constant-float3.png "Flottant 3")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Flottant3</b>

Un nœud Flottant 3 génère un vecteur de Flottant statique à 3 composants. Les composants sont nommés X, Y, Z. Flottant 3 est rare, il est principalement utilisé pour représenter les [coordonnées d&#39;échelle 3D](../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d/cube-3d.md) et comme moyen plus simple de stocker des couleurs sans données d&#39;Alpha.<b>\
</b>

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

Icône de type ![Flottant 4](../../../../assets/fn-constant-float4.png "Flottant 4")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Flottant4</b>

Un Flottant 4 génère un vecteur de Flottant statique à 4 composants. Les composants sont nommés X, Y, Z, W. Le Flottant 4 est très courant, car il s&#39;agit de la méthode préférée pour stocker et définir des informations de [couleur, où les données XYZW représentent des valeurs RVBA.](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/uniform-color/uniform-color.md)<b>\
</b>

</td>
</tr>
</table>

## Autres

Deux types de données supplémentaires existent dans les graphes de fonction de Substance de données : booléens et chaînes. Des chaînes ont été introduites parallèlement au nœud [Texte](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md) dans Designer version 6.

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

Icône ![Booléen](../../../../assets/fn-constant-boolean.png "Booléen")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Booléen</b>

Un Booléen est le type de données le plus simple qui soit, ne connaissant que deux états : Vrai ou Faux, 1 ou 0. Elle est représentée par la couleur blanche. Il n&#39;est pas possible d&#39;échanger entre le Booléen et l&#39;Entier sans [Converti](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/cast-nodes/cast-nodes.md) ou en utilisant [des nœuds logiques](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/logical-nodes/logical-nodes.md). Un Booléen est assez courant et c&#39;est un excellent moyen de contrôler le flux d&#39;une fonction ou d&#39;un graphe, une utilisation typique serait pour un [nœud de commutation.](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blending/switch/switch.md)<b></b>

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Icône de type de chaîne](../../../../assets/fn-constant-string.png "Icône de type de chaîne")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Chaîne</b>

Un nœud de chaîne génère une chaîne statique, c&#39;est-à-dire un fragment de texte. Il s&#39;agit du type de données le plus exotique disponible dans Fonctions, et ne peut généralement pas être utilisé beaucoup en conjonction avec d&#39;autres Noeuds de fonction. Son objectif principal est de fonctionner comme une sortie finale pour le [nœud de texte](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md).

</td>
</tr>
</table>
