---
title: Lissage de l’intersection
description: Designer > graphes de composition de Substances > Référence des nœuds pour les graphes de composition de Substances > Bibliothèque de nœuds > Fonction SDF > Opérateur > Lissage d’intersection
source-git-commit: 3f5ca55e459e04f5b81755565c6f674dbc3c845c
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 1%
---

# Lissage de l’intersection

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icône d&#39;intersection lisse](./3d-sdf-op-intersection-smooth.png "Intersection lisse")

<b>Entrée :</b> Fonction SDF > Opérateur

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Renvoie le volume commun à deux formes SDF, c’est-à-dire le volume créé à l’endroit où deux formes se chevauchent, avec un lissage réglable des bords de leur intersection.

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
| <b>SDF 1</b> *Flottant* | Première forme SDF. |
| <b>SDF 2</b> *Flottant* | Deuxième forme SDF. |
| <b>Smoothness</b> *Flottant* | Smoothness des arêtes à l&#39;intersection des deux formes SDF.<br><br><i>Remarque :</i> des arêtes dures peuvent apparaître à l&#39;intersection des rayons de lissage.<br><br><i>Par défaut : 0</i> |
