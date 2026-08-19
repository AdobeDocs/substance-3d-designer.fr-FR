---
title: Définir le matériau
description: Définissez la couleur de base, la rugosité et le caractère métallique du matériau d’une scène SDF.
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 5%

---


# Définir le matériau

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icône Définir la matière](set-material.png "Définir la matière")

<b>Entrée :</b> Fonction 3D > Matière

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Définissez la couleur de base, la rugosité et le caractère métallique du matériau d’une scène SDF.

Ces valeurs peuvent ensuite être récupérées pour toutes les formes SDF éclaboussées dans les sorties de l&#39;[éclaboussure de forme v2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.md).

</td>
</tr>
</table>

>[!INFO]
> 
> Pour en savoir plus sur les concepts et les workflows impliquant des Fonctions SDF, consultez la page dédiée : [Utilisation des Fonctions SDF](../../working-with-sdf-functions.md)

## Entrées

|                            |                                  |
|----------------------------|----------------------------------|
| <b>Scène SDF</b> *Flotter* | Scène SDF d’entrée. |
| <b>Couleur de base</b> *Float3* | Valeur de couleur de base du RGB à définir. |
| <b>Métallique</b> *Flotter* | Valeur de métal à définir. |
| <b>Rugosité</b> *Flotter* | Valeur de rugosité à définir. |
