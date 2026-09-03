---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/atlas-splitter.html"
breadcrumb-title: ''
description: Utilisez le nœud Atlas splitter pour diviser les atlas de textures en textures individuelles pour le traitement des matériaux numérisés.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Atlas Splitter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Atlas splitter
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '386'
ht-degree: 0%

---


# Atlas splitter

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icône de nœud](atlas-splitter.resources/atlas-splitter-01.png "Icône de nœud")

<b>Entrée :</b> Filtres de matière/Traitement de la numérisation

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Effectue une saisie d&#39;image atlas et divise tous les éléments distincts en *matériaux individuels*.

Il peut également être utilisé pour réorganiser et déplacer tous les éléments dans une grille.

Le nœud fonctionne comme une application avancée du nœud [Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md).

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Mode Grille</b> <i>Booléen</i> | Affiche toutes les formes détectées dans une grille. |
| <b>Opacité de la grille</b> <i>Flotter</i> | Définit l’opacité des lignes de la grille lorsque le mode Grille a la valeur True. Option de débogage |
| <b>Opacité de la sélection de grille</b> <i>Flotter</i> | Définit l’opacité de la mise en surbrillance de la sélection de grille si le mode Grille a la valeur True. Option de débogage |
| <b>Mise à l&#39;échelle automatique</b> <i>Booléen</i> | Redimensionnez automatiquement les formes pour les adapter à la cellule de la grille. |
| <b>Recadrage automatique</b> <i>Booléen</i> | Recadre automatiquement la taille de sortie en fonction de la forme la plus grande afin de réduire l’espace vide. |
| <b>Sélection de forme</b> <i>Nombre entier</i> | En mode Grille, la cellule mise en surbrillance est définie, tandis qu’en dehors du mode Grille, la cellule renvoyée est définie. |
| <b>Ignorer la forme inférieure à</b> <i>Flotter</i> | Ignore les formes dont la diagonale est inférieure à la valeur spécifiée. |
| <b>Rotation automatique</b> <i>Booléen</i> | Fait pivoter automatiquement la forme en fonction de son rapport de taille de cadre de sélection. |
| <b>Rotation</b> <i>Flotter</i> | Angle de rotation de la forme globale |
| <b>Format normal d&#39;entrée</b> <i>Nombre entier</i> | Définissez le format de la normale en entrée. Si vous définissez un format incorrect, le résultat obtenu est incorrect. |
| <b>Réduire le masque d&#39;opacité</b> <i>Nombre entier</i> | Réduit l’échelle du masque d’opacité pour supprimer le bruit potentiel ou le pixel isolé. Il empêche la détection de formes indésirables et augmente également les performances. |
| <b>Largeur De Dilatation</b> <i>Flotter</i> | Applique un effet de dilatation basé sur le masque d’opacité sur toutes les couches, à l’exception de Normal et Height. |
| <b>Activer les entrées supplémentaires</b> <i>Booléen</i> | Met à disposition les entrées et paramètres de l&#39;utilisateur 1 et de l&#39;utilisateur 2 pour tous les mappages supplémentaires non traités. |
| <b>Couleur d&#39;arrière-plan personnalisée</b> <i>Booléen</i> | Permet de choisir une couleur d’arrière-plan personnalisée, au lieu d’une dilatation du contenu de ce calque. |
| <b>Couleur Base color Bg</b> <i>Float3</i> | Couleur BG personnalisée pour la couleur de base. |
| <b>Couleur Bg Normale</b> <i>Float3</i> | Couleur BG personnalisée pour la carte des normales. |
| <b>Couleur Métallique Bg</b> <i>Flotter</i> | Couleur BG personnalisée pour Métallique. |
| <b>Couleur Rugosité Bg</b> <i>Flotter</i> | Couleur BG personnalisée pour la rugosité |
| <b>Couleur Height</b> <i>Flotter</i> | Couleur BG personnalisée pour l’Height |
| <b>Utilisateur 1 Big Color</b> <i>Flotter</i> | Couleur BG personnalisée pour le mappage personnalisé Utilisateur 1 |
| <b>Utilisateur 2 Bg Color</b> <i>Flotter</i> | Couleur BG personnalisée pour le mappage personnalisé Utilisateur 1 |
