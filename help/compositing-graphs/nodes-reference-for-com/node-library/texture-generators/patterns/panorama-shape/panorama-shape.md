---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/panorama-shape.html"
breadcrumb-title: ''
description: Utilisez le nœud Forme de panorama pour créer des formes associées aux coordonnées du panorama en vue de la génération de la texture de l’environnement.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Panorama Shape
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Forme de panorama
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 6%

---


# Forme de panorama

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](panorama-shape.resources/panorama-shape-1.png){width="128px"}

<b>Entrée :</b> Générateurs De Textures > Motifs

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Il s’agit d’un nœud utile pour générer des cartes panoramiques procédurales de type « Studio ». Permet de placer et de modifier des images de projecteur, ainsi que de définir leurs propriétés HDR. Il peut être enchaîné pour plusieurs formes.

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Matrice de forme</b> | Déplace ou translate le résultat. Modifiable en interagissant directement avec la zone de travail. |
| <b>Forme</b> <i>carré, disque</i> | Définit le type de forme. |
| <b>Couleur de forme</b> <i>(valeur de couleur)</i> | Définit la couleur de la forme. |
| <b>Intensité de la forme</b> <i>0.0 - 100.0</i> | Définit l’intensité HDR de la forme. |
| <b>Bordure souple de forme</b> <i>0.0 - 1.0</i> | Modifie le lissage de la bordure de la forme. |
| <b>Intensité de la zone réactive</b> <i>0.0 - 100.0</i> | Définit l’intensité HDR de la zone réactive de la forme. |
| <b>Taille de la zone réactive</b> <i>0.0 - 1.0</i> | Modifie la taille de la zone réactive dans la forme. |
| <b>Suppression de la zone réactive</b> <i>0.0 - 1.0</i> | Modifie la fusion des contours atténués de la zone réactive. |
| <b>Position de la zone réactive</b> <i>0.0 - 1.0</i> | Déplace la zone réactive par rapport à la forme. |
| <b>Activer l&#39;arrière-plan</b> <i>Faux/Vrai</i> | Permet de remplir l’arrière-plan avec une couleur unie. Notez que cela signifie que vous ne pouvez plus les enchaîner par fusion. |
| <b>Couleur d&#39;arrière-plan</b> <i>(valeur de couleur)</i> | Définit la couleur unie de l’arrière-plan. |
| <b>Activer l&#39;entrée de Texture</b> <i>Faux/Vrai</i> | Permet une entrée personnalisée au lieu d’un type de forme prédéfini. |
