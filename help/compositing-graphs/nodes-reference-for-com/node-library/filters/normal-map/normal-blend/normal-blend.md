---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-blend.html"
breadcrumb-title: ''
description: Utilisez le nœud Fusion normale pour fusionner des cartes de normales afin de créer des transitions lisses entre les détails de surface.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Dégradé normal
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 2%

---


# Dégradé normal

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/normal-blend.png){width="128px"}

## Dégradé normal

**Entrée :** *Filtres/Mappage de normales*

**Intermédiaire**

</td>
<td style="border: 0;" valign="top">

## Description

Fusion normale vous permet de fusionner deux cartes normales avec un masque facultatif, tout en vous assurant que toutes les valeurs restent normalisées. Il ne diffère pas beaucoup d&#39;un [nœud de fusion atomique](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md), mais a ajouté des calculs internes pour Normalmaps.

Dégradé de formes normal n’est pas destiné à combiner (incruster) des normales, où la courbe du haut ajoute des détails à la courbe du bas. Pour cela, utilisez plutôt [Combinaison normale](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-combine/normal-combine.md).

## Paramètres

### Entrées

* **NormalFG** : *Entrée couleur*\
  Mappage normal de premier plan/haut.
* **NormalBG** : *Entrée couleur*\
  Background/Bottom Normalmap.
* **Masque** : *Entrée En Niveaux De Gris*\
  Emplacement de masque utilisé pour masquer les effets du nœud. Peut être basculé avec le paramètre « Utiliser le masque ».

### Paramètres

* **Opacité** : *0.0 - 1.0*\
  Opacité de fusion entre le premier plan et l’arrière-plan
* **Utiliser le masque** : *Faux/Vrai*\
  Active ou désactive l&#39;utilisation de la carte de masque.

## Exemples d’images

![](../../../../../../assets/normalblend-ex.gif)

*(.gif format introduit le tramage dans l&#39;exemple, les résultats dans l&#39;application sont lisses)*

</td>
</tr>
</table>
