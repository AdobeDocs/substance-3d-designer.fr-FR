---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-warp.html"
breadcrumb-title: ''
description: Utilisez le nœud Déformation de spline pour déformer des textures le long de tracés de spline afin de créer des motifs courbes et organiques.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Déformation de la spline
user-guide-description: ''
user-guide-title: ''
source-git-commit: e23f692fa31d1e7b9eeac692bb41186441fdda53
workflow-type: tm+mt
source-wordcount: '1135'
ht-degree: 0%

---


# Déformation de la spline

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icône de nœud](spline-warp.resources/spline-warp-icon.png "Icône de nœud")

<b>Entrée :</b> Outils Spline Et Tracé > Outils spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Déplace les splines d&#39;entrée en fonction de la texture d&#39;intensité ou de la texture vectorielle d&#39;entrée.

L&#39;intensité de l&#39;effet de déformation peut être ajustée le long de la spline à l&#39;aide des commandes d&#39;atténuation.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Aperçu</b> <i>Niveaux de gris</i> | Aperçu des splines d&#39;entrée sous forme d&#39;image en niveaux de gris. |
| <b>Couleurs splines</b> <i>Couleur</i> | Coordonnées des points des splines d&#39;entrée codés dans les canaux RVBA d&#39;une image couleur :<br><b>R</b> - position X<br><b>G</b> - position Y<br><b>B</b> - Height<br><b>A</b> - données compressées :<br> - signe : la spline est fermée (négative) ou ouverte (positive);<br> - Valeur absolue : Thickness + 1. |
| <b>Données splines</b> <i>Couleur</i> | Données supplémentaires des splines d&#39;entrée codées dans les canaux RVBA d&#39;une image couleur.<br><b>R</b> - Tangentes X<br><b>G</b> - Tangentes Y<br><b>B</b> - Inutilisé<br><b>A</b> - Inutilisé |
| <b>Quantité de spline</b> <i>Entier</i> | Nombre de splines d&#39;entrée. |
| <b>Carte d&#39;intensité</b> <i>Niveaux de gris</i> | (Disponible lorsque l&#39;option Utiliser la texture vectorielle est définie sur Faux) image en niveaux de gris d&#39;entrée utilisée pour contrôler la direction et l&#39;intensité de l&#39;effet de déformation sur les splines d&#39;entrée.<br>La couleur de chaque pixel de l&#39;image spécifie un multiplicateur pour déplacer les points de la spline le long de leur normale (c&#39;est-à-dire la direction perpendiculaire à la spline), jusqu&#39;à la plage complète de l&#39;image.<br>Les valeurs [0 ; 1] de l&#39;image sont remappées sur la plage [-1 ; 1] lorsqu&#39;elles sont lues comme un multiplicateur : 0 et 1 déplacent la spline de la même distance mais dans des directions opposées. 0,5 laisse la spline en place. |
| <b>Carte vectorielle</b> <i>Niveaux de gris</i> | (Disponible lorsque l’option Utiliser la texture vectorielle est définie sur Vrai) Image couleur d’entrée utilisée pour contrôler la direction et l’intensité de l’effet de déformation sur les splines d’entrée.<br>La couleur de chaque pixel de l&#39;image spécifie le vecteur (X, Y) dont les coordonnées sont codées dans les canaux rouge (X) et vert (Y). +X à droite et +Y en bas.<br>Les valeurs [0 ; 1] de l&#39;image sont remappées sur la plage [-1 ; 1] lorsqu&#39;elles sont lues en tant que coordonnées vectorielles : 0 rouge déplace les points vers la gauche et 0 vert déplace les points vers le haut. 0,5 rouge et vert laisse la spline en place. |
| <b>Courbe D&#39;Atténuation</b> <i>Niveaux de gris</i> | Image décrivant une courbe en utilisant les valeurs de sa première ligne de pixels.<br>Lorsque le paramètre Utiliser la courbe d&#39;atténuation est défini sur True, cette entrée est utilisée pour contrôler l&#39;atténuation de l&#39;effet de déformation près du début et de la fin de la spline.<br>La courbe fournit un profil pour l&#39;atténuation, où le premier pixel de la ligne est l&#39;intensité de l&#39;effet de déformation au début de la spline, et le dernier est l&#39;intensité à la fin. La valeur Niveaux de gris correspond à l’intensité.<br>Vous pouvez utiliser un nœud Courbe pour créer la courbe. |

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
| <b>Intensité de déformation</b> <i>Flotter</i> | Intensité du déplacement des splines. |
| <b>Centre de déformation</b> <i>Flotter</i> | Spécifie la valeur de la courbe d&#39;intensité correspondant au maintien des splines.<br>Une valeur de 0 ou 1 signifie que les splines ne peuvent être déplacées que d&#39;un côté. |
| <b>Mode d&#39;échantillonnage</b> <i>Nombre entier</i> | Méthode de mappage des valeurs de la carte d&#39;intensité ou de la carte vectorielle aux splines :<br>- <i>espace de Texture</i> : les valeurs sont appliquées aux splines où elles se trouveraient si elles étaient placées dans une texture à l&#39;aide des coordonnées UV de la texture. Cela applique efficacement la valeur aux splines « en place »;<br>- <i>Horizontalement le long de la spline</i> : les valeurs sont appliquées directement aux coordonnées des splines codées (voir Entrée des cordons de spline), où chaque ligne est appliquée à une spline différente de haut en bas ;<br>- <i>Heure. le long de la spline (rand. offset X)</i> : les valeurs sont appliquées directement aux coordonnées des splines codées (voir Entrée des cordons de spline), avec un décalage horizontal aléatoire dans la carte d&#39;échelle pour chaque spline (c&#39;est-à-dire chaque ligne dans les cordons de spline);<br>- <i>Hor. le long de la spline (rand. décalage Y)</i> : les valeurs sont appliquées directement aux coordonnées des splines codées (voir Entrée des cœurs de spline), avec un décalage vertical aléatoire dans la carte d&#39;échelle pour chaque spline (c&#39;est-à-dire chaque ligne dans les cœurs de spline). |
| <b>Utiliser la carte vectorielle</b> <i>Booléen</i> | Bascule la méthode de déplacement des splines sur l&#39;utilisation d&#39;une entrée de cartographie vectorielle pour spécifier la direction du displacement.<br>La couleur de chaque pixel de l&#39;image spécifie le vecteur (X, Y) dont les coordonnées sont codées dans les canaux rouge (X) et vert (Y). +X à droite et +Y en bas.<br>Les valeurs [0 ; 1] de l&#39;image sont remappées sur la plage [-1 ; 1] lorsqu&#39;elles sont lues en tant que coordonnées vectorielles : 0 rouge déplace les points vers la gauche et 0 vert déplace les points vers le haut. 0,5 rouge et vert laisse la spline en place. |
| <b>Utiliser la courbe d&#39;atténuation</b> <i>Booléen</i> | Permet de contrôler l’intensité de l’effet de déformation le long d’une spline à l’aide d’une courbe codée dans l’image d&#39;entrée Courbe d’atténuation. |
| <b>Répétition de la carte d&#39;intensité</b> <i>Flotter</i> | (Disponible lorsque le mode d&#39;échantillonnage n&#39;est pas défini sur Espace de Texture) Ajuste la répétition de la courbe d&#39;intensité lorsqu&#39;elle est mappée directement aux coordonnées de la spline (voir Entrée Cœurs de spline). |
| <b>Démarrer l&#39;atténuation</b> <i>Flotter</i> | (Disponible lorsque l&#39;option Utiliser la courbe d&#39;atténuation est définie sur Faux) Multiplicateur pour l&#39;atténuation de l&#39;effet de déformation vers le début de la spline.<br>Une valeur de 1 signifie qu&#39;aucune déformation n&#39;est appliquée au début de la spline. |
| <b>Fin de l&#39;atténuation</b> <i>Flotter</i> | (Disponible lorsque l&#39;option Utiliser la courbe d&#39;atténuation est définie sur Faux) Multiplicateur pour l&#39;atténuation de l&#39;effet de déformation vers la fin de la spline.<br>Une valeur de 1 signifie qu&#39;aucune déformation n&#39;est appliquée à la fin de la spline. |
| <b>Recalculer les Tangentes</b> <i>Booléen</i> | Lorsque la valeur est True, les tangentes d&#39;une spline sont recalculées après l&#39;application de l&#39;effet de déformation.<br>Cela permet de s&#39;assurer que les tangentes de la spline restent cohérentes avec sa trajectoire lorsqu&#39;elle est utilisée dans des nœuds tels que la Dispersion sur la spline ou le mappeur de flux de spline. |
| <b>Aperçu</b> |  |
| <b>Quantité de segments</b> <i>Nombre entier</i> | Ajuste le nombre de segments utilisés pour dessiner la visualisation de la spline dans la sortie d&#39;aperçu.<br>Plus la valeur est élevée, plus la ligne est lisse. |
| <b>Afficher l&#39;assistant de direction</b> <i>Booléen</i> | Affiche un point au début de la spline et une flèche à sa fin dans la sortie Aperçu. |
| <b>Afficher l&#39;enveloppe de Thickness</b> <i>Booléen</i> | Affiche des lignes supplémentaires sur les thickness de la spline. |
| <b>Thickness (px)</b> <i>Flotter</i> | Règle le thickness de visualisation de la spline en pixels dans la sortie Aperçu. |
| <b>Intensité de l&#39;aperçu de l&#39;arrière-plan</b> <i>Flotter</i> | Valeur multipliée par rapport à l’image d&#39;entrée Aperçu en arrière-plan. |

## Exemples

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-warp.resources/SplineWarp-Variant1-Before.jpg" alt="SplineWarp-Variant1-Before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="spline-warp.resources/SplineWarp-Variant1-After.jpg" alt="SplineWarp-Variant1-After">
      <br><i>Après</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-warp.resources/SplineWarp-Variant2-Before.jpg" alt="SplineWarp-Variant2-Before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="spline-warp.resources/SplineWarp-Variant2-After.jpg" alt="SplineWarp-Variant2-After">
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

![Exemple de nœud 1](spline-warp.resources/SplineWarp-Demo.gif "Exemple de nœud 1")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
