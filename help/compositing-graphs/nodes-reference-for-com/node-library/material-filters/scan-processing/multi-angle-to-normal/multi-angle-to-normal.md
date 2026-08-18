---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/multi-angle-to-normal.html"
breadcrumb-title: ''
description: Utilisez le nœud Plusieurs angles vers Normal pour générer des cartes de normales à partir d'images numérisées sous plusieurs angles afin d'obtenir des détails de surface précis.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Multi-Angle to Normal
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Angle multiple à normal
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 1%

---


# Angle multiple à normal

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/multi-angle-to-normal.png){width="128px"}

## Angle multiple à normal

**Entrée :** *Filtres de matière/Traitement de la numérisation*

**Intermédiaire**

</td>
<td style="border: 0;" valign="top">

## Description

Ce nœud construit une carte normale à partir d&#39;un ensemble de photographies/numérisations effectuées dans différentes conditions d&#39;éclairage. Elle permet une conversion Normalmap beaucoup plus précise que lorsque vous tentez d&#39;extraire des normales à partir d&#39;une seule image d&#39;albédo.

Il est plus compliqué que l&#39;Albédo à [plusieurs angles](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md), car il nécessite l&#39;utilisation d&#39;angles d&#39;éclairage définis et précis pour vos entrées. L&#39;angle d&#39;éclairage de chaque échantillon doit être espacé uniformément et les échantillons doivent être saisis dans l&#39;ordre. Ainsi, pour trois échantillons, les angles d&#39;éclairage doivent être pris à : 0, 120, 240 - ou tout décalage uniforme de celui-ci (comme 90, 210, 330).

>[!NOTE]
>
> Voir [Multi-Angle vers l&#39;Albédo](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md) pour la version albédo de ce nœud. Si vous souhaitez prétraiter vos entrées, [Multi-Color Equalizer](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-color-equalizer/multi-color-equalizer.md), [Multi-recadrage](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-crop/multi-crop.md) et [Multi-correctif de clone](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-clone-patch/multi-clone-patch.md) peuvent être utiles, car ils sont destinés à être associés à ces nœuds.

## Paramètres

### Entrées

* **Entrée 1-8** : *Entrée Couleur*

### Paramètres

* **Format normal** : *DirectX, OpenGL*\
  Bascule entre différents formats de mappage normal (inverse la couche verte).
* **Quantité d’échantillons** : *2 - 8* définit la quantité d’échantillons (entrées) à traiter.
* **Intensité** : *0,0 - 1,0* définit l&#39;intensité de la carte normale.
* **Premier angle d&#39;éclairage échantillon** : *0.0 - 360.0* définit la direction de l&#39;angle d&#39;éclairage de la première entrée.
* **Angle du prochain échantillon de lumière** : *dans le sens inverse des aiguilles d&#39;une montre* Définit la direction vers laquelle l&#39;éclairage de l&#39;échantillon suivant se déplace.

## Exemples d’images

|  |
| --- |
| Aucune image n&#39;est jointe à cette page. |

</td>
</tr>
</table>
