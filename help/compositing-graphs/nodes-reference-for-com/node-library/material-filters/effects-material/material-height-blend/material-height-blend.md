---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/material-height-blend.html"
breadcrumb-title: ''
description: Utilisez le nœud Fusion d’Height de matière pour fusionner plusieurs matières en fonction de cartes d’height afin de créer des effets de matière à calques.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Material Height Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Fusion d’Height de matière
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 1%

---


# Fusion d’Height de matière

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/material-height-blend.png){width="128px"}

## Fusion d’Height de matière

**Entrée :** *Filtres/Effets De Matière*

**Intermédiaire**

</td>
<td style="border: 0;" valign="top">

## Description

Ce nœud est une version plus avancée de [Fusion d&#39;Heights](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/height-blend/height-blend.md) qui fusionne deux matériaux en fonction de leurs images de hauteur. Il n&#39;existe pas de masque défini par l&#39;utilisateur. Vous devez donc avoir deux cartes de hauteur, une pour chaque matériau, dont au moins une n&#39;est pas une valeur uniforme.

Cela peut être utile pour combiner deux matériaux différents de haute qualité sans un masque de fusion de haute qualité.

Si vous souhaitez vous fondre dans l&#39;eau ou la neige, les nœuds [Couverture Snow](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/snow-cover/snow-cover.md) et [Niveau d&#39;eau](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/water-level/water-level.md) sont disponibles à la place.

## Paramètres

### Paramètres

* **Canaux**\
  Activez et désactivez les canaux de matériau dans ce groupe, par exemple lorsque vous utilisez des cartes de Specular/brillance au lieu de cartes de métal/rugosité.
* **Décalage de l&#39;Height** :*0.0 - 1.0* décale les hauteurs afin que le niveau de fusion soit déplacé le long de l&#39;axe de l&#39;height. Il s’agit du contrôle principal de la fusion.
* **Contraste** : *0,0 - 1,0*\
  Règle le contraste de la fusion et accentue la netteté des transitions.
* **Mode** : *height équilibré, priorité height bas* bascule entre deux modes de fusion différents.
* **Opacité** : *0.0 - 1.0*\
  Fusion de l’opacité de l’height de premier plan, avec fondu en entrée ou en sortie.
* **Correspondance d&#39;Albédo** : *0.0 - 1.0* quantité de correspondance de couleur interne à effectuer entre les couleurs d&#39;Albédo.

## Exemples d’images

|  |
| --- |
| Aucune image n&#39;est jointe à cette page. |

</td>
</tr>
</table>
