---
title: Cône coiffé
description: Designer > Graphes de composition de Substances > Référence des nœuds pour les graphes de composition de Substances > Bibliothèque de nœuds > Fonction SDF > Primitive > Cône écrêté
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 1%

---


# Cône coiffé

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icône coiffé](./3d-sdf-capped-cone.png "Cône coiffé")

<b>Entrée :</b> Fonction SDF > Primitive

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

L&#39;invention concerne une Fonction SDF pour un cône coiffé de rayons de base et de sommet réglables.

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
| <b>Base de rayon</b> *Flotter* | Rayon de la base du cône coiffé.<br><br><i>Valeur par défaut : 0.5</i> |
| <b>Rayon supérieur</b> *Flotter* | Rayon du cône coiffé.<br><br><i>Valeur par défaut : 0.2</i> |
| <b>Height</b> *Flotter* | Height Z-up du cône coiffé à partir de sa base.<br><br><i>Valeur par défaut : 1</i> |
| <b>Position centrale</b> *Float3* | Position de l&#39;espace universel du pivot du cône coiffé.<br><br><i>Par défaut : (0, 0, 0)</i> |
| <b>P</b> *Float3* | La position spatiale mondiale transformée. Utilisez cette entrée pour appliquer des transformations supplémentaires à l&#39;aide des nœuds <b>Décalage P</b> et <b>Rotation P</b>.<br><br><i>Par défaut : position de l&#39;espace univers non transformée.</i> |
