---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/normal.html"
breadcrumb-title: ''
description: Utilisez le nœud Normal pour traiter et manipuler les textures de map normal afin de contrôler les détails de la surface et l'éclairage.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Normal
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Normale
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 8%

---


# Normale

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Noeud atomique : Normal](../../../../assets/comp_normal_1.png "Noeud atomique : Normal"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Calcule une map normal à partir d’une image en niveaux de gris interprétée comme une map height.

Le nœud convertit un mappage en niveaux de gris d&#39;entrée en une sortie de Map normal d&#39;espace de tangente. Il offre quelques options utilisateur pour définir l’intensité et le codage.

</td>
</tr>
</table>

C&#39;est un nœud très utile qui est souvent utilisé pour convertir les entrées de map height en maps normal pour des matériaux prêts à l&#39;emploi. Il existe des alternatives dans [Sobel normal](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-sobel/normal-sobel.md) et l&#39;Height des unités universelles normales.

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
| <b>Intensité</b> *Flotter* | Modifie l’intensité de la map height.   Définit l’intensité de l’interprétation de la map height d’entrée pour la conversion en normales. En fonction des maps d&#39;entrée, les valeurs supérieures à 100 ont peu plus d’effet. |
| <b>Format normal</b> *Booléen* | Inverse les coordonnées Y de la map height (OpenGL).   Définit le mode de codage de la couche verte (Y). En gros un commutateur « Flip Green/Y ». |
| <b>Contenu Canal Alpha</b> *Booléen* | Remplissez le canal Alpha de la map normal avec la texture d’entrée.   Alpha de remplissage avec l’Alpha Entrée/Force sur 1 : permet de définir le Canal Alpha sur solide, au lieu d’utiliser l’entrée comme Alpha supplémentaire. |

## Connecteurs d’entrée

|  |  |
| --- | --- |
| <b>Entrée</b> *Niveaux de gris* PRINCIPAUX | Image d&#39;entrée interprétée comme une map height. |

## Connecteurs de sortie

|  |  |
| --- | --- |
| <b>Sortie</b> *Couleur* |  |

## Exemples

*Bientôt disponible.*
