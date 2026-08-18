---
title: Mappeur d’éclaboussures de forme v2 en niveaux de gris
description: Designer > Graphes de composition de Substances > Référence des nœuds pour les graphes de composition de Substances > Bibliothèque de nœuds > Générateur > Motif > Éclaboussure de forme v2, mappeur de niveaux de gris
source-git-commit: f688c618b01d3ca8059e67cf0797268e44e94b17
workflow-type: tm+mt
source-wordcount: '1766'
ht-degree: 0%

---


# Mappeur d’éclaboussures de forme v2 en niveaux de gris

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icône de niveaux de gris du mappeur Shape Splatter v2](./shape-splatter-v2-mapper-grayscale.resources/shape-splatter-v2-mapper-grayscale.png "Mappeur Shape Splatter v2 Grayscale")

<b>Entrée :</b> Générateur > Motif

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Mappe les images en niveaux de gris sur les formes générées et dispersées à l&#39;aide du nœud [Shape splatter v2](../shape-splatter-v2/shape-splatter-v2.md) , en utilisant les données supplémentaires fournies par le nœud.<br><br>Les images sont fournies en tant qu&#39;entrées de motif distinctes ou compressées dans un atlas en grille. Elles peuvent être appliquées aux formes à l&#39;aide de la cartographie UV, de la projection triplanaire ou de la cartographie personnalisée.<br><br>Les formes peuvent être teintées et leur luminance ajustée de manière uniforme ou aléatoire par forme.

Voir aussi [Couleur du mappeur v2 des éclaboussures de forme](../shape-splatter-v2-mapper-color/shape-splatter-v2-mapper-color.md).

</td>
</tr>
</table>

>[!INFO]
>
> Ce nœud nécessite des données d&#39;entrée générées par le nœud [Shape splatter v2](../shape-splatter-v2/shape-splatter-v2.md).
> 
> Autres nœuds de la famille Shape splatter v2 :
> * [Éclaboussure de forme v2 au masque](../shape-splatter-v2-to-mask/shape-splatter-v2-to-mask.md)
>
> Les nœuds en niveaux de gris [Atlas en grille](../grid-atlas-grayscale/grid-atlas-grayscale.md) vous permettent de regrouper des images dans un atlas de taille personnalisée, jusqu&#39;à 16 motifs dans 4*4 cellules.

>[!TIP]
> 
> L&#39;échantillon de matière ](../../../../../../function-graphs/nodes-reference-for-fun/function-node-library/function-nodes-sdf-functions/working-with-sdf-functions.md#material-sample) des [**« boulons rouillés »** est disponible pour commencer avec les nœuds Shape Splatter v2.
> 
> Pour en savoir plus sur les concepts et les workflows impliquant des Fonctions SDF, consultez la page dédiée : [Utilisation des Fonctions SDF](../../../../../../function-graphs/nodes-reference-for-fun/function-node-library/function-nodes-sdf-functions/working-with-sdf-functions.md)

<a name="inputs"></a>

## Entrées

