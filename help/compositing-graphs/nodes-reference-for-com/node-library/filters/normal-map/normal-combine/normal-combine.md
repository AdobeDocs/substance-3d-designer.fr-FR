---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-combine.html"
breadcrumb-title: ''
description: Utilisez le nœud Combinaison de normales pour combiner plusieurs cartes de normales pour superposer les détails de surface et les détails.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Combine
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Combinaison normale
user-guide-description: ''
user-guide-title: ''
source-git-commit: 03373417b3d82a278c159aa83baf282b67c9cbe3
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 4%

---


# Combinaison normale

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/normal-combine.png){width="128px"}

<b>Entrée :</b> Filtres > Mappage normal

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Combinaison normale combine les détails de deux cartes normales d&#39;une manière mathématique correcte.

Elle est similaire à la méthode bien connue « Incrustation » d’autres logiciels de retouche d’images 2D, mais fonctionne légèrement différemment en interne (trois options).

</td>
</tr>
</table>

Il s&#39;agit de la meilleure façon et de la plus correcte d&#39;ajouter des détails de carte de normales générées en 2D à une map bakée.

Si vous souhaitez fusionner deux cartes normales sans combiner leurs détails (à l&#39;aide d&#39;un masque, par exemple), vous devez utiliser [Fusion normale](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-blend/normal-blend.md).

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Normal 2</b> <i>Couleur</i> | Description |
| <b>Normal 1</b> <i>Couleur</i> | Description |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Technique</b> *Nombre entier* | Définit la technique de fusion interne à utiliser, en échangeant la vitesse contre la qualité.<br><br>*- Whiteout (qualité faible)<br>* Mélangeur de canaux (qualité élevée)<br>* Orienté vers le détail (qualité élevée)* |

## Exemples
