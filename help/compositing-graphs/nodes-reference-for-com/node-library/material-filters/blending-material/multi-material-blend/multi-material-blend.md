---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/blending-material/multi-material-blend.html"
breadcrumb-title: ''
description: Utilisez le nœud Fusion de plusieurs matériaux pour fusionner plusieurs matériaux afin de créer des combinaisons de matériaux complexes.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Blending (Material) > Multi-Material Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Mélange de plusieurs matériaux
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 1%

---


# Mélange de plusieurs matériaux

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/multi-material-blend.png){width="128px"}

## Mélange de plusieurs matériaux

**Entrée :** *Filtres de matière/Fusion*

**Intermédiaire**

</td>
<td style="border: 0;" valign="top">

## Description

Ce nœud combine plusieurs matériaux basés sur un mappage d’ID de matériau/d’ID de couleur, un qui peut être cuit à partir d’un filet. Il peut contenir jusqu’à 16 matières complètes différentes, quel que soit le type de canaux que vous activez dans le groupe Canaux.

Le nœud est très utile lors de la texturation d&#39;accessoires complets, car il permet une paramétrisation complète des matériaux tout en les combinant dynamiquement tous. Parfait pour texturer des accessoires simples à complexes qui ont des processus d&#39;identification appropriés, ou même pour créer des Substances « Template » entièrement pipées qui correspondent entièrement aux normes de l&#39;équipe.

Gardez à l&#39;esprit que lorsque vous utilisez cette option, Matériau 1, Fente 1 est toujours le matériau par défaut et apparaîtra partout où aucun autre matériau n&#39;apparaît. C’est pourquoi vous ne pouvez pas lui attribuer une couleur. Si vous souhaitez jouer cette vidéo sécurisée, vous pouvez par exemple brancher un [Matériau de base](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/base-material/base-material.md) défini sur un noir grossier.

## Paramètres

### Entrées

* **1 à 16 emplacements de matériau complets** La quantité d&#39;emplacements est déterminée par la liste déroulante **Matériaux**.
* **Color ID** : *Color Input*\
  Mappage d’ID de couleur cuit.

### Paramètres

* **Matières** :*2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16* définit la quantité maximale de différentes matières à fusionner.
* **Canaux**\
  Activez et désactivez les canaux de matériau dans ce groupe, par exemple lorsque vous utilisez des cartes de Specular/brillance au lieu de cartes de métal/rugosité.
* **Matière 2-16** Un groupe apparaît pour chaque matière activée.
  * **Couleur** : *(Valeur de couleur)*Couleur à choisir dans la carte d&#39;ID correspondant à cet emplacement de matière.
  * **Tolérance** :*0.01 - 1.0* Fondu dans les couleurs voisines.
  * **Remplissage** : *0.0 - 1.0* Dureté des transitions : contraste du masque.

## Exemples d’images

|  |
| --- |
| Aucune image n&#39;est jointe à cette page. |

</td>
</tr>
</table>
