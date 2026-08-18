---
title: Faire pivoter
description: Designer > Graphiques de composition de Substances > Référence des nœuds pour les graphiques de composition de Substances > Bibliothèque de nœuds > Fonction SDF > Transformation > Rotation
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 1%

---


# Faire pivoter

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icône Rotation](./3d-sdf-transform-rotate.png "Rotation")

<b>Entrée :</b> Fonction SDF > Transformation

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Faire pivoter une forme SDF autour d’un ou de plusieurs axes à partir d’un point de pivot réglable, tour à tour.<br>Utilisez l&#39;assistant <b>Transformation du pivot</b> de la <b>Visionneuse 3D</b> pour visualiser la rotation effectuée.

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
| <b>Angle</b> *Flotter* | Angle, en tours, auquel la forme SDF est tournée.<br><br>L&#39;angle est visualisé par un cercle dans l&#39;assistant <b>Transformer le pivot</b> de la <b>Visionneuse 3D</b>. Alignez l&#39;appareil photo de manière à voir la flèche <b>Axe</b> au centre de ce cercle pour voir clairement l&#39;angle de votre rotation comme une fraction de tour.<br><br><i>Par défaut : 0</i> |
| <b>Axe</b> *Float3* | Vecteur normalisé définissant l&#39;axe autour duquel la forme SDF est tournée.<br>Par ex. (0, 1, 0) fera pivoter la forme SDF autour de l’axe Y de son point pivot local.<br><br>L&#39;axe est visualisé par une flèche dans l&#39;assistant <b>Transformer le pivot</b> de la <b>Visionneuse 3D</b>. La couleur de la flèche est mappée sur les composants XYZ de ce vecteur.<br><br><i>Valeur par défaut : (0, 1, 0)</i> |
| <b>Position de pivot</b> *Float3* | Position dans l&#39;espace universel du pivot local de la forme SDF, où (0, 0, 0) place le pivot au centre de la forme SDF. Définit l’origine de la rotation.<br><br>Le pivot est visualisé par le début de la flèche dans l&#39;assistant <b>Transformer le pivot</b> de la <b>Visionneuse 3D</b>. |
| <b>P</b> *Float3* | La position spatiale mondiale transformée. Utilisez cette entrée pour appliquer des transformations supplémentaires à l&#39;aide des nœuds <b>Décalage P</b> et <b>Rotation P</b>.<br><br><i>Par défaut : position de l&#39;espace univers non transformée.</i> |
