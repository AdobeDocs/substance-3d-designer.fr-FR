---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/physical-sun-sky.html"
breadcrumb-title: ''
description: Utilisez le nœud Physical SunSky pour générer des environnements d'éclairage physiquement précis du soleil et du ciel pour un aperçu de matériau réaliste.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Physical SunSky
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: SunSky physique
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 1%

---


# Soleil/ciel physique

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/panorama-physical-sun-sky.png){width="200px"}

## Soleil/ciel physique

**Entrée :** *Vue/Outils HDRI 3D*

**Intermédiaire**

</td>
<td style="border: 0;" valign="top">

## Description

Implémentation physique du Soleil et du Ciel basée sur le modèle de puits de lumière Hosek-Wikie. Fournit une excellente base pour une HDRI artificielle.

## Paramètres

* **Position du soleil** :\
  plage = [0,1]x[0,1] (angles longitude-latitude)
* **Turbidité** : *1,0 - 10,0*\
  La turbidité varie de 1 à 10
* **Albédo** : *0.0 - 1.0*\
  Albédo compris entre 0 et 1.
* **Couleur du sol** : *(valeur de couleur)*\
  Couleur du plan au sol.
* **Exposition (EV)** : *-1,0 - 4,0*\
  Valeur d&#39;exposition de la sortie résultante.
* **Taille du soleil** : *0.0 - 4.0*\
  Echelle du soleil, toute valeur différente de 1 n&#39;est pas physiquement correcte. La valeur a des effets subtils !
* **Intensité du soleil** : *0,0 - 1,0*\
  Intensité du disque solaire. Le disque Sun est assez petit, l&#39;effet n&#39;est donc pas immédiatement visible.
* **Intensité du ciel** : *0,0 - 1,0* Intensité du ciel. Affecte également le halo de soleil dans le ciel, et non le disque lui-même.

## Exemples d’images

![](../../../../../../assets/sky-ex.gif)

</td>
</tr>
</table>
