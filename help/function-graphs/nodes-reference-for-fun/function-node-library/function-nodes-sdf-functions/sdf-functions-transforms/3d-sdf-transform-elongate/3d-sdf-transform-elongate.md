---
title: Allongé
description: Designer > graphes de composition de Substance > Référence des nœuds pour les graphes de composition de Substance > Bibliothèque de nœuds > Fonction SDF > Transforme > Allongé
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 1%

---


# Allongé

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

Icône ![Allongement](./3d-sdf-transform-elongate.png "Allongement")

<b>Entrée :</b> Fonction SDF > Transformer

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Allongez une forme SDF à partir d’une position réglable.<br>Étend de manière linéaire et efficace le volume d&#39;une forme SDF à partir d&#39;une tranche réglable.

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
| <b>SDF</b> *Flottant* | Forme SDF d’entrée. |
| <b>Allongement</b> *Flottant3* | La longueur d&#39;allongement sur les axes X, Y, Z. |
| <b>Position centrale</b> *Flottant3* | Position espace monde à partir de laquelle la forme sera allongée.<br>C&#39;est-à-dire, la position de la tranche étant allongée. |
| <b>P</b> *Flottant3* | Position espace monde transformée. Utilisez cette entrée pour appliquer des transformations supplémentaires à l&#39;aide des nœuds <b>Décalage P</b> et <b>Rotation P</b>.<br><br><i>Par défaut : position de l&#39;espace monde non transformé.</i> |
