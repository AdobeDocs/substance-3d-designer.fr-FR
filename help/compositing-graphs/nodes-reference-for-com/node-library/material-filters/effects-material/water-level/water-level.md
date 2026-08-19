---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/water-level.html"
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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 1%

---


# Niveau de l&#39;eau

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/water-level.png){width="128px"}

## Niveau de l&#39;eau

**Entrée :** *Filtres/Effets De Matière*

**Complexe**

</td>
<td style="border: 0;" valign="top">

## Description

Effet tout-en-un qui ajoute un niveau d’eau à une entrée de matière complète. Pour que l’effet fonctionne, la matière d’entrée doit avoir une image de hauteur correcte et de haute qualité. Le résultat est PBR-correct.

## Paramètres

### Entrées

* **Masque** : *Entrée En Niveaux De Gris*\
  Emplacement de masque utilisé pour masquer les effets du nœud.

### Paramètres

* **Canaux**\
  Activez et désactivez les canaux de matériau dans ce groupe, par exemple lorsque vous utilisez des cartes de Specular/brillance au lieu de cartes de métal/rugosité.
* **Niveau d&#39;eau** :*0,0 - 1,0* Contrôle principal pour augmenter ou diminuer le niveau d&#39;eau.
* **Obscurcissement de l&#39;eau** :*0.0 - 1.0* définit la « transparence » générale de l&#39;eau.
* **Humidité des bords** :*0.0 - 1.0* détermine l&#39;aspect humide que devraient présenter les bords de l&#39;eau.
* **Distance d&#39;humidité des bords** : *0.0 - 1.0* définit la distance d&#39;humidité des bords.
* **Niveau de flou de Profondeur** : *0,0 - 1,0* définit le niveau de flou en fonction de la profondeur sous l&#39;eau. Modifie le rayon de flou.
* **Opacité du flou de Profondeur** : *0.0 - 1.0* Détermine la quantité de flou de profondeur fusionnée, qui peut être utilisée pour réduire l&#39;effet du flou.
* **Couleur de la boue** : *(Valeur de couleur)*Définit la couleur de l’effet de boue.
* **Profondeur de la boue** : *0.0 - 1.0* Définit la profondeur à laquelle la boue commence à apparaître, par rapport au niveau de l&#39;eau.
* **Opacité de la boue** : *0.0 - 1.0* définit l’opacité globale de l’effet de boue.
* **Gel** : *0.0 - 1.0* Définit la quantité de givre. Commence à apparaître à partir des bords extérieurs et se déplace vers l&#39;intérieur.
* **Intensité du givre** : *0.0 - 1.0* Définit l&#39;intensité du givre et contrôle l&#39;« opacité » de l&#39;effet.
* **Fissures de givre** : *0.0 - 1.0* Définit la quantité de fissures dans les transitions du gel au liquide.
* **Format normal du givre** : *DirectX/OpenGL* change le canal vert de l&#39;effet Carte normale du givre.

## Exemples d’images

|  |
| --- |
| Aucune image n&#39;est jointe à cette page. |

</td>
</tr>
</table>
