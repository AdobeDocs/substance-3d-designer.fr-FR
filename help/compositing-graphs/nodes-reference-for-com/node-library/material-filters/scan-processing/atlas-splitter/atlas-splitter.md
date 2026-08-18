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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '386'
ht-degree: 0%

---


# Atlas splitter

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icône de nœud](../../../../../../assets/atlas-splitter.png "Icône de nœud")

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

## Paramètres

<b>Mode Grille</b> *Booléen*\
Affiche toutes les formes détectées dans une grille.

<b>Opacité De La Grille</b> *Flottant*\
Définit l’opacité des lignes de la grille lorsque le mode Grille a la valeur True. Option de débogage

<b>Opacité De La Sélection De La Grille</b> *Flottant*\
Définit l’opacité de la mise en surbrillance de la sélection de grille si le mode Grille a la valeur True. Option de débogage

<b>Échelle automatique</b> *Booléenne*\
Redimensionnez automatiquement les formes pour les adapter à la cellule de la grille.

<b>Recadrage automatique</b> *Booléen*\
Recadre automatiquement la taille de sortie en fonction de la forme la plus grande afin de réduire l’espace vide.

<b>Sélection De Forme</b> *Nombre Entier*\
En mode Grille, la cellule mise en surbrillance est définie, tandis qu’en dehors du mode Grille, la cellule renvoyée est définie.

<b>Ignorer la forme inférieure à</b> *Flotter*\
Ignore les formes dont la diagonale est inférieure à la valeur spécifiée.

<b>Rotation automatique</b> *Booléenne*\
Fait pivoter automatiquement la forme en fonction de son rapport de taille de cadre de sélection.

<b>Rotation</b> *Flotter*\
Angle de rotation de la forme globale

<b>Format Normal D&#39;Entrée</b> *Nombre Entier*\
Définissez le format de la normale en entrée. Si vous définissez un format incorrect, le résultat obtenu est incorrect.

<b>Réduire Le Masque D&#39;Opacité</b> *Nombre Entier*\
Réduit l’échelle du masque d’opacité pour supprimer le bruit potentiel ou le pixel isolé. Il empêche la détection de formes indésirables et augmente également les performances.

<b>Largeur de dilatation</b> *Flottant*\
Applique un effet de dilatation basé sur le masque d’opacité sur toutes les couches, à l’exception de Normal et Height.

<b>Activer les entrées supplémentaires</b> *booléennes*\
Met à disposition les entrées et paramètres de l&#39;utilisateur 1 et de l&#39;utilisateur 2 pour tous les mappages supplémentaires non traités.

<b>Couleur d&#39;arrière-plan personnalisée</b> *Booléenne*\
Permet de choisir une couleur d’arrière-plan personnalisée, au lieu d’une dilatation du contenu de ce calque.

<b>Couleur De Base</b> *Float3*\
Couleur BG personnalisée pour la couleur de base.

<b>Couleur Bg Normale</b> *Float3*\
Couleur BG personnalisée pour la carte des normales.

<b>Couleur métallique du sac</b> *Flottant*\
Couleur BG personnalisée pour Métallique.

<b>Couleur De Rugosité</b> *Flottant*\
Couleur BG personnalisée pour la rugosité

<b>Couleur Height</b> *Flottant*\
Couleur BG personnalisée pour l’Height

<b>Utilisateur 1 Big Color</b> *Float*\
Couleur BG personnalisée pour le mappage personnalisé Utilisateur 1

<b>Couleur Bg de l’utilisateur 2</b> *Flottant* Couleur BG personnalisée pour le mappage Utilisateur 1 personnalisé

## Exemples
