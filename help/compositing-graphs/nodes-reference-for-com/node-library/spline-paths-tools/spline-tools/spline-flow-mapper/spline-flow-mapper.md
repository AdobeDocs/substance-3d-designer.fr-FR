---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-flow-mapper.html"
breadcrumb-title: ''
description: Utilisez le nœud Mappeur de flux de spline pour créer des motifs de texture fluide le long des tracés de spline pour des effets organiques.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Flow Mapper
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Spline Flow Mapper
user-guide-description: ''
user-guide-title: ''
source-git-commit: 86e504c9dfe76516c56a7950f0bf70090270a60c
workflow-type: tm+mt
source-wordcount: '711'
ht-degree: 0%

---


# Spline Flow Mapper

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icône de nœud](spline-flow-mapper.resources/spline-flow-mapper-icon.png "Icône de nœud")

<b>Entrée :</b> Outils Spline Et Tracé > Outils spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Dessine une carte d&#39;enchaînement où les données vectorielles d&#39;enchaînement sont dessinées le long des splines d&#39;entrée.

Cela vous permet d&#39;utiliser des splines pour contrôler la direction, la trajectoire, l&#39;intensité et le thickness du flux, ainsi que le dégradé utilisé pour l&#39;atténuation des données tracées dans l&#39;arrière-plan neutre.

</td>
</tr>
</table>

>[!IMPORTANT]
>
> Il peut en résulter des artefacts indésirables en dehors de l&#39;enveloppe de la spline lors de l&#39;utilisation de valeurs de thickness très faibles. Il s’agit d’un problème connu.

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Couleurs splines</b> <i>Couleur</i> | Coordonnées des points des splines d&#39;entrée codés dans les canaux RVBA d&#39;une image couleur :<br><b>R</b> - position X<br><b>G</b> - position Y<br><b>B</b> - Height<br><b>A</b> - données compressées :<br>- Signe : la spline est fermée (négative) ou ouverte (positive);<br>- Valeur absolue : Thickness + 1. |
| <b>Données splines</b> <i>Couleur</i> | Données supplémentaires des splines d&#39;entrée codées dans les canaux RVBA d&#39;une image couleur.<br><b>R</b> - Tangentes X<br><b>G</b> - Tangentes Y<br><b>B</b> - Inutilisé<br><b>A</b> - Inutilisé |
| <b>Quantité de spline</b> <i>Entier</i> | Nombre de splines d&#39;entrée. |
| <b>Courbe De Profil D&#39;Atténuation</b> <i>Niveaux de gris</i> | <span id="_Hlk135812146"></span>Image décrivant une courbe en utilisant les valeurs de sa première ligne de pixels. Lorsque le paramètre Profil d&#39;atténuation est défini sur Courbe de profil d&#39;entrée, cette entrée est utilisée pour contrôler la gamme de dégradé pour l&#39;atténuation des données vectorielles d&#39;écoulement dessinées le long de la spline.<br>Vous pouvez utiliser un nœud [Courbe](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/curve/curve.md) pour créer la courbe. |

<a name="outputs"></a>

## Sorties

