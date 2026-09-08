---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/shape-drop-shadow.html"
breadcrumb-title: ''
description: Utilisez le nœud Ombre portée de forme pour ajouter des effets d’ombre portée aux formes afin de créer une profondeur et une dimension dans les textures.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Shape Drop Shadow
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Ombre portée de la forme
user-guide-description: ''
user-guide-title: ''
source-git-commit: a4ccdbff5343e3ece0312bd9b3318fb236f07308
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 6%

---


# Ombre portée de la forme

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/shape-dropshadow-grayscale.png){width="128px"}

![](../../../../../../assets/shape-dropshadow.png){width="128px"}

<b>Entrée :</b> Filtres > Effets

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Applique l’effet bien connu « Ombre portée » d’un autre logiciel de traitement d’image 2D, sur un masque noir et blanc d’entrée (pour la version en niveaux de gris) ou sur une image avec transparence (pour la version en couleurs).

Il diffère de l&#39;effet [Ombres](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/shadows-filter-node/shadows-filter-node.md) en ce sens qu&#39;il renvoie des images avec une transparence totale appliquée, ce qui donne un effet plus complet similaire à ce que vous attendriez dans d&#39;autres logiciels.

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Angle</b> <i>0.0 - 1.0</i> | Angle d’incidence de la (fausse) lumière. |
| <b>Distance</b> <i>-0.5 - 0.5</i> | Distance à laquelle l’ombre s’étend jusqu’à la forme ou s’en éloigne. |
| <b>Taille</b> <i>0.0 - 1.0</i> | Contrôle le flou/les zones floues de l’ombre. |
| <b>Répartition</b> <i>0.0 - 1.0</i> | L’option Découpe/Seuil de l’effet de flou étend davantage l’ombre. |
| <b>Opacité</b> <i>0.0 - 1.0</i> | Opacité de fusion pour l’effet d’ombre. |
| <b>(Ombre) Couleur</b> <i>(valeur de couleur)</i> | Teinte de couleur à appliquer à l’ombre. |
| <b>Couleur du masque</b> <i>(valeur de couleur) (version en niveaux de gris uniquement)</i> | Couleur unie à utiliser pour la sortie du mappage de transparence. |
| <b>L&#39;Entrée Est Prémultipliée</b> <i>Faux/Vrai (Version Couleur Uniquement)</i> | Indique si l&#39;entrée doit être considérée comme prémultipliée. |
| <b>Prémultiplier La Sortie</b> <i>Faux/Vrai</i> | Indique si la sortie doit être prémultipliée. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/dropshadowex.png" />
        </td>
    </tr>
</table>
