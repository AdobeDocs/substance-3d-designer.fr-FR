---
title: Tore
description: Designer > Graphes de composition de Substances > Référence des nœuds pour les graphes de composition de Substances > Bibliothèque de nœuds > Fonction SDF > Primitive > Torus
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 2%

---


# Tore

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icône de tore](./3d-sdf-torus.png "Tore")

<b>Entrée :</b> Fonction SDF > Primitive

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Une Fonction SDF pour un tore, qui est une forme formée par le balayage d&#39;un cercle mineur le long d&#39;un cercle majeur.<i>Les deux cercles ont des rayons réglables.

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
| <b>Rayon majeur</b> *Flotter* | Rayon du cercle le long duquel le disque mineur est balayé pour former la surface du tore.<br><br><i>Valeur par défaut : 0.5</i> |
| <b>Rayon mineur</b> *Flotter* | Rayon du cercle balayé le long du cercle principal pour former la surface du tore.<br><br><i>Valeur par défaut : 0.2</i> |
| <b>Position centrale</b> *Float3* | Position dans l&#39;espace universel du pivot du tore.<br><br><i>Par défaut : (0, 0, 0)</i> |
| <b>P</b> *Float3* | La position spatiale mondiale transformée. Utilisez cette entrée pour appliquer des transformations supplémentaires à l&#39;aide des nœuds <b>Décalage P</b> et <b>Rotation P</b>.<br><br><i>Par défaut : position de l&#39;espace univers non transformée.</i> |