|  |  |
|:---|:---|
| <b>Sortie</b> <i>Couleur</i> | Flux de sortie codé dans une image couleur. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Quantité de segments</b> <i>Nombre entier</i> | Les splines sont simplifiées en segments avant que les données de flux vectoriel ne les traversent. Plus le nombre de segments est élevé, plus la cartographie de flux le long des courbes est fluide. |
| <b>Mode</b> <i>Nombre entier</i> | Méthode de sélection des splines le long desquelles les données de flux vectoriel doivent être dessinées :<br><br>- <i>Dessiner une liste de splines</i> : toutes les splines de la liste d&#39;entrée sont utilisées ;<br>- <i>Dessiner une seule spline</i> : seule la spline avec l&#39;index spécifié est utilisée ;<br>- <i>Dessiner une plage de splines</i> : seules les splines dont l&#39;index est inclus dans la plage spécifiée sont utilisées. |
| <b>Dessiner l&#39;index spline</b> <i>Entier</i> (disponible lorsque &#39;Mode&#39; est défini sur &#39;Dessiner une seule spline&#39;) | Index de la spline le long de laquelle les données de flux vectoriel doivent être tracées. |
| <b>Tracer la plage de splines</b> <i>Entier 2</i> (disponible lorsque &#39;Mode&#39; est défini sur &#39;Dessiner la plage de splines&#39;) | Plage d&#39;index pour les splines le long desquelles les données de flux vectoriel doivent être tracées. |
| <b>Mode Thickness</b> <i>Nombre entier</i> | Méthode de définition du thickness des données de flux vectoriel dessinées<br><br>- <i>Manuel</i> : définissez le thickness explicitement avec une valeur arbitraire ;<br>- <i>À partir de la spline</i> : utilisez le thickness de la spline. |
| <b>Thickness</b> <i>Flottant</i> (disponible lorsque &#39;Mode Thickness&#39; est défini sur &#39;Manuel&#39;) | Valeur arbitraire pour le thickness des données de flux vectoriel dessinées le long des splines. |
| <b>Multiplicateur de Thickness</b> <i>Flottant</i> (disponible lorsque le mode Thickness est défini sur À partir de la spline) | Multiplicateur global du thickness des données de flux vectoriel dessinées le long des splines, lorsque ce thickness est piloté par celui des splines. |
| <b>Direction</b> <i>Nombre entier</i> | Direction du flux vectoriel par rapport à la spline.<br><br>- <i>Tangente</i> : utiliser le vecteur de tangente de la spline ;<br>- <i>Normal</i> : utiliser le vecteur normal de la spline ;<br>- <i>Normal Miroir</i> : utiliser la version miroir du vecteur normal de la spline. |
| <b>Inverser la direction</b> <i>Booléen</i> | Inverse la direction des splines, ce qui a également un impact sur la direction du vecteur d&#39;écoulement. |
| <b>Profil d&#39;atténuation</b> <i>Nombre entier</i> | Dégradé utilisé pour tracer l&#39;atténuation des données vectorielles d&#39;écoulement dessinées le long de la spline :<br><br>- <i>Linéaire</i> : utilisez un dégradé linéaire ;<br>- <i>Gaussien</i> : utilisez un dégradé gaussien<br>- <i>Courbe de profil d&#39;entrée</i> : utilisez la courbe fournie à l&#39;entrée de la courbe de profil d&#39;atténuation comme dégradé. |
| <b>Démarrer l&#39;atténuation</b> <i>Booléen</i> | <span id="_Hlk135769398"></span>Ajoute un demi-cercle au début de la spline. Le demi-cercle utilise la même atténuation que la spline. |
| <b>Fin de l&#39;atténuation</b> <i>Booléen</i> | Ajoute un demi-cercle à l&#39;extrémité de la spline. Le demi-cercle utilise la même atténuation que la spline. |
| <b>Atténuation De L&#39;Height De La Spline</b> <i>Flotter</i> | L’intensité des données vectorielles de flux dessinées le long de la spline est multipliée par rapport à l’height de la spline, où les données dessinées s’estompent jusqu’à la couleur neutre (0,5, 0,5, 0) de l’arrière-plan lorsque l’height se rapproche de 0. |
| <b>Correction Non Carrée</b> <i>Booléen</i> | Ajustez la position et le thickness des points pour conserver la forme de la spline dans des résolutions autres que carrées. Cela a également un impact sur la distribution uniforme. |

## Exemples

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-flow-mapper.resources/SplineFlowMapper-Variant1-Before.jpg" alt="SplineFlowMapper-Variant1-Before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="spline-flow-mapper.resources/SplineFlowMapper-Variant1-After.jpg" alt="SplineFlowMapper-Variant1-After">
      <br><i>Après</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![Exemple de nœud 2](spline-flow-mapper.resources/SplineFlowMapper-Demo.gif "Exemple de nœud 2")

</td>
</tr>
</table>