|                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|:------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Entrée Atlas en grille</b> *Niveaux de gris* | Image en niveaux de gris de motifs entassés dans une disposition en grille.<br><br>La taille de la grille doit correspondre à celle utilisée par le nœud [Shape splatter v2](../shape-splatter-v2/shape-splatter-v2.md).<br><br>Utilisez le nœud [Atlas en grille grayscale](../grid-atlas-grayscale/grid-atlas-grayscale.md) pour regrouper des motifs distincts dans un atlas en grille. |
| <b>Entrée de motif 1</b> *Niveaux de gris* | Image en niveaux de gris du motif de #1 mappé aux formes.<br><br><i>Conseil :</i> utilisez une résolution proche de la taille maximale que peut avoir le motif lorsqu&#39;il est diffusé. |
| <b>Entrée de motif 2</b> *Niveaux de gris* | Image en niveaux de gris du motif de #2 mappé aux formes.<br><br><i>Conseil :</i> utilisez une résolution proche de la taille maximale que peut avoir le motif lorsqu&#39;il est diffusé. |
| <b>Entrée de motif 3</b> *Niveaux de gris* | Image en niveaux de gris du motif de #3 mappé aux formes.<br><br><i>Conseil :</i> utilisez une résolution proche de la taille maximale que peut avoir le motif lorsqu&#39;il est diffusé. |
| <b>Entrée de motif 4</b> *Niveaux de gris* | Image en niveaux de gris du motif de #4 mappé aux formes.<br><br><i>Conseil :</i> utilisez une résolution proche de la taille maximale que peut avoir le motif lorsqu&#39;il est diffusé. |
| <b>Entrée de motif 5</b> *Niveaux de gris* | Image en niveaux de gris du motif de #5 mappé aux formes.<br><br><i>Conseil :</i> utilisez une résolution proche de la taille maximale que peut avoir le motif lorsqu&#39;il est diffusé. |
| <b>Entrée de motif 6</b> *Niveaux de gris* | Image en niveaux de gris du motif de #6 mappé aux formes.<br><br><i>Conseil :</i> utilisez une résolution proche de la taille maximale que peut avoir le motif lorsqu&#39;il est diffusé. |
| <b>Entrée de motif 7</b> *Niveaux de gris* | Image en niveaux de gris du motif de #7 mappé aux formes.<br><br><i>Conseil :</i> utilisez une résolution proche de la taille maximale que peut avoir le motif lorsqu&#39;il est diffusé. |
| <b>Entrée de motif 8</b> *Niveaux de gris* | Image en niveaux de gris du motif de #8 mappé aux formes.<br><br><i>Conseil :</i> utilisez une résolution proche de la taille maximale que peut avoir le motif lorsqu&#39;il est diffusé. |
| <b>Entrée en arrière-plan</b> *Niveaux de gris* | Image en niveaux de gris utilisée comme arrière-plan pour les formes mappées. |
| <b>Entrée de couleur</b> *Niveaux de gris* | Image en niveaux de gris utilisée pour teinter les formes mappées en fonction de leur position de pivot.<br><br>Utilisez le paramètre d&#39;<b>opacité d&#39;entrée de couleur</b> pour régler l&#39;intensité de la contribution de ces couleurs à la couleur des formes. |
| <b>Normal</b> *Couleur* | Normales calculées pour les formes dispersées, masquées en fonction de la fusion avec l&#39;height d&#39;arrière-plan.<br><br> Si le <b>type de forme</b> est &#39;Atlas en grille&#39;, les normales fournies à l&#39;entrée <b>Atlas en grille normal</b> sont utilisées directement. |
| <b>Splatter UVW</b> *Couleur* | <b>R</b> - Composante U des UV des formes.<br><b>G</b> - Composante V des UV des formes.<br><b>B</b> - height des formes. (W)<br><b>A</b> - Données compressées :<br> - <i>Partie d&#39;entier :</i> Identificateur unique des formes. (ID)<br> - <i>Partie fractionnaire :</i> dépend du <b>type de forme</b> : ID de matériau si SDF/primitif, ID de motif* si entrée de motif/atlas en grille.<br><br><b>* :</b> L’ID de motif est l’index de la forme dans la liste/l’atlas. |
| <b>Données d’éclaboussures 1</b> *Couleur* | <b>R</b> - Composante X de la position sur la surface de la forme, dans l&#39;espace objet.<br><b>G</b> - Composante Y de la position sur la surface de la forme, dans l&#39;espace objet.<br><b>B</b> - Composante Z de la position sur la surface de la forme, dans l&#39;espace objet.<br><b>A</b> - Données compressées :<br> - <i>Partie entière :</i> U de la composante UV des coordonnées des données des formes dans les sorties Données 2/3.<br> - <i>Partie fractionnaire :</i> composante V des coordonnées UV pour les données des formes dans les sorties Données 2/3.<br> - Masque binaire <i>Sign:</i> pour la fusion des formes avec l&#39;height d&#39;arrière-plan. |
| <b>Données d’éclaboussures 2</b> *Couleur* | <b>R</b> - Composant X de la rotation 3D des formes.<br><b>G</b> - Composant Y de la rotation 3D des formes.<br><b>B</b> - Composant Z de la rotation 3D des formes.<br><b>A</b> - La rotation des formes autour de leur normale.<br><br>Toutes les rotations sont définies en nombre de tours. |
| <b>Éclaboussures de données 3</b> *Couleur* | <b>R</b> - Composante X de la position des formes.<br><b>G</b> - Composante Y de la position des formes.<br><b>B</b> - Les formes sont décalées le long de leur normale.<br><b>A</b> - Données compressées :<br> - <i>Partie entière :</i> ID de la forme.<br> - <i>Partie fractionnaire :</i>l’index du motif des formes dans son atlas source. (si vous utilisez un type de motif atlas en grille) |
| <b>Données d’éclaboussures 4</b> *Couleur* | <i>Pixel 1</i><br><b>R</b> - Taille X des images de sortie Data 2/3.<br><b>G</b> - Taille Y des images de sortie Data 2/3.<br><b>B</b> - Taille X de l’image de sortie Data 4.<br><b>A</b> - Taille Y de l’image de sortie Data 4.<br><br><i>Pixel 2</i><br><b>R</b> : type de forme. (E.g. Cube, cylindre, ...)<br><b>G</b> - Données compressées :<br> - <i>Valeur absolue :</i> Numéro d&#39;entrée du motif.<br> - <i>Format Sign:</i> normal du mappage normal de sortie. (Positif : DirectX / Négatif : OpenGL)<br><b>B</b> - Taille X de l&#39;atlas en grille. (C’est-à-dire le nombre de colonnes)<br><b>A</b> - Taille Y de l’atlas en grille. (c’est-à-dire le nombre de lignes) |

