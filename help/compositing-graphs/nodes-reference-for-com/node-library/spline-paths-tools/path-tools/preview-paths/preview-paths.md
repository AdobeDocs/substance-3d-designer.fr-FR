---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/preview-paths.html"
breadcrumb-title: ''
description: Utilisez le nœud Chemins d’aperçu pour visualiser les données de chemin dans la vue 2D à des fins de débogage et de vérification.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Preview Paths
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Tracés d’aperçu
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 1%

---


# Tracés d’aperçu

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icône de nœud](../../../../../../assets/preview-paths-icon.png "Icône de nœud")

<b>Entrée :</b> Outils Spline Et Tracé > Outils De Tracé

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Tracez des segments et des sommets du tracé au-dessus de l’arrière-plan donné. Une couleur aléatoire par tracé.

Vous obtiendrez un résultat similaire à la sortie <b>Aperçu</b> de l&#39;[option Masquer sur les tracés](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md), mais avec plus d&#39;options.

</td>
</tr>
</table>

## Connecteurs d’entrée

<b>Arrière-plan</b> *Couleur*\
Une image d’arrière-plan au-dessus de avec affiche le tracé. Cela contrôle également la taille du rendu.

<b>Tracés</b> *Couleur*\
Liste des chemins d’accès des segments codés. Connectez cette entrée au résultat d&#39;un [masque sur les tracés](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) ou à un autre nœud de traitement de tracé.

## Paramètres

<b>Afficher les coins</b> *Booléen*\
Affiche un carré sur chaque sommet marqué comme angle (fusion additive).

<b>Afficher les sommets</b> *Booléen*\
Affiche une forme circulaire sur chaque sommet (fusion additive). Les coins sont toujours affichés sous forme de carrés.

<b>Thickness des segments (px)</b> *Flotter*\
Ajuste le thickness des segments rendus en pixels.

## Exemples

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Exemple de nœud 1](../../../../../../assets/PathsToSpline-Variant2-Before_1.jpg "Exemple de nœud 1")

</td>
<td style="border: 0;" valign="top">

![Exemple de nœud 2](../../../../../../assets/PathsToSpline-Variant1-Before_1.jpg "Exemple de nœud 2")

</td>
</tr>
</table>
