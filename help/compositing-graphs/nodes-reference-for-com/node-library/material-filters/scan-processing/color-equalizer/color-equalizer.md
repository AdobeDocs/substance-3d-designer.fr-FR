---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/color-equalizer.html"
breadcrumb-title: ''
description: Utilisez le nœud Color Equalizer pour équilibrer les variations de couleur dans les matériaux numérisés afin d’obtenir une apparence de texture homogène.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Color Equalizer
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Color Equalizer
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '345'
ht-degree: 6%

---


# Color Equalizer

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](color-equalizer.resources/color-equalizer-01.png){width="128px"}

<b>Entrée :</b> Filtres de matériau > Traitement des numérisations

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Ce nœud fonctionne comme un [passe-haut](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/highpass/highpass.md) de haute qualité pour les différences de couleurs. Lorsqu’un passe-haut classique supprime la saturation et peut introduire une netteté indésirable, Color Equalizer permet d’atténuer les différences de couleur et de supprimer les teintes indésirables à une échelle sélectionnable par l’utilisateur.

Cette fonction est très utile si une photo ou une numérisation présente des différences de couleur indésirables ou si vous souhaitez supprimer une teinte. Si vous avez utilisé [Passe-haut](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/highpass/highpass.md), ce nœud devrait vous être familier.

Les options de masquage sont destinées à supprimer des teintes très spécifiques ou à fonctionner uniquement dans des plages de valeurs spécifiques. Utilisez-les si vous pensez que l’effet est trop large.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Entrée</b> <i>Entrée couleur</i> |  |
| <b>Entrée de masque</b> <i>Entrée en niveaux de gris</i> | Emplacement de masque utilisé pour masquer les effets du nœud. Uniquement actif lorsque le masque est défini sur « Entrée ». |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Mosaïque d&#39;entrée</b> <i>Faux/Vrai</i> | Conserve éventuellement la répétition sur les contours. |
| <b>Rayon</b> <i>0.0 - 50.0</i> | Définit le rayon d’égalisation. Un rayon plus grand ne supprimera que les grandes différences de couleur. Cela nécessite de retoucher chaque image. |
| <b>Balance des tons clairs/foncés</b> <i>0.0 - 1.0</i> | Paramètre par biais pour laisser ou supprimer les teintes plus sombres. |
| <b>Variation de couleur personnalisée</b> <i>Faux/Vrai</i> | Permet de faire varier l’effet vers une couleur définie par l’utilisateur. |
| <b>Variation de couleur</b> | Uniquement actif si l’option Variation de couleur personnalisée est activée. Les paramètres vous permettent de sélectionner un décalage de teinte vers lequel effectuer l’égalisation. |
| <b>Teinte</b> <i>0.0 - 360.0</i> |  |
| <b>Chrominance</b> <i>0.0 - 1.0</i> |  |
| <b>Luminance</b> <i>0.0 - 1.0</i> |  |
| <b>Source du masque</b> <i>Aucun, Moyenne de l&#39;image, Paramètre de couleur, Entrée</i> | Définissez si un type de masquage doit se produire. Paramètre de couleur active les paramètres supplémentaires ci-dessous. L’entrée bascule sur une entrée de masque définie par l’utilisateur. |
| <b>Masquer</b> | Cette option est uniquement active avec le masquage des paramètres de couleur. Paramètres de masquage supplémentaires pour déterminer le masque en fonction de l’image elle-même. Les paramètres ci-dessous vous permettent de convertir avec précision une teinte en un masque binaire sur lequel l’égalisation est appliquée. Notez que les effets du paramètre Rayon peuvent devenir beaucoup moins prononcés lors de l’utilisation de ces paramètres. |
| <b>Couleur</b> <i>(valeur de couleur)</i> |  |
| <b>Plage de teintes</b> <i>0.0 - 360.0</i> |  |
| <b>Gamme de chrominance</b> <i>0.0 - 1.0</i> |  |
| <b>Plage de luminance</b> <i>0.0 - 1.0</i> |  |
| <b>Flou</b> <i>0.0 - 2.0</i> |  |
| <b>Smoothness</b> <i>0.0 - 2.0</i> |  |
