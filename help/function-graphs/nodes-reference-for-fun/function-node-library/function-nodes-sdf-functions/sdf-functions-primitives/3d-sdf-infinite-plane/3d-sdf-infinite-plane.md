---
title: Plan infini
description: Designer > Graphiques de composition de Substances > Référence des nœuds pour les graphiques de composition de Substances > Bibliothèque de nœuds > Fonction SDF > Primitive > Plan infini
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 1%

---


# Plan infini

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icône de plan infini](./3d-sdf-infinite-plane.png "Plan infini")

<b>Entrée :</b> Fonction SDF > Primitive

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Une Fonction SDF pour un plan infini d&#39;orientation et de position réglables.

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
| <b>Normal</b> *Float3* | Vecteur normal de l&#39;espace universel du plan infini, qui contrôle son orientation.<br>Le vecteur est normalisé.<br><br><i>Par défaut : (0, 0, 1)</i> |
| <b>Position centrale</b> *Flotter* | Position dans l&#39;espace universel du pivot du plan, en tant que distance par rapport à l&#39;origine universelle le long de la normale du plan.<br><br><i>Par défaut : 0</i> |
| <b>P</b> *Float3* | La position spatiale mondiale transformée. Utilisez cette entrée pour appliquer des transformations supplémentaires à l&#39;aide des nœuds <b>Décalage P</b> et <b>Rotation P</b>.<br><br><i>Par défaut : position de l&#39;espace univers non transformée.</i> |
