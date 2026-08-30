---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/edge-detect.html"
breadcrumb-title: ''
description: Utilisez le nœud Détection des contours pour détecter les contours dans les textures de création de contours et d’effets de masque sur les contours.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Edge Detect
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Edge Detect
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 7%

---


# Edge Detect

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](edge-detect.resources/edge-detect.png){width="128px"}

<b>Entrée :</b> Filtres > Effets

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Détecte le contraste d’une image en noir et blanc, puis crée une image en noir et masque blanc mettant en évidence le contraste.

Utile dans de nombreux cas où une sorte de masque pour les bords est nécessaire. N&#39;oubliez pas que cela fonctionne mieux avec une entrée à contraste élevé ; si nécessaire, ajustez le contraste avant de passer quelque chose dans ce nœud.

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Largeur du contour</b> <i>1.0 - 16.0</i> | Largeur des zones détectées autour des bords. |
| <b>Arrondi Des Bords</b> <i>0.0 - 16.0</i> | Arrondit, floute et lisse le masque généré ensemble. |
| <b>Inverser</b> <i>Faux/Vrai</i> | Inverse le résultat. |
| <b>Tolérance</b> <i>0.0 - 1.0</i> | Facteur de seuil de tolérance pour l&#39;emplacement où les arêtes doivent apparaître. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="edge-detect.resources/edge-detect-ex.png" />
        </td>
    </tr>
</table>
