---
title: Rock
description: Designer > Graphes de composition de Substances > Référence des nœuds pour les graphes de composition de Substances > Bibliothèque de nœuds > Fonction SDF > Primitive > Roche
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 1%

---


# Rock

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icône de rocher](./3d-sdf-rock.png "Rock")

<b>Entrée :</b> Fonction SDF > Primitive

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Une Fonction SDF pour une forme de roche paramétrique et aléatoire, construite avec des Fonctions SDF.

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
| <b>Max. facettes</b> *Nombre entier* | Nombre maximal de facettes de la roche (jusqu&#39;à 32).<br><br><i>Valeur par défaut : 8</i> |
| <b>Smoothness</b> *Flotter* | Rayon des arcs arrondis appliqués aux bords de la roche.<br><br><i>Valeur par défaut : 0</i> |
| <b>Aléatoire</b> *Flotter* | Fait bouger l&#39;orientation des faces et la distance par rapport au centre.<br>Par conséquent, plus les valeurs sont élevées, plus la roche est petite.<br><br><i>Valeur par défaut : 0</i> |
| <b>Semence</b> *Flotter* | Valeur initiale pour le paramètre <b>Aléatoire</b>.<br><br><i>Valeur par défaut : 0</i> |
| <b>Échelle</b> *Flotter* | Échelle globale de la forme de la roche.<br>Appliqué après <b>Aléatoire</b> et avant <b>Smoothness</b>.<br><br><i>Par défaut : 0.5</i> |
| <b>Position centrale</b> *Float3* | Position dans l&#39;espace universel du pivot de la roche.<br><br><i>Par défaut : (0, 0, 0.5)</i> |
| <b>P</b> *Float3* | La position spatiale mondiale transformée. Utilisez cette entrée pour appliquer des transformations supplémentaires à l&#39;aide des nœuds <b>Décalage P</b> et <b>Rotation P</b>.<br><i>Par défaut : position de l&#39;espace univers non transformée.</i> |
