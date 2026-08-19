---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/exposure-preview.html"
breadcrumb-title: ''
description: Utilisez le nœud Aperçu de l’exposition pour prévisualiser les réglages d’exposition dans les environnements HDRI avant le rendu final.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Exposure Preview
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Aperçu de l’exposition
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 1%

---


# Aperçu de l’exposition

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/hdr-exposure-preview.png){width="200px"}

## Aperçu de l’exposition

**Entrée :** *Vue/Outils HDRI 3D*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Description

Nœud d’assistant pour prévisualiser les étapes d’exposition. L’utilisateur définit une valeur minimale et maximale, le nœud génère une image beaucoup plus grande avec un certain nombre de versions exposées différentes de l’entrée d’origine. Les différentes versions sont toujours empilées horizontalement, la quantité dépend de la résolution du nœud ou du graphique.

## Paramètres

* **Exposition maximale (EV)** : *-8,0 - 8,0*\
  Exposition maximale de l’image la plus lumineuse du haut.
* **Exposition minimale (EV)** : *-8.0 - 8.0* Exposition minimale de l’image du bas la plus sombre.

## Exemples d’images

![](../../../../../../assets/exp-preview-ex.png)

</td>
</tr>
</table>
