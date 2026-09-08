---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/non-square-transform.html"
breadcrumb-title: ''
description: Utilisez le nœud Transforme non carré pour appliquer des transformations à des textures non carrées avec une mise à l’échelle indépendante X et Y.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Non-Square Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Transforme non carré
user-guide-description: ''
user-guide-title: ''
source-git-commit: 03373417b3d82a278c159aa83baf282b67c9cbe3
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 4%

---


# Transforme non carré

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/safe-transform.png)

![](../../../../../../assets/safe-transform-grayscale.png)

<b>Entrées :</b> Filtres > Transformes

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Version sans carrés de [Transformer 2D](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md). Détecte automatiquement les rapports non carrés et peut transformer des images d&#39;entrée carrées sur une zone de travail non carrée.

Assurez-vous de bien comprendre les [paramètres de Graphe](../../../../../../compositing-graphs/graph-parameters/graph-parameters.md)pour tirer le meilleur parti de ce nœud, car vous devrez définir correctement certains paramètres :

* Votre taille de **Graphe** doit être non carrée, sinon ce nœud n&#39;est pas nécessaire.
* Définissez la taille de sortie du **nœud** de Transforme non carrée sur « *Relatif au parent* ».
* Définissez le mode de répétition du **nœud** sur « *Aucune Répétition* » si vous souhaitez transformer votre entrée à une seule position.

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Mode mosaïque</b> <i>Automatique, Manuel</i> | Activez ou non les compensations automatiques non carrées. |
| <b>Mosaïque</b> <i>1 - 16</i> | Uniquement accessible lorsque le mode Mosaïque est défini sur Manuel. Permet de modifier l’échelle de manière à éviter les répétitions. |
| <b>Décalage</b> <i>0.0 - 1.0</i> | Déplace ou traduit le résultat. Double-cliquez sur le curseur pour entrer des valeurs négatives. |
| <b>Rotation</b> <i>0.0 - 1.0</i> | Fait pivoter l’image d&#39;entrée. |
| <b>Rotation Sécurisée (Carré Uniquement)</b> <i>Faux/Vrai</i> | Contraint sur des valeurs admissibles pour conserver la netteté des pixels. |
| <b>Couleur d&#39;arrière-plan</b> <i>(valeur de couleur)</i> | Couleur d’arrière-plan pour remplir l’image. Visible uniquement lorsque le Mode de répétition [&#x200B; dans les paramètres de base est défini sur « *Aucune Répétition* »](../../../../../../compositing-graphs/graph-parameters/graph-parameters.md). |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/nonsquare-ex.png" />
        </td>
    </tr>
</table>
