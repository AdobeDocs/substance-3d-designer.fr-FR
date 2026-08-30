---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/water-level.html"
breadcrumb-title: ''
description: Utilisez le nœud Niveau d'eau pour fusionner des matériaux en fonction de l'height du niveau d'eau afin de créer des effets d'eau réalistes.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Water Level
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Niveau de l'eau
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 8%

---


# Niveau de l&#39;eau

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](water-level.resources/water-level.png){width="128px"}

<b>Entrée :</b> Filtres de matériau > Effets

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Effet tout-en-un qui ajoute un niveau d’eau à une entrée de matériau complète. Pour que l’effet fonctionne, le matériau d’entrée doit disposer d’une carte de hauteur de qualité supérieure. Le résultat est PBR-correct.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Masquer</b> <i>Entrée en niveaux de gris</i> | Emplacement de masque utilisé pour masquer les effets du nœud. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Canaux</b> | Activez et désactivez les canaux de matériau dans ce groupe, par exemple lorsque vous utilisez des cartes de Specular/brillance au lieu de cartes de métal/rugosité. |
| <b>Niveau d&#39;eau</b> <i>0.0 - 1.0</i> | Contrôle principal pour élever ou abaisser le niveau de l&#39;eau. |
| <b>Obscurcissement de l&#39;eau</b> <i>0.0 - 1.0</i> | Définit la « transparence » générale de l’eau. |
| <b>Humidité des bords</b> <i>0.0 - 1.0</i> | Détermine l’aspect humide que doivent présenter les bords de l’eau. |
| <b>Distance d&#39;humidité des bords</b> <i>0.0 - 1.0</i> | Définit l’étendue des contours humides. |
| <b>Niveau de flou de Profondeur</b> <i>0.0 - 1.0</i> | Définit la quantité de flou en fonction de la profondeur sous l’eau. Modifie le rayon de flou. |
| <b>Opacité du flou de Profondeur</b> <i>0.0 - 1.0</i> | Détermine la quantité de flou de profondeur fusionnée, qui peut être utilisée pour réduire l’effet du flou. |
| <b>Couleur de la boue</b> <i>(valeur de couleur)</i> | Définit la couleur de l’effet de boue. |
| <b>Profondeur des boues</b> <i>0.0 - 1.0</i> | Définit la profondeur à laquelle la boue commence à apparaître par rapport au niveau de l’eau. |
| <b>Opacité de la boue</b> <i>0.0 - 1.0</i> | Définit l’opacité globale de l’effet de boue. |
| <b>Gel</b> <i>0.0 - 1.0</i> | Définit la quantité de givre. Commence à apparaître à partir des bords extérieurs et se déplace vers l&#39;intérieur. |
| <b>Intensité du gel</b> <i>0.0 - 1.0</i> | Définit l’intensité du givre et contrôle l’opacité de l’effet. |
| <b>Fissures de givre</b> <i>0.0 - 1.0</i> | Définit le nombre de fissures dans les transitions de l’état congelé à l’état liquide. |
| <b>Format Normal Frost</b> <i>DirectX/OpenGL</i> | Options Effet givre Normal couche verte. |
