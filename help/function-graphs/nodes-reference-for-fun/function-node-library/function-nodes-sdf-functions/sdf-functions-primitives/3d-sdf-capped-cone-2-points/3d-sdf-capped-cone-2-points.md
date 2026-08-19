---
title: Cône coiffé de 2 points
description: Designer > Graphes de composition de Substances > Référence des nœuds pour les graphes de composition de Substances > Bibliothèque de nœuds > Fonction SDF > Primitive > Cône fermé de 2 points
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 1%

---


# Cône coiffé de 2 points

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

Icône coiffé de 2 points![Icône coiffé de 2 points](./3d-sdf-capped-cone-2-points.png "2 points")

<b>Entrée :</b> Fonction SDF > Primitive

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Fonction SDF d’un cône coiffé défini par les positions de son embase et de son sommet.<br>La base et le haut ont des rayons réglables.

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
| <b>Base de position</b> *Float3* | Position de la base du cône coiffé.<br><br><i>Valeur par défaut : (0, 0, 0)</i> |
| <b>Positionner en haut</b> *Float3* | Position du sommet du cône coiffé.<br><br><i>Par défaut : (0, 0, 1)</i> |
| <b>Base de rayon</b> *Flotter* | Rayon de la base du cône coiffé.<br><br><i>Valeur par défaut : 0.5</i> |
| <b>Rayon supérieur</b> *Flotter* | Rayon du cône coiffé.<br><br><i>Valeur par défaut : 0.2</i> |
| <b>P</b> *Float3* | La position spatiale mondiale transformée. Utilisez cette entrée pour appliquer des transformations supplémentaires à l&#39;aide des nœuds <b>Décalage P</b> et <b>Rotation P</b>.<br><br><i>Par défaut : position de l&#39;espace univers non transformée.</i> |
