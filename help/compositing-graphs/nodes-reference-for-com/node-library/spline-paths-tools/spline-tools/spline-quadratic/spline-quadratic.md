---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-quadratic.html"
breadcrumb-title: ''
description: Utilisez le nœud quadratique spline pour créer des splines quadratiques lisses avec trois points de contrôle.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline (Quadratic)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Spline (quadratique)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4ae20991693573dd44016a411c233b071fa96df6
workflow-type: tm+mt
source-wordcount: '824'
ht-degree: 0%

---


# Spline (quadratique)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Spline (quadratique) : icon](spline-quadratic.resources/spline-quadratic-icon.png "Spline (quadratique) : icon")

<b>Entrée :</b> Outils Spline Et Tracé > Outils spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Génère une spline unique entre deux points <b>p1</b> et <b>p3</b> à des emplacements arbitraires.

La trajectoire de la spline est contrôlée par la tangente « out » de <b>p1</b> et la tangente « in » de <b>p3</b>, *les deux* contrôlées par un seul point <b>p3</b>.

L&#39;étendue de l&#39;arc formé par la spline est *réglable*, de sorte qu&#39;une partie de sa trajectoire à partir de ses extrémités puisse rester droite.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Aperçu</b> <i>Niveaux de gris</i> | Aperçu des splines d&#39;entrée sous forme d&#39;image en niveaux de gris. |
| <b>Couleurs splines</b> <i>Couleur</i> | Coordonnées des points des splines d&#39;entrée codés dans les canaux RVBA d&#39;une image couleur :<br><b>R</b> - position X<br><b>G</b> - position Y<br><b>B</b> - Height<br><b>A</b> - données compressées :<br> - signe : la spline est fermée (négative) ou ouverte (positive);<br> - Valeur absolue : Thickness + 1. |
| <b>Données splines</b> <i>Couleur</i> | Données supplémentaires des splines d&#39;entrée codées dans les canaux RVBA d&#39;une image couleur : <br><b>R</b> - Tangentes X<br><b>G</b> - Tangentes Y<br><b>B</b> - Tangentes Z<br><b>A</b> - Inutilisées |
| <b>Quantité de spline</b> <i>Entier</i> | Nombre de splines d&#39;entrée. |

<a name="outputs"></a>

## Sorties

