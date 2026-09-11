---
title: Symétrie
description: Designer > graphes de composition de Substance > Référence des nœuds pour les graphes de composition de Substance > Bibliothèque de nœuds > Fonction SDF > Opérateur > Symétrie
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 2%

---


# Symétrie

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

Icône ![Symétrie](./3d-sdf-op-symmetry.png "Symétrie")

<b>Entrée :</b> Fonction SDF > Opérateur

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Retourne et duplique une forme SDF sur un plan de symétrie, puis renvoie l&#39;union de la forme SDF de base et de son ou ses doublons.<br>La Symétrie peut être appliquée simultanément sur n&#39;importe quel axe.

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
| <b>Position du plan de symétrie</b> *Flottant3* | Position espace monde du centre du plan de symétrie.<br>Cette position est partagée par tous les plans de symétrie si la symétrie est appliquée sur plusieurs axes.<br><br><i>Par défaut : (0, 0, 0)</i> |
| <b>Axe de miroir</b> *Entier 3* | Définit les axes de miroir souhaités.<br><br>Par exemple, (1, 0, 0) appliquera la symétrie sur l&#39;axe X.<br><br><i>Par défaut : (1, 0, 0)</i> |
| <b>axe de symétrie</b> *Entier 3* | Définit les axes à retourner.<br><br>Par exemple, (1, 0, 0) inversera le sens de la symétrie sur l&#39;axe X.<br><br><i>Par défaut : (0, 0, 0)</i> |
| <b>Prédécalage</b> *Flottant3* | Décalage sur les axes X, Y, Z appliqués à la forme avant l’application de l’opérateur de symétrie. |
