---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/season-filter.html"
breadcrumb-title: ''
description: Utilisez le nœud Filtre de saison pour appliquer des effets de saison aux matériaux afin de créer des variations printanières, estivales, automnales et hivernales.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Season Filter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Filtre de saison
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 0%

---


# Filtre de saison

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/default-icon.png){width="128px"}

## Filtre de saison

**Entrée :** *Filtres/Effets De Matière*

**Complexe**

</td>
<td style="border: 0;" valign="top">

## Description

Ce nœud ajoute des effets tels qu’un niveau d’eau animé, de la neige, de la glace et/ou de la mousse.

Gardez à l’esprit qu’il s’agit d’un filtre plus ancien qui n’est pas destiné à être entièrement PBR-correct. Il est généralement conservé pour des raisons liées à l’héritage/à la compatibilité, même s’il peut être utile dans certains cas. Des versions correctes PBR plus récentes se trouvent dans [Couverture de Snow](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/snow-cover/snow-cover.md) et [Niveau d&#39;eau](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/water-level/water-level.md).

Le nœud nécessite un ensemble approprié d&#39;entrées de matériau, principalement avec une carte de hauteur ou une carte de normales récemment détaillée.

## Paramètres

### Entrées

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
  * **Intensité de la lumière** : *0,0 - 1,0*\
    Intensité de la lumière (simulée).
  * **Angle De La Lumière** : *0,0 - 1,0*\
    Angle d’incidence de la lumière (simulée)
* **Effet**
  * **Effet de l&#39;Height ou normal** : *Height, normal* choisit le mappage d&#39;entrée qui pilote les effets.
  * **Niveau d&#39;eau** : *0.0 - 1.0*&#x200B;Élève ou abaisse le niveau d&#39;eau en fonction des informations d&#39;Height/Normal.
  * **Détails de l&#39;eau** :*0.0 - 1.0* définit la quantité de détails dans l&#39;eau.
  * **Réfraction** : *0,0 - 1,0* Définit la quantité de fausse réfraction dans l’effet.
  * **Réflexion** : *0,0 - 1,0* définit la quantité de faux reflet dans l’effet.
  * **Distance de réflexion** :*0.0 - 1.0* contrôle les visuels de réflexion.
  * **Angle de réflexion** : *0.0 - 1.0* contrôle les visuels de réflexion.
  * **Direction du flux** :*0.0 - 1.0* contrôle le flux de l&#39;animation (utilisez la Substance Player pour la visualisation).
  * **Glace** :*0.0 - 1.0* Définit le degré de congélation de l&#39;eau.
  * **Détails de la glace** :*0.0 - 1.0* Définit la quantité de détails dans la glace.
  * **Snow** : *0.0 - 1.0* Définit la quantité de couverture de neige.
  * **Mousse** : *0,0 - 1,0* définit la quantité de couverture de mousse.
  * **Échelle de mousse** : *1 - 4* définit l’échelle de la texture de mousse générée.
  * **Couleur de la mousse** : *(Valeur de couleur)*Définit la couleur de la mousse.
  * **Couleur de l&#39;eau** : *(Valeur de couleur)*Définit la couleur de l&#39;eau, y compris l&#39;alpha/opacité.
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

|  |
| --- |
| Aucune image n&#39;est jointe à cette page. |

</td>
</tr>
</table>
