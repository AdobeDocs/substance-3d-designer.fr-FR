---
title: Décalage
description: Designer > graphes de composition de Substance > Référence des nœuds pour les graphes de composition de Substance > Bibliothèque de nœuds > Fonction SDF > Transforme > Décalage
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 3%

---


# Décalage

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

Icône ![Décalage](./3d-sdf-transform-offset.png "Décalage")

<b>Entrée :</b> Fonction SDF > Transformer

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Décaler une forme SDF le long d’un vecteur

</td>
</tr>
</table>

<a name='inputs'></a>

|  |  |
| :--- | :--- |
| <b>SDF</b> *Flottant* | Forme SDF d’entrée. |
| <b>Décalage</b> *Flottant3* | Distance de décalage de la forme SDF dans les directions X, Y et Z.<br><br><i>Valeur par défaut : (0, 0, 0)</i> |
| <b>P</b> *Flottant3* | Position espace monde transformée. Utilisez cette entrée pour appliquer des transformations supplémentaires à l&#39;aide des nœuds <b>Décalage P</b> et <b>Rotation P</b>.<br><br><i>Par défaut : position de l&#39;espace monde non transformé.</i> |
