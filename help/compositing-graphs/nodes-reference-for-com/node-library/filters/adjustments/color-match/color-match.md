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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 1%

---


# Correspondance des couleurs

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/color-match-3.png){width="128px"}

## Correspondance des couleurs

**Entrée :** *Filtres/Réglages*

**Complexe**

</td>
<td style="border: 0;" valign="top">

## Description

Tente de faire correspondre la plage de *couleurs source* à une plage de *couleurs cible*, avec prise en charge des emplacements d&#39;entrée pour définir la source et la cible.

Pour les versions plus simples, voir [Remplacer la gamme de couleurs](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/replace-color-range/replace-color-range.md) ou [Remplacer la couleur](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/replace-color/replace-color.md).

## Paramètres

### Entrées

* **Entrée** : Entrée *Couleur*\
  Entrée principale à modifier pour le résultat.
* **Couleur source** : *Entrée de couleur*\
  Emplacement d&#39;entrée pour la couleur source, utilisé uniquement lorsque le mode Couleur source est défini sur *Entrée*.
* **Couleur cible** : emplacement d&#39;entrée *Entrée de couleur* pour la couleur cible, utilisé uniquement lorsque le mode Couleur cible est défini sur *Entrée*.

### Paramètres

* **Mode de la couleur source** : *Moyenne, paramètre, entrée* Définit si la couleur source est définie en calculant la moyenne de l&#39;image d&#39;entrée, en définissant un paramètre ou en utilisant un emplacement d&#39;entrée.
* **Couleur source** : *(Valeur de couleur)* Si le mode Couleur source est défini sur *Paramètre*, ce paramètre détermine la couleur source.
* **Mode colorimétrique cible** : *paramètre, entrée d&#39;image* Définit si la couleur source est définie en calculant la moyenne de l&#39;image d&#39;entrée, en définissant un paramètre ou en utilisant un emplacement d&#39;entrée.
* **Couleur cible** : *(Valeur de couleur)* Si le mode colorimétrique cible est défini sur *Paramètre*, ce paramètre détermine la couleur cible.
* **Variation de couleur personnalisée** : False/True\
  Active une variante de couleur supplémentaire.
* **Variation de couleur**\
  Définit les variations de teinte, de chrominance ou de luminance sur le résultat si cette option est activée.
* **Utiliser le masque** : *Faux/Vrai*\
  Active/désactive l’utilisation de l’entrée ou de la sortie de masque, selon le mode de masque ci-dessous.
* **Mode de masque** : *Paramètre, entrée* Le mode Paramètre génère un masque détaillant la façon dont la couleur a été modifiée. Le mode Entrée permet à un masque de contrôler l’intensité de l’effet Correspondance des couleurs.
* **Masquer**\
  Génère un masque indiquant exactement où l’effet Correspondance des couleurs a été appliqué, avec des commandes supplémentaires pour lisser et flouter le masque obtenu.

## Exemples d’images

|  |
| --- |
| Aucune image n&#39;est jointe à cette page. |

</td>
</tr>
</table>
