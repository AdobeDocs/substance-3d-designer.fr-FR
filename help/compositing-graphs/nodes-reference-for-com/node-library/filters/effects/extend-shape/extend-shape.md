---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/extend-shape.html"
breadcrumb-title: ''
description: Utilisez le nœud Extend Shape pour étendre les formes au-delà de leurs limites afin de créer des effets de masque et de motif étendus.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Extend Shape
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Extend Shape
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 0%

---


# Extend Shape

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](extend-shape.resources/extendshapegrayscale.png){width="200px"}

</td>
<td style="border: 0;" valign="top">

![](extend-shape.resources/extendshapecolor.png){width="200px"}

</td>
</tr>
</table>

<b>Entrée :</b> Filtres > Effets

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Le nœud <b>Extend Shape</b> étend une <i>section</i> de l&#39;<b>entrée</b> sur une direction et une distance définies.

Le paramètre <b>Afficher l&#39;assistant</b> vous permet de visualiser la section étendue et la direction de l&#39;extension.

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Mode</b> <i>Nombre entier</i> | Définit les <i>paramètres</i> utilisés pour appliquer l&#39;extension :<br><br>- <i>Bidirectionnel</i> : la section de l&#39;<b>entrée</b> spécifiée par les <b>position d&#39;extension</b> et <b>angle d&#39;extension</b> est étendue sur la <b>distance d&#39;extension</b> dans des <i>directions opposées</i><br>-<i>unidirectionnelles</i> : la section de l&#39;<b>entrée</b> spécifiée par les <b>position d&#39;extension</b> et <b>extension L&#39;angle</b> est étendu sur la <b>distance d&#39;extension</b> dans une <i>direction unique</i><br>-<i>positions de début/fin</i> : une extension <i>vectorielle</i> est définie par <b>position de début</b> et <b>position de fin</b>. La section <i>perpendiculaire</i> de l&#39;<b>entrée</b> à la <b>position de départ</b> est étendue <i>sur ce vecteur</i> jusqu&#39;à la <b>position de fin</b> |
| <b>Distance d&#39;extension</b> <i>Flotter</i> | Distance sur laquelle la section spécifiée par <b>Position d&#39;extension</b> et <b>Angle d&#39;extension</b> doit être étendue. La distance est exprimée en <i>proportion</i> de l&#39;étendue d&#39;image. |
| <b>Position de l&#39;extension</b> <i>Flotter</i> | La position dans l&#39;image de la section qui doit être étendue. La valeur est exprimée en un <i>décalage par rapport au centre</i>. |
| <b>Angle d&#39;extension</b> <i>Flotter</i> | L&#39;angle de la section qui doit être étendue, en considérant le point de départ est une <i>section verticale</i>. |
| <b>Position de départ</b> <i>Float2</i> | Position de début du <i>vecteur d&#39;extension</i>. |
| <b>Position de fin</b> <i>Float2</i> | Position de fin du <i>vecteur d&#39;extension</i>. |
| <b>Décalage de la Luminance de début</b> <i>Flotter</i> | Applique un décalage de luminance à la zone de l&#39;image <i>précédant</i> la section étendue. Ce décalage de luminance est <i>interpolé le long de la section</i> jusqu&#39;à la luminance de la zone de l&#39;image qui suit la section.<br><br><i>Remarque</i> : ce paramètre n&#39;est disponible que dans la version en <b>niveaux de gris</b> du nœud. |
| <b>Décalage de la Luminance de fin</b> <i>Flotter</i> | Applique un décalage de luminance à la zone de l&#39;image <i>suivant</i> la section étendue. Ce décalage de luminance est <i>interpolé le long de la section</i> jusqu&#39;à la luminance de la zone de l&#39;image précédant la section.<br><br><i>Remarque</i> : ce paramètre n&#39;est disponible que dans la version <b>en niveaux de gris</b> du nœud. |
| <b>Lum. Le décalage ignore les pixels noirs</b> <i>Booléen</i> | Lorsqu&#39;elle est définie sur <i>True</i>, les décalages de luminance spécifiés dans <i>les deux</i> Le <b>décalage de la Luminance de début</b> et le <b>décalage de la Luminance de fin</b> sont uniquement appliqués aux <i>pixels non noirs</i>, c&#39;est-à-dire aux pixels dont la valeur est supérieure à 0.<br><br><i>Remarque</i> : ce paramètre n&#39;est disponible que dans la version en <b>niveaux de gris</b> du nœud. |
| <b>Mode de filtrage</b> <i>Nombre entier</i> | Définit le traitement des résultats échantillonnés lors de l&#39;<i>interpolation</i> entre les pixels :<br><br>-<i>Nearest</i> : échantillonnera exactement la <i>même</i> valeur (plus rapide)<br>-<i>Bilinéaire</i> : appliquera un filtre bilinéaire sur le résultat pour un aspect <i>plus lisse</i> |
| <b>Afficher l&#39;Assistant</b> <i>Booléen</i> | Visualisez la <i>section étendue</i> sous forme d&#39;incrustation avec des flèches indiquant la <i>direction</i> de l&#39;extension. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="extend-shape.resources/extendshape.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="extend-shape.resources/extendshape-variant.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="extend-shape.resources/extendshape-variant2.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="extend-shape.resources/extendshape-node.png" />
        </td>
    </tr>
</table>
