---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/getting-started/workflow-overview.html"
breadcrumb-title: ''
description: Découvrez le workflow essentiel pour créer des matériaux procéduraux dans Substance 3D Designer du début à la fin.
helpx_creative_field: ""
helpx_description: Designer > Getting started > Workflow overview
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Présentation du workflow
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '1206'
ht-degree: 0%

---


# Présentation du workflow

Substance 3D Designer est un éditeur basé sur des nœuds. Cela signifie que presque tous les types de projet ou de ressource impliqueront de placer des nœuds (composantes) et de les connecter pour créer une chaîne d’opérations (un Graphe). Cette page explique le concept des workflows basés sur les nœuds et fournit un résumé des 3 principaux types de Graphes que vous pouvez créer dans Designer.

## Table des matières

[Workflow basé sur les nœuds](#node-workflow)

[Workflow d’Instance de graphe](#instance-workflow)

[Paramètres personnalisés](#custom-parameters)

[types de graphe](#graph-types)

![Flux de données simplifié](workflow-overview.resources/graph-direction.png "Flux de données simplifié")

## Workflow basé sur les nœuds

Travailler dans Designer est différent des autres logiciels de retouche d’images 2D tels que Photoshop. Au lieu d&#39;effectuer une action manuellement (comme ajuster la saturation en accédant à une option de menu et en modifiant un curseur), <b>construisez les étapes logiques</b> de la modification ou de la création de votre image. Cela se produit en construisant un réseau de petits blocs de construction appelés «nœuds». Les données d&#39;image se déplacent de <b> gauche à droite</b> à travers les composantes, connectées par des liens qui déterminent le chemin des informations. Chaque nœud, s&#39;il est connecté, contribuera aux résultats finaux.

Le principal avantage est que votre workflow devient <b>non linéaire</b>. Contrairement aux actions exécutées manuellement qui sont consignées dans une pile de données d&#39;historique, vous pouvez toujours remplacer ou modifier un nœud à tout moment. Si vous estimez que votre tout premier réglage de contraste, qui a affecté le résultat de votre image jusqu’à la fin, a été trop important, vous pouvez toujours revenir en arrière et l’ajuster ou même le découper complètement, sans perdre tout le travail que vous avez effectué par la suite.

![Instances de graphe simplifiées](workflow-overview.resources/sub-graph.png "Instances de graphe simplifiées")

## Workflow d’Instance de graphe

L’instanciation de Graphes est un processus essentiel dans Designer. Il vous permet de créer vos propres nœuds en prenant n&#39;importe quelle taille ou type de Graphe et en le regroupant comme nouveau bloc de construction Node. Ces types de nœuds sont appelés « Instances de graphe » Cela vous permet d&#39;être beaucoup plus efficace, de gagner du temps et de partager le travail avec d&#39;autres. Avez-vous développé une excellente technique pour l&#39;usure des bords par exemple ? Créez-en une Instance de graphe et réutilisez-la vous-même, partagez-la avec la communauté ou votre équipe !

Pour plus d&#39;informations sur les Instances de graphe dans les [graphes de Substance](../../compositing-graphs/substance-compositing-graphs.md), une [section dédiée](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md) est disponible à leur sujet dans la documentation.

![Paramètres de Graphe simplifiés](workflow-overview.resources/parameters-5.png "Paramètres de Graphe simplifiés")

## Paramètres personnalisés

Tous les nœuds de votre chaîne d’opérations auront une forme de contrôle : des boutons, des curseurs, des paramètres que vous pourrez modifier, ce qui influencera le résultat final. Si vous créez un Sous-Graphe, ou si vous voulez exporter votre Fichier de Substance de données vers une autre application, vous pouvez construire votre propre « panneau de contrôle » pour vos fichiers, permettant à quiconque utilisant le Graphe de le modifier avec un panneau de contrôle entièrement unique, exposant des possibilités infinies. [Découvrez le concept général des paramètres personnalisés ici](../../compositing-graphs/compositing-graph-key-con/substance-compositing-graph-key-concepts.md), ou allez plus loin dans la profondeur et [commencez à exposer des paramètres](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md).

## types de graphe

Vous trouverez ci-dessous un résumé des trois types de Graphes que vous pouvez modifier dans Substance 3D Designer, ainsi qu’un lien vers la section correspondante de la documentation.

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

[![](workflow-overview.resources/graph-5.png){width="120px"}](https://substance3d.adobe.com/)

</td>
<td width="100.00%" style="border: 0;" valign="top">

### Graphes Substance

Les [graphes de Substance](https://substance3d.adobe.com/) sont le principal type de graphe créé dans Substance 3D Designer. Leur objectif est de <b>générer et traiter des données d&#39;image 2D</b> qui ne sont pas limitées à une résolution, une couleur ou une forme définie. Ils sont conçus comme des outils de traitement d&#39;image et de génération extrêmement polyvalents, et pas seulement comme des résultats statiques prédéfinis.

Les résultats peuvent se présenter sous la forme d’un motif simple en noir et blanc, d’un filtre qui s’exécute uniquement sur les autres images et ne génère pas de contenu à lui seul, ou même d’un matériau procédural complet avec plusieurs canaux.

Les graphes de Substance sont[le type de graphe le plus largement pris en charge](../../getting-started/overview/overview.md). Ils peuvent être exportés et utilisés dans une multitude de workflows différents.

</td>
</tr>
</table>

#### Exemples

Vous trouverez ci-dessous quelques exemples typiques de cas d’utilisation courants.

+++Forme simple
![Forme simple dans le graphe Substance](workflow-overview.resources/simpleshape.png "Forme simple dans le graphe Substance"){width="512px"}



Une forme de masque simple pour une décalcomanie est créée en générant[un morceau de texte](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md) et une [forme de disque](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape/shape.md), en [extrayant le bord](../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/edge-detect/edge-detect.md) du disque et en [les fusionnant](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md) avant de les définir comme [sortie](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) finale.

Le texte portant le numéro ou le thickness du contour peut être exposé à l’extérieur pour rendre ce graphe plus dynamique.

+++

+++Filtre Réglage
![Filtre d&#39;ajustement dans le graphique de Substance](workflow-overview.resources/simplefilter.png "Filtre d&#39;ajustement dans le graphique de Substance"){width="512px"}



Un graphique de filtre prend une carte normale comme [entrée](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md) (avec un aperçu personnalisé), [la convertit en courbure](../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-smooth/curvature-smooth.md), puis [ajuste le contraste](../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md) pour créer un masque de bords convexes en tant que [sortie](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) finale.

Les valeurs de contraste définies dans l’histogramme peuvent être affichées, ce qui en fait un filtre simple mais utile en combinaison avec l’emplacement d’entrée dynamique.

+++

+++Matière complète
![Matière complète dans le graphique en Substances](workflow-overview.resources/simplematerial.png "Matière complète dans le graphique en Substances"){width="512px"}



Un graphique plus complexe[fusionne deux Matériaux de base](../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/material-blend/material-blend.md). L&#39;un des [Matériaux de base](../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/base-material/base-material.md) est simple, tandis que l&#39;autre utilise des entrées personnalisées pour susciter l&#39;intérêt. Un masque est utilisé pour déterminer lequel des deux matériaux apparaît à l&#39;endroit où il se trouve avant d&#39;être défini comme [sorties](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) finales.

Cet exemple utilise les [modes de création de liens](../../interface/the-graph-view/link-creation-modes/link-creation-modes.md) pour simplifier l&#39;utilisation de plusieurs liens.

+++

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

[![](workflow-overview.resources/function-1.png){width="120px"}](https://substance3d.adobe.com/)

</td>
<td width="100.00%" style="border: 0;" valign="top">

### graphiques de fonction de Substance

Les fonctions <b>traitent des valeurs uniques</b> (entiers, flottants, vecteurs) au lieu de données d&#39;image (ensembles entiers de pixels). Les fonctions sont également des graphes avec des réseaux de nœuds, mais les [nœuds utilisés](../../function-graphs/nodes-reference-for-fun/function-nodes-overview/function-nodes-overview.md) et l&#39;interface sont différents des [graphes de Substance standard](../../compositing-graphs/substance-compositing-graphs.md). Le workflow est entièrement basé sur <b>des opérations mathématiques</b> et n&#39;affiche aucune vignette d&#39;aperçu d&#39;image, ce qui en fait une méthode de travail <b>beaucoup plus avancée</b> avec Substance 3D Designer.

Les fonctions peuvent être utilisées dans de nombreux contextes différents, les principaux étant de modifier le comportement d&#39;[un paramètre exposé](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md), de créer le comportement de [Processeurs de pixels](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md) ou de [FX-Maps](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md) et d&#39;utiliser des [valeurs](../../compositing-graphs/values-compositing-graphs/values-in-substance-compositing-graphs.md) dans un graphe de Substance.

</td>
</tr>
</table>

#### Exemples

Vous trouverez ci-dessous quelques exemples de cas d&#39;utilisation courants des graphiques de fonction de Substance.

+++Fonction simple
![Graphique de fonction simple](workflow-overview.resources/lerpfunction.png "Graphique de fonction simple"){width="256px"}



Fonction simple dans le contexte d&#39;un paramètre exposé. Il obtient une valeur flottante d’entrée appelée « Intensité » qui est déterminée pour aller de 0 à 1 (une plage facile à comprendre) et la remappe vers une plage définie de 0,1 à 0,8. Cela signifie que si l&#39;utilisateur définit l&#39;intensité sur 0, en interne 0,1 sera utilisé, si l&#39;interface utilisateur est définie sur 1, 0,8 sera utilisé, et toute valeur entre les deux sera interpolée linéairement. Ce type de fonction est couramment utilisé lors de l&#39;[exposition de paramètres](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md), mais à l&#39;aide de fonctions personnalisées.

Cette fonction peut également être écrite en tant que *lerp(0.1, 0.8, Intensité)* dans un pseudocode similaire à HLSL ou GLSL.

+++

+++Fonction avancée
![Fonction avancée](workflow-overview.resources/pixel-function.png "Fonction avancée"){width="512px"}



Cette fonction avancée montre le fonctionnement interne d&#39;un [processeur de pixels](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md) conçu pour régler la teinte d&#39;une entrée de table des couleurs en fonction de l&#39;intensité d&#39;une seconde entrée de masque en niveaux de gris.

Il échantillonne les deux entrées avec la variable système « $pos », puis supprime l&#39;Alpha, convertit la valeur de couleur en TSL et modifie la composante de teinte en la multipliant par la valeur de niveaux de gris échantillonnée. Ensuite, il réassemble le vecteur, reconvertit la TSI en RGB et ajoute l’Alpha pour la sortie finale.

dans le pseudo-code, il s&#39;agirait d&#39;une fonction beaucoup plus compliquée qui ne tiendrait pas sur une seule ligne.



+++

### Graphiques MDL

Cette page présente des graphiques MDL dans Substance 3D Designer, qui vous permettent de créer des matériaux MDL et de prévisualiser leur comportement en temps réel.
