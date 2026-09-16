---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/sharpen.html"
breadcrumb-title: ""
description: Utilisez le nœud Netteté pour améliorer les détails et les contours de la texture afin de créer des détails de surface nets et définis.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Sharpen
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Accentuer
user-guide-description: ""
user-guide-title: ""
source-git-commit: 0cb0df528e7f0eb6f3c2d51e35302744952718d5
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 4%
---

# Accentuer

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icône de nœud plus net](sharpen.resources/sharpen-4.png "Icône de nœud plus net")

<b>Entrée :</b> Noeuds atomiques

</td>
<td style="border: 0;" valign="top">

## Description

Le nœud Netteté effectue une opération de netteté sur une entrée. Il s’agit d’un point de repère utile pour appliquer la touche finale de netteté à une image.

</td>
</tr>
</table>

<div data-preserve-html="true" style="text-align: center;"><img src="sharpen.resources/sharpen-tooltip.gif" alt="info-bulle netteté" /></div>

Il est mathématiquement très similaire au filtre Accentuation de Photoshop, bien que son nom soit différent. Cela fonctionne bien pour les cartes de couleur de base, par exemple, mais doit être évité sur les cartes comme les Maps normal et les cartes Métalliques.

## Entrées

<b>Entrée</b> *Couleur/Niveaux De Gris* (Principal)\
Image à accentuer.

## Paramètres

<b>Intensité</b> *Flottant*\
Définit l’intensité de l’effet de renforcement.

<b>Alpha ponctuel</b> *Booléen* (disponible lorsqu&#39;une image couleur est connectée à l&#39;<b>entrée</b>)\
Détermine si le canal Alpha de l’image doit être accentué ou laissé intact.

## Exemples

![Nœud plus net - Exemple 1](sharpen.resources/sharpen-ex.png "Nœud plus net - Exemple 1")
