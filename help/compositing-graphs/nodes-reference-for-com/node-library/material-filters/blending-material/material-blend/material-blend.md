---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/blending-material/material-blend.html"
breadcrumb-title: ''
description: Utilisez le nœud Fusion de matériau pour fusionner des matériaux entiers à l'aide de masques pour créer des effets de matériau composite.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Blending (Material) > Material Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Fusion de matériaux
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '469'
ht-degree: 0%

---


# Fusion de matériaux

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/material-blend.png){width="128px"}

## Fusion de matériaux

**Entrée :** *Filtres de matière/Fusion*

**Complexe**

</td>
<td style="border: 0;" valign="top">

## Description

Fusion de matériaux est l&#39;équivalent de matériau complet multicanal de [le nœud de fusion atomique](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md). Il se mélange entre deux matières complètes (toutes les couches possibles) à partir d’un masque de niveaux de gris, ou éventuellement à partir d’une seule couleur d’un Masque d&#39;identifiant de couleur.

Ce nœud est utile si vous souhaitez fusionner deux matériaux et avoir une texture en niveaux de gris, mais pas d’ID de couleur complet. Si vous avez un biscuit avec ID de couleur et que vous souhaitez fusionner plus de deux matériaux, nous vous suggérons d&#39;utiliser le [mélange de matériaux multiples](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/multi-material-blend/multi-material-blend.md).

## Paramètres

### Entrées

* **ColorID** : *entrée de couleur*\
  Mappage d’ID de couleur cuit facultatif.
* **Masque De Niveaux De Gris** : *Entrée En Niveaux De Gris*\
  Emplacement de masque utilisé pour masquer les effets du nœud.

### Paramètres

* **Canaux**
  * Activez et désactivez les couches de matériau dans ce groupe, lors de l’utilisation de cartes de Specular/brillance au lieu de cartes de métal/rugosité, par exemple.
* **Diffus**
  * **Opacité** : *0.0 - 1.0*\
    Opacité de fusion entre le premier plan et l’arrière-plan
  * **Mode De Fusion** : *Normal, Ajouter, Soustraire, Multiplier, Ajouter/Soustraire, Max, Min, Basculer*
* **Couleur de base**
  * **Opacité** : *0.0 - 1.0*\
    Opacité de fusion entre le premier plan et l’arrière-plan
  * **Mode De Fusion** : *Normal, Ajouter, Soustraire, Multiplier, Ajouter/Soustraire, Max, Min, Basculer*
* **Normal**
  * **Opacité** : *0.0 - 1.0*\
    Opacité de fusion entre le premier plan et l’arrière-plan
* **Specular**
  * **Opacité** : *0.0 - 1.0*\
    Opacité de fusion entre le premier plan et l’arrière-plan
  * **Mode De Fusion** : *Normal, Ajouter, Soustraire, Multiplier, Ajouter/Soustraire, Max, Min, Basculer*
* **Émissif**
  * **Opacité** : *0.0 - 1.0*\
    Opacité de fusion entre le premier plan et l’arrière-plan
  * **Mode De Fusion** : *Normal, Ajouter, Soustraire, Multiplier, Ajouter/Soustraire, Max, Min, Basculer*
* **Lustre**
  * **Opacité** : *0.0 - 1.0*\
    Opacité de fusion entre le premier plan et l’arrière-plan
  * **Mode De Fusion** : *Normal, Ajouter, Soustraire, Multiplier, Ajouter/Soustraire, Max, Min, Basculer*
* **Rugosité**
  * **Opacité** : *0.0 - 1.0*\
    Opacité de fusion entre le premier plan et l’arrière-plan
  * **Mode De Fusion** : *Normal, Ajouter, Soustraire, Multiplier, Ajouter/Soustraire, Max, Min, Basculer*
* **Métallique**
  * **Opacité** : *0.0 - 1.0*\
    Opacité de fusion entre le premier plan et l’arrière-plan
  * **Mode De Fusion** : *Normal, Ajouter, Soustraire, Multiplier, Ajouter/Soustraire, Max, Min, Basculer*
* **Specular level**
  * **Opacité** : *0.0 - 1.0*\
    Opacité de fusion entre le premier plan et l’arrière-plan
  * **Mode De Fusion** : *Normal, Ajouter, Soustraire, Multiplier, Ajouter/Soustraire, Max, Min, Basculer*
* **Occlusion ambiante**
  * **Opacité** : *0.0 - 1.0*\
    Opacité de fusion entre le premier plan et l’arrière-plan
  * **Mode De Fusion** : *Normal, Ajouter, Soustraire, Multiplier, Ajouter/Soustraire, Max, Min, Basculer*
* **Height**
  * **Opacité** : *0.0 - 1.0*\
    Opacité de fusion entre le premier plan et l’arrière-plan
  * **Mode De Fusion** : *Normal, Ajouter, Soustraire, Multiplier, Ajouter/Soustraire, Max, Min, Basculer*
* **Opacité**
  * **Opacité** : *0.0 - 1.0*\
    Opacité de fusion entre le premier plan et l’arrière-plan
  * **Mode De Fusion** : *Normal, Ajouter, Soustraire, Multiplier, Ajouter/Soustraire, Max, Min, Basculer*
* **Masque d&#39;identifiant de couleur** :*Faux/Vrai* Utilisez le Masque d&#39;identifiant de couleur à la place du masque en niveaux de gris. Gardez à l’esprit qu’il ne s’agit que d’une seule couleur !
* **Couleur** : *(Valeur de couleur)*Quelle couleur choisir et convertir en blanc.
* **Flou** :*0.01 - 1.0* Degré de fusion de la couleur sélectionnée avec ses voisines.
* **Remplissage** : *0.0 - 1.0* contraste de transition de la couleur sélectionnée.

## Exemples d’images

|  |
| --- |
| Aucune image n&#39;est jointe à cette page. |

</td>
</tr>
</table>
