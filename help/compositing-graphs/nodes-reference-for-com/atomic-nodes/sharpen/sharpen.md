---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/sharpen.html"
breadcrumb-title: ''
description: Utilisez le nœud Netteté pour améliorer les détails de texture et les bords afin de créer des détails de surface nets et définis.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Sharpen
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Accentuer
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 4%

---


# Accentuer

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icône de nœud plus net](../../../../assets/sharpen-4.png "Icône de nœud plus net")

<b>Entrée :</b> nœuds atomiques

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Le nœud Netteté effectue une opération de netteté sur une entrée. Il s’agit d’un point de repère utile pour appliquer la touche finale de netteté à une image.

</td>
</tr>
</table>

Il est mathématiquement très similaire au filtre Accentuation de Photoshop, bien que son nom soit différent. Elle fonctionne bien pour les cartes couleur de base, par exemple, mais doit être évitée sur les cartes telles que les cartes de normales et les cartes métalliques.

## Entrées

<b>Entrée</b> *Couleur/Niveaux De Gris* (Principal)\
Image à accentuer.

## Paramètres

<b>Intensité</b> *Flotter*\
Définit l’intensité de l’effet de renforcement.

<b>Alpha ponctuel</b> *Booléen* (disponible lorsqu&#39;une image couleur est connectée à l&#39;<b>entrée</b>)\
Détermine si la couche alpha de l’image doit être accentuée ou non.

## Exemples

![Nœud plus net - Exemple 1](../../../../assets/sharpen-ex.png "Nœud plus net - Exemple 1")
