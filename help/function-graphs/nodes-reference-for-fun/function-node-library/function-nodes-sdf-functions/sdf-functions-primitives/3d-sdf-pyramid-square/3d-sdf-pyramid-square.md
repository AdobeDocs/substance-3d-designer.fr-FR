---
title: Pyramide carrée
description: Designer > graphes de composition de Substance > Référence des nœuds pour les graphes de composition de Substance > Bibliothèque de nœuds > Fonction SDF > Primitive > Carré de Pyramide
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 1%

---


# Pyramide carrée

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

Icône ![Pyramide carrée](./3d-sdf-pyramid-square.png "Pyramide carrée")

<b>Entrée :</b> Fonction SDF > Primitive

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

L&#39;invention concerne une Fonction SDF pour pyramide à base carrée, à height et position de base réglables.

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
| <b>Height</b> *Flottant* | Height Z-up de l&#39;apex de la pyramide à partir de sa base.<br><br><i>Valeur par défaut : 1</i> |
| <b>Taille de base</b> *Flottant* | Longueur des bords de base de la pyramide.<br>Tous les bords sont de longueur égale.<br><br><i>Par défaut : 1</i> |
| <b>Position de base</b> *Flottant3* | Position espace monde de la base de la pyramide.<br><br><i>Valeur par défaut : (0, 0, 0)</i> |
| <b>P</b> *Flottant3* | Position espace monde transformée. Utilisez cette entrée pour appliquer des transformations supplémentaires à l&#39;aide des nœuds <b>Décalage P</b> et <b>Rotation P</b>.<br><br><i>Par défaut : position de l&#39;espace monde non transformé.</i> |
