---
title: Union lisse
description: Designer > Graphes de composition de Substances > Référence des nœuds pour les graphes de composition de Substances > Bibliothèque de nœuds > Fonction SDF > Opérateur > Lissage de l’union
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 1%

---


# Union lisse

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icône Union lisse](./3d-sdf-op-union-smooth.png "Union lisse")

<b>Entrée :</b> Fonction SDF > Opérateur

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Renvoie les volumes ajoutés de deux formes SDF, avec un lissage réglable des bords de leur intersection.

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
| <b>SDF 1</b> *Flotter* | Première forme SDF. |
| <b>SDF 2</b> *Flotter* | Deuxième forme SDF. |
| <b>Smoothness</b> *Flotter* | Rayon de lissage, à partir des bords de l&#39;intersection.<br><br><i>Valeur par défaut : 0</i><br><br><i>Remarque :</i> les bords durs peuvent apparaître à l&#39;intersection des rayons de lissage. |
