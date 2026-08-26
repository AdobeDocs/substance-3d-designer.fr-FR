---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-append.html"
breadcrumb-title: ''
description: Utilisez le nœud d'ajout de spline pour ajouter plusieurs splines ensemble afin de créer des tracés continus plus longs.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Append
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Ajouter une spline
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '527'
ht-degree: 0%

---


# Ajouter une spline

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icône de nœud](../../../../../../assets/spline-append-icon.png "Icône de nœud")

<b>Entrée :</b> Outils Spline Et Tracé > Outils spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Les splines sont regroupées sous forme de liste. Ce nœud ajoute une liste de splines d&#39;entrée (#2) à une liste existante (#1).

L&#39;ordre des listes est conservé, c&#39;est-à-dire que l&#39;ajout d&#39;une liste D-E-F sur une liste A-B-C donne une liste A-B-C-D-E-F.

</td>
</tr>
</table>

>[!TIP]
>
> Soyez attentif à l&#39;ordre dans lequel vous ajoutez des splines, car cet ordre est pris en compte dans d&#39;autres nœuds, tels que les nœuds [Dispersion sur splines](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/scatter-on-spline-color/scatter-on-spline-color.md), [Spline Bridge](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-bridge-list/spline-bridge-list.md), etc.

## Connecteurs d’entrée

<b>Aperçu #1</b> *Niveaux de gris* Aperçu du premier ensemble de splines d&#39;entrée sous forme d&#39;image en niveaux de gris.

<b>Spline #1 Coords</b> *Couleur* Les coordonnées du premier ensemble de points splines d&#39;entrée sont codées dans les couches RVBA d&#39;une image couleur.\
<b>R</b> - Position X\
<b>G</b> - Position Y\
<b>B</b> - Height\
<b>A</b> - Données compressées :\
* Signe : la spline est fermée (négative) ou ouverte (positive);\
* Valeur absolue : Thickness + 1.

<b>Données de #1 spline</b> *Couleur* Données supplémentaires du premier ensemble de splines d&#39;entrée codées dans les canaux RVBA d&#39;une image couleur.\
<b>R</b> - Tangentes X\
<b>G</b> - Tangentes Y\
<b>B</b> - Inutilisé\
<b>A</b> - Inutilisé

<b>Quantité de #1 spline</b> *Nombre entier* Nombre de splines d&#39;entrée dans le premier jeu.

<b>Aperçu #2</b> *Niveaux de gris* Aperçu du deuxième ensemble de splines d&#39;entrée sous la forme d&#39;une image en niveaux de gris.

<b>Spline #2 Coords</b> *Couleur* Les coordonnées du deuxième ensemble de points splines d&#39;entrée sont codées dans les canaux RVBA d&#39;une image couleur.\
<b>R</b> - Position X\
<b>G</b> - Position Y\
<b>B</b> - Height\
<b>A</b> - Données compressées :\
* Signe : la spline est fermée (négative) ou ouverte (positive);\
* Valeur absolue : Thickness + 1.

<b>Données de #2 spline</b> *Couleur* Données supplémentaires du deuxième ensemble de splines d&#39;entrée codées dans les canaux RVBA d&#39;une image couleur.\
<b>R</b> - Tangentes X\
<b>G</b> - Tangentes Y\
<b>B</b> - Inutilisé\
<b>A</b> - Inutilisé

<b>Quantité de #2 spline</b> *Nombre entier* Nombre de splines d&#39;entrée dans le deuxième jeu.

## Connecteurs de sortie

<b>Aperçu</b> *Niveaux de gris* L’aperçu des splines de sortie sous forme d’image en niveaux de gris.

<b>Couleurs splines</b> *Couleur* Les coordonnées des points splines de sortie sont codées dans les couches RVBA d&#39;une image couleur.\
<b>R</b> - Position X\
<b>G</b> - Position Y\
<b>B</b> - Height\
<b>A</b> - Données compressées :\
* Signe : la spline est fermée (négative) ou ouverte (positive);\
* Valeur absolue : Thickness + 1.

<b>Données splines</b> *Couleur* Données supplémentaires des splines de sortie codées dans les canaux RVBA d&#39;une image couleur.\
<b>R</b> - Tangentes X\
<b>G</b> - Tangentes Y\
<b>B</b> - Inutilisé\
<b>A</b> - Inutilisé

<b>Quantité de spline</b> *Nombre entier* Nombre de splines de sortie.

## Paramètres

<b>Inverser la direction de la #1 de la spline </b>*Booléenne* Inverse la direction des splines du premier ensemble.

<b>Inverser la direction de la #2 de la spline </b>*Booléenne* Inverse la direction des splines du deuxième ensemble.

+++Prévisualiser
<b>Quantité de segments</b> *Nombre entier* Ajuste le nombre de segments utilisés pour dessiner la visualisation de la spline dans la sortie d&#39;aperçu.\
Plus la valeur est élevée, plus la ligne est lisse.

<b>Afficher l&#39;assistant de direction</b> *Booléen* Affiche un point au début de la spline et une flèche à sa fin dans la sortie Aperçu.

<b>Afficher l&#39;enveloppe de Thickness</b> *Booléen*\
Affiche des lignes supplémentaires sur les thickness de la spline.

<b>Thickness (px)</b> *Flottant* Ajuste le thickness de la visualisation de la spline en pixels dans la sortie d&#39;aperçu.

+++

## Exemples

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Exemple de nœud 1](../../../../../../assets/SplineAppend-Demo.jpg "Exemple de nœud 1")

</td>
<td style="border: 0;" valign="top">

![Exemple de nœud 2](../../../../../../assets/SplineAppend-Graph.jpg "Exemple de nœud 2")

</td>
</tr>
</table>

![Démonstration de nœud](../../../../../../assets/SplineAppend-Demo2.gif "Démonstration de nœud")
