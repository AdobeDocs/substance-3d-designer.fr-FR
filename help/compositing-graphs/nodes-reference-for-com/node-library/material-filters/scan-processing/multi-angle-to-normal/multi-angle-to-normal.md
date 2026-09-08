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
source-git-commit: ca90755a159a7e0297bb26d1e3522b0cfeb6f2ac
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 3%

---


# Angle multiple à normal

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/multi-angle-to-normal.png){width="128px"}

<b>Entrée :</b> Filtres de matériau > Traitement des numérisations

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Ce nœud construit une carte normale à partir d&#39;un ensemble de photographies/numérisations effectuées dans différentes conditions d&#39;éclairage. Elle permet une conversion Normalmap beaucoup plus précise que lorsque vous tentez d&#39;extraire des normales à partir d&#39;une seule image d&#39;albédo.

Il est plus compliqué que l&#39;Albédo à [plusieurs angles](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md), car il nécessite l&#39;utilisation d&#39;angles d&#39;éclairage définis et précis pour vos entrées. L&#39;angle d&#39;éclairage de chaque échantillon doit être espacé uniformément et les échantillons doivent être saisis dans l&#39;ordre. Ainsi, pour trois échantillons, les angles d&#39;éclairage doivent être pris à : 0, 120, 240 - ou tout décalage uniforme de celui-ci (comme 90, 210, 330).

>[!NOTE]
>
> Voir [Multi-Angle vers l&#39;Albédo](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md) pour la version albédo de ce nœud. Si vous souhaitez prétraiter vos entrées, [Multi-Color Equalizer](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-color-equalizer/multi-color-equalizer.md), [Multi-recadrage](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-crop/multi-crop.md) et [Multi-correctif de clone](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-clone-patch/multi-clone-patch.md) peuvent être utiles, car ils sont destinés à être associés à ces nœuds.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Entrée 1-8</b> <i>Entrée couleur</i> |  |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Format normal</b> <i>DirectX, OpenGL</i> | Bascule entre différents formats de mappage normal (inverse la couche verte). |
| <b>Quantité D&#39;Échantillons</b> <i>2 - 8</i> | Définit la quantité d’échantillons (entrées) à traiter. |
| <b>Intensité</b> <i>0.0 - 1.0</i> | Définit l’intensité de la texture Normale. |
| <b>Premier angle d&#39;échantillonnage de la lumière</b> <i>0.0 - 360.0</i> | Définit la direction de l’angle d’éclairage de la première entrée. |
| <b>Angle d&#39;éclairage de l&#39;échantillon suivant</b> <i>Dans le sens inverse des aiguilles d&#39;une montre</i> | Définit la direction dans laquelle se déplace l’éclairage dans l’échantillon suivant. |
