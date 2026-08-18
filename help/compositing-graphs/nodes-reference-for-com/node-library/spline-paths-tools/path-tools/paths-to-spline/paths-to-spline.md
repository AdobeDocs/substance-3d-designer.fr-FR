---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/paths-to-spline.html"
breadcrumb-title: ''
description: Utilisez le nœud Tracés vers spline pour convertir les données de tracé en splines à utiliser avec des nœuds basés sur spline.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Paths to Spline
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Tracés à spline
user-guide-description: ''
user-guide-title: ''
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 1%

---


# Tracés à spline

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icône de nœud](../../../../../../assets/paths-to-splines-icon.png "Icône de nœud")

<b>Entrée :</b> Outils Spline Et Tracé > Outils De Tracé

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Convertit un tracé en splines qui peuvent être visualisées à l&#39;aide d&#39;un nœud de [rendu spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-render/spline-render.md) et traitées à l&#39;aide de [nœuds splines](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-tools.md).

</td>
</tr>
</table>

>[!NOTE]
>
> Les splines sont des courbes qui ne peuvent donc pas conserver la netteté des tracés. Un lissage des formes est attendu lors de la conversion de tracés en splines.

>[!TIP]
>
> Ce nœud peut être utilisé après le nœud [Masquer les tracés](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) pour former une chaîne qui convertit un masque en splines.

## Connecteurs d’entrée

<b>Tracés</b> *Couleur*\
Liste des chemins d’accès des segments codés. Connectez cette entrée au résultat d&#39;un [masque sur les tracés](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) ou à un autre nœud de traitement de tracé.

## Connecteurs de sortie

<b>Couleurs des splines </b>*Color* Les coordonnées des points des splines d&#39;entrée sont codées dans les couches RVBA d&#39;une image couleur :\
    <b>R</b> - Position X\
    <b>G</b> - Position Y\
    <b>B</b> - Height\
    <b>A</b> - Données compressées :\
        * Signe : la spline est fermée (négative) ou ouverte (positive);\
        * Valeur absolue : Thickness + 1.

<b>Données splines</b> *Couleur*\
Données supplémentaires des splines d&#39;entrée codées dans les canaux RVBA d&#39;une image <b>couleur</b> :\
<b>R</b> - Tangentes X\
<b>G</b> - Tangentes Y\
<b>B</b> - Inutilisé\
<b>A</b> - Inutilisé

<b>Quantité de spline</b> *Nombre entier*\
Nombre de splines d&#39;entrée.

## Paramètres

<b>Précision des splines</b> *Nombre entier*\
Logarithme en base 2 (log2) du nombre de sommets échantillonnés dans chaque tracé de l&#39;entrée Tracés pour construire la spline correspondante.

## Exemples

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/PathsToSpline-Variant1-Before.jpg" alt="PathsToSpline-Variant1-Before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="../../../../../../assets/PathsToSpline-Variant1-After.jpg" alt="PathsToSpline-Variant1-After">
      <br><i>Après</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/PathsToSpline-Variant2-Before.jpg" alt="PathsToSpline-Variant2-Before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="../../../../../../assets/PathsToSpline-Variant2-After.jpg" alt="PathsToSpline-Variant2-After">
      <br><i>Après</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>