<a name="outputs"></a>

## Sorties

|               |                     |
|:--------------|:--------------------|
| <b>Sortie</b> | Les formes colorées. |

<a name="parameters"></a>

## Paramètres

|                                            |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|:-------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Mode de projection</b> *Nombre entier* | Méthode de projection des images d&#39;entrée sur les formes :<br><br>- <b>À partir d&#39;UV à éclaboussures :</b> Utilisez les UV fournis par le nœud [Éclaboussures de forme v2](../shape-splatter-v2/shape-splatter-v2.md).<br>- <b>Triplanaire :</b> Utilisez la projection triplanaire pour mapper les images sur les axes XYZ locaux des formes.<br>- <b>Fonction personnalisée :</b> Créez un graphique de fonction pour définir le mappage des images sur les formes. |
| <b>Fonction personnalisée</b> *Flotter* | Spécifie la luminance par pixel des formes sous la forme d&#39;un objet flottant.<br><br>Les variables suivantes sont disponibles :<br>- <code>shape.position.os</code> (Float3) Position de la surface de la forme dans l&#39;espace objet.<br>- <code>shape.position.ws</code> (Float3) Position de la surface de la forme dans l’espace univers*.<br>- <code>shape.normal.os</code> (Float3) Normales de la surface de la forme dans l&#39;espace objet.<br> - <code>shape.normal.ws</code> (Float3) Les normales de la surface de la forme dans l’espace univers*.<br>- <code>shape.id</code> (Flottant) Identificateur unique de la forme.<br>- <code>matériau.id</code> (Flottant) ID de matériau de la surface de la forme, défini par le nœud [Forme éclaboussée v2](../shape-splatter-v2/shape-splatter-v2.md).<br><br>* : l&#39;espace univers de la forme est centré sur son pivot et ne tient pas compte de l&#39;height de la forme. Cela signifie que la seule différence avec l’espace objet est l’orientation.<br><br>Si l&#39;échantillonnage des entrées du nœud [Shape splatter v2 mapper grayscale](shape-splatter-v2-mapper-grayscale.md) est nécessaire, ces emplacements d&#39;entrée de nœud [Sample grayscale](../../../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md) peuvent être utilisés :<br>- 0 : Atlas en grille<br>- 1-8 : Entrée de motif 1-8 |
| <b>Mélange de contraste</b> *Flotter* | La netteté des transitions entre les projections planes, où 1 signifie aucun dégradé de fondu. |
| <b>Projection d&#39;image</b> *Nombre entier* | Quantité d&#39;images <b>d&#39;entrée de motif #</b> distribuées sur les projections planaires contribuant à la cartographie triplanaire.<br><br>Afin de couvrir tous les côtés d’une forme, une projection plane avant (+) et arrière (-) est effectuée sur chaque axe, pour un total de 6 projections.<br><br>- <b>1 image :</b> L’entrée Motif 1 est utilisée pour toutes les projections planes.<br>- <b>3 images :</b> Une entrée Motif distincte est utilisée pour la +/- projection de chaque axe.<br>- <b>6 images :</b> Chaque projection utilise une entrée Motif distincte.<br>- <b>1 image par ID matériau :</b> Utilisez une entrée Motif distincte par ID matériau, où chaque image est utilisé pour toutes les projections planes. |
| <b>Centre de projection</b> *Float3* | Décale la projection triplanaire par axe, dans l’espace objet.<br><br>Le décalage est appliqué à l&#39;<i>espace de projection entier</i>. Par conséquent, un décalage sur un axe affectera le positionnement des textures projetées sur les <i>deux autres</i> axes. |
| <b>Échelle de projection</b> *Flotter* | Ajuste l&#39;échelle des textures projetées sur <i>tous les axes</i>, selon le facteur spécifié. |
| <b>Mode de sélection d&#39;entrée</b> *Nombre entier* | Méthode de sélection des images d’entrée à mapper aux formes.<br><br>Le <b>type de forme</b> sélectionné dans le nœud [Shape splatter v2](../shape-splatter-v2/shape-splatter-v2.md) source change la façon d&#39;affecter des images aux formes :<br><br>-<b>Atlas en grille</b> signifie que les images sont récupérées dans l&#39;« entrée d&#39;Atlas en grille » en faisant correspondre les index de grille (les deux atlas doivent utiliser la même taille de grille)<br>-<b>entrée de motif</b> signifie que les images sont récupérées dans les entrées « # d&#39;entrée de motif » en faisant correspondre les index.<br>-<b>Autres types de formes :</b> les images sont affectées par les index correspondants aux ID de matériau de la forme.<br><br>Les méthodes disponibles pour sélectionner les index sont les suivantes :<br>-<b>À partir des données d&#39;éclaboussures :</b> Faites correspondre les index des images &#39;Entrée de motif&#39; ou &#39;Entrée d&#39;Atlas en grille&#39; aux index des formes attribuées par le nœud [Éclaboussure de forme v2](../shape-splatter-v2/shape-splatter-v2.md).<br>- <b>Manuel :</b> Utilisez l&#39;index spécifié par le paramètre &#39;Index d&#39;image&#39;.<br>-<b>Aléatoire :</b> Utilisez un index aléatoire dans la plage spécifiée par le paramètre &#39;Random range&#39;. |
| <b>Numéro d&#39;entrée du motif</b> *Nombre entier* | Quantité d&#39;images d&#39;entrée <b>de motif #</b> qui doivent être mappées sur les formes. |
| <b>Index d&#39;image</b> *Nombre entier* | Index du motif d&#39;entrée de l&#39;<b>entrée de motif #</b> ou de l&#39;<b>entrée d&#39;Atlas en grille</b> qui doit être mappé sur les formes. |
| <b>Plage aléatoire</b> *Entier2* | La plage d&#39;index de l&#39;<b>entrée de motif #</b> ou de l&#39;<b>entrée d&#39;Atlas en grille</b> dans laquelle ce motif doit être sélectionné aléatoirement pour être mappé sur les formes. |
| <b>Réglage de la luminance</b> *Flotter* | Décalage uniformément appliqué à la luminance de toutes les formes. |
| <b>Luminance aléatoire</b> *Flotter* | Décalage aléatoire, positif ou négatif, appliqué à la luminance des formes, jusqu’aux valeurs spécifiées. |
| <b>Opacité d&#39;entrée de couleur</b> *Flotter* | Intensité de la contribution de l&#39;<b>entrée de couleur</b> aux couleurs des formes, selon le <b>mode de fusion d&#39;entrée de couleur</b> sélectionné. |
| <b>Mode de fusion d&#39;entrée de couleur</b> *Nombre entier* | Opération de mélange des couleurs utilisée pour combiner les images de premier plan et d’arrière-plan.<br><br>Ces opérations sont identiques à leurs homologues dans le nœud [Blend](../../../../atomic-nodes/blend/blend.md).<br><br>Modes disponibles :<br>- <b>Copier</b><br>- <b>Ajouter (densité linéaire)</b><br>- <b>Soustraire</b><br>- <b>Multiplier</b><br>- <b>Superposer</b> |
| <b>Mode mosaïque</b> *Nombre entier* | Axes selon lesquels la texture doit être répétée :<br> - <b>Aucun carrelage</b><br> - <b>Carrelage horizontal</b><br> - <b>Carrelage vertical</b><br> - <b>Carrelage H et V</b> : carrelage horizontal et vertical combiné. |
| <b>Carrelage UV</b> *Flotter* | Ajuste la mosaïque globale des images mappées sur les formes<br><br>Les valeurs élevées entraînent davantage de répétitions. |
| <b>Échelle UV</b> *Float2* | Ajuste la juxtaposition des images mappées sur les formes selon le facteur spécifié, avec des commandes de mise à l’échelle U et V distinctes. Plus la valeur est élevée, plus le nombre de répétitions est élevé. |
| <b>Décalage des UV</b> *Float2* | Applique un décalage au mappage des images sur les formes, ce qui permet un réglage fin du positionnement des images sur les formes.<br><br>Ce décalage est ajouté au <b>décalage aléatoire</b>, le cas échéant. |
| <b>Décalage aléatoire</b> *Flotter* | Applique une quantité aléatoire de décalage positif ou négatif <i>par forme</i> au mappage des images sur les formes, jusqu&#39;à la valeur spécifiée.<br><br>Ce décalage est ajouté au <b>Décalage des UV</b>, le cas échéant. |

