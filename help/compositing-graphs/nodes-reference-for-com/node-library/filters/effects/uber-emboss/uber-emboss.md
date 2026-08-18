---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/uber-emboss.html"
breadcrumb-title: ''
description: Utilisez le nœud Uber Emboss pour créer des effets d’estampage avancés avec des commandes personnalisables de profondeur, d’angle et d’éclairage.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Uber Emboss
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Uber Emboss
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 2%

---


# Uber Emboss

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/uber-emboss.png){width="128px"}

## Uber Emboss

**Entrée :** *Filtres/Effets*

**Intermédiaire**

</td>
<td style="border: 0;" valign="top">

## Description

Version avancée et riche en fonctionnalités de [Emboss](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/emboss/emboss.md). Applique un effet d’éclairage 2D sophistiqué basé sur une courbe de hauteur.

Utile lors de la création d’un éclairage intégré pour certains styles de texture lorsqu’un contrôle important est nécessaire.

## Paramètres

### Entrées

* **Couleur** : *Entrée Couleur*\
  Image de base à modifier.
* **Height** : *Entrée en niveaux de gris*\
  Image de la hauteur utilisée comme pilote pour l’effet.

### Paramètres

* **Couleur ambiante** : *(valeur chromatique)*Couleur utilisée dans les zones ombrées.
* **Couleur diffuse** : *(Valeur de couleur)*Couleur utilisée dans les zones éclairées.
* **Couleur Specular** : *(Valeur de couleur)*Couleur utilisée pour les reflets specular
* **Intensité de la lumière** : *0,0 - 1,0*\
  Intensité de la lumière (simulée).
* **Angle De La Lumière** : *0,0 - 1,0*\
  Angle d’incidence de la lumière (simulée)
* **Intensité du Specular** : *0,0 - 1,0* Intensité des reflets du specular.
* **Brillance du Specular** : *0,0 - 1,0* taille de la mise en évidence du specular.
* **Rugosité diffuse** :*0.0 - 1.0* Rugosité utilisée dans le calcul de l’éclairage diffus.
* **Opacité des ombres** : *0.0 - 1.0* Opacité de fusion des zones ombrées.

## Exemples d’images

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/uberemboss-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
