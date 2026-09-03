---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/directional-warp.html"
breadcrumb-title: ''
description: Utilisez le nœud Déformation directionnelle pour appliquer une distorsion directionnelle aux textures afin de créer des effets de flux et de mouvement.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Directional warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Déformation directionnelle
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 9%

---


# Déformation directionnelle

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Noeud atomique : Déformation directionnelle](directional-warp.resources/directional-warp-01.png "Noeud atomique : Déformation directionnelle"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Déplace les pixels dans une direction spécifiée selon une map d’intensité, ce qui peut entraîner une déformation.

Déforme une entrée dans une direction définie par l’utilisateur, multipliée par une courbe d’intensité définie par l’utilisateur. Son fonctionnement est similaire à celui de la déformation, mais uniquement dans une direction spécifique.

</td>
</tr>
</table>

Le nœud Warp est un nœud assez simple mais utile qui sert de base pour d’autres effets plus avancés. Il existe des alternatives plus avancées, telles que d&#39;autres nœuds connexes intéressants, comme le [flou de Pente](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/slope-blur/slope-blur.md) et la [déformation vectorielle](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/vector-warp/vector-warp.md).

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">



</td>
<td width="83.33%" style="border: 0;" valign="top">



</td>
<td width="100.00%" style="border: 0;" valign="top">



</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Connecteurs de sortie

</td>
<td style="border: 0;" valign="top">

### Exemples

</td>
</tr>
</table>

## Paramètres

|  |  |
| --- | --- |
| <b>Intensité</b> *Flottant* | Définit l’intensité de la déformation. |
| <b>Angle de déformation</b> *Flottant* | Définit l’angle de l’effet de déformation, en nombre de tours. |
| <b>Mode de filtrage d&#39;entrée</b> *Booléen* | Détermine si le filtrage le plus proche ou bilinéaire est utilisé pour échantillonner l&#39;<b>entrée</b>. |
| <b>Décalage de la carte d&#39;intensité</b> *Flotter* | Cette valeur est soustraite des valeurs d&#39;image d&#39;<b>entrée d&#39;intensité</b>. |

## Connecteurs d’entrée

|  |  |
| --- | --- |
| <b>Entrée</b> *Niveaux de gris/Couleur* PRINCIPAL | Image d&#39;entrée en niveaux de gris ou en couleurs sur laquelle l’effet de déformation doit être appliqué. |
| <b>Entrée d&#39;intensité</b> *Niveaux de gris* | Image en niveaux de gris définissant la quantité de déformation à appliquer à l&#39;image <b>en entrée</b>. |

## Connecteurs de sortie

|  |  |
| --- | --- |
| <b>Sortie</b> *Niveaux de gris/Couleur* |  |

## Exemples

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Déformation Directionnelle - Exemple 1](directional-warp.resources/directional-warp-02.gif "Déformation Directionnelle - Exemple 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Déformation Directionnelle - Exemple 2](directional-warp.resources/directional-warp-03.gif "Déformation Directionnelle - Exemple 2"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Déformation Directionnelle - Exemple 3](directional-warp.resources/directional-warp-04.gif "Déformation Directionnelle - Exemple 3"){zoomable="yes"}

</td>
</tr>
</table>
