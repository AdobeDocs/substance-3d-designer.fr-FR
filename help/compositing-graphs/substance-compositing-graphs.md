---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs.html"
breadcrumb-title: ''
description: Découvrez les graphes de composition de Substances dans Substance 3D Designer pour créer des textures procédurales et des workflows de matériau.
helpx_creative_field: ""
helpx_description: Designer > Substance graphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Graphes Substance
user-guide-description: ''
user-guide-title: ''
source-git-commit: 7e53313d3c368803a95ebb1f9eee712ae2a05817
workflow-type: tm+mt
source-wordcount: '345'
ht-degree: 1%

---


# Graphes Substance

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

[![](substance-compositing-graphs.resources/graph-5.png){width="120px"}](https://substance3d.adobe.com/)

</td>
<td width="100.00%" style="border: 0;" valign="top">

Les [graphes de Substance](https://substance3d.adobe.com/) sont le principal type de graphe créé dans Substance 3D Designer. Leur objectif est de <b>générer et traiter des données d&#39;image 2D</b> qui ne sont pas limitées à une résolution, une couleur ou une forme définie. Ils sont conçus comme des outils de traitement d&#39;image et de génération extrêmement polyvalents, et pas seulement comme des résultats statiques prédéfinis.

Les résultats peuvent se présenter sous la forme d’un motif simple en noir et blanc, d’un filtre qui s’exécute uniquement sur les autres images et ne génère pas de contenu à lui seul, ou même d’un matériau procédural complet avec plusieurs canaux.

Les graphes de Substance sont[le type de graphe le plus largement pris en charge](../getting-started/overview/overview.md). Ils peuvent être exportés et utilisés dans une multitude de workflows différents.

</td>
</tr>
</table>

## Exemples

Vous trouverez ci-dessous quelques exemples typiques de cas d’utilisation courants.

+++Forme simple
![Forme simple dans le graphe Substance](substance-compositing-graphs.resources/simpleshape.png "Forme simple dans le graphe Substance"){width="512px"}



Une forme de masque simple pour une décalcomanie est créée en générant[un morceau de texte](../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md) et une [forme de disque](../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape/shape.md), en [extrayant le bord](../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/edge-detect/edge-detect.md) du disque et en [les fusionnant](../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md) avant de les définir comme [sortie](../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) finale.

Le texte portant le numéro ou le thickness du contour peut être exposé à l’extérieur pour rendre ce graphe plus dynamique.

+++

+++Filtre Réglage
![Filtre d&#39;ajustement dans le graphique de Substance](substance-compositing-graphs.resources/simplefilter.png "Filtre d&#39;ajustement dans le graphique de Substance"){width="512px"}



Un graphique de filtre prend une carte normale comme [entrée](../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md) (avec un aperçu personnalisé), [la convertit en courbure](../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-smooth/curvature-smooth.md), puis [ajuste le contraste](../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md) pour créer un masque de bords convexes en tant que [sortie](../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) finale.

Les valeurs de contraste définies dans l’histogramme peuvent être affichées, ce qui en fait un filtre simple mais utile en combinaison avec l’emplacement d’entrée dynamique.

+++

+++Matière complète
![Matière complète dans le graphique en Substances](substance-compositing-graphs.resources/simplematerial.png "Matière complète dans le graphique en Substances"){width="512px"}



Un graphique plus complexe[fusionne deux Matériaux de base](../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/material-blend/material-blend.md). L&#39;un des [Matériaux de base](../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/base-material/base-material.md) est simple, tandis que l&#39;autre utilise des entrées personnalisées pour susciter l&#39;intérêt. Un masque est utilisé pour déterminer lequel des deux matériaux apparaît à l&#39;endroit où il se trouve avant d&#39;être défini comme [sorties](../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) finales.

Cet exemple utilise les [modes de création de liens](../interface/the-graph-view/link-creation-modes/link-creation-modes.md) pour simplifier l&#39;utilisation de plusieurs liens.

+++
