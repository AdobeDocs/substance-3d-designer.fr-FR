---
title: Echelle
description: Designer > Graphiques de composition de Substances > Référence des nœuds pour les graphiques de composition de Substances > Bibliothèque de nœuds > Fonction SDF > Transformation > Échelle
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 3%

---


# Échelle

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

Icône ![Échelle](./3d-sdf-transform-scale.png "Échelle")

<b>Entrée :</b> Fonction SDF > Transformation

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Redimensionnement uniforme d’une forme SDF.

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
| <b>Échelle</b> *Flotter* | Facteur d&#39;échelle uniforme.<br><br><i>Par défaut : 1</i> |
| <b>Position de pivot</b> *Float3* | Position dans l&#39;espace universel du pivot local de la forme SDF, où (0, 0, 0) place le pivot au centre de la forme SDF. <br>Définit l&#39;origine de la mise à l&#39;échelle.<br><br><i>Valeur par défaut : (0, 0, 0)</i> |
| <b>P</b> *Float3* | La position spatiale mondiale transformée. Utilisez cette entrée pour appliquer des transformations supplémentaires à l&#39;aide des nœuds <b>Décalage P</b> et <b>Rotation P</b>.<br><br><i>Par défaut : position de l&#39;espace univers non transformée.</i> |
