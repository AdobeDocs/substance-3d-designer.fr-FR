---
title: Surface d'intersection
description: Designer > graphes de composition de Substance > Référence des nœuds pour les graphes de composition de Substance > Bibliothèque de nœuds > Fonction SDF > Opérateur > Surface d’intersection
source-git-commit: 3f5ca55e459e04f5b81755565c6f674dbc3c845c
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 1%
---

# Surface d&#39;intersection

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icône de surface d&#39;intersection](./3d-sdf-op-intersection-surface.png "Surface d&#39;intersection")

<b>Entrée :</b> Fonction SDF > Opérateur

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Renvoie la surface de la partie d’une forme SDF de base qui est entrecoupée par une autre forme SDF, avec un thickness réglable.

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
| <b>SDF de base</b> *Flottant* | Forme SDF sur laquelle est basée la surface obtenue. |
| <b>SDF d&#39;intersection</b> *Flottant* | La forme SDF croise la forme SDF de base. |
| <b>Thickness</b> *Flottant* | Thickness de la surface résultante.<br><br><i>Valeur par défaut : 0.02</i> |
