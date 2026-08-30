---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-select.html"
breadcrumb-title: ''
description: Utilisez le nœud Sélection de spline pour sélectionner et masquer des zones spécifiques en fonction des tracés de spline dans vos graphiques.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Select
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Sélection spline
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 0%

---


# Sélection spline

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icône de nœud](spline-select.resources/spline-select-icon.png "Icône de nœud")

<b>Entrée :</b> Outils Spline Et Tracé > Outils spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Sélectionne les splines dans la liste d&#39;entrée en fonction des critères spécifiés et génère une nouvelle liste incluant uniquement les splines sélectionnées.

Les splines sélectionnées peuvent également être rognées.

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
| <b>Mode de sélection</b> <i>Nombre entier</i> | Méthode de sélection des splines dans la liste d&#39;entrée :<br>- <i>Première</i> : sélectionne la première spline dans la liste ;<br>- <i>Dernière</i> : sélectionne la dernière spline dans la liste ;<br>- <i>Index</i> : sélectionne la spline avec l&#39;index spécifié ;<br>- <i>Plage</i> : sélectionne les splines dont les index sont inclus dans la plage spécifiée. |
| <b>Index Spline</b> <i>Nombre entier</i> | (Disponible lorsque le « Mode de sélection » est défini sur « Index ») L&#39;index de la spline qui doit être sélectionné. |
| <b>Début de la plage</b> <i>Nombre entier</i> | (Disponible lorsque le mode de sélection est défini sur Plage) L&#39;index le plus bas dans la plage de splines sélectionnées. |
| <b>Fin de plage</b> <i>Nombre entier</i> | (Disponible lorsque le mode de sélection est défini sur Plage) L&#39;index le plus élevé dans la plage de splines sélectionnées. |
| <b>Démarrer</b> <i>Flotter</i> | Décale le début de la partie de la spline qui doit être sélectionnée. Cela permet de raccorder efficacement la spline.<br>La valeur représente la longueur normalisée de la spline. |
| <b>Fin</b> <i>Flotter</i> | Décale l&#39;extrémité de la partie de la spline à sélectionner. Cela permet de raccorder efficacement la spline.<br>La valeur représente la longueur normalisée de la spline. |
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
      <img src="spline-select.resources/SplineSelect-Variant1-Before.jpg" alt="SplineSelect-Variant1-Before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="spline-select.resources/SplineSelect-Variant1-After2.jpg" alt="SplineSelect-Variant1-After2">
      <br><i>Après</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-select.resources/SplineSelect-Variant2-Before.jpg" alt="SplineSelect-Variant2-Before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="spline-select.resources/SplineSelect-Variant2-After.jpg" alt="SplineSelect-Variant2-After">
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

![Exemple de nœud 1](spline-select.resources/SplineSelect-Demo.gif "Exemple de nœud 1")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
