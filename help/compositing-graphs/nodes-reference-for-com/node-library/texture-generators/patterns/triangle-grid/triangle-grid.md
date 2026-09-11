---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/triangle-grid.html"
breadcrumb-title: ''
description: Utilisez le nœud Triangle Grid pour générer des motifs de grille triangulaire afin de créer des textures géométriques dans Substance 3D Designer.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Triangle Grid
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Triangle Grid
user-guide-description: ''
user-guide-title: ''
source-git-commit: b63bc7a45aa6eadef1b72eb05d4a6aded05866a8
workflow-type: tm+mt
source-wordcount: '1114'
ht-degree: 0%

---


# Triangle Grid

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](triangle-grid.resources/trianglegridgrayscale.jpg){width="200px"}

![](triangle-grid.resources/trianglegridcolor.jpg){width="200px"}

<b>Entrée :</b> Générateurs De Textures > Motifs

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Description

Le nœud **Triangle Grid** génère une représentation en niveaux de gris d&#39;une *surface triangulée* sur *vertex* dans l&#39;espace 3D, à l&#39;aide d&#39;une projection orthographique Z vers le bas.

Le paramètre **Sortie couleur** vous permet de sélectionner les données utilisées pour la représentation, ce qui donne différents styles visuels.\
Les *positions* des vertex peuvent être ajustées, ce qui a un impact sur le maillage généré.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Height</b> <i>Niveaux de gris</i> PRINCIPAUX | Entrée d&#39;image en niveaux de gris utilisée pour mapper l&#39;*height*, c&#39;est-à-dire la position Z, des vertex.    L&#39;influence de cette entrée est contrôlée par le paramètre &#39;Multiplicateur d&#39;entrée d&#39;Height&#39;. |
| <b>Carte vectorielle</b> <i>Couleur</i> | Entrée d&#39;image couleur utilisée pour mapper le *displacement* des vertex sur les axes X et Y.    Les décalages X/Y sont respectivement mis en correspondance avec les canaux R/G de l&#39;image.    L&#39;influence de cette entrée est contrôlée par le paramètre &#39;Vector Map Displacement&#39;. |
| <b>Entrée de couleur</b> <i>Couleur</i> | Entrée d&#39;image couleur utilisée pour mapper la *couleur* des vertex, segments ou triangles.    Cette entrée est utilisée lorsque le paramètre Source de couleur est défini sur Entrée de couleur. |

<a name="outputs"></a>

## Sorties

