---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/highpass.html"
breadcrumb-title: ''
description: Utilisez le nœud Passe-haut pour extraire les détails haute fréquence des textures de création des effets de netteté et d’amélioration des détails.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Highpass
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Passe-haut
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 4%

---


# Passe-haut

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](highpass.resources/high-pass-greyscale.png){width="128px"}

![](highpass.resources/high-pass.png){width="128px"}

<b>Entrée :</b> Filtres > Réglages

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Effectue un filtre passe-haut, disponible en couleur ainsi que dans une version en niveaux de gris. Similaire à l’action Photoshop portant le même nom.\
Utile pour supprimer les grandes différences de Luminance dans les images, par exemple lors du nettoyage de textures pour la répétition.

Important : assurez-vous d’utiliser la version appropriée pour vos commentaires. Utilisez « Passe-haut » pour les entrées Couleur et « Niveaux de gris passe-haut » pour les entrées Niveaux de gris.

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Rayon</b> <i>0.0 - 64.0</i> | Rayon du filtre : un petit rayon supprime les petites différences, un rayon plus grand supprime les grandes zones. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="highpass.resources/highpass.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="highpass.resources/highpass-example.png" />
        </td>
    </tr>
</table>
