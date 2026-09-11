---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/levels.html"
breadcrumb-title: ''
description: Utilisez le nœud Niveaux pour régler la luminosité, le contraste et la gamme de tons des textures de correction et d’amélioration des couleurs.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Levels
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Niveaux
user-guide-description: ''
user-guide-title: ''
source-git-commit: 8b6f65bd88f3c83bf6682c7bca91615166389a91
workflow-type: tm+mt
source-wordcount: '554'
ht-degree: 4%

---


# Niveaux

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Noeud atomique : Levels](levels.resources/comp_levels_1.png "Noeud atomique : Levels"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Règle la gamme de tons et la balance des couleurs globales pour les ombres, les tons moyens et les hautes lumières d’une image.

Le nœud Niveaux vous permet de remapper les tons d’une entrée en définissant des facteurs de remappage d’entrée et de sortie, présentés dans une interface d’histogramme familière avec les autres éditeurs d’images 2D.

</td>
</tr>
</table>

Il s’agit de l’un des nœuds principaux les plus utiles de Substance 3D Designer. Il est très souvent utilisé pour remapper et ajuster les valeurs dans un graphe, car il fournit l’interface la plus précise et précise aux valeurs changeantes.

Bien qu&#39;il s&#39;agisse d&#39;un nœud important, pour certains cas d&#39;utilisation, l&#39;interface peut être un peu lourde. Assurez-vous donc de rechercher des alternatives dans [Niveaux automatiques](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/auto-levels/auto-levels.md), [Contraste/Luminosité](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/contrast-luminosity/contrast-luminosity.md) et [Histogramme de balayage](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md).

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

## Exemples

## Paramètres

Le nœud offre deux interfaces pour ajuster ses valeurs : l’histogramme et les curseurs. Vous pouvez basculer entre eux avec le bouton le plus à droite dans la barre d’en-tête « Paramètres spécifiques » :

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Le bouton jaune en surbrillance active/désactive l’interface entre les curseurs de valeur de l’histogramme (en haut) (en bas)

</td>
<td width="66.67%" style="border: 0;" valign="top">

![](levels.resources/levels-2-1.png)

![](levels.resources/levels-1-1.png)

</td>
</tr>
</table>

|  |  |
| --- | --- |
| <b>Entrée basse du niveau</b> *Flottant/Flottant 4* | Définit les niveaux de surbrillance de l’image d&#39;entrée. Remappe les valeurs d’entrée Faible pour obtenir un noir complet. |
| <b>Entrée haute du niveau</b> *Flottant/Flottant 4* | Définit les niveaux de surbrillance de l’image d&#39;entrée.  Les remappages saisissent des valeurs élevées pour obtenir un blanc complet. |
| <b>Entrée moyenne du niveau</b> *Flottant/Flottant 4* | Définit les niveaux de tons moyens de l’image d&#39;entrée.  Remappe les valeurs intermédiaires d’entrée pour obtenir un gris moyen. |
| <b>Niveau bas</b> *Flottant/Flottant 4* | Définit les niveaux de surbrillance de l’image de sortie.  Verrouille les valeurs de noir en sortie pour définir une limite. |
| <b>Sortie haute du niveau</b> *Flottant/Flottant 4* | Définit les niveaux de surbrillance de l’image de sortie.  Verrouille les valeurs de blanc en sortie pour définir une limite. |
| <b>Pince intermédiaire</b> *Booléen* | Détermine si la valeur d&#39;entrée transformée est fixée à [0, 1] avant de calculer le niveau de sortie. |

## Guide d’utilisation

Regardez cette présentation vidéo du nœud Levels et de son éditeur d’histogrammes :

### Actions rapides

Dans la barre d’en-tête « Paramètres spécifiques », vous trouverez des boutons permettant d’accéder aux fonctions pratiques de l’histogramme :

![Actions rapides du nœud de niveaux](levels.resources/levels-2.png "Actions rapides du nœud de niveaux")

<b>1 - Inverser :</b> permute les valeurs des paramètres « Niveau bas sortant » et « Sortie haute du niveau ».

<b>2 - Niveau automatique :</b> ajuste automatiquement les valeurs des paramètres « Entrée basse du niveau » et « Entrée haute du niveau » respectivement à la valeur la plus basse et à la valeur la plus élevée présentes dans l&#39;image.

<b>3 - Changer d&#39;interface :</b> basculer entre les éditeurs d&#39;histogramme et de curseur.

### Histogramme

L’éditeur d’histogramme est destiné aux réglages visuels et rapides pour lesquels des valeurs précises ne sont pas vraiment nécessaires et l’expose de paramètres n’est pas importante. Il s’agit généralement du moyen le plus rapide et le plus simple de travailler avec les niveaux.

![](levels.resources/levels-histo.gif)

Selon le type d’entrée (Couleur ou Niveaux de gris), vous pouvez utiliser la liste déroulante au-dessus de l’histogramme pour choisir la couche que vous modifiez.

### Curseurs

L&#39;éditeur de curseurs se débarrasse de tout éditeur visuel et ne présente que des curseurs numériques, utiles surtout si vous souhaitez fixer ou remapper à des valeurs très exactes, ou si vous avez l&#39;intention d&#39;[exposer l&#39;un de ces paramètres](../../../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md), car cela est uniquement possible dans l&#39;éditeur de curseurs.

Les curseurs changent en fonction d’une entrée de couleur ou de niveaux de gris : les entrées de couleur créent 4 curseurs pour chaque canal RVBA séparément, les niveaux de gris n’ont qu’un seul curseur, ce qui facilite leur utilisation. Voir la liste de paramètres ci-dessus pour obtenir une explication sur chaque curseur.

## Connecteurs d’entrée

|  |  |
| --- | --- |
| <b>Entrée</b> *Niveaux de gris/Couleur* PRINCIPAL | Image à traiter. |

## Connecteurs de sortie

|  |  |
| --- | --- |
| <b>Sortie</b> *Niveaux de gris/Couleur* |  |

## Exemples

*Bientôt disponible.*
