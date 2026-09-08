---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/blend.html"
breadcrumb-title: ''
description: Utilisez le nœud Fusion pour fusionner deux textures à l’aide de différents modes de fusion afin de créer des effets composites.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Fusion
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '332'
ht-degree: 9%

---


# Fusion

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Noeud atomique : Fusion](../../../../assets/comp_blend_1.png "Noeud atomique : Fusion"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Combine deux images à l’aide d’un mode de fusion spécifié et d’un masque facultatif.

Il s&#39;agit du nœud le plus utile de tous les Noeuds atomiques. Presque tous les Graphes que vous construisez dans [Substance 3D Designer](https://www.adobe.com/fr/products/substance3d-designer.html) utiliseront ce nœud.

</td>
</tr>
</table>

Sa fonctionnalité est similaire à celle consistant à avoir deux calques au-dessus l&#39;un de l&#39;autre dans [Substance 3D Painter](https://www.adobe.com/products/substance3d-painter.html) ou [Photoshop](https://www.adobe.com/ch_fr/products/photoshop/landpa.html), qui se fondent l&#39;un dans l&#39;autre selon le mode de fusion que vous définissez sur le calque supérieur.

>[!TIP]
>
> Découvrez les modes de fusion disponibles dans le nœud de Fusion de données de [cette page dédiée](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blending-modes-des/blending-modes-description.md).

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
| <b>Opacité</b> *Flotter* | Opacité du calque de premier plan fusionné avec l’arrière-plan. Il fonctionne indépendamment de l’entrée Opacité et agit comme un multiplicateur supplémentaire. |
| <b>Mode de fusion</b> *Entier* [Statique](../../../../glossary/glossary.md) | Définit l’opération de fusion à utiliser.   Consultez la [page dédiée aux modes de fusion](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blending-modes-des/blending-modes-description.md). |
| <b>Simulation de transparence</b> *Entier* [Statique](../../../../glossary/glossary.md) | Détermine le comportement de fusion lorsque les entrées de couleur ont des Canaux Alphas :<ul data-preserve-html="true"> <li data-preserve-html="true">Utiliser l’alpha de la source</li> <li data-preserve-html="true">Ignorer l’alpha</li> <li data-preserve-html="true">Simulation de transparence droite</li> <li data-preserve-html="true">Simulation de transparence prémultipliée</li> </ul> |
| <b>Zone de recadrage</b> *Flottant 4* [Statique](../../../../glossary/glossary.md) | Permet de définir une zone de recadrage personnalisée qui se comporte comme un masque d’opacité supplémentaire. Toute zone recadrée affiche uniquement l’arrière-plan. |

## Connecteurs d’entrée

|  |  |
| --- | --- |
| <b>Premier plan</b> *Niveaux de gris/Couleur* | Calque supérieur ou de premier plan de l’opération de fusion. |
| <b>Arrière-plan</b> *Niveaux de gris/Couleur* PRINCIPAL | Calque inférieur ou d’arrière-plan de l’opération de fusion. |
| <b>Opacité</b> *Niveaux de gris* | Entrée de masque d’Alpha facultative. |

>[!IMPORTANT]
>
> Les nœuds de fusion ont des entrées dynamiques qui basculent entre les niveaux de gris et les couleurs en fonction de vos connexions.<b> Un nœud de fusion ne peut fusionner que deux entrées du même type</b>.
> 
> La connexion d’une entrée Couleur et Niveaux de gris au premier plan et à l’arrière-plan crée une ligne de connexion en pointillé rouge, ce qui signifie une erreur de calcul.
> 
> C’est la principale raison pour laquelle les nouveaux utilisateurs rencontrent des problèmes de connexion entre les couleurs et les niveaux de gris : assurez-vous que les deux connexions sont du même type !

## Connecteurs de sortie

|  |  |
| --- | --- |
| <b>Sortie</b> *Niveaux de gris/Couleur* |  |

## Exemples

*Bientôt disponible.*
