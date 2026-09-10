---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/utilities-mesh-based-generators/material-mesh-data-blender.html"
breadcrumb-title: ''
description: Utilisez le nœud Matériau Maillage Data Blender pour fusionner les données de maillage de matériau afin de créer des transitions fluides entre différentes zones de matériau.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Utilities (Mesh Based Generators) > Material Mesh Data Blender
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Matériau Maillage Data Blender
user-guide-description: ''
user-guide-title: ''
source-git-commit: 1ea5f4e048a3b4591bf71d9b18707837dac1bf6f
workflow-type: tm+mt
source-wordcount: '572'
ht-degree: 8%

---


# Matériau Maillage Data Blender

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](material-mesh-data-blender.resources/material-mesh-data-blender.png){width="128px"}

<b>Entrée :</b> Générateurs basés sur le Maillage > Utilitaires

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Ce nœud est destiné à faciliter l’ajout de détails en fonction de données bakées. Il est livré avec de nombreux curseurs pour modifier un matériau d&#39;entrée complet, en fonction de toutes les maps bakées comme entrée. Faites des essais, car il y a beaucoup d&#39;options.

Elle est utile pour ajouter une mise en surbrillance des contours en fonction de la courbure ou d’autres textures, pour fusionner certains éléments AO avec la couleur de Diffuse/de base, pour ajouter une Occlusion de Specular en fonction de la Courbure et/ou de l’AO, etc.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Entrée de Matériau complète (groupe « Matériau »)</b> | Ensemble complet de cartes de matériau.<br><br>Ceux-ci sont modifiés par ce nœud, puis renvoyés en tant que sortie. |
| <b>Occlusion ambiante</b> <i>Entrée en niveaux de gris</i> | Map bakée utilisée pour les effets internes et le masquage. |
| <b>Courbure</b> <i>Entrée en niveaux de gris</i> | Map bakée utilisée pour les effets internes et le masquage. |
| <b>Height</b> <i>Entrée en niveaux de gris</i> |  |
| <b>Normal</b> <i>Entrée couleur</i> |  |
| <b>Couleur Vertex</b> <i>Entrée couleur</i> |  |
| <b>Espace universel normal</b> <i>Entrée couleur</i> |  |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Canaux</b> | Activez et désactivez les canaux de matériau dans ce groupe, par exemple lorsque vous utilisez des cartes de Specular/brillance au lieu de cartes de métal/rugosité. Affecte la disponibilité des paramètres ci-dessous. |
| <b>Maps bakées</b> | Indique si les maps bakées répertoriées doivent être utilisées pour les calculs. Affecte la disponibilité des paramètres ci-dessous. |
| <b>Diffuse AO</b> <i>0.0 - 1.0</i> | Quantité d’Ambient occlusion à fusionner dans le Diffuse. |
| <b>Bords nets</b> Diffuse <i>0.0 - 1.0</i> | Valeur de la courbe de référence à fusionner avec le diffus. |
| <b>Couleur De Diffuse À Partir De La Couleur De Vertex</b> <i>0.0 - 1.0</i> | Degré de fusion de la couleur du sommet dans le mode Diffus. |
| <b>Diffuse Pré-Éclairage</b> <i>0.0 - 1.0</i> | Quantité de (faux) pré-éclairage, en fonction des normales de l’espace universel. |
| <b>Balance de l&#39;éclairage des dessins animés</b> <i>0.0 - 1.0</i> | Permet de passer d’un éclairage réaliste à un éclairage caricatural pour le diffus. |
| <b>Calques De Pré-Éclairage De Dessin Animé Par Diffuse</b> <i>0 - 10</i> | Contrôle l’aspect des calculs d’éclairage du dessin animé. |
| <b>Contours de dessin animé Diffuse</b> <i>0.0 - 1.0</i> | Contrôle l’aspect des calculs d’éclairage du dessin animé. |
| <b>Base color AO</b> <i>0.0 - 1.0</i> | Quantité d’Occlusion ambiante à fusionner avec la couleur de base. |
| <b>Base color des contours nets</b> <i>0.0 - 1.0</i> | Quantité de courbe de référence à fusionner avec la couleur de base. |
| <b>Base color À Partir De La Couleur Du Vertex</b> <i>0.0 - 1.0</i> | Degré de fusion de la couleur du sommet avec la couleur de base. |
| <b>Intensité normale du Matériau</b> <i>0.0 - 1.0</i> | Intensité de fusion de la texture normale (tangente) cuite. |
| <b>SpecularAO</b> <i>0.0 - 1.0</i> | Intensité de fusion de l&#39;AO dans le Specular. |
| <b>Bords nets Specular vifs</b> <i>0.0 - 1.0</i> | Force de fusion de la Courbure dans le Specular. |
| <b>Contours de dessin animé Specular</b> <i>0.0 - 1.0</i> | Force de fusion d’un effet de contour de Specular de dessin animé, en fonction de la Courbure. |
| <b>Brillance des contours sombres et nets</b> <i>0.0 - 1.0</i> | Force de fusion de la Courbure dans la Brillance. |
| <b>Rugosité Des Bords Nets Et Lumineux</b> <i>0.0 - 1.0</i> | Force de fusion de la Courbure dans la Rugosité. |
| <b>Contours de dessin animé de Rugosité</b> <i>0.0 - 1.0</i> | Force de fusion d’un effet de contour de Rugosité de dessin animé, en fonction de la Courbure. |
| <b>Bords nets Métalliques et clairs</b> <i>0.0 - 1.0</i> | Force de fusion de la Courbure dans le Métallique. |
| <b>Contours Métalliques De Dessin Animé</b> <i>0.0 - 1.0</i> | Force de fusion d’un effet de contour Métallique de dessin animé, en fonction de la Courbure. |
| <b>Intensité du matériel AO</b> <i>0.0 - 1.0</i> | force de fusion de l&#39;AO de map bakée avec l&#39;AO généré par Matériau, degré de regroupement des deux cartes AO. |
| <b>Intensité du Matériau Height</b> <i>0.0 - 1.0</i> | Fusion force de l&#39;Height de la map bakée avec l&#39;Height généré par le Matériau, degré auquel combiner les deux cartes de hauteur. |
| <b>Type de fusion de Matériau Height</b> <i>Renforcer, Interpolation</i> | Mode fusion pour combiner les deux cartes de hauteur. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="material-mesh-data-blender.resources/blenddata-ex.gif" />
        </td>
    </tr>
</table>
