---
title: Cylindre 2 points
description: Designer > Graphiques de composition de Substances > Référence des nœuds pour les graphiques de composition de Substances > Bibliothèque de nœuds > Fonction SDF > Primitive > Cylindre 2 points
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 1%

---


# Cylindre 2 points

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

Icône ![Cylindre 2 points](./3d-sdf-cylinder-2-points.png "Cylindre 2 points")

<b>Entrée :</b> Fonction SDF > Primitive

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Une Fonction SDF pour un barillet de rayon réglable défini par les positions de ses disques de départ et d&#39;arrivée.

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
| <b>Démarrer</b> *Float3* | Position du disque de démarrage du cylindre.<br><br><i>Par défaut : (0, 0, 0)</i> |
| <b>Fin</b> *Float3* | Position du disque d&#39;extrémité du cylindre.<br><br><i>Par défaut : (0, 0, 1)</i> |
| <b>Rayon</b> *Flotter* | Rayon du cylindre.<br><br><i>Par défaut : 0.25</i> |
| <b>P</b> *Float3* | La position spatiale mondiale transformée. Utilisez cette entrée pour appliquer des transformations supplémentaires à l&#39;aide des nœuds <b>Décalage P</b> et <b>Rotation P</b>.<br><br><i>Par défaut : position de l&#39;espace univers non transformée.</i> |
