---
title: Courbure (inexacte)
description: Designer > graphes de composition de Substance > Référence des nœuds pour les graphes de composition de Substance > Bibliothèque de nœuds > Fonction SDF > Transforme > Courbure (inexact)
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 1%

---


# Courbure (inexacte)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

Icône ![Courbure (inexacte)](./3d-sdf-transform-bend.png "Courbure (inexacte)")

<b>Entrée :</b> Fonction SDF > Transformer

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Permet de plier une forme SDF autour de son axe Y local entre un point de départ et un point d&#39;arrivée formant un angle.<br><br><i>Remarque :</i>cette fonction de transformation étant inexacte, des artefacts peuvent apparaître lors de son rendu.

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
| <b>Angle</b> *Flottant* | Angle, en tours, de la rotation appliquée à la fin du pli. |
| <b>Démarrer</b> *Flottant* | Position universelle sur l’axe Z où commence la courbure. Tout le volume en dessous n&#39;est pas plié. |
| <b>Fin</b> *Flottant* | Position universelle sur l’axe Z à l’endroit où se termine le pliage. Tout le volume ci-dessus pivote uniformément selon l’angle spécifié. |
| <b>P</b> *Flottant3* | Position espace monde transformée. Utilisez cette entrée pour appliquer des transformations supplémentaires à l&#39;aide des nœuds <b>Décalage P</b> et <b>Rotation P</b>.<br><br><i>Par défaut : position de l&#39;espace monde non transformé.</i> |
