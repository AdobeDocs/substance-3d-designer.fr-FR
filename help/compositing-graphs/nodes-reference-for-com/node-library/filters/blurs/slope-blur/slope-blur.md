---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/slope-blur.html"
breadcrumb-title: ''
description: Utilisez le nœud Flou de Pente pour appliquer des effets de flou directionnels en fonction des pentes de map height de création de flou directionnel.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Slope Blur
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Flou de pente
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5efb14d81ad72b1982785319e446d7eb318c9a03
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 3%

---


# Flou de pente

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](slope-blur.resources/slope-blur.png){width="128px"}

![](slope-blur.resources/slope-blur-grayscale.png){width="128px"}

<b>Entrée :</b> Filtres > Flous

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Effectue un flou avancé de haute qualité lorsque l’Anisotropie/la direction est pilotée par une « carte de Pente » en niveaux de gris. Imaginez-le comme l&#39;Effet de flou de Pente suivant les pentes de votre mappage de Pente comme s&#39;il s&#39;agissait d&#39;une carte de hauteur, similaire à la [Déformation directionnelle](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/directional-warp/directional-warp.md) (sur laquelle elle est basée en interne).

Il s’agit de l’un des flous les plus intéressants et puissants de Designer. Il peut être utilisé pour obtenir des effets très intéressants et inattendus, tels que l&#39;écaillage et l&#39;altération des bords ou le maculage et la fuite de dirt ou de rouille.

Important : assurez-vous d’utiliser la version appropriée pour vos commentaires. Utilisez « Flou de Pente » pour les entrées Couleur ou « Flou de Pente en niveaux de gris » pour les entrées Niveaux de gris.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Pente</b> <i>Entrée en niveaux de gris</i> | Carte de pente pour piloter l&#39;angle de l&#39;anisotropie. Idéalement, cette option doit contenir des dégradés en pente ; les transitions brutales et nettes ne fonctionneront pas bien ! |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Exemples</b> <i>0 - 32</i> | Quantité d&#39;échantillons, affecte la qualité au détriment de la vitesse. |
| <b>Intensité</b> <i>0.0 - 16.0</i> | Niveau de flou ou force. |
| <b>Mode</b> <i>Flou, Min, Max</i> | Mode de fusion pour les passes de flou consécutives. Le « flou » se comporte davantage comme un [flou anisotrope](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/anisotropic-blur/anisotropic-blur.md) standard, tandis que Min « rongera » les zones existantes et Max « étalera » les zones blanches. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="slope-blur.resources/slopeblur01.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="slope-blur.resources/slopeblur02.gif" />
        </td>
    </tr>
</table>
