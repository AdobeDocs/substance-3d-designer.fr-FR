---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/dripping-rust.html"
breadcrumb-title: ''
description: Utilisez le nœud Rouille d'égouttage pour générer des motifs d'égouttage de rouille en fonction de la géométrie du maillage et de la direction de la gravité.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Dripping Rust
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Rouille goutte-à-goutte
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2c331b568074714ea71231410f997f965e2bcdaa
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 7%

---


# Rouille goutte-à-goutte

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](dripping-rust.resources/dripping-rust.png){width="128px"}

<b>Entrée :</b> Générateurs basés sur le Maillage > Générateurs de masque

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Génère une image en noir et masque blanc en fonction des maps bakées et des paramètres utilisateur. Similaire à [Masques adaptables](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) dans [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Ce masque représente des flocons de rouille et des taches, avec des fuites qui s&#39;écoulent.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Courbure</b> <i>Entrée en niveaux de gris</i> | Mappage baké ou généré pour faciliter le placement des rouilles. |
| <b>Ambient occlusion</b> <i>Entrée en niveaux de gris</i> | Mappage baké ou généré pour faciliter le placement des rouilles. |
| <b>Position</b> <i>Entrée en niveaux de gris</i> | Carte bakée ou générée pour les directions de goutte à goutte. |
| <b>Masquer (facultatif)</b> <i>Entrée en niveaux de gris</i> | Emplacement de masque utilisé pour masquer les effets du nœud. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Répartition des Rouilles</b> <i>0.0 - 1.0</i> | Contrôle principal de la quantité de rouille. |
| <b>Contraste de Rouille</b> <i>0.0 - 1.0</i> | Définit la quantité de contraste dans les taches de rouille générées (n’affecte pas les gouttes). |
| <b>Répartition du Smoothness</b> <i>0.0 - 1.0</i> | Quantité d’effet de flou/maculage à appliquer aux taches de rouille. |
| <b>Intensité des gouttes</b> <i>0.0 - 1.0</i> | Définit la force et la longueur des gouttes à partir des taches. |
| <b>Smoothness gouttes</b> <i>0.0 - 1.0</i> | Niveau de flou et de lissage à appliquer aux gouttes. |
| <b>Quantité D&#39;Échantillons Goutte</b> <i>0 - 32</i> | Définit le niveau de qualité (étapes) de l’effet gouttes. A un léger effet sur la vitesse. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="dripping-rust.resources/dripping-rust-ex3.gif" />
        </td>
    </tr>
</table>
