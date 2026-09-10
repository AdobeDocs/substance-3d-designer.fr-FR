---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/utilities-mesh-based-generators/material-selector.html"
breadcrumb-title: ''
description: Utilisez le nœud Sélecteur de Matériau pour sélectionner des matériaux en fonction des données de maillage afin de créer des effets de texture à matériaux multiples.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Utilities (Mesh Based Generators) > Material Selector
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Sélecteur de matériau
user-guide-description: ''
user-guide-title: ''
source-git-commit: 1ea5f4e048a3b4591bf71d9b18707837dac1bf6f
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 5%

---


# Sélecteur de matériau

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](material-selector.resources/material-selector.png){width="128px"}

<b>Entrée :</b> Générateurs basés sur le Maillage > Utilitaires

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Convertit un Map id de couleur en binaire, noir et masque blanc. Permet de fusionner et de combiner différentes couleurs dans un seul masque.

C&#39;est pratique si vous ne voulez pas utiliser la [Fusion multi-Matériaux](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/multi-material-blend/multi-material-blend.md) et que vous préférez l&#39;utiliser manuellement, ou si vous voulez l&#39;utiliser manuellement à d&#39;autres endroits.

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Matériaux</b> <i>1 - 16</i> | Définit le nombre de matériaux pour lesquels la combinaison est activée. |
| <b>Activer les #1-16 de Matériau</b> <i>Faux/Vrai</i> | Active/désactive la fusion et la combinaison de couleurs dans le masque de sortie final. Peut être activé pour autant de couleurs que vous souhaitez combiner. |
| <b>Matériau #1-16</b> <i>(valeur de couleur)</i> | Sélecteur de couleurs pour la couleur des matériaux à convertir en noir et blanc. |
| <b>Paramètres du sélecteur de couleurs</b> | Modifie la fusion et la conversion de la couleur en noir et blanc. |
| <b>Flou</b> <i>0.01 - 1.0</i> | Degré de fusion avec les couleurs voisines. |
| <b>Remplissage</b> <i>0.0 - 1.0</i> | Netteté de la transition, comme Contraste. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="material-selector.resources/matselector-ex.png" />
        </td>
    </tr>
</table>
