---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/emboss-with-gloss.html"
breadcrumb-title: ''
description: Utilisez le nœud Embossage avec brillance pour créer des effets d’estampage avec des cartes de brillance afin d’ajouter de la profondeur et de la brillance aux textures.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Emboss With Gloss
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Embossage avec brillance
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 6%

---


# Embossage avec brillance

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](emboss-with-gloss.resources/emboss-with-gloss-01.png){width="128px"}

<b>Entrée :</b> Filtres > Effets

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Applique un effet d’estampage avec ajout de brillance (réflexion au specular) sur une couleur et l’entrée d’height. Ajoute essentiellement un faux éclairage baké à une image en fonction des informations sur l’height. Utile pour certains styles de texture qui nécessitent un éclairage baké dans les textures.

Pour une version avec plus d&#39;options, voir [Uber Embossage](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/uber-emboss/uber-emboss.md). Il existe également une version atomique plus simple de l&#39;[Embossage](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/emboss/emboss.md).

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Couleur</b> <i>Entrée couleur</i> |  |
| <b>Height</b> <i>Entrée en niveaux de gris</i> |  |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Couleur des tons clairs</b> <i>(valeur de couleur)</i> | Couleur de la surbrillance du specular. |
| <b>Couleur des tons foncés</b> <i>(valeur de couleur)</i> | Couleur utilisée dans les zones ombrées/non éclairées. |
| <b>Brillant</b> <i>0.0 - 0.5</i> | Taille de surbrillance de la brillance. |
| <b>Intensité</b> <i>0.0 - 10.0</i> | Intensité du ton clair. |
| <b>Angle de la lumière</b> <i>0.0 - 1.0</i> | Angle d’incidence de la lumière (simulée). |
