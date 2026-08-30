---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/emboss.html"
breadcrumb-title: ''
description: Utilisez le nœud Estampage pour appliquer des effets d’estampage aux textures et ajouter ainsi une profondeur et un relief aux détails d’une surface.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Emboss
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Estampage
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 9%

---


# Estampage

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nœud atomique : Emboss](emboss.resources/comp_emboss_1.png "Nœud atomique : Emboss"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Applique un effet d’embossage en éclairant les côtés des formes d’une image selon une direction de source lumineuse spécifiée.

C’est-à-dire que le nœud exécute un ombrage 2D simple sur la base de 2 entrées, simulant la chute de lumière sur une surface avec une variation d’height et de profondeur.

</td>
</tr>
</table>

Ce nœud n’est pas souvent utilisé pour les projets de type PBR, mais il peut être utile dans certains cas où vous souhaitez un éclairage simple et cuit dans votre texture. L&#39;[estampage avec brillance](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/emboss-with-gloss/emboss-with-gloss.md) et l&#39;[estampage Uber](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/uber-emboss/uber-emboss.md) offrent une fonctionnalité similaire, mais plus étendue.

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
| <b>Intensité</b> *Flotter* | Règle l&#39;intensité globale de l&#39;effet d&#39;illumination.   Définit l’intensité de la courbe de transfert de l’height et, par conséquent, l’intensité de l’effet d’éclairage |
| <b>Angle de la lumière</b> *Flotter* | Définit l’angle selon lequel la lumière est simulée.   Définit l’angle d’éclairage de la mise en surbrillance de l’image gaufrée |
| <b>Mettre en surbrillance la couleur</b> *Float/Float4* | Définit la couleur des zones orientées vers l’angle de la lumière.   Définit la couleur de la surbrillance si l’image d’entrée est en couleur. |
| <b>Couleur de l&#39;ombre</b> *Float/Float4* | Définit la couleur des zones orientées à l’opposé de l’angle d’éclairage.   Définit la couleur des zones ombrées de l’image gaufrée. |

## Connecteurs d’entrée

|  |  |
| --- | --- |
| <b>Entrée</b> *Niveaux de gris/Couleur* PRINCIPAL | Fournit les couleurs de base non ombrées. Voyez-la comme une sorte de texture de couleur diffuse ou de couleur de base. |
| <b>Entrée d&#39;intensité</b> *Niveaux de gris* | Représente la carte de hauteur utilisée pour calculer l&#39;éclairage sur la surface. Le noir est faible et le blanc est élevé. |

## Connecteurs de sortie

|  |  |
| --- | --- |
| <b>Sortie</b> *Niveaux de gris/Couleur* |  |

## Exemples

*Bientôt disponible.*
