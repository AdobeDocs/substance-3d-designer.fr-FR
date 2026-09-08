---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/ambient-occlusion-hbao-filter-node.html"
breadcrumb-title: ''
description: Utilisez le noeud de filtrage HBAO d'Ambient occlusion pour générer des cartes d'ambient occlusion à l'aide d'algorithmes basés sur l'horizon pour un ombrage réaliste.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Ambient Occlusion (HBAO) (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Ambient occlusion (HBAO) (Noeud de filtrage)
user-guide-description: ''
user-guide-title: ''
source-git-commit: a4ccdbff5343e3ece0312bd9b3318fb236f07308
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 5%

---


# Ambient occlusion (HBAO) (Noeud de filtrage)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/hbao.png){width="128px"}

<b>Entrée :</b> Filtres > Effets

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Prend une carte de hauteur comme entrée et génère une carte d’Ambient occlusion à partir de celle-ci. Il utilise Horizon-Based Ambient occlusion, un algorithme initialement destiné à la génération d&#39;AO en temps réel dans l&#39;espace de l&#39;écran. Très utile pour créer des cartes AO procédurales à partir de cartes de hauteur procédurales.

Pour une autre version plus avancée mais plus lente d&#39;AO, voir [Ambient occlusion (RTAO)](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/ambient-occlusion-rtao/ambient-occlusion-rtao.md)

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Utiliser les unités mondiales</b> <i>Faux/Vrai</i> | Active/désactive l’utilisation des unités World ou Screen-space. Active des paramètres supplémentaires qui permettent un contrôle plus précis. |
| <b>Profondeur d&#39;Height</b> <i>0.0 - 1.0</i> | Utilisé uniquement lorsque Unités universelles est défini sur Faux. Contrôle la mise à l’échelle globale. |
| <b>Taille de la surface</b> <i>0.0 - 1000.0</i> | Utilisé uniquement lorsque Unités universelles est défini sur Vrai. Contrôle la mise à l’échelle globale. |
| <b>Échelle d&#39;Height (cm)</b> <i>0.0 - 1000.0</i> | Utilisé uniquement lorsque Unités universelles est défini sur Vrai. Contrôle la mise à l’échelle globale. |
| <b>Rayon</b> <i>0.0 - 1.0</i> | Contrôle la diffusion de l’AO. |
| <b>Qualité</b> <i>4 échantillons, 8 échantillons, 16 échantillons</i> | Définit le niveau de qualité en déterminant la quantité d&#39;échantillons utilisée pour le calcul. |
| <b>Optimisation GPU</b> <i>Faux/Vrai</i> | Active l’optimisation GPU interne et accélère le traitement. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/image2021-6-18-11-11-11-1.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/image2021-6-18-11-11-22.png" />
        </td>
    </tr>
</table>
