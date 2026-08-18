---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/anisotropic-blur.html"
breadcrumb-title: ''
description: Utilisez le nœud Flou anisotrope pour appliquer des effets de flou directionnel afin de créer un flou directionnel et des traînées.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Anisotropic Blur
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Flou anisotrope
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 1%

---


# Flou anisotrope

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/anisotropic-blur-grayscale.png){width="128px"}

![](../../../../../../assets/anisotropic-blur.png){width="128px"}

## Flou anisotrope (Niveaux de gris)

**Entrée :** *Filtres/Flous*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Description

Effectue un [flou directionnel](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/directional-blur/directional-blur.md) de haute qualité, avec quelques paramètres pour personnaliser l&#39;apparence. Également appelé « flou de mouvement ».

Important : assurez-vous d’utiliser la version appropriée pour vos commentaires. Utilisez « Flou anisotrope » pour les valeurs Couleur ou « Niveaux de gris anisotrope » pour les valeurs Niveaux de gris.

## Paramètres

* **Intensité** : *0,0 - 16,0* Intensité (rayon) du flou. Plus cette valeur est élevée, plus le flou sera important.
* **Anisotropie** : *0.0 - 1.0* Directionnalité du flou. La définition de ce paramètre sur 0,0 revient à appliquer un flou normal.
* **Angle** : *0,0 - 1,0* définit l’angle de la direction du flou.
* **Qualité** :*0 - 1* bascule entre un flou [box](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blur/blur.md) et un flou HQ en interne. La vitesse change pour la qualité.

## Exemples d’images

![](../../../../../../assets/aniso-blur-example.gif)

</td>
</tr>
</table>
