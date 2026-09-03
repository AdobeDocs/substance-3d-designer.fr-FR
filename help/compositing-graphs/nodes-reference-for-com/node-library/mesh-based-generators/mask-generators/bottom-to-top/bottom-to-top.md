---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/bottom-to-top.html"
breadcrumb-title: ''
description: Utilisez le nœud De bas en haut pour générer des masques de dégradé de bas en haut en fonction de la position universelle par maillage.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Bottom To Top
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: De bas en haut
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 5%

---


# De bas en haut

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](bottom-to-top.resources/bottom-to-top-01.png){width="128px"}

<b>Entrée :</b> Générateurs basés sur le Maillage > Générateurs de masque

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Génère un masque noir et blanc en fonction des maps bakées et des paramètres utilisateur. Similaires aux [masques dynamiques](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/features/smart-materials-and-masks) dans [Painter](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/home).

Cela génère une transition du blanc vers le noir du bas vers le haut d&#39;un modèle, ce qui est utile pour effectuer des réductions et des sélections basées sur la géométrie.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Position</b> <i>Entrée couleur</i> | Mappage de position baké. Obligatoire ! |
| <b>Rugosité</b> <i>Entrée en niveaux de gris</i> | Cela n’a rien à voir avec la rugosité PBR, mais il s’agit d’une carte de variation (facultative) pour rompre la transition. N’apparaît que lorsque la Rugosité est définie sur une valeur supérieure à 0. |
| <b>Masquer (facultatif)</b> <i>Entrée en niveaux de gris</i> | Emplacement de masque utilisé pour masquer les effets du nœud. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Niveau</b> <i>0.0 - 1.0</i> | Déplace le niveau moyen du résultat entre noir et blanc, comme un réglage de la luminosité. |
| <b>Contraste</b> <i>0.0 - 1.0</i> | Règle le contraste de la transition. |
| <b>Variation_Rugosité</b> <i>0.0 - 1.0</i> | Détermine la quantité de mappage de Rugosité à fusionner pour la variation. Augmenter cette valeur sur 0 révèle l&#39;emplacement de mappage. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="bottom-to-top.resources/bottom-to-top-02.gif" />
        </td>
    </tr>
</table>
