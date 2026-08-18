---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/caustics.html"
breadcrumb-title: ''
description: Utilisez le nœud Caustique pour générer des motifs de lumière caustique afin de créer des effets d'éclairage sous-marin et réfractif.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Caustics
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Caustique
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 0%

---


# Caustique

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/rt-caustics-grayscale.png){width="128px"}

**Entrée :** *Générateurs De Texture**/Bruits*

**Complexe**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Description

Génère des réverbérations projetées en fonction d’une courbe d’height et d’une direction de la lumière.Disponible en niveaux de gris et en couleurs, les différences sont subtiles, mais la version couleur ajoute des effets de dispersion des couleurs. La lumière est projetée à partir d&#39;un seul point, aucune carte d&#39;environnement n&#39;est utilisée.

</td>
</tr>
</table>

## Paramètres

* **Espace colorimétrique de sortie** : *Raw, sRGB*\
  Définissez l’espace colorimétrique de sortie.
* **Taille de la grille de photons** : *Auto, 512, 1024, 2048, 4096*\
  Définit la qualité en ajustant la taille de la grille, mais utilise par défaut l’entrée correspondante. Peut être utilisé pour accélérer le calcul.
* **Échelle D&#39;Height De Surface** : *0.0 - 1.0*\
  Multiplicateur pour déterminer comment l’height est interprété.
* **Position De L&#39;Height De Surface** : *0.0 - 1.0*\
  Définissez la distance de la surface de réfraction par rapport à la projection.
* **IOR de surface** : *1.0 - 2.0*\
  Définissez l’index de réfraction. Dans la version couleur, cette option ajoute plus de dispersion des couleurs.
* **Taille du photon** : *1,0 - 50,0*\
  La taille du photon affecte la netteté de l’effet.
* **Dispersion** : *0.0 - 0.01 (version couleur uniquement)*\
  Affectez uniquement la dispersion des couleurs. Non visible lorsque l&#39;IOR est faible.
* **Variation** : *0.0 - 1.0*\
  Ajoutez une variation irrégulière aux particules de photons projetées.
* **Position claire** :\
  Déplace la position de la lumière. Effectuez également cette opération à l’aide d’un gadget dans la vue 2D.
* **Couleur d&#39;arrière-plan** : *(valeur de couleur) (version de couleur uniquement)*\
  Modifiez la couleur d’arrière-plan. Limité au noir dans la version en niveaux de gris.
* **Extension non carrée** : *Faux/Vrai*\
  Activez la compensation de la courbure et de l’étirement avec des rapports non carrés.

## Exemples d’images

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/rt-caustics-grayscale-1.png" width="300px"/></div> |
| --- |
|  |
