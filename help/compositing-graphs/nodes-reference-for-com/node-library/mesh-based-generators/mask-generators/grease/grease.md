---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/grease.html"
breadcrumb-title: ''
description: Utilisez le nœud Graisse pour générer des masques d'accumulation de graisse en fonction de la géométrie du maillage et des zones de contact.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Grease
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Graisse
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 5%

---


# Graisse

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](grease.resources/grease-01.png){width="128px"}

<b>Entrée :</b> Générateurs basés sur le Maillage > Générateurs de masque

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Génère un masque noir et blanc en fonction des maps bakées et des paramètres utilisateur. Similaires aux [masques dynamiques](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) dans [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Ce masque est spécialement conçu pour les visages de personnages et d’autres zones spécifiques. Génère un masque de type peau-graisse sur les zones à faible thickness.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Thickness</b> <i>Entrée en niveaux de gris</i> | Placage de Thickness cuit sur lequel repose l’ensemble de l’effet. Obligatoire ! |
| <b>Bruit</b> <i>Entrée en niveaux de gris</i> | Carte Bruit en option pour remplacer l’usure/salissures de la graisse. |
| <b>Masquer (facultatif)</b> <i>Entrée en niveaux de gris</i> | Emplacement de masque utilisé pour masquer les effets du nœud. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Niveau</b> <i>0.0 - 1.0</i> | Définit la quantité totale d’effet à afficher. |
| <b>Contraste</b> <i>0.0 - 1.0</i> | Règle le contraste du résultat. |
| <b>Seuil de Thickness</b> <i>0.0 - 1.0</i> | Définit le thickness minimum auquel l’effet doit apparaître. Tout aussi important que le niveau, ajustez-le en fonction de votre carte de Thickness. |
| <b>Remplacer le Bruit</b> <i>Faux/Vrai</i> | Définir pour remplacer la carte d&#39;usure/salissures de graisse interne avec un emplacement d&#39;entrée personnalisé. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="grease.resources/grease-02.gif" />
        </td>
    </tr>
</table>
