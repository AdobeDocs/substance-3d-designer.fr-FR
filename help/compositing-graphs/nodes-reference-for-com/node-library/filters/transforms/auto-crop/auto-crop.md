---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/auto-crop.html"
breadcrumb-title: ''
description: Utilisez le nœud Recadrage automatique pour recadrer automatiquement les textures afin de supprimer les bordures vides et d’optimiser les dimensions de la texture.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Auto Crop
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Recadrage automatique
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 1%

---


# Recadrage automatique

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](auto-crop.resources/autocropgrayscale.png){width="200px"}

</td>
<td style="border: 0;" valign="top">

![](auto-crop.resources/autocropcolor.png){width="200px"}

</td>
</tr>
</table>

<b>Entrées :</b> Filtres > Transformes

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Le nœud **Recadrage automatique** ajuste l&#39;**entrée** de sorte que son contenu soit placé au *centre* de l&#39;image sans être redimensionné, ou *redimensionné à la plage* de l&#39;image.

Le contenu de l&#39;image est défini par une case ajustée aux *premier et dernier pixels* sur **X** et **Y** dont les valeurs sont *supérieures à 0* (c&#39;est-à-dire non noires). La version **Color** vous permet de choisir dans le RGB et les Canaux Alphas pour définir cette zone.

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Mode</b> <i>Nombre entier</i> | Définir la méthode de recadrage à appliquer :<br><br>- <i>Recadrer le carré</i> : l&#39;image est recadrée de sorte que la forme soit au centre de la plus petite image <i>carrée</i> qui peut l&#39;inclure entièrement<br>- <i>Recadrer automatiquement</i> : l&#39;image est recadrée de sorte que la forme soit au centre de la plus petite image <i>carrée ou non carrée</i> qui peut l&#39;inclure entièrement<br>- <i>Adapter (conserver le rapport)</i> : l&#39;image est redimensionnée à la <i>plage complète</i> de l&#39;image tout en conservant ses <i>proportions</i> (c’est-à-dire le rapport largeur/longueur)<br>- <i>Remplissage (Étiré)</i> : l’image est redimensionnée à <i>sa taille totale</i> |
| <b>Utiliser alpha</b> <i>Booléen</i> | Utilisez le canal Alpha de l&#39;<b>entrée</b> pour déterminer les <i>limites</i> du contenu de l&#39;image à recadrer. Lorsqu&#39;il est défini sur <i>Faux</i>, les pixels noirs sont utilisés à la place.<br><br><i>Remarque :</i> ce paramètre est uniquement disponible dans la version <b>Color</b> du nœud. |
| <b>Mode de filtrage</b> <i>Nombre entier</i> | Définit le traitement des résultats échantillonnés lors de l&#39;<i>interpolation</i> entre les pixels :<br><br>-<i>Au plus proche</i> : échantillonnera exactement la <i>même</i> valeur (plus rapide)<br>-<i>Bilinéaire</i> : appliquera un filtre bilinéaire sur le résultat pour un aspect <i>plus lisse</i><br>-<i>Auto</i> : utilise le mode le plus approprié des deux modes ci-dessus en fonction du <b>Mode</b> sélectionné pour le recadrage |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="auto-crop.resources/autocrop-demo-01-resized.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="auto-crop.resources/autocrop-variant2.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="auto-crop.resources/autocrop-variant.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="auto-crop.resources/autocrop-variant4.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="auto-crop.resources/autocrop-variant3.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="auto-crop.resources/autocrop-node.png" />
        </td>
    </tr>
</table>
