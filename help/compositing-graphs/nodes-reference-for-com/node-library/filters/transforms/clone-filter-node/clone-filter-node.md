---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/clone-filter-node.html"
breadcrumb-title: ''
description: Utilisez le noeud de filtrage Clone pour dupliquer et décaler des zones de texture afin de créer des motifs et des effets de répétition homogènes.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Clone (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Clone (Noeud de filtrage)
user-guide-description: ''
user-guide-title: ''
source-git-commit: f792519db40504d7bb888acf0dc418c6ebfd688a
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 4%

---


# Clone (Noeud de filtrage)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](clone-filter-node.resources/clone-4.png)

<b>Entrées :</b> Filtres > Transformes

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Clone l’image d&#39;entrée une fois à un emplacement spécifié. Peut fonctionner comme un outil de « tampon de duplication » brut.

Nécessite un certain soin pour obtenir les résultats escomptés :

* Idéalement, l’image d&#39;entrée doit avoir un canal Alpha (comme une décalcomanie), car la fusion n’est qu’une copie directe.
* Le masque étant défini par défaut sur le noir, une valeur de niveaux de gris blanc uniforme doit au moins être utilisée pour visualiser les résultats.
* Le décalage se découpe facilement en dehors de l’image. Utilisez donc des valeurs faibles.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Source</b> <i>Entrée couleur</i> | Image à dupliquer. Important : idéalement, l’image aura un canal Alpha ! |
| <b>Masquer</b> <i>Entrée en niveaux de gris</i> | Emplacement de masque utilisé pour masquer les effets du nœud. Par défaut, c’est le noir ! |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Décalage</b> <i>-</i> | Déplace ou translate le résultat. Positif correspond à Gauche et Haut, Négatif à Droite et Bas. Utilisez de petites valeurs, 1,0 et plus le déplace en dehors de l’image ! |
| <b>Masque de flou</b> <i>0.0 - 10.0</i> | Appliquez un filtre de flou au masque pour adoucir les contours. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="clone-filter-node.resources/clone-example.png" />
        </td>
    </tr>
</table>
