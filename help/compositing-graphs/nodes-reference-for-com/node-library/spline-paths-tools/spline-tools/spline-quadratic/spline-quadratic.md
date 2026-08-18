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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '843'
ht-degree: 0%

---


# Spline (quadratique)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Spline (quadratique) : icon](../../../../../../assets/spline-quadratic-icon.png "Spline (quadratique) : icon")

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

## Connecteurs d’entrée

|  |  |
| --- | --- |
| <b>Aperçu</b> *Niveaux de gris* | Aperçu des splines d’entrée sous forme d’image en niveaux de gris. |
| <b>Couleurs splines</b> *Couleur* | Coordonnées des points des splines d&#39;entrée codés dans les canaux RVBA d&#39;une image couleur : <b>R</b> - Position X <b>G</b> - Position Y <b>B</b> - Height <b>A</b> - Données compressées : - Signe : la spline est fermée (négative) ou ouverte (positive) ; - Valeur absolue : Thickness + 1. |
| <b>Données splines</b> *Couleur* | Données supplémentaires des splines d&#39;entrée codées dans les canaux RVBA d&#39;une image couleur : <b>R</b> - Tangentes X <b>G</b> - Tangentes Y <b>B</b> - Tangentes Z <b>A</b> - Inutilisées |
| <b>Quantité de spline</b> *Nombre entier* | Nombre de splines d&#39;entrée. |

## Connecteurs de sortie

|  |  |
| --- | --- |
| <b>Aperçu</b> *Niveaux de gris* | Aperçu des splines de sortie sous forme d’image en niveaux de gris. |
| <b>Couleurs splines</b> *Couleur* | Coordonnées des points des splines de sortie codés dans les canaux RVBA d&#39;une image couleur : <b>R</b> - Position X <b>G</b> - Position Y <b>B</b> - Height <b>A</b> - Données compressées : - Signe : la spline est fermée (négative) ou ouverte (positive) ; - Valeur absolue : Thickness + 1. |
| <b>Données splines</b> *Couleur* | Données supplémentaires des splines de sortie codées dans les canaux RVBA d&#39;une image couleur : <b>R</b> - Tangentes X <b>G</b> - Tangentes Y <b>B</b> - Tangentes Z <b>A</b> - Inutilisées |
| <b>Quantité de spline</b> *Nombre entier* | Nombre de splines de sortie. |

## Paramètres

|  |  |
| --- | --- |
| <b>Inverser la direction</b> *Booléen* | Inverse la direction de la spline. |
| <b>Distribution uniforme</b> *Booléen* | Lorsque *True*, les points de la spline sont espacés de manière régulière du début à la fin. |
| <b>Ajouter une spline d&#39;entrée</b> *Booléen* | Ajoute la spline générée à la fin de la liste des splines connectées aux entrées de <b>spline</b>. |
| <b>Correction non carrée</b> *Booléen* | Ajustez la position et le thickness des points pour conserver la forme de la spline dans des résolutions autres que carrées. Cela a également un impact sur la distribution uniforme. |
| <b>Smoothness</b> *Flotter* | Ajuste la *plage de l&#39;arc* formé par la spline, où 1 signifie que la spline est entièrement incurvée sur toute sa longueur et 0 signifie qu&#39;elle est entièrement droite. L&#39;arc progresse à partir du point <b>p3</b> le long de la spline jusqu&#39;à ses extrémités. |

+++Hauteur

|  |  |
| --- | --- |
| <b>height de démarrage</b> *Flotter* | Ajuste l&#39;height du point <b>p1</b> où une valeur inférieure signifie un emplacement plus bas ou plus profond.  Cela a un impact sur l&#39;height de la spline à <b>p1</b>. |
| <b>height final</b> *Flotter* | Ajuste l&#39;height du point <b>p3</b> où une valeur inférieure signifie un emplacement plus bas ou plus profond.  Cela a un impact sur le thickness de la spline à <b>p3</b>. |
| <b>height de tangente automatique</b> *Booléen* | Ajuste l&#39;height du point <b>p3</b> où une valeur inférieure signifie un emplacement plus bas ou plus profond.  Cela a un impact sur le thickness de la spline à <b>p3</b>. |
| <b>height tangent</b> *Flotter* | Ajuste l&#39;height piloté par les tangentes contrôlées par le point <b>p2</b>.  Cela a un impact sur l&#39;height le long de la spline, car il s&#39;éloigne de <b>p1</b> et entre dans <b>p3</b>.   *Remarque :* ce paramètre n&#39;est disponible que lorsque <b>height de tangente automatique</b> est défini sur « False ». |


