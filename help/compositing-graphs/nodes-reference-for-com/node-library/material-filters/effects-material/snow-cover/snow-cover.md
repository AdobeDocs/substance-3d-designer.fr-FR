---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/snow-cover.html"
breadcrumb-title: ''
description: Utilisez le nœud Couverture Snow pour ajouter des effets d'accumulation de neige aux matériaux en fonction de l'angle de la surface et de la position.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Snow Cover
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Couverture de Snow
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 2%

---


# Couverture de Snow

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/snow-cover.png){width="128px"}

## Couverture de Snow

**Entrée :** *Filtres/Effets De Matière*

**Intermédiaire**

</td>
<td style="border: 0;" valign="top">

## Description

Effet tout-en-un pour ajouter de la neige sur un matériau complet. Repose fortement sur une bonne carte de hauteur de haute qualité, comme celle d’un photoscan. Le résultat est censé être correct pour le PBR.

## Paramètres

### Entrées

* **Masque (facultatif)** : *Entrée en niveaux de gris*\
  Emplacement de masque utilisé pour masquer les effets du nœud.

### Paramètres

* **Canaux**\
  Activez et désactivez les canaux de matériau dans ce groupe, par exemple lorsque vous utilisez des cartes de Specular/brillance au lieu de cartes de métal/rugosité.
* **Snow frais** :*0.0 - 1.0* Règle la quantité de neige dans les zones surélevées. Le résultat est lié au paramètre Snow fondu.
* **Snow fondu** :*0.0 - 1.0* Définit la quantité de neige fondue dans les coins les plus bas.
* **Accumulation** : *0,0 - 1,0* Affecte principalement la sortie d’Height, détermine l’effet d’empilement d’heights.
* **Smoothness** :*0.0 - 1.0* Définit le lissage des détails de l&#39;height en fonction de l&#39;accumulation de neige.
* **Intensité des flocons** : *0.0 - 1.0* affecte principalement la carte normale, l&#39;intensité des détails des flocons.

## Exemples d’images

|  |
| --- |
| Aucune image n&#39;est jointe à cette page. |

</td>
</tr>
</table>
