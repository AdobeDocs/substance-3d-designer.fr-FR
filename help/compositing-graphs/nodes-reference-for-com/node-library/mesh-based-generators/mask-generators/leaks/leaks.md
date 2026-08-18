---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/leaks.html"
breadcrumb-title: ''
description: Utilisez le nœud Fuites pour générer des motifs de fuite basés sur la géométrie du maillage afin de créer des taches d'eau et des effets de fluide.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Leaks
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Fuites
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '333'
ht-degree: 1%

---


# Fuites

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/leaks.png){width="128px"}

## Fuites

**Entrée :** *Générateurs basés sur le maillage**/Générateurs de masques*

**Intermédiaire**

</td>
<td style="border: 0;" valign="top">

## Description

Génère un masque noir et blanc en fonction des maps bakées et des paramètres utilisateur. Similaires aux [masques dynamiques](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) dans [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Ce nœud représente des stries de dirt et de crasse qui fuient à partir des arêtes vives. Comme les traînées sont générées avec la position cuite, elles s&#39;étendent toujours vers le bas.

Assurez-vous de modifier le masque de variation : comme il détermine le placement des traînées, il peut avoir une influence beaucoup plus grande qu’avec d’autres générateurs de masques.

## Paramètres

### Entrées

* **Position** : *Entrée En Niveaux De Gris*\
  Carte de position ancrée, utilisée pour l’orientation des stries. Obligatoire !
* **Courbure** : *Entrée en niveaux de gris*\
  Map bakée utilisée pour la mise en place des stries. Obligatoire !
* **Occlusion ambiante** : *Entrée en niveaux de gris*\
  Map bakée utilisée pour les effets internes et le masquage. Recommandé, mais vous pouvez utiliser un blanc plat à la place.
* **Espace universel normal** : *entrée de couleur*\
  Carte normale de l&#39;espace mondial au four, utilisée pour la direction des stries. Obligatoire !
* **Masque De Variation** : *Entrée En Niveaux De Gris*\
  Masque de variation facultatif, activez en définissant le remplacement sur True.
* **Masque (facultatif)** : *Entrée en niveaux de gris*\
  Emplacement de masque utilisé pour masquer les effets du nœud.

### Paramètres

* **Niveau** : *0.0 - 1.0*\
  Niveau total du résultat. Révèle progressivement l&#39;effet, affecte également la longueur. Doit être réglé assez haut pour obtenir de longs gouttes.
* **Contraste** : *0,0 - 1,0*\
  Règle le contraste du résultat.
* **Variation** : *0.0 - 1.0* Définit la quantité de variation à grande échelle utilisée pour masquer les stries. La définition de cette valeur sur 0 entraîne des traînées uniformes complètes, évitez-la.
* **Longueur** :*0,0 - 8,0* Longueur de la strie goutte à goutte. Si vous définissez une valeur trop élevée à petite échelle, des pas visibles apparaissent. Jouez aussi avec le niveau.
* **Occlusion** : *X, Y, Z, None* Définit la direction que l&#39;AO doit affecter.
* **Remplacer le masque de variation** :*Faux/Vrai* Permet de remplacer le masque de variation par un emplacement d&#39;entrée personnalisé. L’utilisation de masques plus clairsemés ou plus denses peut être intéressante et constitue un bon moyen de contrôler les gouttes.

## Exemples d’images

![](../../../../../../assets/leaks-ex.gif)

</td>
</tr>
</table>
