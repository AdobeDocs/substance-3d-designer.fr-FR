---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/non-uniform-blur.html"
breadcrumb-title: ''
description: Utilisez le nœud Flou non uniforme pour appliquer un flou d’intensités différentes dans les directions X et Y pour des effets anisotropes.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Non Uniform Blur
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Flou non uniforme
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 9%

---


# Flou non uniforme

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](non-uniform-blur.resources/non-uniform-blur-01.png){width="128px"}

![](non-uniform-blur.resources/non-uniform-blur-02.png){width="128px"}

<b>Entrée :</b> Filtres > Flous

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Applique un flou de haute qualité dont l’intensité est déterminée par un masque de saisie. Les options permettent d’ajouter les options Anisotropie et Assymétrie.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Carte du flou</b> <i>Entrée en niveaux de gris</i> | Mappage de masque pour piloter la force de l&#39;effet. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Intensité</b> <i>0.0 - 50.0</i> | Force maximale d’application du flou. Masqué par la courbe de transfert du flou. Ce paramètre n’aura donc aucun effet sur les zones noires de cette courbe. |
| <b>Anisotropie</b> <i>0.0 - 1.0</i> | Ajoute éventuellement une directivité à l’effet de flou. Piloté par le paramètre Angle. |
| <b>Asymétrie</b> <i>0.0 - 1.0</i> | Ajoute éventuellement un biais à l’échantillonnage. Piloté par le paramètre Angle. |
| <b>Angle</b> <i>0.0 - 1.0</i> | Angle pour définir la directivité et le biais d’échantillonnage. |
| <b>Exemples</b> <i>1 - 16</i> | Quantité d’échantillons, détermine la qualité. Multiplié par le nombre de lames. |
| <b>Lames</b> <i>1 - 9</i> | Quantité de secteurs d&#39;échantillonnage, détermine la qualité. Multiplié par la quantité d&#39;échantillons. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="non-uniform-blur.resources/non-uniform-blur-03.gif" /><br><i>L'exemple ci-dessous est généré par une rampe de dégradé (à 90 degrés) dans l'emplacement Courbe de transfert de flou.</i>
        </td>
    </tr>
</table>
