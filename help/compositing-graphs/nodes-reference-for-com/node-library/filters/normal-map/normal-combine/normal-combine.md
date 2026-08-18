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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 2%

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

## Connecteurs d’entrée

Description de la <b>couleur normale 2</b> *couleur*

Description de la <b>couleur normale 1</b> *couleur*

## Paramètres

<b>Technique</b> *Entier* Définit la technique de fusion interne à utiliser, en négociant la vitesse pour la qualité.\
*- Whiteout (qualité inférieure)
* Mélangeur de couches (haute qualité)
* Orienté vers le détail (haute qualité)*

## Exemples
