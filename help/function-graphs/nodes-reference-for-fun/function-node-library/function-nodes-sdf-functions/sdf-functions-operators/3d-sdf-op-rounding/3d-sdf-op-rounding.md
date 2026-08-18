---
title: Arrondi
description: Designer > Graphiques de composition de Substances > Référence des nœuds pour les graphiques de composition de Substances > Bibliothèque de nœuds > Fonction SDF > Opérateur > Arrondi
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 2%

---


# Arrondi

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icône d&#39;arrondi](./3d-sdf-op-rounding.png "Arrondi")

<b>Entrée :</b> Fonction SDF > Opérateur

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Développe une forme SDF, la gonfle et lisse ses bords nets.

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
| <b>Rayon</b> *Flotter* | Rayon des arcs arrondis appliqués aux bords de la forme.<br><br><i>Remarque :</i> les arêtes dures peuvent apparaître à l&#39;intersection des rayons d&#39;arrondi.<br><br><i>Valeur par défaut : 0.05</i> |
