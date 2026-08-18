---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/color-burn.html"
breadcrumb-title: ''
description: Utilisez le nœud de fusion Densité couleur + pour obscurcir les textures en augmentant le contraste afin de créer des effets d’ombre et de densité +.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Color Burn
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Densité couleur +
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 9%

---


# Densité couleur +

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/color-burn.png){width="128px"}

## Densité couleur +

**Entrée :** *Filtres/Fusion*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Description

Effectue un mélange Densité couleur + entre le premier plan et l’arrière-plan. Mathématiquement, la formule est 1 - (1 - Arrière-plan) / Premier plan.

## Paramètres

### Entrées

* **Premier Plan** : *Entrée Couleur*
* **Arrière-Plan** : *Entrée Couleur*
* **Masque** : *Entrée En Niveaux De Gris*\
  Emplacement de masque utilisé pour masquer les effets du nœud.

### Paramètres

* **Opacité** : *0.0 - 1.0*\
  Opacité de fusion entre le premier plan et l’arrière-plan.
* **Fusion D&#39;Alpha** : *Faux/Vrai*\
  Active/désactive la fusion des couches alpha Premier plan et Arrière-plan. Si cette option est définie sur False, la couche alpha du premier plan est ignorée.

## Exemples d’images

</td>
</tr>
</table>
