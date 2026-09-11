---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/shape-glow.html"
breadcrumb-title: ''
description: Utilisez le nœud Shape Glow pour ajouter des effets de lueur aux formes et aux textures afin de créer des effets visuels lumineux et atmosphériques.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Shape Glow
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Shape Glow
user-guide-description: ''
user-guide-title: ''
source-git-commit: 67f8f59bf50387b87e9009b042f269208c665c65
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 4%

---


# Shape Glow

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](shape-glow.resources/shape-glow-grayscale.png){width="128px"}

![](shape-glow.resources/shape-glow.png){width="128px"}

<b>Entrée :</b> Filtres > Effets

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Crée une lueur diffuse autour d’un masque d’entrée (pour la version en niveaux de gris) ou d’une forme avec un canal Alpha (pour la version en couleurs). Comparé à [Glow](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/glow/glow.md), ce réglage est plus proche de celui d&#39;autres logiciels de retouche d&#39;images 2D, car il s&#39;agit d&#39;un effet plus complet avec plus de commandes.

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Mode</b> <i>Souple, Précis</i> | Bascule entre deux modes de précision. |
| <b>Largeur</b> <i>-1.0 - 1.0</i> | Détermine l’étendue de la lueur. |
| <b>Répartition</b> <i>0.0 - 1.0</i> | L’option Découpe/Seuil de l’effet de flou donne l’impression que la lueur est solide près de la forme. |
| <b>Opacité</b> <i>0.0 - 1.0</i> | Opacité de fusion pour l’effet Rayonnement. |
| <b>(Ombre) Couleur</b> <i>(valeur de couleur)</i> | Teinte de couleur à appliquer au rayonnement. |
| <b>Couleur du masque</b> <i>(valeur de couleur) (version en niveaux de gris uniquement)</i> | Couleur unie à utiliser pour la sortie du mappage de transparence. |
| <b>L&#39;Entrée Est Prémultipliée</b> <i>Faux/Vrai (Version Couleur Uniquement)</i> | Indique si l&#39;entrée doit être considérée comme prémultipliée. |
| <b>Prémultiplier La Sortie</b> <i>Faux/Vrai</i> | Indique si la sortie doit être prémultipliée. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="shape-glow.resources/shapeglow-ex.png" />
        </td>
    </tr>
</table>
