---
title: Capsule
description: Designer > Graphes de composition de Substances > Référence des nœuds pour les graphes de composition de Substances > Bibliothèque de nœuds > Fonction SDF > Primitive > Capsule
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 2%

---


# Capsule

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icône de capsule](./3d-sdf-capsule.png "Capsule")

<b>Entrée :</b> Fonction SDF > Primitive

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

L&#39;invention concerne une Fonction SDF pour une capsule de longueur et de rayon réglables.<br>La capsule est le résultat du pontage de deux sphères.

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
| <b>Démarrer</b> *Float3* | Position de la sphère de départ.<br><br><i>Valeur par défaut : (0, 0, 0)</i> |
| <b>Fin</b> *Float3* | Position de la sphère d&#39;extrémité.<br><br><i>Valeur par défaut : (0, 0, 1)</i> |
| <b>Rayon</b> *Flotter* | Rayon des sphères de début et de fin.<br><br><i>Valeur par défaut : 0.25</i> |
| <b>Commencer/terminer au bout</b> *Booléen* | Détermine si les positions <b>Début</b> et <b>Fin</b> doivent être situées aux extrémités des sphères.<br>Autrement dit, détermine si l&#39;height de la capsule doit inclure le rayon des sphères.<br><br><i>Valeur par défaut : False</i> |
| <b>Position centrale</b> *Float3* | Position de l&#39;espace universel du pivot de la capsule.<br><br><i>Par défaut : (0, 0, 0)</i> |
| <b>P</b> *Float3* | La position spatiale mondiale transformée. Utilisez cette entrée pour appliquer des transformations supplémentaires à l&#39;aide des nœuds <b>Décalage P</b> et <b>Rotation P</b>.<br><br><i>Par défaut : position de l&#39;espace univers non transformée.</i> |
