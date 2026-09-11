---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/uber-emboss.html"
breadcrumb-title: ''
description: Utilisez le nœud Uber Embossage pour créer des effets d’embossage avancés avec des commandes personnalisables de profondeur, d’angle et d’éclairage.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Uber Emboss
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Uber Embossage
user-guide-description: ''
user-guide-title: ''
source-git-commit: 67f8f59bf50387b87e9009b042f269208c665c65
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 9%

---


# Uber Embossage

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](uber-emboss.resources/uber-emboss.png){width="128px"}

<b>Entrée :</b> Filtres > Effets

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Version avancée et riche en fonctionnalités de [Embossage](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/emboss/emboss.md). Applique un effet d’éclairage 2D sophistiqué basé sur une courbe de hauteur.

Utile lors de la création d’un éclairage baké pour certains styles de texture pour lesquels beaucoup de contrôle est nécessaire.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Couleur</b> <i>Entrée couleur</i> | Image de base à modifier. |
| <b>Height</b> <i>Entrée en niveaux de gris</i> | Image de la hauteur utilisée comme pilote pour l’effet. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Couleur ambiante</b> <i>(valeur de couleur)</i> | Couleur utilisée dans les zones ombrées. |
| <b>Couleur Diffuse</b> <i>(valeur de couleur)</i> | Couleur utilisée dans les zones éclairées. |
| <b>Couleur Specular</b> <i>(valeur de couleur)</i> | Couleur utilisée pour les reflets specular |
| <b>Intensité de la lumière</b> <i>0.0 - 1.0</i> | Intensité de la lumière (simulée). |
| <b>Angle de la lumière</b> <i>0.0 - 1.0</i> | Angle d’incidence de la lumière (simulée) |
| <b>Intensité du Specular</b> <i>0.0 - 1.0</i> | Intensité des reflets du specular. |
| <b>Brillance Specular</b> <i>0.0 - 1.0</i> | Taille du ton clair du specular. |
| <b>Rugosité</b> <i>0.0 - 1.0</i> | Rugosité utilisée pour calculer l’éclairage diffus. |
| <b>Opacité des ombres</b> <i>0.0 - 1.0</i> | Opacité de fusion des zones ombrées. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="uber-emboss.resources/uberemboss-ex.png" />
        </td>
    </tr>
</table>
