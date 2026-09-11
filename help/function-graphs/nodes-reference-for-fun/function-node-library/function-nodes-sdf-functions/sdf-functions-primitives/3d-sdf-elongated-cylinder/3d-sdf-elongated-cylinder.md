---
title: Cylindre allongé
description: Designer > graphes de composition de Substance > Référence des nœuds pour les graphes de composition de Substance > Bibliothèque de nœuds > Fonction SDF > Primitive > Cylindre allongé
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 1%

---


# Cylindre allongé

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icône de cylindre allongé](./3d-sdf-elongated-cylinder.png "Cylindre allongé")

<b>Entrée :</b> Fonction SDF > Primitive

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

L&#39;invention concerne une Fonction SDF pour cylindre allongé de longueur, de rayon et d&#39;arrondi réglables.<br>Le cylindre allongé résulte du pontage de deux cylindres.

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
| <b>Height</b> *Flottant* | Height Z-up des cylindres de début et d&#39;extrémité par rapport à leur socle.<br><br><i>Valeur par défaut : 0.5</i> |
| <b>Rayon</b> *Flottant* | Rayon des cylindres de début et de fin.<br><br><i>Valeur par défaut : 0.5</i> |
| <b>Arrondi</b> *Flottant* | Rayon des arcs arrondis appliqués aux bords du cylindre allongé.<br><br><i>Remarque :</i> les arêtes dures peuvent apparaître à l&#39;intersection des rayons d&#39;arrondi.<br><br><i>Valeur par défaut : 0</i> |
| <b>Position centrale</b> *Flottant3* | Position espace monde du pivot du cylindre allongé.<br><br><i>Par défaut : (0, 0, 0)</i> |
| <b>Distance d’allongement</b> *Flottant* | Distance le long de laquelle le cylindre de départ est allongé.<br>C&#39;est-à-dire la distance entre les centres des cylindres de départ et d&#39;arrivée.<br><br><i>Par défaut : 0.5</i> |
| <b>P</b> *Flottant3* | Position espace monde transformée. Utilisez cette entrée pour appliquer des transformations supplémentaires à l&#39;aide des nœuds <b>Décalage P</b> et <b>Rotation P</b>.<br><br><i>Par défaut : position de l&#39;espace monde non transformé.</i> |
