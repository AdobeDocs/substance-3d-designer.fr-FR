---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/utilities-mesh-based-generators/3d-planar-projection.html"
breadcrumb-title: ''
description: Utilisez le nœud de Projection Planaire 3D pour projeter des textures sur les surfaces du maillage à l'aide de la projection planaire pour le placage de texture.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Utilities (Mesh Based Generators) > 3D Planar Projection
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: projection Planaire 3D
user-guide-description: ''
user-guide-title: ''
source-git-commit: fbf066c7185f74dcbf35156afc3873d192f77abc
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 7%

---


# projection Planaire 3D

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/3d-planar-gray.png)![](../../../../../../assets/3d-planar.png)

<b>Entrée :</b> Générateurs basés sur le Maillage > Utilitaires

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Effectue une projection planaire en fonction des données de maillage bakées (Position et Maps normal universelles). Permet de projeter et de placer des décalcomanies entre les seams, indépendamment du mappage UV d’origine.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Mappage de position</b> <i>Entrée couleur</i> | Mappage de position baké |
| <b>Espace universel normal</b> <i>Entrée couleur</i> | Carte de Normale de l&#39;espace monde bakée |
| <b>Texture projetée</b> <i>Entrée couleur</i> | Texture d’entrée pour projeter sur la cible. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Positionnement</b> |  |
| <b>Entrée de projet</b> <i>Position UV, Position Espace monde</i> | Choisissez si la position de la projection est définie en 2D/UV ou en 3D/Espace monde. |
| <b>Position d&#39;UV cible</b> | Uniquement avec Entrée de position, à utiliser de préférence pour sélectionner un point dans la Vue 2D sur le mappage de position. |
| <b>Position cible</b> <i>(valeur de couleur)</i> | Uniquement avec l’entrée Position Espace monde, vous permet de définir une coordonnée 3D exacte. |
| <b>Cible normale</b> <i>(valeur de couleur)</i> |  |
| <b>Rotation</b> <i>0.0 - 1.0</i> | Fait pivoter la texture projetée selon son axe normal. |
| <b>Échelle</b> <i>0.0 - 1.0</i> | Définissez l’échelle globale de la texture projetée. |
| <b>Taille</b> <i>0.0 - 2.0</i> | Effectuez une mise à l’échelle non uniforme sur la texture projetée. |
| <b>Masquage</b> |  |
| <b>Profondeur Maximale</b> <i>0.0 - 1.0</i> | Détermine la profondeur à laquelle la texture projetée apparaîtra et le moment où elle sera coupée. |
| <b>Atténuation de Profondeur</b> <i>0.0 - 1.0</i> | Définissez la transition pour que la profondeur de coupure soit soudaine ou estompée. |
| <b>Seuil Normal</b> <i>-1.0 - 1.0</i> | Définissez le seuil pour les surfaces qui ne sont pas exactement alignées sur la normale de la projection. |
| <b>Atténuation normale</b> <i>0.0 - 1.0</i> | Définissez la transition pour les surfaces non alignées sur soudaine ou atténuation. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/3d-planar-projection-ex.gif" />
        </td>
    </tr>
</table>
