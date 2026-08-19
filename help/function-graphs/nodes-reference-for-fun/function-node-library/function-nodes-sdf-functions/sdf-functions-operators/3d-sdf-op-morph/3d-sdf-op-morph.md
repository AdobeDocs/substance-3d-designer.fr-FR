---
title: Morphe
description: Designer > Graphiques de composition de Substances > Référence des nœuds pour les graphiques de composition de Substances > Bibliothèque de nœuds > Fonction SDF > Opérateur > Morphe
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 1%

---


# Morphe

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icône de morphe](./3d-sdf-op-morph.png "Morphe")

<b>Entrée :</b> Fonction SDF > Opérateur

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Renvoie l’interpolation linéaire entre une forme SDF de base et une forme SDF cible en fonction d’un facteur de mélange réglable.

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
| <b>SDF de base</b> *Flotter* | Forme SDF de base. |
| <b>Cible SDF</b> *Flotter* | Forme SDF cible. |
| <b>Facteur de mélange</b> *Flotter* | Facteur de mélange utilisé pour transformer les formes d’entrée, où 0 est la forme de base et 1 la forme cible. |