+++

+++Épaisseur

|  |  |
| --- | --- |
| <b>Démarrer le thickness</b> *Flotter* | Ajuste le thickness du point <b>p1</b>. Cela a un impact sur le thickness de la spline à <b>p1</b>.   *Remarque :* le Thickness est utilisé par des nœuds spline spécifiques. |
| <b>Fin de thickness</b> *Flotter* | Ajuste le thickness du point <b>p3</b>. Cela a un impact sur le thickness de la spline à <b>p3</b>.   *Remarque :* le Thickness est utilisé par des nœuds spline spécifiques. |
| <b>thickness tangent automatique</b> *Booléen* | Définit automatiquement le thickness des tangentes de la spline pour une interpolation linéaire entre le <b>Thickness de début</b> et le <b>Thickness de fin</b>.   *Remarque :* le Thickness est utilisé par des nœuds spline spécifiques. |
| <b>thickness tangent</b> *Flotter* | Ajuste le thickness entraîné par les tangentes contrôlées par le point <b>p2</b>.  Cela a un impact sur le thickness le long de la spline, car il s&#39;éloigne de <b>p1</b> et entre dans <b>p3</b>.   *Remarque :* le Thickness est utilisé par des nœuds spline spécifiques.  *Remarque 2 :* ce paramètre est uniquement disponible lorsque <b>thickness tangent automatique</b> est défini sur « False ». |


+++

+++Coordonnées des points

|  |  |
| --- | --- |
| <b>p1</b> *Float2* | Définit la position du point <b>p1</b> dans l&#39;espace de texture. |
| <b>p2</b> *Float2* | Définit la position du point <b>p2</b> dans l&#39;espace de texture.  Le point <b>p2</b> contrôle les *tangentes* des points <b>p1</b> et <b>p3</b>. |
| <b>p3</b> *Float2* | Définit la position du point <b>p3</b> dans l&#39;espace de texture. |


+++

+++Prévisualiser

|  |  |
| --- | --- |
| <b>Afficher les tangentes</b> *Booléen* | Affiche la tangente de « sortie » du point <b>p1</b> et la tangente d&#39;« entrée » du point <b>p3</b> dans la sortie <b>Aperçu</b>. Inverse la direction de la spline. |
| <b>Afficher l&#39;assistant de direction</b> *Booléen* | Affiche un point au début de la spline et une flèche à sa fin dans la sortie <b>Aperçu</b>. |
| <b>Afficher l&#39;enveloppe de thickness</b> *Booléen* | Affiche des lignes supplémentaires sur les thickness de la spline. |
| <b>Quantité de segments</b> *Nombre entier* | Ajuste le nombre de segments utilisés pour dessiner la visualisation de la spline dans la sortie <b>Aperçu</b>.  Plus la valeur est élevée, plus la ligne est lisse. |
| <b>Thickness (px)</b> *Flotter* | Ajuste le thickness en pixels de la visualisation de la spline dans la sortie <b>Aperçu</b>. |


+++

## Exemples

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Spline (Quadratique) : Exemple 1](../../../../../../assets/spline-quadratic-example-1.png "Spline (Quadratique) : Exemple 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Spline (Quadratique) : Exemple 2](../../../../../../assets/spline-quadratic-example-2.png "Spline (Quadratique) : Exemple 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Spline (Quadratique) : Demo](../../../../../../assets/spline-quadratic-demo.gif "Spline (Quadratique) : Demo"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
