---
title: Torsion (inexacte)
description: Designer > Graphiques de composition de Substances > Référence des nœuds pour les graphiques de composition de Substances > Bibliothèque de nœuds > Fonction SDF > Transformation > Torsion (inexact)
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 1%

---


# Torsion (inexacte)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

Icône ![Torsion (inexacte)](./3d-sdf-transform-twist.png "Torsion (inexacte)")

<b>Entrée :</b> Fonction SDF > Transformation

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Tournez une forme SDF autour de son axe Z local entre un point de départ et un point d’arrivée, à un angle réglable.<br><br><i>Remarque :</i>comme cette fonction de transformation est inexacte, des artefacts peuvent apparaître lors du rendu.

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
| <b>SDF</b> *Flotter* | Forme SDF d’entrée. |
| <b>Angle</b> *Flotter* | Angle, en tours, de la rotation appliquée à la fin de la torsion. |
| <b>Démarrer</b> *Flotter* | Position universelle sur l’axe Z où commence la torsion. Tout le volume en dessous n’est pas tordu. |
| <b>Fin</b> *Flotter* | Position universelle sur l’axe Z à l’endroit où la torsion se termine. Tout le volume ci-dessus pivote uniformément selon l’angle spécifié. |
| <b>P</b> *Float3* | La position spatiale mondiale transformée. Utilisez cette entrée pour appliquer des transformations supplémentaires à l&#39;aide des nœuds <b>Décalage P</b> et <b>Rotation P</b>.<br><br><i>Par défaut : position de l&#39;espace univers non transformée.</i> |
