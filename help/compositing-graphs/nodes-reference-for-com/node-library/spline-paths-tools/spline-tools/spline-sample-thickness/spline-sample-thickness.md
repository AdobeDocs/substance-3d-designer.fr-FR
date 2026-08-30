---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-sample-thickness.html"
breadcrumb-title: ''
description: Utilisez le nœud Thickness d'échantillon de spline pour échantillonner les valeurs de thickness le long des splines afin de créer des effets procéduraux.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Sample Thickness
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Thickness d’échantillon spline
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '598'
ht-degree: 0%

---


# Thickness d’échantillon spline

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icône de nœud](spline-sample-thickness.resources/spline-sample-thickness-icon.png "Icône de nœud")

<b>Entrée :</b> Outils Spline Et Tracé > Outils spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Modifie le thickness des splines d&#39;entrée en mappant une texture de Thickness d&#39;entrée sur elles.

L’effet de la courbe de transfert d’height mappée peut être ajusté en modifiant son mode de fusion et l’opacité de cet effet.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Aperçu</b> <i>Niveaux de gris</i> | Aperçu des splines d’entrée sous forme d’image en niveaux de gris. |
| <b>Couleurs splines</b> <i>Couleur</i> | Coordonnées des points des splines d&#39;entrée codés dans les canaux RVBA d&#39;une image couleur :<br><b>R</b> - position X<br><b>G</b> - position Y<br><b>B</b> - Height<br><b>A</b> - données compressées :<br> - signe : la spline est fermée (négative) ou ouverte (positive);<br> - Valeur absolue : Thickness + 1. |
| <b>Données splines</b> <i>Couleur</i> | Données supplémentaires des splines d&#39;entrée codées dans les canaux RVBA d&#39;une image couleur.<br><b>R</b> - Tangentes X<br><b>G</b> - Tangentes Y<br><b>B</b> - Inutilisé<br><b>A</b> - Inutilisé |
| <b>Quantité de spline</b> <i>Nombre entier</i> | Nombre de splines d&#39;entrée. |
| <b>Mappage de Thickness</b> <i>Niveaux de gris</i> | Image en niveaux de gris d&#39;entrée utilisée pour modifier le thickness de la spline d&#39;entrée. |

<a name="outputs"></a>

## Sorties

|  |  |
|:---|:---|
| <b>Aperçu</b> <i>Niveaux de gris</i> | Aperçu des splines de sortie sous forme d’image en niveaux de gris. |
| <b>Couleurs splines</b> <i>Couleur</i> | Coordonnées des points des splines de sortie codés dans les canaux RVBA d&#39;une image couleur.<br><b>R</b> - Position X<br><b>G</b> - Position Y<br><b>B</b> - Height<br><b>A</b> - Données compressées :<br> - Signe : la spline est fermée (négative) ou ouverte (positive);<br> - Valeur absolue : Thickness + 1. |
| <b>Données splines</b> <i>Couleur</i> | Données supplémentaires des splines de sortie codées dans les canaux RVBA d&#39;une image couleur.<br><b>R</b> - Tangentes X<br><b>G</b> - Tangentes Y<br><b>B</b> - Inutilisé<br><b>A</b> - Inutilisé |
| <b>Quantité de spline</b> <i>Nombre entier</i> | Nombre de splines de sortie. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Mode d&#39;échantillonnage</b> <i>Nombre entier</i> | Méthode de mappage des valeurs de la Map thickness aux splines :<br>- <i>espace de Texture</i> : les valeurs sont appliquées aux splines où elles se trouveraient si elles étaient placées dans une texture à l&#39;aide des coordonnées UV de la texture. Cela applique efficacement la valeur aux splines « en place »;<br>- <i>Horizontalement le long de la spline</i> : les valeurs sont appliquées directement aux coordonnées des splines codées (voir Entrée des cordons de spline), où chaque ligne est appliquée à une spline différente de haut en bas ;<br>- <i>Heure. le long de la spline (rand. offset X)</i> : les valeurs sont appliquées directement aux coordonnées des splines codées (voir Entrée des cordons de spline), avec un décalage horizontal aléatoire dans la carte d&#39;échelle pour chaque spline (c&#39;est-à-dire chaque ligne dans les cordons de spline);<br>- <i>Hor. le long de la spline (rand. décalage Y)</i> : les valeurs sont appliquées directement aux coordonnées des splines codées (voir Entrée des cœurs de spline), avec un décalage vertical aléatoire dans la carte d&#39;échelle pour chaque spline (c&#39;est-à-dire chaque ligne dans les cœurs de spline). |
| <b>Opacité</b> <i>Flotter</i> | Multiplicateur de l&#39;intensité de la contribution de la Map thickness au thickness de la spline. |
| <b>Mode de fusion</b> <i>Nombre entier</i> | Méthode de fusion des données de la Map thickness avec le <span id="_Hlk135820484"></span>thickness:<br>-<i>copie</i> de la spline d&#39;entrée : remplacement du thickness de la spline par les valeurs de Map height ;<br>-<i>ajout</i> : ajout des valeurs de Map thickness au thickness de la spline ;<br>-<i>Subtract</i> : valeurs de Subtract au Map thickness de la spline ;<br>-<i>multiplication</i> : multiplication des valeurs de thickness par rapport au Map thickness de la spline. |
| <b>Aperçu</b> |  |
| <b>Quantité de segments</b> <i>Nombre entier</i> | Ajuste le nombre de segments utilisés pour dessiner la visualisation de la spline dans la sortie d&#39;aperçu.<br>Plus la valeur est élevée, plus la ligne est lisse. |
| <b>Afficher l&#39;assistant de direction</b> <i>Booléen</i> | Affiche un point au début de la spline et une flèche à sa fin dans la sortie Aperçu. |
| <b>Afficher l&#39;enveloppe de Thickness</b> <i>Booléen</i> | Affiche des lignes supplémentaires sur les thickness de la spline. |
| <b>Thickness (px)</b> <i>Flotter</i> | Règle le thickness de visualisation de la spline en pixels dans la sortie Aperçu. |

## Exemples

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-sample-thickness.resources/SplineSampleThickness-Variant1-Before.jpg" alt="SplineSampleThickness-Variant1-Before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="spline-sample-thickness.resources/SplineSampleThickness-Variant1-After.jpg" alt="SplineSampleThickness-Variant1-After">
      <br><i>Après</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-sample-thickness.resources/SplineSampleThickness-Variant2-Before.jpg" alt="SplineSampleThickness-Variant2-Before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="spline-sample-thickness.resources/SplineSampleThickness-Variant2-After.jpg" alt="SplineSampleThickness-Variant2-After">
      <br><i>Après</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Exemple de nœud 1](spline-sample-thickness.resources/SplineSampleThickness-Variant1-After1.jpg "Exemple de nœud 1")

</td>
<td style="border: 0;" valign="top">

![Exemple de nœud 2](spline-sample-thickness.resources/SplineSampleThickness-Demo.gif "Exemple de nœud 2")

</td>
</tr>
</table>
