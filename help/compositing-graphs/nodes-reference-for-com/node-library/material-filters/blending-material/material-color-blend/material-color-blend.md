---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/blending-material/material-color-blend.html"
breadcrumb-title: ''
description: Utilisez le nœud Fusion de couleur de matériau pour fusionner des couches de couleur entre les matériaux afin de créer des effets de matériau composite.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Blending (Material) > Material Color Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Mélange de couleurs de matière
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '466'
ht-degree: 0%

---


# Mélange de couleurs de matière

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/material-color-blend.png){width="128px"}

## Mélange de couleurs de matière

**Entrée :** *Filtres de matière/Fusion*

**Intermédiaire**

</td>
<td style="border: 0;" valign="top">

## Description

Ce nœud permet d’effectuer des réglages sur un matériau multicanal complet en mélangeant des couleurs unies par-dessus. C&#39;est la principale différence avec le [mélange d&#39;ajustement de matière](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/material-adjustment-blend/material-adjustment-blend.md), qui permet uniquement des ajustements de type [Niveaux](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/levels/levels.md) des couches, tandis que ce nœud utilise des ajustements de type [mélange](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md) avec une couleur unie.

Ce nœud est particulièrement utile lorsque vous souhaitez soit introduire un conseil de couleur plat dans Couleur diffuse ou Couleur de base, soit « aplatir » d’autres couches à l’aide d’une valeur de couleur unie définie.

## Paramètres

### Entrées

* **ColorID** : *entrée de couleur*\
  Emplacement de masque utilisé pour masquer les effets du nœud.
* **Masque De Niveaux De Gris** : *Entrée En Niveaux De Gris*\
  Emplacement de masque utilisé pour masquer les effets du nœud.

### Paramètres

* **Canaux**
  * Activez et désactivez les couches de matériau dans ce groupe, lors de l’utilisation de cartes de Specular/brillance au lieu de cartes de métal/rugosité, par exemple.
* **Diffus**
  * **Couleur** : *(Valeur de couleur)*Quelle valeur de couleur fusionner au-dessus de la couche diffuse ?
  * **Opacité** : *0.0 - 1.0*\
    Opacité de fusion entre le premier plan et l’arrière-plan.
  * **Mode de fusion** : *Normal, Ajouter, Soustraire, Multiplier, Ajouter/Soustraire, Max, Min, Basculer* le mode de fusion à utiliser dans l&#39;opération.
* **Couleur de base**
  * Fusionne une couleur unie au-dessus de cette couche avec des options comme dans le groupe Diffuse.
* **Normal**
  * **Source** : *Height, masque*
  * **Mode de fusion** : *Combiner, Fusionner*
  * **Intensité des Heights** : *0,0 - 1,0*
  * **Opacité de l&#39;Height** : *0.0 - 1.0*
  * **Format** : *DirectX, OpenGL*
* **Specular**
  * Fusionne une couleur unie au-dessus de cette couche avec des options comme dans le groupe Diffuse.
* **Émissif**
  * Fusionne une couleur unie au-dessus de cette couche avec des options comme dans le groupe Diffuse.
* **Lustre**
  * Fusionne une couleur unie au-dessus de cette couche avec des options comme dans le groupe Diffuse.
* **Rugosité**
  * Fusionne une couleur unie au-dessus de cette couche avec des options comme dans le groupe Diffuse.
* **Métallique**
  * Fusionne une couleur unie au-dessus de cette couche avec des options comme dans le groupe Diffuse.
* **Specular level**
  * Fusionne une couleur unie au-dessus de cette couche avec des options comme dans le groupe Diffuse.
* **Occlusion ambiante**
  * Fusionne une couleur unie au-dessus de cette couche avec des options comme dans le groupe Diffuse.
* **Height**
  * Fusionne une couleur unie au-dessus de cette couche avec des options comme dans le groupe Diffuse.
* **Opacité**
  * Fusionne une couleur unie au-dessus de cette couche avec des options comme dans le groupe Diffuse.
* **Masque d&#39;identifiant de couleur** :*Faux/Vrai* Utilisez le Masque d&#39;identifiant de couleur à la place du masque en niveaux de gris. Gardez à l’esprit qu’il ne s’agit que d’une seule couleur !\
  Active toutes les options ci-dessous.
* **Couleur** : *(Valeur de couleur)*Quelle couleur choisir et convertir en blanc.
* **Flou** :*0.01 - 1.0* Degré de fusion de la couleur sélectionnée avec ses voisines.
* **Remplissage** : *0.0 - 1.0* contraste de transition de la couleur sélectionnée.

## Exemples d’images

|  |
| --- |
| Aucune image n&#39;est jointe à cette page. |

</td>
</tr>
</table>
