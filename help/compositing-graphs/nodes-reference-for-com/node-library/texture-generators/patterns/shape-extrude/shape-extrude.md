---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape-extrude.html"
breadcrumb-title: ''
description: Utilisez le nœud Extrusion de forme pour extruder des formes et créer des effets de profondeur de type 3D dans les textures Substance 3D Designer.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Shape Extrude
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Extrusion de forme
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '453'
ht-degree: 0%

---


# Extrusion de forme

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/shape-extrude.png){width="128px"}

## Extrusion de forme

**Entrée :** *Générateurs de textures**/Motifs*

**Complexe**

</td>
<td style="border: 0;" valign="top">

## Description

Nœud avancé qui permet le rendu d’entrées de « forme » binaires 2D sur des hauteurs de cartes rotées en 3D. Fonctionne comme une extrusion dans un assemblage 3D, où une forme est extrudée le long de son axe, créant ainsi un volume. En association avec le masque de dégradé de profil, des corps de type Révolution/Tour peuvent également être créés. Très utile pour créer des formes artificielles complexes pour les images de hauteur.

## Paramètres

### Entrées

* **Entrée de forme d’extrusion** :*Entrée en niveaux de gris* Si l’option Forme d’extrusion est définie sur Personnalisée, vous pouvez insérer votre propre masque de forme binaire ici (de préférence).
* **Dégradé De Profil** : *Entrée En Niveaux De Gris\
  Si le Type de profil est défini sur Dégradé vertical, peut être utilisé pour définir l&#39;échelle de la forme le long de l&#39;axe, pour les corps de révolution.*
* **Masque De Profil** : *Entrée En Niveaux De Gris*\
  Emplacement du masque utilisé pour masquer ou afficher la forme extrudée le long de son axe. Permet de rompre la continuité de la forme le long de son axe. Interprétée uniquement comme binaire : les valeurs PUT en niveaux de gris sont arrondies à 0 ou 1.

### Paramètres

* **Height d&#39;extrusion** : *0.0 -* 1.0\
  Quantité pour extruder la forme par le haut à partir du centre.
* **Extrusion de la Profondeur** : *0,0 - 1,0* quantité d&#39;extrusion de la forme par le bas à partir du centre.
* **Extrusion de forme** : *Cube, cylindre, entrée personnalisée* Utilisez des formes intégrées ou saisissez votre propre forme personnalisée en externe.
* **Taille de la forme d&#39;extrusion** : *0.0 - 1.0* Seule l&#39;option Cube et cylindre intégrés détermine la taille de la forme de base et peut être mise à l&#39;échelle de manière non uniforme.
* **Échelle** : *0.0 - 1.0*\
  Définissez l’échelle globale de l’effet. Avec les formes intégrées, il s’agit d’une échelle de forme de base uniforme, qui n’affecte pas l’Height ni la Profondeur.\
  Avec l’option Entrée personnalisée, le résultat final est mis à l’échelle de manière uniforme.
* **Type de profil** : *Dégradé vertical droit, masque* Contrôle principal pour déterminer le comportement de l’effet et l’utilisation de cartes d’entrée supplémentaires facultatives.\
  Direct est le comportement d’extrusion standard. Le dégradé vertical permet de personnaliser les valeurs d’échelle le long de l’axe entier. Le masque permet de masquer les sections le long de l’axe par masque.
* **Height du biseau** :*0.0 - 1.0* Définissez la distance à laquelle le biseau atteint l&#39;axe d&#39;extrusion.
* **Intensité du biseau** : *0,0 - 1,0* Définissez l’amplitude à laquelle le biseau se rétracte de la forme d’origine.
* **Courbe en biseau** : *-1.0 - 1.0* Définir la courbe convexe ou concave de l&#39;effet de biseau. Une valeur de 0 signifie qu’il n’y a pas de courbe.
* **Biseau miroir** :*faux/vrai* basculez pour appliquer le biseau en haut comme en bas de la forme.
* **Multiplicateur de réduction d&#39;échelle** : *0 - 2* Contrôle de réduction d&#39;échelle facile intégré. Peut être utilisé pour ajouter rapidement un anticrénelage. Veillez à augmenter également la résolution des nœuds.
* **Position** :\
  Contrôle principal de la rotation du résultat dans l’espace 3D. Correspond à l&#39;interactivité Gizmo dans la vue 2D.
* **Plage de sortie** : *[0, 1], [-1, 1]*Définissez les valeurs minimales et maximales de sortie. Si la plage est définie sur [-1,1], les valeurs négatives sont affichées en noir.

## Exemples d’images

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/shape-extrude-1.png" width="256px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
