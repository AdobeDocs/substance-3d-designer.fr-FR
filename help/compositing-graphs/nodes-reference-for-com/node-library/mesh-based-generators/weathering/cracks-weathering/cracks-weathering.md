---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/cracks-weathering.html"
breadcrumb-title: ''
description: Utilisez le nœud Fissures Weathering pour ajouter des motifs de fissures aux matériaux en fonction de la courbure du maillage et des points de contrainte.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Cracks Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Fissures Weathering
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 1%

---


# Fissures Weathering

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/cracks-weathering.png){width="128px"}

## Fissures Weathering

**Entrée :** *Générateurs À Maillage**/Résilience*

**Complexe**

</td>
<td style="border: 0;" valign="top">

## Description

Il s’agit d’un effet matériel qui fonctionne sur plusieurs canaux à la fois. Il ajoute un motif de fissure aléatoire, avec un contrôle sur l’étendue et la profondeur.

Assurez-vous de bien comprendre les [modes de création de liens](../../../../../../interface/the-graph-view/link-creation-modes/link-creation-modes.md) lorsque vous travaillez avec des matériaux complets.

## Paramètres

### Entrées

* **Courbure** : *Entrée en niveaux de gris*\
  Mappage cuit ou généré utilisé pour les effets internes et le masquage.
* **Height** : *Entrée en niveaux de gris*\
  Mappage cuit ou généré utilisé pour les effets internes et le masquage.
* **Masque** : *Entrée En Niveaux De Gris*\
  Emplacement de masque utilisé pour masquer les effets du nœud. Peut être basculé avec le paramètre « Mask ».

### Paramètres

* **Canaux**
  * Activez et désactivez les canaux de matériau dans ce groupe, par exemple lorsque vous utilisez des cartes de Specular/brillance au lieu de cartes de métal/rugosité.
* **Avancé**
  * **Format normal** : *DirectX, OpenGL*\
    Bascule entre différents formats de mappage normal (inverse la couche verte).
  * **Masque** : *Faux/Vrai*\
    Active ou désactive l&#39;utilisation de la carte de masque.
* **Effet**
  * **Propagation des Fissures** : *0.0 - 1.0*&#x200B;Étendue des fissures. Il s’agit de la commande principale de cet effet.
  * **Profondeur des Fissures** : *0,0 - 1,0* Profondeur de l’effet de fissure. Cela affecte principalement l’height et affecte légèrement le thickness visuel.
* **Fusion**
  * Contrôle la force de fusion de l’effet dans chaque couche obtenue.

## Exemples d’images

![](../../../../../../assets/cracks-ex.gif)

</td>
</tr>
</table>
