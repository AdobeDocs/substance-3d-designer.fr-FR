---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/color-equalizer.html"
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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 1%

---


# Color Equalizer

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/color-equalizer.png){width="128px"}

## Color Equalizer

**Entrée :** *Filtres de matière/Traitement de la numérisation*

**Complexe**

</td>
<td style="border: 0;" valign="top">

## Description

Ce nœud fonctionne comme un [passe-haut](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/highpass/highpass.md) de haute qualité pour les différences de couleurs. Lorsqu’un passe-haut classique supprime la saturation et peut introduire une netteté indésirable, Color Equalizer permet d’atténuer les différences de couleur et de supprimer les teintes indésirables à une échelle sélectionnable par l’utilisateur.

Cette fonction est très utile si une photo ou une numérisation présente des différences de couleur indésirables ou si vous souhaitez supprimer une teinte. Si vous avez utilisé [Passe-haut](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/highpass/highpass.md), ce nœud devrait vous être familier.

Les options de masquage sont destinées à supprimer des teintes très spécifiques ou à fonctionner uniquement dans des plages de valeurs spécifiques. Utilisez-les si vous pensez que l’effet est trop large.

## Paramètres

### Entrées

* **Entrée** : *Entrée Couleur*
* **Entrée de masque** :*Entrée en niveaux de gris*\
  Emplacement de masque utilisé pour masquer les effets du nœud. Uniquement actif lorsque le masque est défini sur « Entrée ».

### Paramètres

* **Mosaïque d’entrée** : *Faux/Vrai* Conserve éventuellement la mosaïque sur les bords.
* **Rayon** : *0,0 - 50,0* Définit le rayon d&#39;égalisation. Un rayon plus grand ne supprimera que les grandes différences de couleur. Cela nécessite de retoucher chaque image.
* **Balance des tons clairs/foncés** : *0.0 - 1.0* Paramètre de biais pour laisser ou supprimer les teintes plus sombres.
* **Variation de couleur personnalisée** : *Faux/Vrai* permet de faire varier l&#39;effet vers une couleur spécifiée par l&#39;utilisateur.
* **Variation de couleur**\
  Uniquement actif si l’option Variation de couleur personnalisée est activée. Les paramètres vous permettent de sélectionner un décalage de teinte vers lequel effectuer l’égalisation.
  * **Teinte** : *0.0 - 360.0*
  * **Chrominance** : *0.0 - 1.0*
  * **Luma** : *0.0 - 1.0*
* **Source du masque** : *Aucun, Moyenne de l&#39;image, Paramètre de couleur, Entrée* Définissez si un type de masquage doit se produire. Paramètre de couleur active les paramètres supplémentaires ci-dessous. L’entrée bascule sur une entrée de masque définie par l’utilisateur.
* **Masquer**\
  Cette option est uniquement active avec le masquage des paramètres de couleur. Paramètres de masquage supplémentaires pour déterminer le masque en fonction de l’image elle-même. Les paramètres ci-dessous vous permettent de convertir avec précision une teinte en un masque binaire sur lequel l’égalisation est appliquée. Notez que les effets du paramètre Rayon peuvent devenir beaucoup moins prononcés lors de l’utilisation de ces paramètres.
  * **Couleur** : *(valeur chromatique)*
  * **Plage de teintes** : *0.0 - 360.0*
  * **Plage de chrominance** : *0,0 - 1,0*
  * **Plage de luminance** : *0,0 - 1,0*
  * **Flou** : *0.0 - 2.0*
  * **Smoothness** : *0.0 - 2.0*

## Exemples d’images

|  |
| --- |
| Aucune image n&#39;est jointe à cette page. |

</td>
</tr>
</table>