|  |  |
|:---|:---|
| <b>Aperçu</b> <i>Niveaux de gris</i> | Aperçu des splines de sortie sous forme d&#39;image en niveaux de gris. |
| <b>Couleurs splines</b> <i>Couleur</i> | Coordonnées des points des splines de sortie codés dans les canaux RVBA d&#39;une image couleur :<br><b>R</b> - position X<br><b>G</b> - position Y<br><b>B</b> - Height<br><b>A</b> - données compressées :<br> - signe : la spline est fermée (négative) ou ouverte (positive);<br> - Valeur absolue : Thickness + 1. |
| <b>Données splines</b> <i>Couleur</i> | Données supplémentaires des splines de sortie codées dans les canaux RVBA d&#39;une image couleur : <br><b>R</b> - Tangentes X<br><b>G</b> - Tangentes Y<br><b>B</b> - Tangentes Z<br><b>A</b> - Inutilisées |
| <b>Quantité de spline</b> <i>Nombre entier</i> | Nombre de splines de sortie. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Inverser la direction</b> <i>Booléen</i> | Inverse la direction de la spline. |
| <b>Distribution uniforme</b> <i>Booléen</i> | Lorsque <i>True</i>, les points de la spline sont espacés de manière régulière du début à la fin. |
| <b>Ajouter une spline d&#39;entrée</b> <i>Booléen</i> | Ajoute la spline générée à la fin de la liste des splines connectées aux entrées de <b>spline</b>. |
| <b>Correction non carrée</b> <i>Booléen</i> | Ajustez la position et le thickness des points pour conserver la forme de la spline dans des résolutions autres que carrées. Cela a également un impact sur la distribution uniforme. |
| <b>Smoothness</b> <i>Flotter</i> | Ajuste la <i>plage de l&#39;arc</i> formé par la spline, où 1 signifie que la spline est entièrement incurvée sur toute sa longueur et 0 signifie qu&#39;elle est entièrement droite. L&#39;arc progresse à partir du point <b>p3</b> le long de la spline jusqu&#39;à ses extrémités. |
| <b>Height</b> |  |
| <b>height de démarrage</b> <i>Flottant</i> | Ajuste l&#39;height du point <b>p1</b> où une valeur inférieure signifie un emplacement plus bas ou plus profond.<br>Cela a un impact sur l&#39;height de la spline à <b>p1</b>. |
| <b>height final</b> <i>Flottant</i> | Ajuste l&#39;height du point <b>p3</b> où une valeur inférieure signifie un emplacement plus bas ou plus profond.<br>Cela a un impact sur le thickness de la spline à <b>p3</b>. |
| <b>height de la tangente automatique</b> <i>Booléen</i> | Ajuste l&#39;height du point <b>p3</b> où une valeur inférieure signifie un emplacement plus bas ou plus profond.<br>Cela a un impact sur le thickness de la spline à <b>p3</b>. |
| <b>height de la Tangente</b> <i>Flottant</i> | Ajuste l&#39;height piloté par les tangentes contrôlées par le point <b>p2</b>.<br>Cela a un impact sur l&#39;height le long de la spline, car il s&#39;éloigne de <b>p1</b> et entre dans <b>p3</b>.<br><i>Remarque :</i> ce paramètre n&#39;est disponible que lorsque <b>height de tangente automatique</b> est défini sur « False ». |
| <b>Thickness</b> |  |
| <b>Démarrer le thickness</b> <i>Flottant</i> | Ajuste le thickness du point <b>p1</b>. Cela a un impact sur le thickness de la spline à <b>p1</b>.<br><i>Remarque :</i> le Thickness est utilisé par des nœuds de spline spécifiques. |
| <b>Fin de thickness</b> <i>Flottant</i> | Ajuste le thickness du point <b>p3</b>. Cela a un impact sur le thickness de la spline à <b>p3</b>.<br><i>Remarque :</i> le Thickness est utilisé par des nœuds de spline spécifiques. |
| <b>thickness de tangente automatique</b> <i>Booléen</i> | Définit automatiquement le thickness des tangentes de spline pour une interpolation linéaire entre le <b>Thickness de début</b> et le <b>Thickness de fin</b>.<br><i>Remarque :</i> le Thickness est utilisé par des nœuds de spline spécifiques. |
| <b>thickness de Tangente</b> <i>Flottant</i> | Ajuste le thickness entraîné par les tangentes contrôlées par le point <b>p2</b>.<br>Cela a un impact sur le thickness le long de la spline, car il s&#39;éloigne de <b>p1</b> et entre dans <b>p3</b>.<br><i>Remarque :</i> le Thickness est utilisé par des nœuds de spline spécifiques.<br><i>Remarque 2 :</i> ce paramètre est uniquement disponible lorsque <b>thickness de tangente automatique</b> est défini sur « False ». |
| <b>Coordonnées des points</b> |  |
| <b>p1</b> <i>Flottant 2</i> | Définit la position du point <b>p1</b> dans l&#39;espace de texture. |
| <b>p2</b> <i>Flottant 2</i> | Définit la position du point <b>p2</b> dans l&#39;espace de texture.<br>Le point <b>p2</b> contrôle les <i>tangentes</i> des points <b>p1</b> et <b>p3</b>. |
| <b>p3</b> <i>Flottant 2</i> | Définit la position du point <b>p3</b> dans l&#39;espace de texture. |
| <b>Aperçu</b> |  |
| <b>Afficher les tangentes</b> <i>Booléen</i> | Affiche la tangente « out » de <b>p1</b> et la tangente « in » de <b>p3</b> dans la sortie <b>Aperçu</b>. Inverse la direction de la spline. |
| <b>Afficher l&#39;assistant de direction</b> <i>Booléen</i> | Affiche un point au début de la spline et une flèche à sa fin dans la sortie <b>Aperçu</b>. |
| <b>Afficher l&#39;enveloppe de thickness</b> <i>Booléen</i> | Affiche des lignes supplémentaires sur les thickness de la spline. |
| <b>Quantité de segments</b> <i>Entier</i> | Ajuste le nombre de segments utilisés pour dessiner la visualisation de la spline dans la sortie <b>Aperçu</b>.<br>Plus la valeur est élevée, plus la ligne est lisse. |
| <b>Thickness (px)</b> <i>Flottant</i> | Ajuste le thickness en pixels de la visualisation de la spline dans la sortie <b>Aperçu</b>. |

## Exemples

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Spline (Quadratique) : Exemple 1](spline-quadratic.resources/spline-quadratic-example-1.png "Spline (Quadratique) : Exemple 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Spline (Quadratique) : Exemple 2](spline-quadratic.resources/spline-quadratic-example-2.png "Spline (Quadratique) : Exemple 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Spline (Quadratique) : Demo](spline-quadratic.resources/spline-quadratic-demo.gif "Spline (Quadratique) : Demo"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
