---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/white-noise.html"
breadcrumb-title: ''
description: Utilisez le nœud Bruit blanc pour générer des motifs de bruit blanc afin de créer des variations de texture et des effets aléatoires.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > White noise
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Bruit blanc
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 5%

---


# Bruit blanc

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Bruit blanc - Icône](white-noise.resources/white-noise-01.png "Bruit blanc - Icône"){width="200px"}

<b>Entrée :</b> Générateurs de textures > Bruits

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Génère un bruit blanc à l’aide de l’une des trois méthodes ciblant différentes formes d’histogramme : uniforme, gaussien et triangulaire.

</td>
</tr>
</table>

<a name="outputs"></a>

## Sorties

|  |  |
|:---|:---|
| <b>Sortie</b> <i>Niveaux de gris</i> | Le bruit généré est une image bitmap en niveaux de gris. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Distribution de Bruits</b> <i>Nombre entier</i> | La méthode de répartition des ingrédients pour cibler une forme d’histogramme :<ul data-preserve-html="true"> <li data-preserve-html="true"><i>Uniforme :</i> histogramme plat.</li> <li data-preserve-html="true"><i>Gaussien :</i> histogramme représentant une distribution normale, semblable à une courbe en cloche.</li> <li data-preserve-html="true"><i>Triangle :</i> un histogramme triangulaire.</li> </ul> |
| <b>Désordre</b> <i>Flotter</i> | Déplace les ingrédients du bruit.    Cela peut être utilisé pour animer le bruit. |
| <b>Désorganiser la vitesse</b> <i>Flotter</i> | Ajuste la distance de displacement appliquée par le paramètre <b>Désordre</b>.    Cela permet de contrôler la vitesse du displacement lors de l’animation du bruit. |

## Exemples

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Bruit blanc - Exemple 1](white-noise.resources/white-noise-02.png "Bruit blanc - Exemple 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Bruit blanc - Exemple 2](white-noise.resources/white-noise-03.gif "Bruit blanc - Exemple 2"){zoomable="yes"}

</td>
</tr>
</table>
