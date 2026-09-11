---
title: Torus coiffé
description: Designer > graphes de composition de Substance > Référence des nœuds pour les graphes de composition de Substance > Bibliothèque de nœuds > Fonction SDF > Primitive > Tore coiffé
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 0%

---


# Torus coiffé

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icône de tore coiffé](./3d-sdf-capped-torus.png "Tore coiffé")

<b>Entrée :</b> Fonction SDF > Primitive

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Une Fonction SDF pour un tore coiffé, où le balayage du petit cercle le long d&#39;un grand cercle peut être coiffé à un angle.<br>Les deux cercles ont des rayons réglables.

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
| <b>Rayon majeur</b> *Flottant* | Rayon du cercle principal le long duquel le cercle secondaire est balayé pour former la surface du tore.<br><br><i>Valeur par défaut : 0.5</i> |
| <b>Rayon mineur</b> *Flottant* | Rayon du petit cercle balayé le long du grand cercle pour former la surface du tore.<br><br><i>Valeur par défaut : 0.2</i> |
| <b>Angle</b> *Flottant* | Angle central, à tour de rôle, définissant l&#39;arc de rognage du cercle principal le long duquel le cercle secondaire ne sera pas balayé.<br><br><i>Par défaut : 0.75</i> |
| <b>Décalage de l&#39;angle</b> *Flottant* | Décalage, le long du rayon principal, de l&#39;arc de raccord le long duquel le cercle secondaire ne sera pas balayé.<br><br><i>Valeur par défaut : 0</i> |
| <b>Symétrique</b> *Booléen* | Détermine si l&#39;arc de raccord doit être dessiné dans une ou deux directions.<br><br><i>Valeur par défaut : True</i> |
| <b>Position centrale</b> *Flottant3* | Position espace monde du pivot du tore coiffé.<br><br><i>Valeur par défaut : (0, 0, 0.5)</i> |
| <b>P</b> *Flottant3* | Position espace monde transformée. Utilisez cette entrée pour appliquer des transformations supplémentaires à l&#39;aide des nœuds <b>Décalage P</b> et <b>Rotation P</b>.<br><br><i>Par défaut : position de l&#39;espace monde non transformé.</i> |
