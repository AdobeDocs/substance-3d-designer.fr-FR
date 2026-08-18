---
title: Rotation P
description: Designer > Graphiques de composition de Substances > Référence des nœuds pour les graphiques de composition de Substances > Bibliothèque de nœuds > Fonction SDF > Transformation > Rotation P
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

<b>Entrée :</b> Fonction SDF > Transformation

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Faites pivoter l&#39;espace universel autour d&#39;un axe selon un angle réglable.<br>La sortie de la position universelle transformée peut être connectée à l&#39;entrée <b>P</b> de la plupart des Fonctions SDF pour les définir dans cet espace universel transformé.<br><br>Utilisez l&#39;assistant <b>Transformation du pivot</b> de la <b>Visionneuse 3D</b> pour visualiser la rotation effectuée.<br><br><i>Conseil :</i> les transformations P peuvent être enchaînées, mais gardez à l&#39;esprit que les résultats dépendent de l&#39;ordre des opérations.

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
| <b>Angle</b> *Flotter* | Angle, tour à tour, selon lequel l’espace univers est incliné.<br><br>L&#39;angle est visualisé par un cercle dans l&#39;assistant <b>Transformer le pivot</b> de la <b>Visionneuse 3D</b>. Alignez l&#39;appareil photo de manière à voir la flèche de l&#39;<b>axe</b> au centre de ce cercle pour voir clairement l&#39;angle de votre rotation en tant que fraction de tour. |
| <b>Axe</b> *Float3* | Vecteur normalisé définissant l&#39;axe autour duquel l&#39;espace universel est tourné.<br>Par ex. (0, 1, 0) fait pivoter l&#39;espace universel autour de l&#39;axe Y du point pivot.<br><br>L&#39;axe est visualisé par une flèche dans l&#39;assistant <b>Transformer le pivot</b> de la <b>Visionneuse 3D</b>. La couleur de la flèche est mappée sur les composants XYZ de ce vecteur.<br><br><i>Valeur par défaut : (0, 1, 0)</i> |
| <b>Position de pivot</b> *Float3* | Position dans l&#39;espace universel du pivot définissant l&#39;origine de la rotation.<br><br>Le point pivot est visualisé par le début de la flèche dans l&#39;assistant <b>Transformer le pivot</b> de la <b>Visionneuse 3D</b>. |
| <b>P</b> *Float3* | La position spatiale mondiale transformée. Utilisez cette entrée pour appliquer des transformations supplémentaires à l&#39;aide des nœuds <b>Décalage P</b> et <b>Rotation P</b>.<br><br><i>Par défaut : position de l&#39;espace univers non transformée.</i> |
