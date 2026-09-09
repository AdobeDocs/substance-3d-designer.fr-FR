---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/glow.html"
breadcrumb-title: ''
description: Utilisez le nœud Lueur pour ajouter des effets de lueur aux textures afin de créer des états de matériau lumineux et émissifs.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Glow
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Lueur
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2ea5b90ca7a4cbcd0b0049b156e8ded334aa0ceb
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 5%

---


# Lueur

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](glow.resources/glow-greyscale.png){width="128px"}

![](glow.resources/glow-3.png){width="128px"}

<b>Entrée :</b> Filtres > Effets

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Applique un effet de type « Lueur externe », comme dans d’autres logiciels de retouche d’images courants. Ajoute essentiellement un contour en dégradé de fondu autour de l’entrée.

Gardez à l’esprit qu’il ne s’agit pas d’une fonctionnalité prévue pour les images avec des couches Alpha, comme vous pourriez vous y attendre. Même la version en couleurs ne prévoit que des masques binaires, noir et blanc en entrée ; elle ne permet d’utiliser qu’une lueur colorée. Si vous recherchez une version qui fonctionne sur les images avec transparence, consultez [Shape Glow](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/shape-glow/shape-glow.md).

Important : assurez-vous d’utiliser la version appropriée pour vos commentaires. Utilisez Lueur pour les entrées Couleur ou Lueur en niveaux de gris pour les entrées Niveaux de gris.

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Quantité de lueur</b> <i>0.0 - 1.0</i> | Opacité globale de l’effet Rayonnement. |
| <b>Effacer la quantité</b> <i>0.0 - 1.0</i> | Seuil indiquant quand il faut supprimer l’effet de lueur. Utile pour les zones semi-transparentes. |
| <b>Taille de la lueur</b> <i>0.0 - 20.0</i> | Détermine l’étendue de l’effet de lueur. |
| <b>Couleur de lueur</b> <i>(valeur de couleur) (version de couleur uniquement)</i> | Définit la couleur de l’effet de lueur. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="glow.resources/glow-ex.png" />
        </td>
    </tr>
</table>
