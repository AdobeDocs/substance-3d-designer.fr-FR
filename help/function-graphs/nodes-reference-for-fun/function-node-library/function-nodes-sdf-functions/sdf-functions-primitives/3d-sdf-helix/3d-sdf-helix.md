---
title: Hélice (environ)
description: Designer > Graphes de composition de Substances > Référence des nœuds pour les graphes de composition de Substances > Bibliothèque de nœuds > Fonction SDF > Primitive > Hélice (approx.)
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---


# Hélice (environ)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Hélice (environ) icon](./3d-sdf-helix.png "Helix (approx.)")

<b>Entrée :</b> Fonction SDF > Primitive

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Fonction SDF d’approximation d’une hélice, qui est une forme obtenue en balayant un cercle le long d’un enroulement incurvé vers le haut autour d’un axe.<br><br><i>Remarque :</i>Cette Fonction SDF étant une approximation, des artefacts peuvent apparaître lors de son rendu.

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
| <b>Rayon majeur</b> *Flotter* | Distance de la courbe d&#39;enroulement par rapport à l&#39;axe.<br><br><i>Valeur par défaut : 0.4</i> |
| <b>Rayon mineur</b> *Flotter* | Rayon du cercle balayé le long de la courbe pour former la surface de l&#39;hélice.<br><br><i>Valeur par défaut : 0.1</i> |
| <b>Height</b> *Flotter* | Height Z-up de l&#39;hélice.<br><br><i>Par défaut : 0.5</i> |
| <b>Enroulements</b> *Flotter* | Nombre de fois où la courbe s&#39;enroule complètement autour de l&#39;axe par incréments de 0,5.<br>C&#39;est-à-dire, combien de fois l&#39;hélice va tourner dans un height de 0,5.<br><br><i>Par défaut : 4</i> |
| <b>Position centrale</b> *Float3* | Position de l&#39;espace universel du pivot de l&#39;hélice.<br><br><i>Par défaut : (0, 0, 0)</i> |
| <b>P</b> *Float3* | La position spatiale mondiale transformée. Utilisez cette entrée pour appliquer des transformations supplémentaires à l&#39;aide des nœuds <b>Décalage P</b> et <b>Rotation P</b>.<br><br><i>Par défaut : position de l&#39;espace univers non transformée.</i> |
