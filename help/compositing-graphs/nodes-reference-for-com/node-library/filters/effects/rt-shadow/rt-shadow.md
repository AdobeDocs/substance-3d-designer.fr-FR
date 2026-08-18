---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/rt-shadow.html"
breadcrumb-title: ''
description: Utilisez le nœud Ombres RT pour calculer des informations d'ombre en temps réel à partir de la géométrie afin de créer des effets d'éclairage dynamiques.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > RT Shadows
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Tons foncés RT
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 0%

---


# Tons foncés RT

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

Icône de nœud ![Ombres RT](../../../../../../assets/rt-shadow.png "Ombres RT")

<b>Entrée :</b> *Filtres/Effets*

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Description

Génère des ombres avec lancer de rayon à partir d’une entrée de courbe de transfert d’height.

Ce nœud ne doit pas être utilisé en combinaison avec le moteur CPU (SSE) en raison du temps de calcul.

</td>
</tr>
</table>

## Paramètres

<b>Exemples</b> *Nombre entier*\
Nombre de rayons utilisés pour calculer les ombres.\
Plus la valeur est élevée, plus le résultat est fluide et précis, au détriment des performances.

<b>Mode</b> *Nombre entier*\
Méthode de dessin des ombres sur la surface.

<b>Échelle D&#39;Height</b> *Flottant*\
Multiplicateur de l’intensité de la courbe d’height d’entrée.

<b>Position Claire </b>*Float2*\
La position de la source lumineuse sur une sphère entourant la surface :
* <b>X</b> : position horizontale, en nombre de tours ;
* <b>Y</b> : position verticale, où 0,5 correspond au zénith et 0/1 à l&#39;horizon.

<b>Intensité de la lumière</b> *Flottant*\
Intensité de la source lumineuse.

<b>Taille légère</b> *Float2* (disponible lorsque <b>Mode</b> est défini sur *Ombré*)\
Taille de la source de lumière sous forme de rectangle.

<b>Échelle de la lumière (ombres douces)</b> *Flotter*\
Multiplicateur de la contribution de la <b>taille de la lumière</b> à la direction des rayons.\
Plus la valeur est élevée, plus les ombres sont lisses.

<b>Garder La Lumière Au-Dessus De L&#39;Horizon</b> *Booléen*\
Si la <b>position de la lumière</b> est définie de manière à placer la lumière sous l&#39;horizon, ce paramètre empêche la lumière de franchir ce seuil, ce qui signifie que les valeurs Y sont ajustées à la plage [0;1].

<b>Opacité de l&#39;ombre</b> *Flottant*\
Multiplicateur de l’opacité des tons foncés dessinés sur la surface.

<b>Atténuation Des Ombres</b> *Flottant*\
Multiplicateur pour l&#39;atténuation des ombres à mesure qu&#39;elles s&#39;éloignent de leur projection.\
Une valeur de 0 donne des ombres uniformes (des ombres légères sont toujours appliquées).

<b>Longueur max. des ombres</b> *Flottant*\
Distance maximale à laquelle une ombre peut être dessinée de sa projection.\
Une valeur de 0 ne produit aucune ombre visible.

## Exemples d’images

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Nœud des ombres RT - Exemple 1](../../../../../../assets/RTShadows-01.jpg "Nœud des ombres RT - Exemple 1")

</td>
<td style="border: 0;" valign="top">

![Nœud des ombres RT - Exemple 2](../../../../../../assets/RTShadows-02.jpg "Nœud des ombres RT - Exemple 2")

</td>
<td style="border: 0;" valign="top">

![Nœud des ombres RT - Exemple 3](../../../../../../assets/RTShadows-03.jpg "Nœud des ombres RT - Exemple 3")

</td>
</tr>
</table>
