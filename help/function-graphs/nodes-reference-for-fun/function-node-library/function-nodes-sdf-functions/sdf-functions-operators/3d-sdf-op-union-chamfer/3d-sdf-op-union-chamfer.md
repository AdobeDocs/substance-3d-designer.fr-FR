---
title: Chambre de l'Union
description: Designer > Graphes de composition de Substances > Référence des nœuds pour les graphes de composition de Substances > Bibliothèque de nœuds > Fonction SDF > Opérateur > Chanfrein de l'union
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 1%

---


# Chambre de l&#39;Union

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icône de chanfrein d&#39;union](./3d-sdf-op-union-chamfer.png "Chanfrein d&#39;union")

<b>Entrée :</b> Fonction SDF > Opérateur

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Renvoie les volumes ajoutés de deux formes SDF, avec un volume supplémentaire de rayon réglable le long des arêtes de leur intersection.

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
| <b>Rayon</b> *Flotter* | Rayon du volume ajouté le long des bords de l&#39;intersection des formes.<br><br><i>Valeur par défaut : 0</i> |
