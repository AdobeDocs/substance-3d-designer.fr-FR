---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/exposure-preview.html"
breadcrumb-title: ''
description: Utilisez le nœud Aperçu de l’exposition pour prévisualiser les réglages d’exposition dans les environnements HDRI avant le rendu final.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Exposure Preview
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Aperçu de l’exposition
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 7%

---


# Aperçu de l’exposition

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](exposure-preview.resources/hdr-exposure-preview.png){width="200px"}

<b>Entrée :</b> vue 3D > Outils HDRI

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Nœud d’assistant pour prévisualiser les étapes d’exposition. L’utilisateur définit une valeur minimale et maximale, le nœud génère une image beaucoup plus grande avec un certain nombre de versions exposées différentes de l’entrée d’origine. Les différentes versions sont toujours empilées horizontalement, la quantité dépend de la résolution du nœud ou du graphique.

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Exposition maximale (EV)</b> <i>-8.0 - 8.0</i> | Exposition maximale de l’image la plus lumineuse du haut. |
| <b>Exposition Min (EV)</b> <i>-8.0 - 8.0</i> | Exposition minimale de l’image la plus sombre du bas. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="exposure-preview.resources/exp-preview-ex.png" />
        </td>
    </tr>
</table>
