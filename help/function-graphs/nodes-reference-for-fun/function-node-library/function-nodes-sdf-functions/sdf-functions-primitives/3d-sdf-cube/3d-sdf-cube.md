---
title: Cube
description: Designer > graphes de composition de Substance > Référence des nœuds pour les graphes de composition de Substance > Bibliothèque de nœuds > Fonction SDF > Primitive > Cube
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 2%

---


# Cube

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icône de cube](./3d-sdf-cube.png "Cube")

<b>Entrée :</b> Fonction SDF > Primitive

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Fonction SDF pour un cube, avec taille XYZ réglable et arrondi des bords.

</td>
</tr>
</table>

<a name='inputs'></a>

>[!INFO]
> 
> Pour en savoir plus sur les concepts et les workflows impliquant des Fonctions SDF, consultez la page dédiée : [Utilisation des Fonctions SDF](../../working-with-sdf-functions.md)

## Entrées

|  |  |
| :--- | :--- |
| <b>Taille</b> *Flottant3* | Taille du cube sur X, Y et Z.<br><br><i>Valeur par défaut : (1, 1, 1)</i> |
| <b>Arrondi</b> *Flottant* | Rayon des arcs arrondis appliqués aux bords du cube.<br><br><i>Remarque :</i> les arêtes dures peuvent apparaître à l&#39;intersection des rayons d&#39;arrondi.<br><br><i>Valeur par défaut : 0</i> |
| <b>Position de pivot (locale)</b> *Flottant3* | Position espace monde du pivot local du cube, où (0, 0, 0) place le pivot au centre du cube.<br><br><i>Par défaut : (0, 0, -0.5)</i> |
| <b>Position centrale</b> *Flottant3* | Position espace monde du pivot du cube.<br><br><i>Par défaut : (0, 0, 0)</i> |
| <b>P</b> *Flottant3* | Position espace monde transformée. Utilisez cette entrée pour appliquer des transformations supplémentaires à l&#39;aide des nœuds <b>Décalage P</b> et <b>Rotation P</b>.<br><br><i>Par défaut : position de l&#39;espace monde non transformé.</i> |
