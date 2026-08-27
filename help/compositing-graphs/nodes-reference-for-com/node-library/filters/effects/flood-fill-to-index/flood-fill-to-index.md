---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill-to-index.html"
breadcrumb-title: ''
description: Utilisez le nœud Flood Fill à Index pour remplir des régions avec des valeurs d’index afin de créer des motifs numérotés et étiquetés.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill to Index
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Flood Fill à l’index
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 2%

---


# Flood Fill à l’index

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/floodfill-index.png){width="200px"}

## Flood Fill à l’index

**Entrée :** *Filtres/Effets*

**Complexe**

</td>
<td style="border: 0;" valign="top">

## Description

Flood Fill à l’index convertit chaque cellule Flood Fill en une valeur correspondant à son numéro d’index, en commençant par 0 dans le coin supérieur gauche. Il peut être utilisé pour renvoyer des teintes en niveaux de gris sous une forme normalisée (0,0 à 1,0, divisé par autant de cellules que celles trouvées par Flood Fill) ou sous la forme d’une valeur HDR non répartie (0 à n où n est le nombre de cellules).

En outre, le Flood Fill à Index utilise des [valeurs](../../../../../values-compositing-graphs/values-in-substance-compositing-graphs.md), renvoyant la quantité de formes trouvées et la table de données interne facultative.

### Entrées

* **Boîte de Flood Fill** : *mappage d&#39;entrée de couleur* Flood Fill standard. Obligatoire.
* **Informations sur la forme spéciale** : *entrée de couleur* mappage Flood Fill supplémentaire, doit être explicitement activé sur le nœud Flood Fill précédent et doit être connecté !

### Paramètres

* **Sortie** : *normalisée, entier* Déterminez si la sortie est dans la plage LDR 0-1 ou HDR 0-n.
* **Ignorer les formes inférieures à** : *0.0 - 1.0* valeur de tolérance pour l&#39;ignorance des petites formes.
* **Afficher la table de données du Flood Fill** : *Faux/Vrai* renvoie des données supplémentaires (débogage) pour une utilisation avancée.

## Exemples

![](../../../../../../assets/flood-fill-ex02.jpg)

</td>
</tr>
</table>
