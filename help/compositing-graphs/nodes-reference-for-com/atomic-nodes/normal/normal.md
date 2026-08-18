---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/normal.html"
breadcrumb-title: ''
description: Utilisez le nœud Normal pour traiter et manipuler les textures de texture normales afin de contrôler les détails de la surface et l'éclairage.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Normal
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Normale
user-guide-description: ''
user-guide-title: ''
source-git-commit: ea96f5a148246d20263c4ecf0b67d0b4a51f28a8
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 8%

---


# Normale

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nœud atomique : normal](../../../../assets/comp_normal_1.png "Nœud atomique : normal"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Calcule une map normal à partir d’une image en niveaux de gris interprétée comme une map height.

Le nœud convertit une map en niveaux de gris en sortie map tangent-espace Normal. Il offre quelques options utilisateur pour définir l’intensité et le codage.

</td>
</tr>
</table>

Il s&#39;agit d&#39;un nœud très utile, souvent utilisé pour convertir les entrées de mappage d&#39;height en mappages normaux pour les matériaux prêts à l&#39;emploi. Il existe des alternatives dans [Sobel normal](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-sobel/normal-sobel.md) et l&#39;Height des unités universelles normales.

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
| <b>Intensité</b> *Flotter* | Modifie la courbe d’intensité des heights.   Définit l’intensité de l’interprétation de la texture d’height d’entrée pour la conversion en normales. En fonction des cartes d’entrée, les valeurs supérieures à 100 ont peu plus d’effet. |
| <b>Format normal</b> *Booléen* | Inverse les coordonnées Y de la courbe d’height (OpenGL).   Définit le mode de codage de la couche verte (Y). En gros un commutateur « Flip Green/Y ». |
| <b>Contenu de canal Alpha</b> *Booléen* | Remplissez la couche alpha de la texture normale avec la texture d&#39;entrée.   Alpha de remplissage avec l’Alpha Entrée/Force sur 1 : permet de définir le canal d’Alpha sur solide, au lieu d’utiliser l’entrée comme Alpha supplémentaire. |

## Connecteurs d’entrée

|  |  |
| --- | --- |
| <b>Entrée</b> *Niveaux de gris* PRINCIPAUX | Image d’entrée interprétée comme une carte d’height. |

## Connecteurs de sortie

|  |  |
| --- | --- |
| <b>Sortie</b> *Couleur* |  |

## Exemples

*Bientôt disponible.*
