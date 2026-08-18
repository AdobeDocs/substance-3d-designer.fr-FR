---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/difference.html"
breadcrumb-title: ''
description: Utilisez le nœud de fusion Différence pour fusionner des textures en utilisant le mode de différence pour créer des effets d'inversion et de contraste.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Difference
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Différence
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 6%

---


# Différence

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/difference.png){width="128px"}

## Différence

**Entrée :** *Filtres/Fusion*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Description

Effectue un mode de fusion Différence entre les entrées Avant et Arrière-plan. Soustrait l’arrière-plan du premier plan, renvoyant un résultat absolu (jamais une valeur négative).

## Paramètres

### Entrées

* **Arrière-Plan** : *Entrée Couleur*
* **Premier Plan** : *Entrée Couleur*
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
