---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/multi-color-equalizer.html"
breadcrumb-title: ''
description: Utilisez le nœud Color Equalizer multiple pour égaliser les couleurs sur plusieurs couches de texture afin d’assurer un traitement cohérent des matériaux numérisés.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Multi Color Equalizer
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Color Equalizer multiple
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2c331b568074714ea71231410f997f965e2bcdaa
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 7%

---


# Color Equalizer multiple

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](multi-color-equalizer.resources/color-equalizer-multi.png){width="128px"}

<b>Entrée :</b> Filtres de matériau > Traitement des numérisations

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Il s&#39;agit de la version multi-entrée de [Color Equalizer](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/color-equalizer/color-equalizer.md). Il homogénéise les différences de couleur et supprime les teintes indésirables à une échelle sélectionnable par l’utilisateur. Il est principalement destiné à être utilisé avec des photos multi-angles, qui sont ensuite combinées avec [Multi-angle à l&#39;Albédo](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md) ou [Multi-angle à la normale](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-normal/multi-angle-to-normal.md).

>[!NOTE]
>
> Pour plus d&#39;informations, consultez le [Color Equalizer](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/color-equalizer/color-equalizer.md) d&#39;origine.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Entrée 1-8</b> <i>Entrée couleur</i> | Entrées multiples à traiter. |
| <b>Entrée de masque</b> <i>Entrée en niveaux de gris</i> | Emplacement de masque utilisé pour masquer les effets du nœud. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Nombre d&#39;entrées</b> <i>1 - 8</i> | Définit le nombre d’entrées à traiter en parallèle. |
| <b>Mosaïque d&#39;entrée</b> <i>Faux/Vrai</i> | Conserve éventuellement la répétition sur les contours. |
| <b>Rayon</b> <i>0.0 - 50.0</i> | Définit le rayon d’égalisation. Un rayon plus grand ne supprimera que les grandes différences de couleur. Cela nécessite de retoucher chaque image. |
| <b>Balance des tons clairs/foncés</b> <i>0.0 - 1.0</i> | Paramètre par biais pour laisser ou supprimer les teintes plus sombres. |
| <b>Variation de couleur personnalisée</b> <i>Faux/Vrai</i> | Permet de faire varier l’effet vers une couleur définie par l’utilisateur. |
| <b>Variation de couleur</b> | Uniquement actif si l’option Variation de couleur personnalisée est activée. Les paramètres vous permettent de sélectionner un décalage de teinte vers lequel effectuer l’égalisation. |
| <b>Teinte</b> <i>0.0 - 360.0</i> |  |
| <b>Chrominance</b> <i>0.0 - 1.0</i> |  |
| <b>Luminance</b> <i>0.0 - 1.0</i> |  |
| <b>Source du masque</b> <i>Aucun, Moyenne de l&#39;image, Paramètre de couleur, Entrée</i> | Définit si un masquage doit avoir lieu. Paramètre de couleur active des paramètres supplémentaires ci-dessous. L’entrée bascule sur une entrée de masque définie par l’utilisateur. |
| <b>Masquer</b> | Uniquement actif avec le masquage des paramètres de couleur. Contient des paramètres de masquage supplémentaires pour déterminer le masque en fonction de l&#39;image elle-même. Les paramètres ci-dessous vous permettent de convertir avec précision une teinte en un masque binaire sur lequel l’égalisation est appliquée. Notez que les effets du paramètre Rayon peuvent devenir beaucoup moins prononcés lors de l’utilisation de ces paramètres. |
| <b>Couleur</b> <i>(valeur de couleur)</i> |  |
| <b>Plage de teintes</b> <i>0.0 - 360.0</i> |  |
| <b>Gamme de chrominance</b> <i>0.0 - 1.0</i> |  |
| <b>Plage de luminance</b> <i>0.0 - 1.0</i> |  |
| <b>Flou</b> <i>0.0 - 2.0</i> |  |
| <b>Smoothness</b> <i>0.0 - 2.0</i> |  |
