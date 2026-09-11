---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/waveform-1.html"
breadcrumb-title: ''
description: Utilisez le nœud Waveform 1 pour générer des motifs de forme d’onde afin de créer des textures organiques et des variations procédurales.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Waveform 1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Forme d’onde 1
user-guide-description: ''
user-guide-title: ''
source-git-commit: db5ad9a6ad1d03fedcc3d760cc8886501d16b87f
workflow-type: tm+mt
source-wordcount: '350'
ht-degree: 1%

---


# Forme d’onde 1

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Forme D’Onde 1 - Icône](waveform-1.resources/waveform_01_v2.png "Forme D’Onde 1 - Icône"){width="200px"}

<b>Entrée :</b> générateurs de Textures > Bruits

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Disposition horizontale de motifs sélectionnés par l’utilisateur empilés dans une forme semblable à une forme d’onde.

</td>
</tr>
</table>

<a name="outputs"></a>

## Sorties

|  |  |
|:---|:---|
| <b>Sortie</b> <i>Niveaux de gris</i> | Le bruit généré est un bitmap en niveaux de gris. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Exemples</b> <i>Entier</i> | Quantité de motifs placés le long de l’axe X pour dessiner la forme d’onde, où une valeur plus faible donne un aspect plus étagé. |
| <b>Fonction</b> <i>Entier</i> | Fonction utilisée pour dessiner la forme d’onde.   Cela contrôle la taille verticale du motif placé sur chaque échantillon :<ul data-preserve-html="true"> <li data-preserve-html="true"><i>bruit de valeurs :</i> distribution aléatoire des valeurs</li> <li data-preserve-html="true"><i>Cosinus :</i> les valeurs suivent la progression d&#39;une fonction cosinus</li> <li data-preserve-html="true"><i>Fonction personnalisée :</i> utilisez une fonction créée par l&#39;utilisateur pour piloter les valeurs</li> </ul> |
| <b>Fonction personnalisée</b> <i>Flottant</i>   *Disponible lorsque &#39;Function&#39; est défini sur &#39;Fonction personnalisée&#39;* | Calcule la taille verticale du motif placé sur chaque échantillon.   Variables disponibles :<ul data-preserve-html="true"> <li data-preserve-html="true"><b>pos</b> (<i>float</i>) Position du motif à l&#39;axe X. Elle peut être utilisée pour sélectionner des motifs.</li> </ul> |
| <b>Rugosité</b> <i>Flottant</i> | Effectue une interpolation entre une forme d’onde propre et lisse et une autre plus irrégulière et mieux répartie.    Cela peut être considéré comme un signal propre par rapport au bruit blanc. |
| <b>Échelle</b> <i>Entier</i> | Plage horizontale de la forme d’onde visible dans l’image. |
| <b>Amplitude min.</b> <i>Flottant</i> | Valeur minimale (ou thickness) de la forme d’onde. |
| <b>Amplitude max.</b> <i>Flottant</i> | Valeur maximale (ou thickness) de la forme d’onde. |
| <b>Bruit</b> <i>Flottant</i> | Applique un bruit à la forme d’onde qui la soustrait aléatoirement de sa plage verticale. |
| <b>Position</b> <i>Entier</i> | Position de la forme d’onde dans l’image :<ul data-preserve-html="true"> <li data-preserve-html="true"><i>Centré :</i> l&#39;origine se trouve au centre vertical de l&#39;image</li> <li data-preserve-html="true"><i>Bas :</i> l&#39;origine se trouve en bas de l&#39;image</li> </ul> |
| <b>Motif</b> <i>Entier</i> | Motif placé sur chaque échantillon de la forme d’onde. |
| <b>Variation de motif</b> <i>Flottant</i> | Un réglage supplémentaire est disponible pour certains motifs. |
| <b>Désordre</b> <i>Flottant</i> | Déplace les valeurs de la forme d’onde.    Cette action peut être utilisée pour l’animer. |
| <b>Désorganiser la vitesse</b> <i>Flottant</i> | Ajuste la distance de displacement appliquée par le paramètre <b>Désordre</b>.    Vous pouvez l’utiliser pour contrôler la vitesse de displacement lors de l’animation de la forme d’onde. |

## Exemples

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Forme D&#39;Onde 1 - Exemple 1](waveform-1.resources/waveform_01_v2_speed0.1_aniso0.gif "Forme D&#39;Onde 1 - Exemple 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
