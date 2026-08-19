---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape-splatter-to-mask.html"
breadcrumb-title: ''
description: Utilisez le nœud Éclaboussure de forme en masque pour convertir les motifs d’éclaboussure de forme en masques pour le mélange de matériaux et les effets.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Shape Splatter to Mask
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Éclaboussure de forme en masque
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 1%

---


# Éclaboussure de forme en masque

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/shape-splatter-to-mask.png){width="128px"}

## Éclaboussure de forme en masque

**Entrée :** *Générateurs de textures**/Motifs*

**Intermédiaire**

</td>
<td style="border: 0;" valign="top">

## Description

Convertit les données d&#39;[éclaboussure de forme](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter/shape-splatter.md) en un masque noir et blanc en fonction de l&#39;ID de motif. Permet, par exemple, de créer un masque d’un certain type de motif uniquement. Propose des options supplémentaires pour sélectionner une plage d’ID de motif et masquer de manière aléatoire certaines formes.

## Paramètres

### Paramètres

* **Plage de début de l’ID de motif** : *1 - 8* Définissez le premier ID de motif dans la plage à sélectionner.
* **Plage de fin d’ID de motif** : *1 - 8* Définissez le dernier ID de motif dans la plage à sélectionner.
* **Masque aléatoire** :*0,0 - 1,0* Définissez la proportion de motifs à masquer de manière aléatoire.
* **Sortie** : *Masque binaire, Masque d&#39;entier, Valeurs de niveaux de gris* Déterminez le type de valeurs de sortie. Le masque binaire renvoie uniquement des valeurs de 0 ou 1 en noir et blanc. Le masque d’entier encode les valeurs supérieures jusqu’à 8 pour chaque motif au format HDR. Les valeurs de niveaux de gris répartissent la plage de manière proportionnelle entre 0 et 1.

</td>
</tr>
</table>
