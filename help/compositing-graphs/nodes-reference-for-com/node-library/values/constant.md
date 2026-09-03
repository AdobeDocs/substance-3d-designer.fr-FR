---
helpx_url: ""
breadcrumb-title: ''
description: Accédez aux nœuds de constantes dans Substance 3D Designer pour définir des valeurs constantes dans les graphiques de Substances.
helpx_creative_field: ""
helpx_description: ""
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Constante
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '508'
ht-degree: 0%

---


# Constante

Les nœuds constants permettent de créer une valeur statique utilisable dans les graphes en Substance.

Vous trouverez ces nœuds dans la section **Valeurs > Constantes** de la bibliothèque.\
Ils incluent tous un simple nœud [Value processor](../../atomic-nodes/value-processor/value-processor.md) générant la valeur.

+++ Nœuds constants dans la bibliothèque

![constants-library.png](constant.resources/constant-01.png)

+++

<p style="text-align: center;"><img src="./constant.resources/constant-02.png" alt="Nœud flottant constant" /></p>

## Entiers

Les entiers constants génèrent des nombres entiers et ont un pas de 1.

[Ils peuvent être convertis en flottants](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/cast-nodes/cast-nodes.md), ce qui est recommandé lors de toute opération plus complexe que les ajouts, les soustractions et les comparaisons simples.

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

Icône ![Type d&#39;entier](constant.resources/constant-03.png "Icône Type d&#39;entier")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Nombre entier</b>

Un entier a un seul composant. Il est utile comme index pour effectuer des sélections, par exemple :

* sélection d&#39;une option présentée à l&#39;utilisateur sous forme de menu déroulant (voir « Liste déroulante » dans [cette page](../../../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)).
* sélection de l&#39;entrée d&#39;un nœud [commutateur multiple](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blending/multi-switch/multi-switch.md).<b></b>

>[!IMPORTANT]
>
> Les <b>entiers négatifs</b> dans les fonctions de paramètre ne sont *pas pris en charge*. Voir [cette page](../../../../technical-issues/parameters-not-working/parameters-not-working-as-expected.md) dans la section « Problèmes techniques » pour une solution.

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

Icône de type ![Entier2](constant.resources/constant-04.png "Entier2")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Entier2</b>

Un nœud Integer2 génère un vecteur entier statique à 2 composantes avec des composantes (X, Y).

Un cas d&#39;utilisation courant d&#39;Integer2 est de définir les tailles de grille X et Y, comme dans le nœud [Tile Generator](../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md).

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

Icône de type ![Integer3](constant.resources/constant-05.png "Icône de type Integer3")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Entier3</b>

Un nœud Integer3 génère un vecteur entier statique à 3 composantes avec des composantes (X, Y, Z).

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

Icône de type ![Integer4](constant.resources/constant-06.png "Icône de type Integer4")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Entier4</b>

Un nœud Integer4 génère un vecteur entier statique à 4 composantes avec des composantes (X, Y, Z, W).

</td>
</tr>
</table>

## Flotteurs

Les valeurs Flottant constantes génèrent des nombres fractionnaires, c’est-à-dire qu’elles prennent en charge les valeurs après le signe décimal et peuvent être ajustées par incréments inférieurs à 1. (Par défaut : 0,01)

Les valeurs [flottantes peuvent être converties en nombres entiers](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/cast-nodes/cast-nodes.md), mais elles seront arrondies à l&#39;entier supérieur ou inférieur le plus proche, ce qui signifie que les données et l&#39;exactitude sont perdues.

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Icône de type flottant](constant.resources/constant-07.png "Icône de type flottant")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Flotter</b>

Un objet Float a un seul composant et est très couramment utilisé pour toute valeur unique nécessitant une précision.

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

Icône de type ![Float2](constant.resources/constant-08.png "Float2")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Float2</b>

Un nœud Float2 génère un vecteur à 2 composantes avec des composantes (X, Y).

Float2 est couramment utilisé pour [l&#39;échantillonnage des coordonnées](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md), les [transformations de décalage](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/transforms.md) et la manipulation vectorielle 2D générale.

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

Icône de type ![Float3](constant.resources/constant-09.png "Float3")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Float3</b>

Un nœud Float3 génère un vecteur à 3 composantes (X, Y, Z).

Float3 est principalement utilisé lors de l&#39;utilisation d&#39;objets 3D et de [coordonnées d&#39;échelle 3D](../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d/cube-3d.md), comme dans les [nœuds SDF 3D](../../../../function-graphs/nodes-reference-for-fun/function-node-library/function-node-library.md#sdf-functions), et comme moyen plus simple de stocker des couleurs RGB, c&#39;est-à-dire sans Alpha.

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

Icône de type ![Float4](constant.resources/constant-10.png "Float4")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Float4</b>

Un objet Float4 génère un vecteur à 4 composantes (X, Y, Z, W).

Float4 est le moyen préféré de stocker et de définir des informations de couleur où les valeurs XYZW sont mappées à RVBA, comme dans le [nœud de couleur uniforme](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/uniform-color/uniform-color.md).

</td>
</tr>
</table>

## Non numérique

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Icône de type booléen](constant.resources/constant-11.png "Icône de type booléen")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Booléen</b>

Un Booléen est le type de données le plus simple qui soit, ne connaissant que deux états : <code>true</code> ou <code>false</code>.

Ce type est assez courant lorsque vous travaillez avec des paramètres de bascule et des conditions [If/Else](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/control-nodes/control-nodes.md).Les <br>booléens sont un moyen simple et efficace de contrôler le flux d&#39;une fonction ou d&#39;un graphe, par exemple à l&#39;aide d&#39;un [nœud de commutation](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blending/switch/switch.md).

</td>
</tr>
</table>
