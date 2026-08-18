---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/height-blend.html"
breadcrumb-title: ''
description: Utilisez le nœud Fusion Height pour fusionner des textures en fonction de cartes d'height afin de créer des transitions de matériau réalistes.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Height Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Dégradé de formes Height
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 2%

---


# Dégradé de formes Height

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/height-blend.png){width="128px"}

## Dégradé de formes Height

**Entrée :** *Filtres/Effets De Matière*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Description

Combine deux cartes de hauteur en fonction de leurs informations d&#39;height. Génère une carte de hauteur fusionnée, mais également un masque noir et blanc qui peut être utilisé ailleurs.

Cela est utile lorsque vous avez deux cartes de hauteur de haute qualité à combiner, mais pas nécessairement un matériau complet, comme c&#39;est le cas pour le [mélange d&#39;Height de matériau](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/material-height-blend/material-height-blend.md).

## Paramètres

### Entrées

* **Height en haut** : *Entrée en niveaux de gris*
* **Height bas** : *Entrée en niveaux de gris*
* **Masque (facultatif)** : *Entrée en niveaux de gris*\
  Emplacement de masque utilisé pour masquer les effets du nœud.

### Paramètres

* **Décalage de l&#39;Height** :*0.0 - 1.0* décale les hauteurs afin que le niveau de fusion soit déplacé le long de l&#39;axe de l&#39;height. Il s’agit du contrôle principal de la fusion.
* **Contraste** : *0,0 - 1,0*\
  Règle le contraste de la fusion et accentue la netteté des transitions.
* **Mode** : *height équilibré, priorité height bas* bascule entre deux modes de fusion différents.
* **Opacité** : *0.0 - 1.0*\
  Fusion de l’opacité de l’height de premier plan, avec fondu en entrée ou en sortie.

## Exemples d’images

|  |
| --- |
| Aucune image n&#39;est jointe à cette page. |

</td>
</tr>
</table>
