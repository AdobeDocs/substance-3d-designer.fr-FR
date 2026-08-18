---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/slope-blur.html"
breadcrumb-title: ''
description: Utilisez le nœud Flou de Pente pour appliquer des effets de flou directionnel en fonction des pentes de courbe d’height pour créer un flou directionnel.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Slope Blur
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Flou de pente
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 1%

---


# Flou de pente

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/slope-blur.png){width="128px"}

![](../../../../../../assets/slope-blur-grayscale.png){width="128px"}

## Flou de pente (niveaux de gris)

**Entrée :** *Filtres/Flous*

**Intermédiaire**

</td>
<td style="border: 0;" valign="top">

## Description

Effectue un flou avancé de haute qualité lorsque l’Anisotropie/la direction est pilotée par une « carte de Pente » en niveaux de gris. Imaginez-le comme l&#39;effet Flou de Pente suivant les pentes de votre carte de Pente comme s&#39;il s&#39;agissait d&#39;une carte de hauteur, similaire à la [Déformation directionnelle](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/directional-warp/directional-warp.md) (sur laquelle il est basé en interne).

Il s’agit de l’un des flous les plus intéressants et puissants de Designer. Il peut être utilisé pour obtenir des effets très intéressants et inattendus, tels que l&#39;écaillage et l&#39;altération des bords ou le maculage et la fuite de dirt ou de rouille.

Important : assurez-vous d’utiliser la version appropriée pour vos commentaires. Utilisez « Flou de Pente » pour les entrées Couleur ou « Flou de Pente en niveaux de gris » pour les entrées Niveaux de gris.

## Paramètres

### Entrées

* **Pente** : *Pente de l&#39;entrée en niveaux de gris* pour déterminer l&#39;angle de l&#39;anisotropie. Idéalement, cette option doit contenir des dégradés en pente ; les transitions brutales et nettes ne fonctionneront pas bien !

### Paramètres

* **Échantillons** : *0 - 32* La quantité d’échantillons affecte la qualité au détriment de la vitesse.
* **Intensité** : *0,0 - 16,0*\
  Niveau ou intensité du flou.
* **Mode** : *Flou, Min, Max*|\
  Mode de fusion pour les passes de flou consécutives. Le « flou » se comporte davantage comme un [flou anisotrope](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/anisotropic-blur/anisotropic-blur.md) standard, tandis que Min « rongera » les zones existantes et Max « étalera » les zones blanches.

## Exemples d’images

![](../../../../../../assets/slopeblur01.gif)

![](../../../../../../assets/slopeblur02.gif)

</td>
</tr>
</table>
