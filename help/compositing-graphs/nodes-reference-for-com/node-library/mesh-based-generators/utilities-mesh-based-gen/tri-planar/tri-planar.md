---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/utilities-mesh-based-generators/tri-planar.html"
breadcrumb-title: ''
description: Utilisez le nœud Tri Planaire pour projeter des textures à partir de trois plans orthogonaux pour une correspondance de texture transparente sur une géométrie complexe.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Utilities (Mesh Based Generators) > Tri Planar
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Tri Planaire
user-guide-description: ''
user-guide-title: ''
source-git-commit: 1ea5f4e048a3b4591bf71d9b18707837dac1bf6f
workflow-type: tm+mt
source-wordcount: '443'
ht-degree: 6%

---


# Tri Planaire

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](tri-planar.resources/triplanar-1.png){width="128px"}

![](tri-planar.resources/triplanar-grayscale.png){width="128px"}

<b>Entrée :</b> Générateurs basés sur le Maillage > Utilitaires

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Ce nœud avancé effectue le mappage des Projections triplanaires en 2D, en fonction de la position bakée et des données de Normale de l&#39;espace monde. Cela signifie qu’il convertit pratiquement toutes les coordonnées UV en un mappage (principalement) sans seam, basé sur le maillage lui-même.

C&#39;est une bonne façon d&#39;éviter les seams sans avoir à refaire à chaque fois (il est possible d&#39;obtenir quelque chose de similaire avec le baker). L&#39;inconvénient est que ce nœud est assez lourd et donc pas rapide.

Gardez à l’esprit que vos bakes doivent être d’une grande précision : les bakes 8 bits ne donneront pas de très bons résultats.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Position</b> <i>Entrée couleur</i> | Mappage de position baké. Idéalement, précision de 16 bits ou supérieure. |
| <b>Espace universel normal</b> <i>Entrée couleur</i> | Carte de Normale de l&#39;espace monde bakée, idéalement précision de 16 bits ou plus. |
| <b>Entrée X</b> <i>Entrée Couleur (Entrée Niveaux De Gris)</i> | Map d&#39;entrée de remappage de l’Espace monde UV via la Projection triplanaire. Utilisé pour tous les Axes lorsque la valeur Entrée image est définie sur 1, pour l’axe X si elle est définie sur 3. |
| <b>Entrée Y</b> <i>Entrée Couleur (Entrée Niveaux De Gris)</i> | Uniquement si le paramètre Entrées image est défini sur 3. Map d&#39;entrée de remappage de l’Espace monde UV vers l’Axe Y. |
| <b>Entrée Z</b> <i>Entrée Couleur (Entrée Niveaux De Gris)</i> | Uniquement si le paramètre Entrées image est défini sur 3. Map d&#39;entrée de remappage de l’Espace monde UV vers l’Axe Z. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Projection</b> <i>Tous les axes, X uniquement, Y uniquement, Z uniquement</i> | Définit les Axes avec lesquels fusionner. |
| <b>Entrées d&#39;image</b> <i>1 entrée, 3 entrées</i> | Indiquez si vous souhaitez utiliser une carte pour tous les Axes ou une carte spécifique par Axe. |
| <b>Mode de fusion</b> <i>linéaire, avancé</i> | Augmente la précision. |
| <b>Contraste de fusion</b> <i>0.001 - 1.0</i> | Contraste de transition, fusion entre des transitions lisses ou dures. |
| <b>Facteur de normalisation</b> <i>0.0 - 1.0</i> | Améliore la fusion des projections en rétablissant la perte de contraste dans la zone de fusion. |
| <b>Répétition de Texture</b> <i>0.0 - 10.0</i> | Nombre de fois où placer les textures d’entrée en mosaïque. |
| <b>Rotation globale</b> <i>0.0 - 1.0</i> | Rotation globale pour tous les Axes. |
| <b>Corriger la Projection mise en miroir</b> <i>Faux/Vrai</i> | Définissez le mode de gestion des Projections mises en miroir. |
| <b>Rotation X</b> <i>0.0 - 1.0</i> | Rotation individuelle sur l’axe X de la projection. |
| <b>Rotation Y</b> <i>0.0 - 1.0</i> | Rotation individuelle sur l’axe Y de la projection. |
| <b>Rotation Z</b> <i>0.0 - 1.0</i> | Rotation individuelle sur l’axe Z de la projection. |
| <b>Décalage X</b> <i>0.0 - 1.0</i> | Décalage sur l’axe X de la projection. |
| <b>Décalage aléatoire X</b> <i>0.0 - 1.0</i> | Autoriser la randomisation du décalage de l&#39;axe X. |
| <b>Décalage Y</b> <i>0.0 - 1.0</i> | Décalage sur l’axe Y de la projection. |
| <b>Décalage aléatoire Y</b> <i>0.0 - 1.0</i> | Permet la randomisation du décalage de l’axe Y. |
| <b>Décalage Z</b> <i>0.0 - 1.0</i> | Décalage sur l’axe Z de la projection. |
| <b>Décalage aléatoire Z</b> <i>0.0 - 1.0</i> | Permet la randomisation du décalage de l’axe Z. |
