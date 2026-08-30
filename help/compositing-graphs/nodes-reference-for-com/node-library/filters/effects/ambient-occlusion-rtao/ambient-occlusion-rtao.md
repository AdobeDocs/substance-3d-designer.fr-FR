---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/ambient-occlusion-rtao.html"
breadcrumb-title: ''
description: Utilisez le nœud d'Occlusion ambiante (RTAO) pour générer des cartes d'occlusion ambiante en temps réel à partir de cartes d'height pour un ombrage réaliste.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Ambient Occlusion (RTAO)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Occlusion ambiante (RTAO)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 1%

---


# Occlusion ambiante (RTAO)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icône de nœud RTAO](ambient-occlusion-rtao.resources/rt-ao.png "Icône de nœud RTAO")

<b>Entrée :</b> Filtres > Effets

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Génère une carte d&#39;Occlusion ambiante en fonction d&#39;une entrée de carte d&#39;height.

Ce filtre donne des résultats plus précis que le HBAO, mais ne doit pas être utilisé en combinaison avec le moteur CPU (SSE) en raison du temps de calcul.

Voir [Occlusion ambiante (HBAO) (nœud de filtre)](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/ambient-occlusion-hbao/ambient-occlusion-hbao-filter-node.md) pour une alternative plus simple et plus rapide.

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Utiliser la Taille physique</b> <i>Booléen</i> | Activez/désactivez cette option pour utiliser les paramètres de Taille physique afin de déterminer l’échelle d’height. |
| <b>Taille physique</b> <i>Float3</i> <i>(Disponible lorsque <b>Utiliser la Taille physique</b> est défini sur <i>Vrai</i>)</i> | Ajuste l’échelle d’height en fonction de la taille physique réelle de la surface |
| <b>Exemples</b> <i>Nombre entier</i> | Nombre de rayons utilisés pour calculer l&#39;ambient occlusion.<br>Une valeur plus élevée offre un résultat plus lisse et plus précis au détriment des performances. |
| <b>Échelle d&#39;Height</b> <i>Flotter</i> <i>(Disponible lorsque <b>Utiliser la Taille physique</b> est défini sur <i>Faux</i>)</i> | Multiplicateur de l’intensité de l’entrée de courbe de transfert d’height. |
| <b>Distribution</b> <i>Nombre entier</i> | Définit la méthode de distribution. Affecte la réduction vers les zones ombrées, |
| <b>Distance Maximale</b> <i>Flotter</i> | Définit la distance maximale que les rayons peuvent parcourir pour être occultés. |
| <b>Angle de répartition</b> <i>Flotter</i> | Définit l’angle d’étalement des rayons sur lesquels la prise de vue doit être effectuée. Une valeur de 1 correspond à un hémisphère entier. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="ambient-occlusion-rtao.resources/image2021-6-18-11-7-48.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="ambient-occlusion-rtao.resources/image2021-6-18-11-9-0-1.png" />
        </td>
    </tr>
</table>
