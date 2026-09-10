---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/dust.html"
breadcrumb-title: ''
description: Utilisez le nœud Dust pour générer des masques d’accumulation de dusts en fonction de la géométrie du maillage afin de créer des effets de dust et de crasse réalistes.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Dust
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Dust
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2c331b568074714ea71231410f997f965e2bcdaa
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 5%

---


# Dust

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](dust.resources/dust.png){width="128px"}

<b>Entrée :</b> Générateurs basés sur le Maillage > Générateurs de masque

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Génère un masque noir et blanc en fonction des maps bakées et des paramètres utilisateur. Similaires aux [masques dynamiques](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) dans [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Ce masque représente le dust accumulé dans les zones obstruées, les zones basses, ainsi que seulement dans les zones qui prennent face vers le haut. Nécessite un AO et des Normales des espaces monde bakés appropriés pour fonctionner.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Occlusion ambiante</b> <i>Entrée en niveaux de gris</i> | Map bakée utilisée pour le placement du dust. Obligatoire ! |
| <b>Espace universel normal</b> <i>Entrée couleur</i> | Map bakée utilisée pour le placement du dust. Obligatoire ! |
| <b>Bruit</b> <i>Entrée en niveaux de gris</i> | Mappage de dust personnalisé (facultatif), s’affiche uniquement lorsque l’option Remplacer le Bruit est définie sur Vrai. |
| <b>Masquer (facultatif)</b> <i>Entrée en niveaux de gris</i> | Emplacement de masque utilisé pour masquer les effets du nœud. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Niveau</b> <i>0.0 - 1.0</i> | Définit le montant total du dust. |
| <b>Contraste</b> <i>0.0 - 1.0</i> | Règle le contraste du dust. |
| <b>Montant de l&#39;Occlusion</b> <i>0.0 - 1.0</i> | Définit l’influence de l’AO ; plus de dust apparaîtra dans les zones occultées. |
| <b>Opacité du Bruit</b> <i>0.0 - 1.0</i> | Définit la quantité de bruit visible dans les zones poussiéreuses. |
| <b>Remplacer le Bruit</b> <i>Faux/Vrai</i> | Défini pour utiliser l’entrée de mappage de dust personnalisé. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="dust.resources/dust-ex.gif" />
        </td>
    </tr>
</table>
