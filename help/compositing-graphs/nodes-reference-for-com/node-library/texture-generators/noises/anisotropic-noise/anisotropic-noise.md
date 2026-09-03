---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/anisotropic-noise.html"
breadcrumb-title: ''
description: Utilisez le nœud Bruit anisotrope pour générer des motifs de bruit directionnel afin de créer des effets de texture anisotrope.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Anisotropic noise
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Bruit anisotrope
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 1%

---


# Bruit anisotrope

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Bruit anisotrope - Icône](anisotropic-noise.resources/anisotropic-noise-01.png "Bruit anisotrope - Icône"){width="200px"}

<b>Entrée :</b> Générateurs de textures > Bruits

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Une pile horizontale ou verticale de bandes de couleur aléatoire s&#39;estompant les unes dans les autres.

La quantité de bandes est réglable, de même que le smoothness de leurs transitions.

</td>
</tr>
</table>

## Sorties

|  |  |
|:---|:---|
| <b>Sortie</b> <i>Niveaux de gris</i> | Le bruit généré est une image bitmap en niveaux de gris. |

## Paramètres

|  |  |
|:---|:---|
| <b>X</b> <i>Nombre entier</i> | Quantité de bandes sur l&#39;axe X. |
| <b>Quantité Y</b> <i>Nombre entier</i> | Nombre de bandes sur l&#39;axe Y. |
| <b>Quantité Y par résolution</b> <i>Booléen</i> | Si la valeur est True, le nombre de bandes sur l&#39;axe Y sera égal à la taille de l&#39;image sur cet axe. |
| <b>Rotation</b> <i>Booléen</i> | Fait pivoter le bruit de 90 degrés. |
| <b>Smoothness</b> <i>Flotter</i> | La quantité de fondu entre les bandes, où 0 n&#39;est pas un fondu et 1 s&#39;estompe sur toute leur longueur. |
| <b>Interpolation de Smoothness</b> <i>Flotter</i> | La pondération des deux méthodes d&#39;interpolation appliquées pour fondre les bandes, où 0 est linéaire et 1 est gaussien. |
| <b>Désordre</b> <i>Flotter</i> | Déplace les ingrédients du bruit.   Cela peut être utilisé pour animer le bruit. |
| <b>Désorganiser la vitesse</b> <i>Flotter</i> | Ajuste la distance de displacement appliquée par le paramètre <b>Désordre</b>.   Cela permet de contrôler la vitesse du displacement lors de l’animation du bruit. |
| <b>Expansion non carrée</b> <i>Booléen</i> | Dans les images non carrées, la mosaïque générée reste carrée et étend la génération de bruit aux limites de l’image. |

## Exemples

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Bruit anisotrope - Exemple 1](anisotropic-noise.resources/anisotropic-noise-02.png "Bruit anisotrope - Exemple 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Bruit anisotrope - Exemple 2](anisotropic-noise.resources/anisotropic-noise-03.gif "Bruit anisotrope - Exemple 2"){zoomable="yes"}

</td>
</tr>
</table>
