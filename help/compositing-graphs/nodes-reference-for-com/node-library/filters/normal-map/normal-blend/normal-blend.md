---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-blend.html"
breadcrumb-title: ''
description: Utilisez le nœud Fusion normale pour fusionner des maps normal afin de créer des transitions lisses entre les détails d'une surface.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Dégradé normal
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 3%

---


# Dégradé normal

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](normal-blend.resources/normal-blend-01.png){width="128px"}

<b>Entrée :</b> Filtres > Map normal

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

La Fusion normale vous permet de fusionner deux mappages normaux avec un masque facultatif, tout en vous assurant que toutes les valeurs restent normalisées. Il ne diffère pas beaucoup d&#39;un [nœud de Fusion atomique](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md), mais a ajouté des calculs internes pour Normalmaps.

La Fusion des normales n&#39;est pas destinée à la combinaison (superposition) de cartes normales, où la carte du haut ajoute des détails à la carte du bas. Pour cela, utilisez plutôt [Combinaison normale](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-combine/normal-combine.md).

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>NormalFG</b> <i>Entrée couleur</i> | Mappage normal de premier plan/haut. |
| <b>NormalBG</b> <i>Entrée couleur</i> | Background/Bottom Normalmap. |
| <b>Masquer</b> <i>Entrée en niveaux de gris</i> | Emplacement de masque utilisé pour masquer les effets du nœud. Peut être basculé avec le paramètre « Utiliser le masque ». |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Opacité</b> <i>0.0 - 1.0</i> | Opacité de fusion entre le premier plan et l’arrière-plan |
| <b>Utiliser le masque</b> <i>Faux/Vrai</i> | Active ou désactive l&#39;utilisation de la carte de masque. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="normal-blend.resources/normal-blend-02.gif" /><br><i>(.gif format introduit le dithering dans l'exemple, les résultats dans l'application sont lisses)</i>
        </td>
    </tr>
</table>
