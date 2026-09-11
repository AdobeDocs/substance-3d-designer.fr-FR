---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape-extrude.html"
breadcrumb-title: ''
description: Utilisez le nœud Extrusion de forme pour extruder des formes et créer des effets de profondeur de type 3D dans les textures Substance 3D Designer.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Shape Extrude
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Extrusion de forme
user-guide-description: ''
user-guide-title: ''
source-git-commit: dbfe5b7ce453a6178d8d970698d3a5f8225151b4
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 5%

---


# Extrusion de forme

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](shape-extrude.resources/shape-extrude.png){width="128px"}

<b>Entrée :</b> Générateurs De Textures > Motifs

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Nœud avancé qui permet le rendu d’entrées de « forme » binaires 2D sur des hauteurs de cartes rotées en 3D. Fonctionne comme une extrusion dans un assemblage 3D, où une forme est extrudée le long de son axe, créant ainsi un volume. En association avec le masque de dégradé de profil, des corps de type Révolution/Tour peuvent également être créés. Très utile pour créer des formes artificielles complexes pour les images de hauteur.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Extrusion De L&#39;Entrée De Forme</b> <i>Entrée en niveaux de gris</i> | Si l’option Forme d’extrusion est définie sur Personnalisée, vous pouvez insérer votre propre masque de forme binaire (de préférence) ici. |
| <b>Dégradé de profil</b> <i>Entrée en niveaux de gris</i> | Si le Type de profil est défini sur Dégradé vertical, peut être utilisé pour définir l&#39;échelle de la forme le long de l&#39;axe, pour les corps de révolution. |
| <b>Masque de profil</b> <i>Entrée en niveaux de gris</i> | Emplacement du masque utilisé pour masquer ou afficher la forme extrudée le long de son axe. Permet de rompre la continuité de la forme le long de son axe. Interprétée uniquement comme binaire : les valeurs PUT en niveaux de gris sont arrondies à 0 ou 1. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Height d&#39;extrusion</b> <i>0.0 - 1.0</i> | Quantité pour extruder la forme par le haut à partir du centre. |
| <b>Extrusion de la Profondeur</b> <i>0.0 - 1.0</i> | Quantité pour extruder la forme par le bas à partir du centre. |
| <b>Extrusion de forme</b> <i>Cube, Cylindre, Entrée personnalisée</i> | Utilisez des formes intégrées ou saisissez votre propre forme personnalisée en externe. |
| <b>Taille de la forme d&#39;extrusion</b> <i>0.0 - 1.0</i> | Utilisé uniquement avec les options Cube et Cylindre intégrées, détermine la taille de la forme de base et peut être mis à l’échelle de manière non uniforme. |
| <b>Échelle</b> <i>0.0 - 1.0</i> | Définissez l’échelle globale de l’effet. Avec les formes intégrées, il s’agit d’une échelle de forme de base uniforme, qui n’affecte ni l’Height ni la Profondeur.<br><br>Avec l’entrée personnalisée, l’ensemble du résultat final est mis à l’échelle de manière uniforme. |
| <b>Type de profil</b> <i>Dégradé vertical droit, Masque</i> | Contrôle principal pour déterminer le comportement de l&#39;effet et l&#39;utilisation de maps d&#39;entrée supplémentaires facultatives.<br><br>L’option Droite correspond au comportement d’extrusion standard. Le dégradé vertical autorise des valeurs d’échelle personnalisées sur l’ensemble de l’axe, le masque permet de masquer des sections sur chaque axe. |
| <b>Height du biseau</b> <i>0.0 - 1.0</i> | Définissez la distance du biseau le long de l’axe d’extrusion. |
| <b>Intensité du biseau</b> <i>0.0 - 1.0</i> | Définissez le degré de retrait du biseau de la forme d’origine. |
| <b>Courbe en biseau</b> <i>-1.0 - 1.0</i> | Définissez la courbe convexe ou concave de l’effet Biseau. Une valeur de 0 signifie qu’il n’y a pas de courbe. |
| <b>Biseau miroir</b> <i>Faux/Vrai</i> | Activez/désactivez cette option pour appliquer le biseau en haut et en bas de la forme. |
| <b>Multiplicateur de réduction d&#39;échelle</b> <i>0 - 2</i> | Commande de réduction d’échelle facile intégrée. Peut être utilisé pour ajouter rapidement un anticrénelage. Veillez à augmenter également la résolution des nœuds. |
| <b>Position</b> | Contrôle principal de la rotation du résultat dans l’espace 3D. Correspond à l&#39;interface Gizmo dans la Vue 2D. |
| <b>Plage de sortie</b> <i>[0, 1], [-1, 1]</i> | Définissez les valeurs minimales et maximales de sortie. Si la plage est définie sur [-1,1], les valeurs négatives sont affichées en noir. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="shape-extrude.resources/shape-extrude-1.png" />
        </td>
    </tr>
</table>
