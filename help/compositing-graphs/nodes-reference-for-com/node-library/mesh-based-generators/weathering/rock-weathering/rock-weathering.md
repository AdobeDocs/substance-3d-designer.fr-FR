---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/rock-weathering.html"
breadcrumb-title: ''
description: Utilisez le nœud Altération rocheuse pour générer des motifs d'altération sur les surfaces rocheuses en fonction de la géométrie du maillage pour obtenir des effets d'érosion réalistes.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Rock Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Altération Des Roches
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 1%

---


# Altération Des Roches

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/rock-weathering.png){width="128px"}

## Altération Des Roches

**Entrée :** *Générateurs À Maillage**/Résilience*

**Complexe**

</td>
<td style="border: 0;" valign="top">

## Description

## Paramètres

### Entrées

* **Occlusion ambiante** : *Entrée en niveaux de gris*\
  Map bakée utilisée pour les effets internes et le masquage.
* **Courbure** : *Entrée en niveaux de gris*\
  Map bakée utilisée pour les effets internes et le masquage.
* **WS normal** : *entrée de couleur*\
  Baked World Space Normalmap utilisé pour les effets internes et le masquage.
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
  * **Dust** : *0.0 - 1.0*
  * **Sale** : *0.0 - 1.0*
  * **Usure Des Bords** : *0.0 - 1.0*
  * **Roche usagée** : *0.0 - 1.0*
  * **Échelle Des Fissures** : *1.0 - 60.0*
  * **Intensité des Fissures** : *0,0 - 1,0*
  * **Âge** : *0,0 - 1,0*
  * **Seuil D’Âge** : *0,0 - 1,0*
  * **Échelle Scratches Des Contours Nets** : *1.0 - 32.0*
  * **Intensité de la déformation Scratches des bords nets** : *0.0 - 1.0*
  * **Désaturation De La Roche Utilisée** : *0,0 - 1,0*
  * **Luminosité rocheuse utilisée** : *0,0 - 1,0*
* **Fusion**
  * **Intensité diffuse** : *0,0 - 1,0*\
    Intensité de fusion du diffus.
  * **Intensité des couleurs de base** : *0.0 - 1.0*\
    Intensité de fusion de la couleur de base.
  * **Intensité normale** : *0,0 - 64,0*\
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

![](../../../../../../assets/rock-ex.gif)

</td>
</tr>
</table>
