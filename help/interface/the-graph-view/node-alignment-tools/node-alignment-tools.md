---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/the-graph-view/node-alignment-tools.html"
breadcrumb-title: ''
description: Utilisez les outils d’alignement des nœuds pour organiser et aligner les nœuds dans la vue graphique afin de rendre les graphiques plus nets et plus lisibles.
helpx_creative_field: ""
helpx_description: Designer > Interface > The graph view > Node alignment tools
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Outils d’alignement des nœuds
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 1%

---


# Outils d’alignement des nœuds

![Barre d&#39;outils d&#39;alignement des nœuds](node-alignment-tools.resources/node-alignment-tools-01.png "Barre d&#39;outils d&#39;alignement des nœuds"){zoomable="yes"}

Les outils d&#39;alignement des nœuds vous permettent d&#39;organiser les nœuds dans des graphiques pour améliorer leur lisibilité et leur expérience de création. Ils proposent des actions permettant d’aligner les nœuds, de les répartir uniformément et de les aligner sur la grille.

Ils agissent sur les <b>nœuds actuellement sélectionnés uniquement</b>.

>[!NOTE]
>
> Raccourcis clavier
> 
> Certaines actions disposent de raccourcis clavier pour un accès rapide : H, V et S. Ils s’affichent entre parenthèses dans la liste des actions ci-dessous.
> 
> Notez que ces raccourcis remplaceront tout [raccourci clavier attribué aux nœuds](../../../interface/preferences-window/preferences-window.md).

## Alignements

Les nœuds peuvent être alignés horizontalement et verticalement, avec trois modes pour chaque axe :

### Alignements horizontaux

<b>![](node-alignment-tools.resources/node-alignment-tools-02.png) Gauche :</b> alignez le côté gauche des nœuds sélectionnés sur le côté gauche du nœud le plus à gauche.

<b>![](node-alignment-tools.resources/node-alignment-tools-03.png) Centre (H) :</b> Alignez le centre horizontal des nœuds sélectionnés sur le centre horizontal du cadre de sélection qui les entoure.

<b>![](node-alignment-tools.resources/node-alignment-tools-04.png) Droite :</b> alignez le côté droit des nœuds sélectionnés sur le côté droit du nœud le plus à droite.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Outils d&#39;alignement de nœud : left](node-alignment-tools.resources/node-alignment-tools-05.gif "Outils d&#39;alignement de nœud : left"){zoomable="yes"}

*À Gauche*

</td>
<td style="border: 0;" valign="top">

![Outils d&#39;alignement des nœuds : centre](node-alignment-tools.resources/node-alignment-tools-06.gif "Outils d&#39;alignement des nœuds : centre"){zoomable="yes"}

*Centrer*

</td>
<td style="border: 0;" valign="top">

![Outils d&#39;alignement de nœud : right](node-alignment-tools.resources/node-alignment-tools-07.gif "Outils d&#39;alignement de nœud : right"){zoomable="yes"}

*Droite*

</td>
</tr>
</table>

### Alignements verticaux

<b>![](node-alignment-tools.resources/node-alignment-tools-08.png) Haut :</b> Alignez le bord supérieur des nœuds sélectionnés sur le bord supérieur du nœud le plus haut.

<b>![](node-alignment-tools.resources/node-alignment-tools-09.png) Milieu (V) :</b> Alignez le centre vertical des nœuds sélectionnés sur le centre vertical du cadre de sélection qui les entoure.

<b>![](node-alignment-tools.resources/node-alignment-tools-10.png) Bas :</b> Alignez le bas des nœuds sélectionnés sur le bas du nœud le plus bas.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Outils d&#39;alignement des nœuds : top](node-alignment-tools.resources/node-alignment-tools-11.gif "Outils d&#39;alignement des nœuds : top"){zoomable="yes"}

*Haut*

</td>
<td style="border: 0;" valign="top">

![Outils d&#39;alignement de nœud : milieu](node-alignment-tools.resources/node-alignment-tools-12.gif "Outils d&#39;alignement de nœud : milieu"){zoomable="yes"}

*Milieu*

</td>
<td style="border: 0;" valign="top">

![Outils d&#39;alignement des nœuds : bas](node-alignment-tools.resources/node-alignment-tools-13.gif "Outils d&#39;alignement des nœuds : bas"){zoomable="yes"}

*Bas*

</td>
</tr>
</table>

### Empilement

L&#39;option ![](node-alignment-tools.resources/node-alignment-tools-14.png) <b>Empiler</b> vous permet d&#39;<b>éviter tout chevauchement</b> lors de l&#39;utilisation des alignements. Elle est activée par défaut.

Lorsque cette option est activée, les nœuds sont déplacés le plus loin possible vers la position de référence jusqu&#39;à ce qu&#39;ils entrent en collision avec un autre nœud dans la sélection. Cela permet de les empiler dans l’axe sélectionné avec une marge d’une cellule de grille moyenne entre chaque nœud.

![Outils d&#39;alignement des nœuds : empilement](node-alignment-tools.resources/node-alignment-tools-15.gif "Outils d&#39;alignement des nœuds : empilement"){zoomable="yes"}

## Distributions

Les nœuds peuvent être répartis uniformément entre les nœuds à chaque extrémité de la sélection actuelle sur l&#39;axe souhaité.

<b>![](node-alignment-tools.resources/node-alignment-tools-16.png) horizontalement :</b> nœuds sont répartis uniformément entre les nœuds les plus à gauche et à droite de la sélection.

<b>![](node-alignment-tools.resources/node-alignment-tools-17.png) Verticalement :</b> nœuds sont répartis uniformément entre les nœuds les plus élevés et les plus bas de la sélection.

Les distributions visent un <b>espacement régulier</b> entre les nœuds, quelle que soit leur taille.

Lorsque plusieurs nœuds ont leurs centres parfaitement alignés sur l&#39;axe sélectionné, ils restent et sont <b>traités comme un</b> dans la distribution. Le *plus grand* des nœuds alignés est utilisé pour calculer l&#39;espacement pair.

Notez que lorsque la taille totale des nœuds sélectionnés est supérieure à l&#39;espace disponible sur l&#39;axe sélectionné, des chevauchements peuvent se produire.

<table>
<tr style="border: 0;">
<td width="58.33%" style="border: 0;" valign="top">

![Outils d&#39;alignement des nœuds : distribution horizontale](node-alignment-tools.resources/node-alignment-tools-18.gif "Outils d&#39;alignement des nœuds : distribution horizontale"){zoomable="yes"}

*Horizontalement*

</td>
<td width="100.00%" style="border: 0;" valign="top">

![Outils d&#39;alignement des nœuds : distribution verticale](node-alignment-tools.resources/node-alignment-tools-19.gif "Outils d&#39;alignement des nœuds : distribution verticale"){zoomable="yes"}

*Verticalement*

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="58.33%" style="border: 0;" valign="top">

## Magnétisme de la grille

L&#39;action <b>Accrocher (S) ![](node-alignment-tools.resources/node-alignment-tools-20.png)</b> déplace chaque nœud sélectionné de sorte que son coin supérieur gauche repose sur le point le plus proche sur la grille moyenne.

</td>
<td width="100.00%" style="border: 0;" valign="top">

![Outils d&#39;alignement de nœud : accrochage à la grille](node-alignment-tools.resources/node-alignment-tools-21.gif "Outils d&#39;alignement de nœud : accrochage à la grille"){zoomable="yes"}

</td>
</tr>
</table>
