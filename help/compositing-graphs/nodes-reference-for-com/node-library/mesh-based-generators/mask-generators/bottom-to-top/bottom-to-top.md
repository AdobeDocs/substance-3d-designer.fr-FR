---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/bottom-to-top.html"
breadcrumb-title: ''
description: Utilisez le nœud De bas en haut pour générer des masques de dégradé de bas en haut en fonction de la position du maillage dans le monde.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Bottom To Top
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: De bas en haut
user-guide-description: ''
user-guide-title: ''
source-git-commit: c002fea6f396f09ccb3218bd290db812d8367dc4
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 1%

---


# De bas en haut

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/bottom-to-top.png){width="128px"}

## De bas en haut

**Entrée :** *Générateurs basés sur le maillage/Générateurs de masques*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Description

Génère un masque noir et blanc en fonction des maps bakées et des paramètres utilisateur. Similaires aux [masques dynamiques](https://experienceleague.adobe.com/fr/docs/substance-3d-painter/using/features/smart-materials-and-masks) dans [Painter](https://experienceleague.adobe.com/fr/docs/substance-3d-painter/using/home).

Cela génère une transition du blanc vers le noir du bas vers le haut d&#39;un modèle, ce qui est utile pour effectuer des réductions et des sélections basées sur la géométrie.

## Paramètres

### Entrées

* **Position** : *Entrée Couleur*\
  Mappage de position ancrée. Obligatoire !
* **Rugosité :** *Entrée en niveaux de gris*\
  Cela n’a rien à voir avec la rugosité PBR, mais il s’agit d’une carte de variation (facultative) pour rompre la transition. S’affiche uniquement lorsque la rugosité est définie sur une valeur supérieure à 0.
* **Masque (facultatif)** : *Entrée en niveaux de gris*\
  Emplacement de masque utilisé pour masquer les effets du nœud.

### Paramètres

* **Niveau** : *0.0 - 1.0*\
  Déplace le niveau moyen du résultat entre noir et blanc, comme un réglage de la luminosité.
* **Contraste** : *0,0 - 1,0*\
  Règle le contraste de la transition.
* **Rugosité\_Variation** : *0.0 - 1.0* détermine la quantité de la carte de rugosité à fusionner pour la variation. Augmenter cette valeur sur 0 révèle l&#39;emplacement de mappage.

## Exemples d’images

![](../../../../../../assets/bottom-to-top-ex.gif)

</td>
</tr>
</table>
