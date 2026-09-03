---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/point-list.html"
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
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 1%

---


# Liste de points

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icône de nœud](point-list.resources/point-list-01.png "Icône de nœud")

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

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Aperçu</b> <i>Niveaux de gris</i> | Aperçu des points sous forme d’image en niveaux de gris. |
| <b>Entrée de liste de points</b> <i>Couleur</i> | Liste des points d&#39;entrée codés dans les canaux RVBA d&#39;une image couleur :<br><b>R</b> - position X<br><b>G</b> - position Y<br><b>B</b> - Height<br><b>A</b> - données compressées :<br> * partie Entier : Smoothness ;<br> * partie fractionnaire : Thickness. |
| <b>Entrée de numéro de point</b> <i>Nombre entier</i> | Nombre de points d’entrée. |

<a name="outputs"></a>

## Sorties

|  |  |
|:---|:---|
| <b>Aperçu</b> <i>Niveaux de gris</i> | Aperçu des points sous forme d’image en niveaux de gris. |
| <b>Liste de points</b> <i>Couleur</i> | Liste de sortie des points codés dans les canaux RVBA d&#39;une image couleur :<br><b>R</b> - position X<br><b>G</b> - position Y<br><b>B</b> - Height<br><b>A</b> - données compressées :<br> * partie Entier : Smoothness ;<br> * partie fractionnaire : Thickness. |
| <b>Numéro De Point</b> <i>Nombre entier</i> | Nombre de points en sortie. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Numéro De Point</b> <i>Nombre entier</i> | Nombre de points générés. |
| <b>Ajustement du Smoothness global</b> <i>Flotter</i> | Applique un décalage uniforme à la valeur par smoothness de tous les points.<br>La valeur de smoothness résultante est répartie sur la plage [0;1]. |
| <b>Propriétés des points</b> |  |
| <b>p# Propriétés</b> <i>Float3</i> | Définit les propriétés du point p#.<br>*- Height :* Ajuste l&#39;height du point où une valeur inférieure signifie un emplacement plus bas ou plus profond ;<br>*- Smoothness :* Décale le début du lissage de la spline à p#, où une valeur de 0 entraîne une trajectoire dure et 1 une trajectoire entièrement lisse ;<br>*- Thickness :* Ajuste le thickness de la spline à p#. Le thickness est utilisé par des nœuds Spline spécifiques. |
| <b>Coordonnées Des Points</b> |  |
| <b>p#</b> <i>Float2</i> | Définit la position du point p# dans l’espace de texture. |
| <b>Aperçu</b> |  |
| <b>Afficher les libellés</b> <i>Booléen</i> | Pour chaque point, affiche le nom du point en regard de celui-ci dans la sortie « Aperçu ». |
| <b>Taille de l&#39;étiquette</b> <i>Float</i> (disponible lorsque « Afficher les libellés » est défini sur « Vrai ») | Taille du libellé de chaque point dans l’espace de la texture, où 0,1 correspond à un dixième de la largeur de la texture. |
| <b>Afficher les points</b> <i>Booléen</i> | Affiche les points dans la sortie Aperçu. |
| <b>Taille Des Points</b> <i>Float</i> (disponible lorsque « Afficher les points » est défini sur « Vrai ») | Rayon des points dans l’espace de la texture, où 0,1 correspond à un dixième de la largeur de la texture. |

## Exemples

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Exemple de nœud 1](point-list.resources/point-list-02.jpg "Exemple de nœud 1")

</td>
<td style="border: 0;" valign="top">

![Exemple de nœud 2](point-list.resources/point-list-03.gif "Exemple de nœud 2")

</td>
</tr>
</table>
