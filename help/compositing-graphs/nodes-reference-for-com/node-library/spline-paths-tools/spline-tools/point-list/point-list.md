---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/point-list.html"
breadcrumb-title: ''
description: Utilisez le nœud Liste de points pour créer et gérer des listes de points pour la génération de splines et de tracés.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Point List
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Liste de points
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 0%

---


# Liste de points

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icône de nœud](../../../../../../assets/point-list-icon.png "Icône de nœud")

<b>Entrée :</b> Outils Spline Et Tracé > Outils spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Génère une liste de points à traverser par une spline.

Si une liste de points existante est fournie aux entrées <b>Point</b>, la liste générée est ajoutée à la liste d&#39;entrée.

</td>
</tr>
</table>

>[!TIP]
>
> Ce nœud peut être utilisé pour fournir des points au nœud [spline (polyquadratique)](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-poly-quadratic/spline-poly-quadratic.md) afin de construire des splines.

>[!IMPORTANT]
>
> Les connecteurs <b>Liste de points</b> et <b>Numéro de point</b> ne sont *pas compatibles* avec les connecteurs <b>Cordon spline</b>, <b>Données spline</b> et <b>Quantité spline</b>, car ils reposent sur des données différentes.

## Connecteurs d’entrée

<b>Aperçu </b>*en niveaux de gris* Aperçu des points sous forme d’image en niveaux de gris.

<b>Entrée de liste de points</b> *Couleur*\
Liste des points d’entrée codés dans les couches RVBA d’une image couleur :\
    <b>R</b> - Position X\
    <b>G</b> - Position Y\
    <b>B</b> - Height\
    <b>A</b> - Données compressées :\
            * Partie entière : Smoothness ;\
            * Fraction : Thickness.

<b>Entrée de numéro de point</b> *Nombre entier*\
Nombre de points d’entrée.

## Connecteurs de sortie

<b>Aperçu </b>*en niveaux de gris* Aperçu des points sous forme d’image en niveaux de gris.

<b>Liste de points </b>*Couleur*\
Liste de sortie des points codés dans les couches RVBA d’une image couleur :\
    <b>R</b> - Position X\
    <b>G</b> - Position Y\
    <b>B</b> - Height\
    <b>A</b> - Données compressées :\
            * Partie entière : Smoothness ;\
            * Fraction : Thickness.

<b>Nombre De Points </b>*Entier*\
Nombre de points en sortie.

## Paramètres

<b>Numéro De Point</b> *Nombre entier* Nombre de points générés.

<b>Ajustement du Smoothness global</b> *Flottant* Applique un décalage uniforme à la valeur de smoothness de tous les points.\
La valeur de smoothness résultante est fixée à la plage [0;1].

+++Propriétés des points
<b>p# Propriétés</b> *Float3* Définit les propriétés du point p#.\
*- Height :* ajuste l&#39;height du point où une valeur inférieure signifie un emplacement plus bas ou plus profond ;\
*- Smoothness :* décale le début du lissage de la spline à p#, où une valeur de 0 entraîne une trajectoire dure et 1 une trajectoire entièrement lisse ;\
*- Thickness :* ajuste le thickness de la spline à p#. Le thickness est utilisé par des nœuds Spline spécifiques.

+++

+++Coordonnées des points
<b>p#</b> *Float2* Définit la position du point p# dans l’espace de texture.

+++

+++Prévisualiser
<b>Afficher les libellés</b> *booléens*\
Pour chaque point, affiche le nom du point en regard de celui-ci dans la sortie « Aperçu ».

<b>Taille des libellés</b> *Flottant* (disponible lorsque « Afficher les libellés » est défini sur « Vrai »)\
Taille du libellé de chaque point dans l’espace de la texture, où 0,1 correspond à un dixième de la largeur de la texture.

<b>Afficher les points</b> *booléens*\
Affiche les points dans la sortie Aperçu.

<b>Taille des points</b> *Flottant* (disponible lorsque « Afficher les points » est défini sur « Vrai »)\
Rayon des points dans l’espace de la texture, où 0,1 correspond à un dixième de la largeur de la texture.

+++

## Exemples

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Exemple de nœud 1](../../../../../../assets/PointList-Variant1.jpg "Exemple de nœud 1")

</td>
<td style="border: 0;" valign="top">

![Exemple de nœud 2](../../../../../../assets/PointList-Demo1.gif "Exemple de nœud 2")

</td>
</tr>
</table>
