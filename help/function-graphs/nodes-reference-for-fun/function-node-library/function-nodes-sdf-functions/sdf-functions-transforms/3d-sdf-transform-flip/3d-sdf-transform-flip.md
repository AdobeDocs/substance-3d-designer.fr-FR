---
title: Inverser
description: Designer > graphes de composition de Substance > Référence des nœuds pour les graphes de composition de Substance > Bibliothèque de nœuds > Fonction SDF > Transforme > Symétrie
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 3%

---


# Inverser

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Symétrie de l&#39;icône](./3d-sdf-transform-flip.png "Symétrie")

<b>Entrée :</b> Fonction SDF > Transformer

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Applique un transforme miroir à la forme SDF d’entrée.<br>Effectue essentiellement une échelle négative sur les axes sélectionnés.

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
| <b>Axe de miroir</b> *Entier 3* | Utilisez un Entier 3 pour définir l&#39;axe de miroir souhaité.<br>Par ex. (1, 0, 0) reflétera l&#39;axe X.<br><br><i>Par défaut : (1, 0, 0)</i> |
| <b>P</b> *Flottant3* | Position espace monde transformée. Utilisez cette entrée pour appliquer des transformations supplémentaires à l&#39;aide des nœuds <b>Décalage P</b> et <b>Rotation P</b>.<br><br><i>Par défaut : position de l&#39;espace monde non transformé.</i> |