|  |  |
|:---|:---|
| <b>Sortie</b> <i>Couleur</i> | Image de sortie. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Sortie couleur</b> *Entier* | La méthode de représentation de la surface triangulée:<ul data-preserve-html="true"> <li data-preserve-html="true"><b>Par Vertex :</b> une couleur est attribuée à chaque vertex et interpolée sur la surface du triangle</li> <li data-preserve-html="true"><b>Par triangle :</b> une couleur plate est affectée à chaque triangle</li> <li data-preserve-html="true"><b>Ligne fine</b><b>:</b> applique un contour aux segments entre les vertex</li> <li data-preserve-html="true"><b>Distance jusqu&#39;au contour</b><b>:</b> effectue le rendu de la distance jusqu&#39;au segment le plus proche sur chaque triangle</li> <li data-preserve-html="true"><b>Centre</b><b>:</b> restitue la distance normalisée par rapport au barycentre de chaque triangle</li> </ul> |
| <b>Triangulation</b> *Entier* | Définit la méthode de triangulation de la surface, c&#39;est-à-dire la *paire de vertex opposés* dans un quad à relier :<ul data-preserve-html="true"> <li data-preserve-html="true"><b>Auto :</b> sélectionne automatiquement la paire de vertex, ce qui fait que les triangles <i>sont orientés le moins loin</i> de la caméra<br/> <b>45° :</b> connectez les vertex opposés, ce qui donne une ligne <i>tournée de 45°</i> par rapport à l&#39;axe X droit</li> <li data-preserve-html="true"><b>-45° :</b> connectez les vertex opposés, ce qui a pour effet de faire tourner la ligne <i>de -45°</i> par rapport à l&#39;axe X droit</li> <li data-preserve-html="true"><b>Quincux horizontal :</b> alternent l&#39;orientation de triangulation <i>une rangée sur deux</i> de vertex</li> <li data-preserve-html="true"><b>Quincux vertical :</b> alterne l&#39;orientation de triangulation <i>une colonne sur deux</i> de vertex<br/> </li> </ul> |
| <b>X Quantité</b> *Entier* | Nombre de vertex générés sur l’axe X. |
| <b>Quantité Y</b> *Entier* | Nombre de vertex générés sur l’axe Y. |
| <b>Multiplicateur De Position Aléatoire</b> *Flottant* | Règle l’intensité de l’effet de déformation principal. |
| <b>Position Aléatoire</b> *Flottant 2* | Ajuste l&#39;intensité du décalage aléatoire appliqué aux positions X et Y de chaque vertex, par rapport à la *taille de leur cellule* dans la grille.   Ce décalage *pile* avec les paramètres <b>Décalage Quincux</b> et <b>Displacement de mappage vectoriel</b>. |
| <b>Displacement de mappage vectoriel</b> *Flottant* | Ajuste la quantité *globale* de displacement appliquée à chaque vertex à l&#39;aide des valeurs *échantillonnées* à partir de l&#39;entrée <b>Carte vectorielle</b>.    Ce décalage *pile* avec les paramètres <b>Position aléatoire</b> et <b>Décalage Quincux</b>. |
| <b>Décalage Quincux X</b> *Flottant* | Applique le décalage spécifié à *une ligne sur deux* de vertex, par rapport à la *taille de leur cellule* dans la grille.   Ce décalage *pile* avec les paramètres <b>Position aléatoire</b> et <b>Displacement de carte vectorielle</b>. |
| <b>Décalage Quincux Y</b> *Flottant* | Applique le décalage spécifié à *une colonne sur deux* de vertex, par rapport à la *taille de leur cellule* dans la grille.    Ce décalage *pile* avec les paramètres <b>Position aléatoire</b> et <b>Displacement de carte vectorielle</b>. |
| <b>Rotation</b> *Flottant* | Applique le degré de rotation *spécifié* à chaque vertex autour de sa *position de base*, c&#39;est-à-dire sa position *avant* le décalage aléatoire et le displacement.    Cette rotation *pile* avec le paramètre <b>trouble de rotation</b>. |
| <b>Trouble De La Rotation</b> *Flottant* | Applique un degré de rotation *aléatoire* à chaque vertex autour de sa *position de base*, c&#39;est-à-dire sa position *avant* le décalage aléatoire et le displacement.    Cette rotation *pile* avec le paramètre <b>Rotation</b>. |
| <b>Multiplicateur d&#39;entrée Height</b> *Flottant* | Ajuste la position Z de chaque vertex à l&#39;aide des valeurs *échantillonnées* à partir de l&#39;entrée <b>Height</b>.    Ce décalage *pile* avec le paramètre <b>Height aléatoire</b>. |
| <b>Height aléatoire</b> *Flottant* | Applique un décalage aléatoire à la position Z de chaque vertex.  Ce décalage *pile* avec le paramètre <b>Multiplicateur d&#39;entrée d&#39;Height</b>. |
| <b>Mode Fusion</b> *Entier* | Définit la méthode de fusion des valeurs des *triangles superposés*. Le mode vous permet de sélectionner *lequel* des triangles doit être visible : <ul data-preserve-html="true"> <li data-preserve-html="true"><b>Min :</b> Texte</li> <li data-preserve-html="true"><b>Max. :</b> Texte</li> <li data-preserve-html="true"><b>Test De Profondeur</b> : Texte</li> <li data-preserve-html="true"><b>Fusion d&#39;Alpha :</b> texte</li> </ul>Remarque : les modes de fusion disponibles dépendent de la valeur du paramètre <b>Sortie couleur</b>. |
| <b>Source de couleur</b> *Entier* *Disponible lorsque le paramètre « Sortie couleur » est défini sur « Par Vertex », « Par triangle » ou « Ligne fine ».* | Définit la méthode d&#39;*acquisition de la couleur*, c&#39;est-à-dire de la luminance, qui doit être attribuée au vertex, au triangle ou au segment, en fonction du mode <b>Sortie couleur</b> sélectionné :<ul data-preserve-html="true"> <li data-preserve-html="true"><b>Height</b><b>:</b> utilisez l&#39;height du vertex comme luminance</li> <li data-preserve-html="true"><b>Aléatoire</b><b>:</b> utiliser une valeur de luminance aléatoire</li> <li data-preserve-html="true"><b>Entrée couleur</b><b>:</b> utilisez la valeur échantillonnée à partir de l&#39;entrée <b style="">Entrée couleur</b></li> </ul> |
| <b>Opacité de la source de couleur</b> *Flottant* *Disponible lorsque le paramètre « Sortie couleur » est défini sur « Ligne fine ».* | Contrôle le *remplacement* de la valeur <b>Couleur de ligne</b> avec les valeurs résultant de la <b>Source de couleur</b> sélectionnée.   Remarque : lorsque cette valeur est définie sur 1, le paramètre <b>Couleur de ligne</b> n&#39;a aucun impact. |
| <b>Distance jusqu&#39;au Thickness du contour</b> *Flottant* *Disponible lorsque le paramètre « Sortie couleur » est défini sur « Distance jusqu&#39;au contour ».* | Définit le thickness du dégradé de distance. Une valeur inférieure donne un dégradé *plus court*. |
| <b>Couleur de ligne</b> *Flottant/Flottant 4* *Disponible lorsque le paramètre « Sortie couleur » est défini sur « Ligne fine ».* | Valeur de luminance des segments.   Remarque : lorsque la valeur <b>Opacité de la source de couleur</b> est définie sur 1, ce paramètre n&#39;a aucun impact. |
| <b>Couleur d&#39;arrière-plan</b> *Flottant/Flottant 4* *Disponible lorsque le paramètre « Sortie couleur » est défini sur « Ligne fine ».* | Valeur de luminance de l’arrière-plan visible entre les segments.   Remarque : lorsque le <b>mode Fusion</b> est défini sur *Max*, l&#39;arrière-plan remplace les segments où il est *plus lumineux*, comme prévu. |
| <b>Mode générateur de couleurs aléatoire</b> *Entier* *Disponible lorsque le paramètre « Sortie couleur » est défini sur « Par Vertex », « Par triangle » ou « Ligne fine » et que le paramètre « Source couleur » est défini sur « Aléatoire ».* | La méthode d&#39;acquisition de la germe utilisée dans la distribution pseudo-aléatoire des couleurs:<ul data-preserve-html="true"> <li data-preserve-html="true"><b>Générateur aléatoire global</b><b>:</b> hérite du générateur du graphe du nœud</li> <li data-preserve-html="true"><b>Valeur initiale manuelle</b><b> :</b> utilisez une valeur initiale distincte personnalisée</li> </ul> |
| <b>Générateur aléatoire de couleurs</b> *Entier* *Disponible lorsque le paramètre « Mode générateur de couleur aléatoire » est défini sur « Générateur manuel » et que le paramètre « Source de couleur » est défini sur « Aléatoire ».* | Valeur initiale discrète utilisée dans la distribution de couleurs pseudo-aléatoire. |
| <b>Extension non carrée</b> *Booléen* | Active la compensation de la courbure et de la étire avec des proportions non carrées. |

## Exemples

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Triangle Grid : Exemple 1](triangle-grid.resources/triangle_grid_color_example_1.jpg "Triangle Grid : Exemple 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Triangle Grid : Exemple 2](triangle-grid.resources/trianglegrid-variant2.png "Triangle Grid : Exemple 2"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Triangle Grid : Exemple 3](triangle-grid.resources/trianglegridcolor-variant2.jpg "Triangle Grid : Exemple 3"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Triangle Grid : Exemple 4](triangle-grid.resources/triangle_grid_color_example_2.jpg "Triangle Grid : Exemple 4"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Triangle Grid : Exemple 5](triangle-grid.resources/trianglegridcolor-variant4.jpg "Triangle Grid : Exemple 5"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Triangle Grid : Exemple 6](triangle-grid.resources/trianglegridcolor-variant3.jpg "Triangle Grid : Exemple 6"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Triangle Grid : Cuir](triangle-grid.resources/trianglegrid-demo.png "Triangle Grid : Cuir"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Triangle Grid : Graphe](triangle-grid.resources/trianglegrid-node.png "Triangle Grid : Graphe"){zoomable="yes"}

</td>
</tr>
</table>
