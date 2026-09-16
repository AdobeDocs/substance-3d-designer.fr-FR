---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/directional-blur.html"
breadcrumb-title: ""
description: Utilisez le nœud Flou directionnel pour appliquer des effets de flou dans une direction spécifique afin de créer des effets de flou directionnel et de traînée.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Directional blur
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Flou directionnel
user-guide-description: ""
user-guide-title: ""
source-git-commit: a22681c0410386966a80a0170c62fae57da6ef74
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 8%
---

# Flou directionnel

<table>
<tr style="border: 0;">
<td style="border: 0; width:33.33%; vertical-align:top">

![Noeud atomique : Flou directionnel](directional-blur.resources/comp_dirmotionblur_1.png "Noeud atomique : Flou directionnel"){width="100%"}

<b>Entrée :</b> Noeuds atomiques

</td>
<td style="border: 0;" valign="top">

Applique un floutage dans une direction spécifiée selon une map d’intensité.

Ce nœud effectue une opération similaire à un flou directionnel sur une entrée. Contrairement au nœud « [Flou](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blur/blur.md) » standard, qui applique un flou uniforme dans toutes les directions, le « Flou directionnel » fonctionne selon un angle défini par l&#39;utilisateur.

</td>
</tr>
</table>

<table>
<tr style="border: 0">
<td style="border: 0; width: 15%"></td>
<td style="border: 0; text-align: center"><img src="directional-blur.resources/directional-blur-tooltip.gif" alt="info-bulle flou directionnel" /></td>
<td style="border: 0; width: 15%"></td>
</tr>
</table>

Comme pour le flou, il s&#39;agit également d&#39;une opération plus rapide et de qualité médiocre. Une alternative étendue et de meilleure qualité est fournie dans [Flou anisotrope](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/anisotropic-blur/anisotropic-blur.md), avec un compromis de performances


## Flou directionnel et anisotrope

Les images ci-dessous montrent le flou directionnel et le flou [anisotrope](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/anisotropic-blur/anisotropic-blur.md) en vigueur sur la même forme d&#39;entrée, avec des paramètres similaires. Le flou anisotrope a été défini sur anisotropie totale et haute qualité.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<b>Flou directionnel</b>

![Comparaison du flou directionnel](directional-blur.resources/dirblur-01.png "Comparaison du flou directionnel"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

<b>Flou anisotrope</b>

![Comparaison du flou anisotrope](directional-blur.resources/aniso-01.png "Comparaison du flou anisotrope"){zoomable="yes"}

</td>
</tr>
</table>


## Paramètres

|  |  |
| --- | --- |
| <b>Intensité</b> *Flottant* | Définit le rayon de flou en pixels. |
| <b>Angle</b> *Flottant* | La direction de l&#39;effet de flou en nombre de tours dans le sens horaire, en partant de l&#39;horizontale - c&#39;est-à-dire le vecteur de direction (1, 0). |

## Connecteurs d’entrée

|  |  |
| --- | --- |
| <b>Entrée</b> *Niveaux de gris/Couleur* [PRIMAIRE](../../../../glossary/glossary.md) | Image à traiter. |


## Exemples

*Bientôt disponible.*
