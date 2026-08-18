---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/pbr-albedo-safe-color.html"
breadcrumb-title: ''
description: Utilisez le nœud Couleur admissible pour l'Albédo PBR pour vous assurer que les couleurs d'albédo se trouvent dans des plages physiquement plausibles pour les matériaux PBR.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > PBR Utilities > PBR Albedo Safe Color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Couleur sécurisée pour l’Albédo PBR
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 1%

---


# Couleur sécurisée pour l’Albédo PBR

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/pbr-albedo-safe-color.png){width="128px"}

## Couleur sécurisée pour l’Albédo PBR

**Entrée :** *Filtres de matériaux/Utilitaires PBR*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Description

Il s’agit d’un nœud utilitaire qui effectue des corrections si les valeurs Couleur de base ou Diffuse se trouvent en dehors d’une plage acceptable et PBR. Lorsqu’il est défini sur Métallique, le nœud tente également de corriger les valeurs de couleur de base en fonction de l’intensité métallique.

Voir également [couleur de base PBR / validation métallique](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/pbr-basecolor-metallic/pbr-basecolor-metallic-validate.md) pour obtenir un retour visuel sur les zones qui pourraient être erronées.

C&#39;est utile comme outil de correction rapide, surtout quand on apprend encore PBR, mais pas comme mesure absolue qui est toujours censée être correcte.

## Paramètres

* **Workflow PBR** :*couleur de base : métallique, diffuse, Specular* bascule entre deux workflows PBR différents.
* **Tolérance** : *0,0 - 1,0* Niveau de tolérance pour les valeurs qui sont hors limites.

## Exemples d’images

|  |
| --- |
| Aucune image n&#39;est jointe à cette page. |

</td>
</tr>
</table>
