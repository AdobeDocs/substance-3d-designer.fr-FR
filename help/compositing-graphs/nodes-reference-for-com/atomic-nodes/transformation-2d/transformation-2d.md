---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/transformation-2d.html"
breadcrumb-title: ''
description: Utilisez le nœud Transformation 2D pour appliquer des transformations 2D aux textures, y compris la translation, la rotation et la mise à l’échelle.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Transformation 2D
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Transformation 2D
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 5%

---


# Transformation 2D

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nœud atomique : transformation 2D](../../../../assets/comp_transformation_1.png "Nœud atomique : transformation 2D"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Applique une matrice de transformation 2D à une image : translation, rotation, mise à l’échelle, symétrie et cisaillement.

Elle est assez similaire à la transformation (Ctrl-T) dans Photoshop, ou à l’utilisation du manipulateur de mappage 2D dans Substance 3D Painter.

</td>
</tr>
</table>

C&#39;est un nœud extrêmement utile et largement appliqué, il permet d&#39;augmenter la mosaïque, de supprimer la mosaïque, de placer une image dans une position spécifique, d&#39;étirer ou d&#39;écraser une entrée, etc.

Il ne peut toutefois pas correspondre parfaitement à certaines applications, de sorte que les nœuds suivants peuvent être intéressants : [Transformation sécurisée](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/safe-transform/safe-transform.md), [Transformation non carrée](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/non-square-transform/non-square-transform.md), [Transformation quadrillée](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/quad-transform/quad-transform.md) et [Transformation trapézoïdale](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/trapezoid-transform/trapezoid-transform.md).

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">



</td>
<td width="83.33%" style="border: 0;" valign="top">



</td>
<td width="100.00%" style="border: 0;" valign="top">



</td>
</tr>
</table>

>[!TIP]
>
> Désactivation de la juxtaposition
> 
> Définissez la [méthode d&#39;héritage](../../../../glossary/glossary.md) du [paramètre de base](../../../../glossary/glossary.md) &#39;Tiling mode&#39; sur &#39;Absolute&#39;, ce qui vous permet ensuite de définir la valeur du paramètre sur &#39;No Tiling&#39; :
> 
> ![](../../../../assets/tilingmode.png)

>[!NOTE]
>
> Les valeurs de mise à l&#39;échelle et de rotation dans les propriétés du nœud sont *relatives à la transformation actuelle* et ne sont pas appliquées à la vue 2D tant que vous n&#39;avez pas cliqué sur le bouton Appliquer.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Connecteurs de sortie

</td>
<td style="border: 0;" valign="top">

### Exemples

</td>
</tr>
</table>

## Paramètres

|  |  |
| --- | --- |
| <b>Matrice de transformation</b> *Float4* | Ouvrez la matrice de transformation sous-jacente pour la modifier directement. Permet de modifier la rotation et la mise à l’échelle. Peut également être ajusté à l&#39;aide de l&#39;objet dans la vue 2D.   Avertissement : ils ne sont pas directement corrélés à la vue et constituent des ajustements relatifs qui peuvent être appliqués par étapes. |
| <b>Décalage</b> *Float2* | Définit le displacement 2D de l’image. Permet de modifier la position ou le décalage Peut également être ajusté via l&#39;objet dans la vue 2D.   Est directement lié à la sortie de la vue 2D. |
| <b>Mode Mipmap</b> *Nombre entier* | Vous permet de passer à un niveau manuel [mipmap](../../../../glossary/glossary.md), qui réduit les artefacts dans une image à l&#39;aide du filtrage de texture. |
| <b>Niveau du mipmap</b> *Nombre entier* | Définit le niveau [mipmap](../../../../glossary/glossary.md) à utiliser.     *Disponible lorsque le mode Mipmap est défini sur « Manuel »* |
| <b>Cache</b> *Float4* | Couleur utilisée comme arrière-plan lorsque la juxtaposition de transformations est désactivée. C’est-à-dire qu’il définit la couleur utilisée lorsque l’entrée transformée ne couvre pas une zone de la sortie.   Peut être rendu transparent si vous travaillez en couleur RVBA. |
| <b>Filtrage</b> *Nombre entier* | Définit la méthode de sous-échantillonnage utilisée. Ne fonctionne pas particulièrement bien lorsque le Niveau du mipmap est réduit. |

## Connecteurs d’entrée

|  |  |
| --- | --- |
| <b>Entrée</b> *Niveaux de gris/Couleur* PRINCIPAL | Image à transformer. |

## Connecteurs de sortie

|  |  |
| --- | --- |
| <b>Sortie</b> *Niveaux de gris/Couleur* |  |

## Exemples

*Bientôt disponible.*
