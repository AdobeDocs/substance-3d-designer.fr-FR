---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/symmetry-slice.html"
breadcrumb-title: ''
description: Utilisez le nœud Tranche de Symétrie pour découper des textures le long des axes de symétrie afin de créer des motifs et des effets en miroir.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Symmetry Slice
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Tranche de symétrie
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 6%

---


# Tranche de symétrie

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](symmetry-slice.resources/symmetry-slice-01.png){width="128px"}

<b>Entrées :</b> Filtres > Transformes

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Nœud d&#39;opération complexe de Symétrie/mise en miroir. Permet une grande variété d&#39;opérations géométriques avec un contrôle total, mais nécessite quelques essais.

Comparé à [Miroir](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/mirror-filter-node/mirror-filter-node.md) et [Symétrie](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/symmetry/symmetry.md), ce nœud dispose de beaucoup plus d&#39;options.

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Mode Symétrie</b> <i>0 - 6</i> | Sélectionnez la géométrie de symétrie/la ligne de symétrie. Les options sont Horizontal, Vertical, Diagonale Gauche-Droite, Diagonale Droite-Gauche, Inversion verticale, Angle et Angle diagonal. |
| <b>Mode de transfert</b> <i>0 - 6</i> | mode fusion. Les options sont les suivantes : |
| <b>Fusionner</b> <i>0.0 - 1.0</i> | Fusion l’image d’origine dans le résultat. |
| <b>Symétrie</b> <i>Faux/Vrai</i> | Retourne l&#39;origine, ce qui signifie que le côté origine de l&#39;opération est inversé. La symétrie de gauche à droite par exemple se transforme de droite à gauche. |
| <b>Symétrie2</b> <i>Faux/Vrai</i> | Utilisé uniquement lorsque le mode de Symétrie est 5 ou 6. Inverser l’origine des angles. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="symmetry-slice.resources/symmetry-slice-02.png" />
        </td>
    </tr>
</table>
