---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-circle.html"
breadcrumb-title: ''
description: Utilisez le nœud Cercle spline pour créer des splines circulaires afin de générer des motifs et des formes arrondis.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Circle
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Cercle spline
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '672'
ht-degree: 0%

---


# Cercle spline

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icône de nœud](spline-circle.resources/spline-circle-01.png "Icône de nœud")

<b>Entrée :</b> Outils Spline Et Tracé > Outils spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Génère une spline unique en forme de cercle.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Aperçu</b> <i>Niveaux de gris</i> | Aperçu des splines d’entrée sous forme d’image en niveaux de gris. |
| <b>Couleurs splines</b> <i>Couleur</i> | Coordonnées des points des splines d&#39;entrée codés dans les canaux RVBA d&#39;une image couleur :<br><b>R</b> - position X<br><b>G</b> - position Y<br><b>B</b> - Height<br><b>A</b> - données compressées :<br>- Signe : la spline est fermée (négative) ou ouverte (positive);<br>- Valeur absolue : Thickness + 1. |
| <b>Données splines</b> <i>Couleur</i> | Données supplémentaires des splines d&#39;entrée codées dans les canaux RVBA d&#39;une image couleur.<br><b>R</b> - Tangentes X<br><b>G</b> - Tangentes Y<br><b>B</b> - Inutilisé<br><b>A</b> - Inutilisé |
| <b>Quantité de spline</b> <i>Nombre entier</i> | Nombre de splines d&#39;entrée. |

<a name="outputs"></a>

## Sorties

|  |  |
|:---|:---|
| <b>Aperçu</b> <i>Niveaux de gris</i> | Aperçu des splines de sortie sous forme d’image en niveaux de gris. |
| <b>Couleurs splines</b> <i>Couleur</i> | Coordonnées des points des splines de sortie codés dans les canaux RVBA d&#39;une image couleur.<br><b>R</b> - Position X<br><b>G</b> - Position Y<br><b>B</b> - Height<br><b>A</b> - Données compressées :<br>- Signe : la spline est fermée (négative) ou ouverte (positive);<br>- Valeur absolue : Thickness + 1. |
| <b>Données splines</b> <i>Couleur</i> | Données supplémentaires des splines de sortie codées dans les canaux RVBA d&#39;une image couleur.<br><b>R</b> - Tangentes X<br><b>G</b> - Tangentes Y<br><b>B</b> - Inutilisé<br><b>A</b> - Inutilisé |
| <b>Quantité de spline</b> <i>Nombre entier</i> | Nombre de splines de sortie. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Rayon du cercle</b> <i>Flotter</i> | Ajuste le rayon du cercle dans l’espace de la texture. |
| <b>Pré-Rotation Du Cercle</b> <i>Flotter</i> | Applique une rotation au cercle de base avant l’application de la propriété Taille. |
| <b>Taille du cercle</b> <i>Float2</i> | Ajuste la taille horizontale (X) et verticale (Y) du cercle. |
| <b>Après-Rotation Du Cercle</b> <i>Flotter</i> | Applique une rotation au cercle de base après l’application de la propriété Taille. |
| <b>Position du cercle</b> <i>Float2</i> | Définit la position du centre du cercle dans l’espace de la texture. |
| <b>Démarrer le Thickness</b> <i>Flotter</i> | Ajuste le thickness du point de départ du cercle. Ce thickness est interpolé le long de la spline jusqu&#39;au Thickness d&#39;extrémité.<br>Remarque : le Thickness est utilisé par des nœuds de spline spécifiques. |
| <b>Fin de Thickness</b> <i>Flotter</i> | Ajuste le thickness de l’extrémité du cercle. Ce thickness est interpolé le long de la spline jusqu&#39;au Thickness de départ.<br>Remarque : le Thickness est utilisé par des nœuds de spline spécifiques. |
| <b>Height de démarrage</b> <i>Flotter</i> | Ajuste l’height du point de départ du cercle, où une valeur plus faible signifie un emplacement plus bas ou plus profond. Cet height est interpolé le long de la spline jusqu&#39;à l&#39;Height Fin. |
| <b>Height final</b> <i>Flotter</i> | Ajuste l’height de l’extrémité du cercle, à l’endroit où une valeur plus faible signifie un emplacement plus bas ou plus profond. Cet height est interpolé le long de la spline à partir de l&#39;Height Début. |
| <b>Rogner</b> <i>Float2</i> | Décale les points de départ et d&#39;arrivée de la spline le long du cercle. Ces valeurs sont normalisées. |
| <b>Spirale</b> <i>Flotter</i> | Déplace le point de départ du cercle de son rayon vers son centre. La distance depuis le centre est ensuite interpolée le long de la spline jusqu&#39;à l&#39;extrémité de la spline. Cette valeur est normalisée. |
| <b>Virages en spirale</b> <i>Flotter</i> | Définit le nombre de tours effectués par la spirale autour de son centre. |
| <b>Puissance en spirale</b> <i>Flotter</i> | Applique une courbe de puissance à la distance depuis le centre utilisée pour dessiner la spirale. Une valeur supérieure à un signifie qu&#39;une plus grande partie de la spirale reste proche du centre. |
| <b>Inverser la direction</b> <i>Booléen</i> | Inverse la direction de la spline. |
| <b>Distribution uniforme</b> <i>Booléen</i> | Lorsque la valeur est True, les points de la spline sont régulièrement espacés du début à la fin. |
| <b>Ajouter une spline d&#39;entrée</b> <i>Booléen</i> | Ajoute la spline générée à la fin de la liste des splines connectées aux entrées de <b>spline</b>. |
| <b>Correction Non Carrée</b> <i>Booléen</i> | Ajustez la position et le thickness des points pour conserver la forme de la spline dans des résolutions autres que carrées. Cela a également un impact sur la distribution uniforme. |
| <b>Aperçu</b> |  |
| <b>Afficher l&#39;assistant de direction</b> <i>Booléen</i> | Affiche un point au début de la spline et une flèche à sa fin dans la sortie Aperçu. |
| <b>Afficher l&#39;enveloppe de Thickness</b> <i>Booléen</i> | Affiche des lignes supplémentaires sur les bords du thickness de la spline. |
| <b>Quantité de segments</b> <i>Nombre entier</i> | Ajuste le nombre de segments utilisés pour dessiner la visualisation de la spline dans la sortie Aperçu. Plus la valeur est élevée, plus la ligne est lisse. |
| <b>Thickness (px)</b> <i>Flotter</i> | Règle le thickness en pixels de la visualisation de la spline dans la sortie Aperçu. |

## Exemples

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Exemple de nœud 1](spline-circle.resources/spline-circle-02.jpg "Exemple de nœud 1")

</td>
<td style="border: 0;" valign="top">

![Exemple de nœud 2](spline-circle.resources/spline-circle-03.gif "Exemple de nœud 2")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Exemple 3](spline-circle.resources/spline-circle-04.jpg "Exemple 3")

</td>
<td style="border: 0;" valign="top">

![Exemple 4](spline-circle.resources/spline-circle-05.jpg "Exemple 4")

</td>
</tr>
</table>
