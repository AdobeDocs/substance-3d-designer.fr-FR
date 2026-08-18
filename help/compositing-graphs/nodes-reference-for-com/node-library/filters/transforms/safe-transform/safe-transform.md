---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/safe-transform.html"
breadcrumb-title: ''
description: Utilisez le nœud Transformation sécurisée pour appliquer des transformations tout en préservant les limites de la texture et en évitant les artefacts.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Safe Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Transformation sécurisée
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 1%

---


# Transformation sécurisée

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/safe-transform.png)

![](../../../../../../assets/safe-transform-grayscale.png)

## Transformation sécurisée (niveaux de gris)

**Entrée :** *Filtres/Transformations*

**Intermédiaire**

</td>
<td style="border: 0;" valign="top">

## Description

Version sans mosaïque de [Transformation 2D](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md). Permet de mettre à l’échelle, de faire pivoter et de décaler sans casser la mosaïque et sans perdre les détails des pixels (perte de netteté) en raison de petits décalages et rotations.

Utile pour transformer le bruit lorsque un contrôle maximal ou une netteté parfaite sont requis.

## Paramètres

* **Mosaïque** : *1 - 16* réduit l&#39;entrée en la juxtaposant.
* **Mode de décalage** : *manuel, aléatoire* bascule vers un décalage aléatoire au lieu d&#39;un décalage défini manuellement.
* **Décalage** : *0,0 - 1,0*\
  Déplace ou traduit le résultat. S’assure que les pixels sont accrochés et non interpolés.
* **Rotation** : *0.0 - 1.0* Fait pivoter l&#39;entrée le long de l&#39;angle.
* **Rotation admissible de la vignette** : *Faux/Vrai* détermine le comportement de la rotation, s&#39;il doit s&#39;aligner sur des valeurs admissibles qui ne floutent aucun pixel.
* **Symétrie** : *aucune, X, Y, X+Y*
* **Couleur d&#39;arrière-plan** : *(valeur de couleur) (version de couleur uniquement)*
* **Mode Mipmap** : *Automatique, manuel* Détermine le mode mipmap. Le réglage manuel permet d’obtenir des résultats plus nets.
* **Niveau du mipmap** : *0 - 10* Lorsque le mode Mipmap est défini sur Manuel, vous pouvez choisir un autre Mipmap.

## Exemples d’images

|  |
| --- |
| Aucune image n&#39;est jointe à cette page. |

</td>
</tr>
</table>
