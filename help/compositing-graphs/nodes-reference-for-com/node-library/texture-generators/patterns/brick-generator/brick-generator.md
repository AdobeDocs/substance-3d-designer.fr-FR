---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/brick-generator.html"
breadcrumb-title: ''
description: Utilisez le nœud Brick Generator pour créer des motifs de briques procéduraux avec des propriétés personnalisables de taille, de décalage et de mortier.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Brick Generator
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Générateur de briques
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 0%

---


# Générateur de briques

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/brick-generator.png){width="128px"}

## Générateur de briques

**Entrée :** *Générateurs de textures**/Motifs*

**Intermédiaire**

</td>
<td style="border: 0;" valign="top">

## Description

Générateur de motif de briques avancé. Propose de nombreuses options pour générer spécifiquement des motifs de briques artificiels

Pour plus d&#39;options, voir [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md).

## Paramètres

* **Briques** : *1 - 64* définit la quantité de briques dans les axes X et Y.
* **Biseau** :*0.0 - 1.0* Modifie le profil de biseau des briques, permet de le modifier dans deux directions, ainsi que de définir le profil de retrait et l’arrondi des angles.
* **Conserver le rapport** :*Faux/Vrai* Le profil en biseau est lié ou non à la taille de la brique.
* **Espace** :*0,0 - 1,0* Espace à laisser entre les briques. Gardez à l’esprit que Biseau introduit également un espace. Par conséquent, définir également des biseaux signifie que vous devez compenser avec ce paramètre.
* **Taille moyenne** : *0,0 - 1,0* décalage du motif de brique, modifie la taille d&#39;une colonne ou d&#39;une ligne sur deux.
* **Height** : *-1.0 - 1.0* Modifie les profils d&#39;height. Permet l’introduction de la variation de luminance et toutes sortes de randomisation.
* **Pente** : *-1.0 - 1.0* Introduit une pente par brique, comme si certaines briques étaient inclinées.
* **Décalage** : *0,0 - 1,0*\
  Décale les briques par ligne et affecte l’espacement par ligne.
* **Extension non carrée** : *Faux/Vrai*\
  Permet la compensation de la courbure et de l’étirement avec des proportions non carrées.

## Exemples d’images

![](../../../../../../assets/brick-generator-ex-01.gif)

![](../../../../../../assets/brick-generator-ex-02.gif)

</td>
</tr>
</table>
