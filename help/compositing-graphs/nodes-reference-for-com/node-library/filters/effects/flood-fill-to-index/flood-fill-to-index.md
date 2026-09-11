---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill-to-index.html"
breadcrumb-title: ''
description: Utilisez le nœud Flood Fill à Index pour remplir des régions avec des valeurs d’index afin de créer des motifs numérotés et étiquetés.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill to Index
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Flood Fill à l’index
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2ea5b90ca7a4cbcd0b0049b156e8ded334aa0ceb
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 3%

---


# Flood Fill à l’index

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](flood-fill-to-index.resources/floodfill-index.png){width="200px"}

<b>Entrée :</b> Filtres > Effets

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Flood Fill à l’index convertit chaque cellule Flood Fill en une valeur correspondant à son numéro d’index, en commençant par 0 dans le coin supérieur gauche. Il peut être utilisé pour renvoyer des teintes en niveaux de gris sous une forme normalisée (0,0 à 1,0, divisé par autant de cellules que le Flood Fill en trouve) ou sous la forme d’une valeur HDR non répartie (0 à n où n est le nombre de cellules).

En outre, le Flood Fill à Index utilise des [valeurs](../../../../../values-compositing-graphs/values-in-substance-compositing-graphs.md), renvoyant la quantité de formes trouvées et la table de données interne facultative.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Boîte de Flood Fill</b> <i>Entrée couleur</i> | Map d&#39;entrée de Flood Fill standard. Obligatoire. |
| <b>Informations sur la forme spéciale</b> <i>Entrée couleur</i> | Mappage de Flood Fill supplémentaire, doit être explicitement activé sur le nœud de Flood Fill précédent et doit être connecté !. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Sortie</b> <i>Normalisé, Entier</i> | Déterminez si la sortie est dans la plage LDR 0-1 ou HDR 0-n. |
| <b>Ignorer la forme inférieure à</b> <i>0.0 - 1.0</i> | Valeur de tolérance pour ignorer les petites formes. |
| <b>Afficher la table de données du Flood Fill</b> <i>Faux/Vrai</i> | Renvoie des données supplémentaires (débogage) pour une utilisation avancée. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="flood-fill-to-index.resources/flood-fill-ex02.jpg" />
        </td>
    </tr>
</table>
