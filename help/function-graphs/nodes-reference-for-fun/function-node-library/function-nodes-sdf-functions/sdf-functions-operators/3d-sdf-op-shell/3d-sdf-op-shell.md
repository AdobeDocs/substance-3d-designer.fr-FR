---
title: Coquille
description: Designer > graphes de composition de Substances > Référence des nœuds pour les graphes de composition de Substances > Bibliothèque de nœuds > Fonction SDF > Opérateur > Coque
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 4%

---


# Coquille

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

Icône ![Shell](./3d-sdf-op-shell.png "Shell")

<b>Entrée :</b> Fonction SDF > Opérateur

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Crée une forme SDF creuse, avec un thickness réglable pour l’enveloppe résultante.

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
| <b>Thickness</b> *Flottant* | Le thickness de la coque, appliqué à la fois vers l&#39;intérieur et vers l&#39;extérieur.<br>Le shell est arrondi lorsque le thickness est augmenté.<br><br><i>Par défaut : 0.02</i> |
