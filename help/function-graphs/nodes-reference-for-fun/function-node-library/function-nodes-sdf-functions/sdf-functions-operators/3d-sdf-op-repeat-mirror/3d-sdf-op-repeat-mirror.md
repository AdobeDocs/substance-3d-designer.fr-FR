---
title: Répétition de la plage de symétrie
description: Designer > graphes de composition de Substance > Référence des nœuds pour les graphes de composition de Substance > Bibliothèque de nœuds > Fonction SDF > Opérateur > Répéter la plage de symétrie
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 0%

---


# Répétition de la plage de symétrie

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

Icône ![Répéter la plage miroir](./3d-sdf-op-repeat-mirror.png "Répéter la plage miroir")

<b>Entrée :</b> Fonction SDF > Opérateur

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Permet de dupliquer une forme SDF et de la dupliquer autant de fois qu’il le faut à l’espacement normal dans les axes positifs ou négatifs X, Y et Z.<br>Chaque fois que cet opérateur répète une forme, il la reflète également. Cela entraîne visuellement une alternance entre l’orientation d’origine de la forme et une copie inversée.

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
| <b>Quantité +</b> *Entier 3* | Nombre de doublons le long des axes positifs X, Y, Z.<br><br><i>Par défaut : (2, 0, 0)</i> |
| <b>Quantité -</b> *Entier 3* | Nombre de doublons le long des axes négatifs X, Y, Z.<br><br><i>Valeur par défaut : (2, 0, 0)</i> |
| <b>Espacement</b> *Flottant3* | Espace monde entre chaque duplicata.<br><br>L&#39;espacement est visualisé par un assistant cubique, dont la taille correspond à l&#39;espace entre les doublons dans les directions X, Y et Z. L&#39;espacement commence à la <b>position d&#39;origine</b> et est augmenté symétriquement à partir de celle-ci.<br><br><i>Par défaut : (2, 2, 2)</i> |
| <b>Position d&#39;origine</b> *Flottant3* | Définit le centre de la forme SDF qui sera dupliquée.<br><br>La position d&#39;origine est visualisée par la position centrale de l&#39;assistant cubique.<br><br><i>Par défaut : (0, 0, 0)</i> |
| <b>P</b> *Flottant3* | Position espace monde transformée. Utilisez cette entrée pour appliquer des transformations supplémentaires à l&#39;aide des nœuds <b>Décalage P</b> et <b>Rotation P</b>.<br><br><i>Par défaut : position de l&#39;espace monde non transformé.</i> |
