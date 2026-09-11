---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/color-match.html"
breadcrumb-title: ''
description: Utilisez le nœud Correspondance des couleurs pour faire correspondre les couleurs entre les textures afin de créer des palettes de couleurs cohérentes et d’harmoniser les textures.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Color Match
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Correspondance des couleurs
user-guide-description: ''
user-guide-title: ''
source-git-commit: 49bf753c2fa3d673b519b3ed87cc8bc82616bee6
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 1%

---


# Correspondance des couleurs

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](color-match.resources/color-match-3.png){width="128px"}

<b>Entrée :</b> Filtres > Réglages

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Tente de faire correspondre la plage de *couleurs source* à une plage de *couleurs cible*, avec prise en charge des emplacements d&#39;entrée pour définir la source et la cible.

Pour les versions plus simples, voir [Remplacer la gamme de couleurs](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/replace-color-range/replace-color-range.md) ou [Remplacer la couleur](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/replace-color/replace-color.md).

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Entrée</b> <i>Entrée couleur</i> | Entrée principale à modifier pour le résultat. |
| <b>Couleur source</b> <i>Entrée couleur</i> | Emplacement d&#39;entrée pour la couleur source, utilisé uniquement lorsque le mode Couleur source est défini sur *Entrée*. |
| <b>Couleur cible</b> <i>Entrée couleur</i> | Emplacement d&#39;entrée pour la couleur cible, utilisé uniquement lorsque le mode Couleur cible est défini sur *Entrée*. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Mode de la couleur source</b> <i>Moyenne, Paramètre, Entrée</i> | Indique si la couleur source est définie en calculant la moyenne de l’image d&#39;entrée, en définissant un paramètre ou en utilisant un emplacement d’entrée. |
| <b>Couleur source</b> <i>(valeur de couleur)</i> | Si le mode de la couleur source est défini sur *Paramètre*, ce paramètre détermine la couleur source. |
| <b>Mode colorimétrique cible</b> <i>Paramètre, Entrée Image</i> | Indique si la couleur source est définie en calculant la moyenne de l’image d&#39;entrée, en définissant un paramètre ou en utilisant un emplacement d’entrée. |
| <b>Couleur cible</b> <i>(valeur de couleur)</i> | Si le mode colorimétrique cible est défini sur *Paramètre*, ce paramètre détermine la couleur cible. |
| <b>Variation de couleur personnalisée</b> <i>Faux/Vrai</i> | Active une variante de couleur supplémentaire. |
| <b>Variation de couleur</b> | Définit les variations de teinte, de chrominance ou de Luminance sur le résultat si cette option est activée. |
| <b>Utiliser le masque</b> <i>Faux/Vrai</i> | Active/désactive l’utilisation de l’entrée ou de la sortie de masque, selon le mode de masque ci-dessous. |
| <b>Mode Masque</b> <i>Paramètre, Entrée</i> | Le mode Paramètre génère un masque détaillant la façon dont la couleur a été modifiée. Le mode Entrée permet à un masque de contrôler la force de l’effet Correspondance des couleurs. |
| <b>Masquer</b> | Génère un masque indiquant exactement où l’effet Correspondance des couleurs a été appliqué, avec des commandes supplémentaires pour lisser et flouter le masque obtenu. |
