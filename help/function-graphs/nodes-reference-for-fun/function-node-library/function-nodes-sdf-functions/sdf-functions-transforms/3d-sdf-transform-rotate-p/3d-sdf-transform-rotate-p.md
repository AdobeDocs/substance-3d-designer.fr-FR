---
title: Rotation P
description: Designer > graphes de composition de Substance > Référence des nœuds pour les graphes de composition de Substance > Bibliothèque de nœuds > Fonction SDF > Transforme > Rotation P
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 0%

---


# Rotation P

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

Icône ![Rotation P](./3d-sdf-transform-rotate-p.png "Rotation P")

<b>Entrée :</b> Fonction SDF > Transformer

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Faites pivoter l’espace monde autour d’un axe selon un angle réglable.<br>La position universelle transformée en sortie peut être connectée à l&#39;entrée <b>P</b> de la plupart des Fonctions SDF pour les définir dans cet espace monde transformé.<br><br>Utilisez l&#39;assistant de <b>pivot de Transforme</b> de la <b>visionneuse 3D</b> pour visualiser la rotation effectuée.<br><br><i>Conseil :</i> les transformes P peuvent être enchaînés, mais gardez à l&#39;esprit que les résultats dépendent de l&#39;ordre des opérations.

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
| <b>Angle</b> *Flottant* | Angle, en tours, auquel l’espace monde pivote.<br><br>L&#39;angle est visualisé par un cercle dans l&#39;assistant <b>pivot de Transforme</b> de la <b>visionneuse 3D</b>. Alignez la caméra pour voir la flèche <b>Axe</b> au centre de ce cercle afin de voir clairement l&#39;angle de votre rotation comme une fraction de tour. |
| <b>Axe</b> *Flottant3* | Vecteur normalisé définissant l&#39;axe autour duquel l&#39;espace monde est tourné.<br>Par ex. (0, 1, 0) fait pivoter l&#39;espace monde autour de l&#39;axe Y du point pivot.<br><br>L&#39;axe est visualisé par une flèche dans l&#39;assistant <b>Transformer le pivot</b> de la <b>Visionneuse 3D</b>. La couleur de la flèche est mappée sur les composants XYZ de ce vecteur.<br><br><i>Valeur par défaut : (0, 1, 0)</i> |
| <b>Position de pivot</b> *Flottant3* | Position espace monde du pivot définissant l&#39;origine de la rotation.<br><br>Le point pivot est visualisé par le début de la flèche dans l&#39;assistant <b>Transformer le pivot</b> de la <b>Visionneuse 3D</b>. |
| <b>P</b> *Flottant3* | Position espace monde transformée. Utilisez cette entrée pour appliquer des transformations supplémentaires à l&#39;aide des nœuds <b>Décalage P</b> et <b>Rotation P</b>.<br><br><i>Par défaut : position de l&#39;espace monde non transformé.</i> |
