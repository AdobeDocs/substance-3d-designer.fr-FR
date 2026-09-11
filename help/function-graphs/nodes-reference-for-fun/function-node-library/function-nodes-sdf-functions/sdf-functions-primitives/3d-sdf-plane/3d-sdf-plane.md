---
title: Plan
description: Designer > graphes de composition de Substance > Référence des nœuds pour les graphes de composition de Substance > Bibliothèque de nœuds > Fonction SDF > Primitive > Plan
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 2%

---


# Plan

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icône de plan](./3d-sdf-plane.png "Plan")

<b>Entrée :</b> Fonction SDF > Primitive

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Fonction SDF pour un plan d&#39;orientation, de position et de taille réglables.

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
| <b>Normal</b> *Flottant3* | Vecteur de normale de l&#39;espace monde du plan qui contrôle son orientation.<br>Le vecteur est normalisé.<br><br><i>Par défaut : (0, 0, 1)</i> |
| <b>Taille</b> *Flottant 2* | Taille du plan en X et Y.<br><br><i>Par défaut : (1, 1)</i> |
| <b>Thickness</b> *Flottant* | Thickness du plan, appliqué dans toutes les directions.<br>Le plan est arrondi lorsque le thickness est augmenté.<br><br><i>Par défaut : 0</i> |
| <b>Position centrale</b> *Flottant3* | Position espace monde du pivot du plan.<br><br><i>Par défaut : (0, 0, 0)</i> |
| <b>P</b> *Flottant3* | Position espace monde transformée. Utilisez cette entrée pour appliquer des transformations supplémentaires à l&#39;aide des nœuds <b>Décalage P</b> et <b>Rotation P</b>.<br><br><i>Par défaut : position de l&#39;espace monde non transformé.</i> |
