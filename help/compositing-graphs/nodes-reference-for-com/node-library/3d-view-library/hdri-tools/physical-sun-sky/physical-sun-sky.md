---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/physical-sun-sky.html"
breadcrumb-title: ''
description: Utilisez le nœud Physical SunSky pour générer des environnements d'éclairage physiquement précis du soleil et du ciel pour un aperçu réaliste du matériau.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Physical SunSky
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: SunSky physique
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9aaf135d4c336ea0cff865524ad1ccd5dcc225bd
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 9%

---


# Soleil/ciel physique

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](physical-sun-sky.resources/panorama-physical-sun-sky.png){width="200px"}

<b>Entrée :</b> vue 3D > Outils HDRI

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Implémentation physique du Soleil et du Ciel basée sur le modèle de puits de lumière Hosek-Wikie. Fournit une excellente base pour une HDRI artificielle.

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Position du soleil</b> | plage = [0,1]x[0,1] (angles longitude-latitude) |
| <b>Turbidité</b> <i>1.0 - 10.0</i> | La turbidité varie de 1 à 10 |
| <b>Albédo</b> <i>0.0 - 1.0</i> | Albédo compris entre 0 et 1. |
| <b>Couleur Sol</b> <i>(valeur de couleur)</i> | Couleur du plan du sol. |
| <b>Exposition (EV)</b> <i>-1.0 - 4.0</i> | Valeur d&#39;exposition de la sortie résultante. |
| <b>Taille du soleil</b> <i>0.0 - 4.0</i> | Echelle du soleil, toute valeur différente de 1 n&#39;est pas physiquement correcte. La valeur a des effets subtils ! |
| <b>Intensité du soleil</b> <i>0.0 - 1.0</i> | Intensité du disque solaire. Le disque Sun est assez petit, l&#39;effet n&#39;est donc pas immédiatement visible. |
| <b>Intensité du ciel</b> <i>0.0 - 1.0</i> | Intensité du ciel. Affecte également le halo de soleil dans le ciel, et non le disque lui-même. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="physical-sun-sky.resources/sky-ex.gif" />
        </td>
    </tr>
</table>
