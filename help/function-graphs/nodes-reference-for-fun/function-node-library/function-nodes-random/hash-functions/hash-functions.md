---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/function-node-library/function-nodes-random/hash-functions.html"
breadcrumb-title: ''
description: Utilisez les fonctions de hachage dans les graphes de fonction pour générer des valeurs aléatoires déterministes en fonction des coordonnées d'entrée.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Function node library > Random > Hash
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Fonctions de hachage
user-guide-description: ''
user-guide-title: ''
source-git-commit: 81c39001686736d41614fd59247d53e6d8438def
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 1%

---


# Fonctions de hachage

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nœud de hachage : icon](hash-functions.resources/hash-icon.png "Nœud de hachage : icon"){width="200px"}

<b>Fonctions In:</b> > Aléatoire

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Calcule une valeur pseudo-aléatoire comprise entre 0 et 1, en fonction d&#39;une valeur d&#39;entrée utilisée comme valeur de départ.

Le numéro dans le titre indique le type de valeur entrée et sortie. Par exemple : Hash 23 prend une valeur float2 en entrée et sort une valeur float3.

</td>
</tr>
</table>

Lorsqu&#39;un nœud de hachage génère une valeur de plusieurs composants, chaque composant a une valeur pseudo-aléatoire différente.

Versions disponibles, avec leur type d’entrée et de sortie :

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<b>Hachage 11:</b> Flottant → Flottant

<b>Hachage 14:</b> Flottant → Flottant 4

<b>Hachage 21:</b> Flottant 2 → Flottant

<b>Hachage 22:</b> Flottant 2 → Flottant 2

</td>
<td style="border: 0;" valign="top">

<b>Hachage 24:</b> Flottant 2 → Flottant 4

<b>Hash31:</b> Flottant 3 → Flottant

<b>Hachage 32:</b> Flottant 3 → Flottant 2

</td>
</tr>
</table>

## Connecteurs d’entrée

|  |  |
| --- | --- |
| <b>Entrée</b> | Valeur utilisée comme valeur de départ pour calculer la sortie pseudo-aléatoire. |

## Exemples

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Exemple de hachage 14](hash-functions.resources/hash14-example.png "Exemple de hachage 14"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Exemple de hachage 32](hash-functions.resources/hash32-example.png "Exemple de hachage 32"){zoomable="yes"}

</td>
</tr>
</table>
