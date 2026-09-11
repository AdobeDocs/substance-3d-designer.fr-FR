---
title: 'Soustraction lisse '
description: 'Designer > graphes de composition de Substance > Référence des nœuds pour les graphes de composition de Substance > Bibliothèque de nœuds > Fonction SDF > Opérateur > Lissage de la soustraction '
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 1%

---


# Soustraction lisse

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

Icône ![Lissage de la soustraction](./3d-sdf-op-subtraction-smooth.png "Lissage de la soustraction ")

<b>Entrée :</b> Fonction SDF > Opérateur

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Soustrait le volume de la forme SDF1 de la forme SDF2, avec un lissage réglable appliqué à l’intersection des deux.

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
| <b>SDF 1</b> *Flottant* | Forme SDF soustraite de. |
| <b>SDF 2</b> *Flottant* | La forme SDF est soustraite de la forme SDF 1. |
| <b>Smoothness</b> *Flottant* | Lissage appliqué à l&#39;intersection des deux formes.<br><br><i>Remarque :</i> des bords durs peuvent apparaître à l&#39;intersection des rayons de lissage. |
