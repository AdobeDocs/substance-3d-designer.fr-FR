---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/blending-material/material-adjustment-blend.html"
breadcrumb-title: ''
description: Utilisez le nœud Fusion Réglage matière pour fusionner les réglages de matière entre les matières afin d'affiner les effets composites.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Blending (Material) > Material Adjustment Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Fusion ajustement matière
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 1%

---


# Fusion ajustement matière

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/material-adjustment-blend.png){width="128px"}

## Fusion ajustement matière

**Entrée :** *Filtres de matière/Fusion*

**Intermédiaire**

</td>
<td style="border: 0;" valign="top">

## Description

Ce nœud permet de régler tous les canaux d’un matériau complet, en fonction d’un masque. Il est conçu pour faciliter et accélérer un flux de production matériel complet.

Cette option est utile lorsque vous souhaitez ajuster quelques couches d’un matériau (comme éclaircir une diffusion et assombrir une rugosité) en fonction du même masque.

## Paramètres

### Entrées

* **Masque d&#39;identifiant de couleur** : *Entrée couleur*\
  Emplacement de masque utilisé pour masquer les effets du nœud.
* **Masque De Niveaux De Gris** : *Entrée En Niveaux De Gris*\
  Emplacement de masque utilisé pour masquer les effets du nœud.

### Paramètres

* **Canaux**\
  Active et désactive les couches de matériau dans ce groupe, par exemple lors de l’utilisation de cartes de Specular/brillance au lieu de cartes de métal/rugosité.\
  Cela active et désactive également l’apparence des groupes pertinents du canal.
* **Diffus**\
  Effectue des opérations de réglage sur la couche diffuse, dans les zones définies par le masque.
* **Couleur de base**\
  Effectue des opérations de réglage sur la couche de couleur de base, dans les zones définies par le masque.
* **Normal**
  * **Intensité** : *0,0 - 1,0* Atténuation de l&#39;intensité normale
* **Specular**\
  Effectue des opérations de réglage sur la couche de Specular, dans les zones définies par le masque.
* **Émissif**\
  Effectue des opérations de réglage sur la couche émissive, dans les zones définies par le masque.
* **Lustre**\
  Effectue des opérations de réglage sur la couche Lustre, dans les zones définies par le masque.
* **Rugosité**\
  Effectue des opérations de réglage sur la couche de rugosité, dans les zones définies par le masque.
* **Métallique**\
  Effectue des opérations de réglage sur la couche métallique, dans les zones définies par le masque.
* **Specular level**\
  Effectue des opérations de réglage sur la couche de Specular level, dans les zones définies par le masque.
* **Occlusion ambiante**\
  Effectue des opérations de réglage sur la couche Occlusion ambiante, dans les zones définies par le masque.
* **Height**\
  Effectue des opérations de réglage sur la couche Height, dans les zones définies par le masque.
* **Opacité**\
  Effectue des opérations de réglage sur la couche d’opacité, dans les zones définies par le masque.
* **Masque d&#39;identifiant de couleur** : *Faux/Vrai* Définissez pour utiliser Masque d&#39;identifiant de couleur au lieu du masque en niveaux de gris.
* **Tolérance** :*0.01 - 1.0* Si l’option Masque d&#39;identifiant de couleur est activée, elle détermine l’étendue de la couleur de sélection de l’ID de couleur.
* **Couleur** : *(Valeur de couleur)*Définit la couleur à choisir dans le mappage d&#39;ID de couleur et le masque.
* **Remplissage** : *0.0 - 1.0* détermine le contraste de fusion/les transitions du masquage Color ID.

## Exemples d’images

|  |
| --- |
| Aucune image n&#39;est jointe à cette page. |

</td>
</tr>
</table>
