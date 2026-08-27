---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs.html"
breadcrumb-title: ''
description: Apprenez à créer et à utiliser des graphiques de fonctions de Substance dans Designer pour créer des fonctions personnalisées et des réseaux de nœuds réutilisables.
helpx_creative_field: ""
helpx_description: Designer > Substance function graphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: graphiques de fonction de Substance
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 0%

---


# graphiques de fonction de Substance

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

[![](../assets/function-1.png){width="120px"}](https://substance3d.adobe.com/)

</td>
<td style="border: 0;" valign="top">

[graphes de fonction de Substance](https://substance3d.adobe.com/) <b>traitez des valeurs uniques</b> (entiers, flots, vecteurs) au lieu de données d&#39;image (ensembles entiers de pixels). Les fonctions sont également des graphes avec des réseaux de nœuds, mais les [nœuds utilisés](../function-graphs/nodes-reference-for-fun/function-nodes-overview/function-nodes-overview.md) et l&#39;interface sont différents des [graphes de Substance standard](../compositing-graphs/substance-compositing-graphs.md). Le workflow est entièrement basé sur <b>des opérations mathématiques</b> et n&#39;affiche aucune vignette d&#39;aperçu d&#39;image, ce qui en fait une méthode de travail <b>beaucoup plus avancée</b> avec Substance 3D Designer.

Les fonctions peuvent être utilisées dans de nombreux contextes différents, les principaux étant de modifier le comportement d&#39;[un paramètre exposé](../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md), de créer le comportement de [Processeurs de pixels](../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md) ou de [FX-Maps](../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md) et d&#39;utiliser des [valeurs dans les graphes de Substance](../compositing-graphs/values-compositing-graphs/values-in-substance-compositing-graphs.md).

</td>
</tr>
</table>

## Exemples

Vous trouverez ci-dessous quelques exemples d’utilisations courantes des Fonctions.

### Fonction simple

![](../assets/lerpfunction_1.png)

Fonction simple dans le contexte d&#39;un paramètre exposé. Il obtient une valeur flottante d’entrée appelée « Intensité » qui est déterminée pour aller de 0 à 1 (une plage facile à comprendre) et la remappe vers une plage définie de 0,1 à 0,8. Cela signifie que si l&#39;utilisateur définit l&#39;intensité sur 0, en interne 0,1 sera utilisé, si l&#39;interface utilisateur est définie sur 1, 0,8 sera utilisé, et toute valeur entre les deux sera interpolée linéairement. Ce type de fonction est couramment utilisé lors de l&#39;[exposition de paramètres](../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md), mais à l&#39;aide de fonctions personnalisées.

Cette fonction peut également être écrite en tant que *lerp(0.1, 0.8, Intensité)* dans un pseudocode similaire à HLSL ou GLSL.

### Fonction avancée

![](../assets/pixel-function_1.png){width="545px"}

Cette fonction avancée montre le fonctionnement interne d&#39;un [processeur de pixels](../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md) conçu pour régler la teinte d&#39;une entrée de table des couleurs en fonction de l&#39;intensité d&#39;une seconde entrée de masque en niveaux de gris.

Il échantillonne les deux entrées avec la variable système « $pos », puis supprime l&#39;Alpha, convertit la valeur de couleur en TSL et modifie la composante de teinte en la multipliant par la valeur de niveaux de gris échantillonnée. Ensuite, il réassemble le vecteur, reconvertit la TSI en RGB et ajoute l’Alpha pour la sortie finale.

dans le pseudo-code, il s&#39;agirait d&#39;une fonction beaucoup plus compliquée qui ne tiendrait pas sur une seule ligne.
