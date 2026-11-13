---
title: Décalage P
description: Designer > graphes de composition de Substance > Référence des nœuds pour les graphes de composition de Substance > Bibliothèque de nœuds > Fonction SDF > Transforme > Décalage P
source-git-commit: 3f5ca55e459e04f5b81755565c6f674dbc3c845c
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 1%
---

# Décalage P

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

Icône ![Décalage P](./3d-sdf-transform-offset-p.png "Décalage P")

<b>Entrée :</b> Fonction SDF > Transformer

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Décale l’espace monde le long d’un vecteur.<br>La position universelle transformée en sortie peut être connectée à l&#39;entrée <b>P</b> de la plupart des Fonctions SDF pour les définir dans cet espace monde transformé.<br><br><i>Conseil :</i> les transformes P peuvent être enchaînés, mais gardez à l&#39;esprit que les résultats dépendent de l&#39;ordre des opérations.

</td>
</tr>
</table>

<a name='inputs'></a>

>[!INFO]
> 
> Pour en savoir plus sur les concepts et les workflows impliquant des Fonctions SDF, consultez la page dédiée : [Utilisation des Fonctions SDF](../../../../../../learning-tutorials/nodes/working-with-sdf-functions/working-with-sdf-functions.md)

## Entrées

|  |  |
| :--- | :--- |
| <b>Décalage</b> *Flottant3* | Distance de décalage de l’espace monde dans les directions X, Y et Z. |
| <b>P</b> *Flottant3* | Position espace monde transformée. Utilisez cette entrée pour appliquer des transformations supplémentaires à l&#39;aide des nœuds <b>Décalage P</b> et <b>Rotation P</b>.<br><br><i>Par défaut : position de l&#39;espace monde non transformé.</i> |
