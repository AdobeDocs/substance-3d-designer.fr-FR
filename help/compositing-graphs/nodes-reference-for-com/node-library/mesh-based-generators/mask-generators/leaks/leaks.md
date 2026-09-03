---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/leaks.html"
breadcrumb-title: ''
description: Utilisez le nœud Fuites pour générer des motifs de fuite basés sur la géométrie du maillage afin de créer des taches d'eau et des effets de fluide.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Leaks
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Fuites
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '333'
ht-degree: 3%

---


# Fuites

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](leaks.resources/leaks-01.png){width="128px"}

<b>Entrée :</b> Générateurs basés sur le Maillage > Générateurs de masque

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Génère un masque noir et blanc en fonction des maps bakées et des paramètres utilisateur. Similaires aux [masques dynamiques](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) dans [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Ce nœud représente des stries de dirt et de crasse qui fuient à partir des arêtes vives. Comme les traînées sont générées avec la position cuite, elles s&#39;étendent toujours vers le bas.

Assurez-vous de modifier le masque de variation : comme il détermine le placement des traînées, il peut avoir une influence beaucoup plus grande qu’avec d’autres générateurs de masques.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Position</b> <i>Entrée en niveaux de gris</i> | Carte de position ancrée, utilisée pour l’orientation des stries. Obligatoire ! |
| <b>Courbure</b> <i>Entrée en niveaux de gris</i> | Map bakée utilisée pour la mise en place des stries. Obligatoire ! |
| <b>Occlusion ambiante</b> <i>Entrée en niveaux de gris</i> | Map bakée utilisée pour les effets internes et le masquage. Recommandé, mais vous pouvez utiliser un blanc plat à la place. |
| <b>Espace monde normal</b> <i>Entrée couleur</i> | Carte normale de l&#39;espace mondial au four, utilisée pour la direction des stries. Obligatoire ! |
| <b>Masque de variation</b> <i>Entrée en niveaux de gris</i> | Masque de variation facultatif, activez en définissant le remplacement sur True. |
| <b>Masquer (facultatif)</b> <i>Entrée en niveaux de gris</i> | Emplacement de masque utilisé pour masquer les effets du nœud. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Niveau</b> <i>0.0 - 1.0</i> | Niveau total du résultat. Révèle progressivement l&#39;effet, affecte également la longueur. Doit être réglé assez haut pour obtenir de longs gouttes. |
| <b>Contraste</b> <i>0.0 - 1.0</i> | Règle le contraste du résultat. |
| <b>Variation</b> <i>0.0 - 1.0</i> | Définit le degré de variation à grande échelle utilisé pour masquer les stries. La définition de cette valeur sur 0 entraîne des traînées uniformes complètes, évitez-la. |
| <b>Longueur</b> <i>0.0 - 8.0</i> | La longueur de la strie s&#39;écoule. Si vous définissez une valeur trop élevée à petite échelle, des pas visibles apparaissent. Jouez aussi avec le niveau. |
| <b>Occlusion</b> <i>X, Y, Z, Aucun</i> | Définit la direction dans laquelle l’AO doit intervenir. |
| <b>Remplacer le masque de variation</b> <i>Faux/Vrai</i> | Permet de remplacer le masque de variation par un emplacement d’entrée personnalisé. L’utilisation de masques plus clairsemés ou plus denses peut être intéressante et constitue un bon moyen de contrôler les gouttes. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="leaks.resources/leaks-02.gif" />
        </td>
    </tr>
</table>
