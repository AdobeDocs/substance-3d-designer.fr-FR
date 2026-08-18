---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/moss-weathering.html"
breadcrumb-title: ''
description: Utilisez le nœud altération de la mousse pour ajouter des motifs de croissance de mousse aux matériaux en fonction de la courbure et de la position du maillage.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Moss Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Altération De La Mousse
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 1%

---


# Altération De La Mousse

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/moss-weathering.png){width="128px"}

## Altération De La Mousse

**Entrée :** *Générateurs À Maillage**/Résilience*

**Complexe**

</td>
<td style="border: 0;" valign="top">

## Description

Il s’agit d’un effet matériel qui fonctionne sur plusieurs canaux à la fois. Il génère un effet de mousse sur-développée, avec un seul contrôle pour la propagation.

Cet effet fonctionne mieux avec une carte de position de l&#39;espace universel et une carte de hauteur supplémentaire. Bien que ce ne soit pas une exigence exacte, cela confère à l&#39;effet un placement plus crédible.

Assurez-vous de bien comprendre les [modes de création de liens](https://support.allegorithmic.com/documentation/display/SD5/Link+Creation+Modes) lorsque vous travaillez avec des matériaux complets.

## Paramètres

### Entrées

* **Position** : *Entrée Couleur*\
  Baking World Space Position.
* **Height** : *Entrée en niveaux de gris*\
  Entrée Heightmap supplémentaire.
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
  * **Propagation de la mousse** : *0.0 - 1.0* définit la propagation de la mousse. Pousse par étapes, d&#39;une couverture légère à une mousse épaisse, épaisse et foncée.
* **Fusion**
  * **Intensité diffuse** : *0,0 - 1,0*\
    Intensité de fusion du diffus.
  * **Intensité des couleurs de base** : *0.0 - 1.0*\
    Intensité de fusion de la couleur de base.
  * **Intensité normale** : *0,0 - 1,0*\
    Intensité de fusion de la normale.
  * **Intensité du Specular** : *0,0 - 1,0*\
    Intensité de fusion du Specular.
  * **Intensité du brillant** : *0.0 - 1.0*\
    Intensité de fusion du brillant.
  * **Intensité de la rugosité** : *0.0 - 1.0*\
    Intensité de fusion de la rugosité.
  * **Intensité de l&#39;Occlusion ambiante** : *0,0 - 1,0*\
    Intensité de fusion de l&#39;Occlusion ambiante.
  * **Intensité des Heights** : *0,0 - 1,0*\
    Intensité de fusion de l&#39;Height.

## Exemples d’images

![](../../../../../../assets/moss-ex.gif)

</td>
</tr>
</table>
