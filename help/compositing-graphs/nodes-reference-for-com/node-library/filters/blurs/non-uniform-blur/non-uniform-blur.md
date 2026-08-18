---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/non-uniform-blur.html"
breadcrumb-title: ''
description: Utilisez le nœud Flou non uniforme pour appliquer un flou d’intensités différentes dans les directions X et Y pour des effets anisotropes.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Non Uniform Blur
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Flou non uniforme
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 2%

---


# Flou non uniforme

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/non-uniform-blur-grayscale.png){width="128px"}

![](../../../../../../assets/non-uniform-blur.png){width="128px"}

## Flou non uniforme (niveaux de gris)

**Entrée :** *Filtres/Flous*

**Intermédiaire**

</td>
<td style="border: 0;" valign="top">

## Description

Applique un flou de haute qualité dont l’intensité est déterminée par un masque de saisie. Les options permettent d’ajouter les options Anisotropie et Assymétrie.

## Paramètres

### Entrées

* **Carte du flou** : *entrée en niveaux de gris* carte du masque pour renforcer l&#39;effet.

### Paramètres

* **Intensité** : *0,0 - 50,0* Intensité maximale pour appliquer le flou. Masqué par la courbe de transfert du flou. Ce paramètre n’aura donc aucun effet sur les zones noires de cette courbe.
* **Anisotropie** : *0.0 - 1.0* Ajoute éventuellement une directivité à l’effet de flou. Piloté par le paramètre Angle.
* **Asymétrie** : *0.0 - 1.0* Ajoute éventuellement un biais à l&#39;échantillonnage. Piloté par le paramètre Angle.
* **Angle** :*0,0 - 1,0* Angle pour définir la directivité et le biais d’échantillonnage.
* **Échantillons** : *1 - 16* La quantité d’échantillons détermine la qualité. Multiplié par le nombre de lames.
* **Lames** : *1 -* 9\
  Quantité de secteurs d&#39;échantillonnage, détermine la qualité. Multiplié par la quantité d&#39;échantillons.

## Exemples d’images

*L&#39;exemple ci-dessous est généré par une rampe de dégradé (à 90 degrés) dans l&#39;emplacement Courbe de transfert de flou.*

![](../../../../../../assets/nonuniform-example.gif)

</td>
</tr>
</table>
