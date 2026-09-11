---
title: Ellipsoïde
description: Designer > graphes de composition de Substance > Référence des nœuds pour les graphes de composition de Substance > Bibliothèque de nœuds > Fonction SDF > Primitive > Ellipsoïde
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 1%

---


# Ellipsoïde

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icône d&#39;ellipsoïde](./3d-sdf-ellipsoid.png "Ellipsoïde")

<b>Entrée :</b> Fonction SDF > Primitive

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Fonction SDF d’un ellipsoïde, qui est une forme arrondie de rayon tridimensionnel réglable.

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
| <b>Rayon</b> *Flottant3* | Rayon de l&#39;ellipsoïde en X, Y et Z.<br><br><i>Valeur par défaut : (0,35, 0,35, 0,5)</i> |
| <b>Position centrale</b> *Flottant3* | Position espace monde du pivot de l&#39;ellipsoïde.<br><br><i>Par défaut : (0, 0, 0)</i> |
| <b>P</b> *Flottant3* | Position espace monde transformée. Utilisez cette entrée pour appliquer des transformations supplémentaires à l&#39;aide des nœuds <b>Décalage P</b> et <b>Rotation P</b>.<br><br><i>Par défaut : position de l&#39;espace monde non transformé.</i> |
