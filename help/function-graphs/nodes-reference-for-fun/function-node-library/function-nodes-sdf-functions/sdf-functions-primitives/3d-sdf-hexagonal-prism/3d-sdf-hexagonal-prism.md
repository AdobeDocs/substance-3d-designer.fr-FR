---
title: Prisme hexagonal
description: Designer > graphes de composition de Substance > Référence des nœuds pour les graphes de composition de Substance > Bibliothèque de nœuds > Fonction SDF > Primitive > Prisme hexagonal
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 1%

---


# Prisme hexagonal

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icône de prisme hexagonal](./3d-sdf-hexagonal-prism.png "Prisme hexagonal")

<b>Entrée :</b> Fonction SDF > Primitive

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Fonction SDF pour prisme à 6 faces d&#39;height, de rayon et d&#39;arrondi réglables.

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
| <b>Height</b> *Flottant* | Height Z vers le haut du prisme hexagonal à partir de sa base.<br><br><i>Valeur par défaut : 1</i> |
| <b>Rayon</b> *Flottant* | Rayon du prisme hexagonal.<br><br><i>Valeur par défaut : 0,5</i> |
| <b>Arrondi</b> *Flottant* | Rayon des arcs arrondis appliqués aux bords du prisme hexagonal.<br><br><i>Remarque :</i> les arêtes dures peuvent apparaître à l&#39;intersection des rayons d&#39;arrondi.<br><br><i>Valeur par défaut : 0</i> |
| <b>Position centrale</b> *Flottant3* | Position espace monde du pivot du prisme hexagonal.<br><br><i>Par défaut : (0, 0, 0)</i> |
| <b>P</b> *Flottant3* | Position espace monde transformée. Utilisez cette entrée pour appliquer des transformations supplémentaires à l&#39;aide des nœuds <b>Décalage P</b> et <b>Rotation P</b>.<br><br><i>Par défaut : position de l&#39;espace monde non transformé.</i> |
