---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/reaction-diffusion-fast.html"
breadcrumb-title: ''
description: Utilisez le nœud Réaction Diffusion Rapide pour générer des motifs organiques à l'aide d'algorithmes de réaction-diffusion rapide pour les textures procédurales.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Reaction Diffusion Fast
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Réaction Diffusion Rapide
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 1%

---


# Réaction Diffusion Rapide

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icône du nœud de diffusion de réaction](../../../../../../assets/reaction-diffusion.png "Icône du nœud de diffusion de réaction")

<b>Entrée :</b> Filtres > Effets

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Ce nœud réalise un effet de réaction-diffusion sur une image en niveaux de gris d&#39;entrée.

La réaction-diffusion est un processus par lequel la matière se répand (diffuse) et interagit (réagit) avec d’autres matières. Il s&#39;agit d&#39;un modèle mathématique qui simule ce qui se passe dans la nature lorsque certains motifs se forment sur la peau des animaux par exemple.

Ce nœud est optimisé pour les performances et effectue certains compromis de précision pour la vitesse.

</td>
</tr>
</table>

## Connecteurs d’entrée

<b>Entrée</b> *Niveaux de gris* Image en niveaux de gris à laquelle l&#39;effet Réaction-diffusion doit être appliqué.

## Connecteurs de sortie

<b>Sortie </b>*Niveaux de gris* Image en niveaux de gris représentant l&#39;effet Réaction-diffusion appliqué à l&#39;image d&#39;entrée.

## Paramètres

<b>Rayon</b> *Flottant*&#x200B;Étendue de l’effet.

<b>Contraste</b> *Flotter*\
Règle le contraste de l’entrée et sert de seuil.

## Exemples

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Exemple 1](../../../../../../assets/reactdiff03.png "Exemple 1")

</td>
<td style="border: 0;" valign="top">

![Exemple 2](../../../../../../assets/reactdiff02.png "Exemple 2")

</td>
<td style="border: 0;" valign="top">

![Exemple 3](../../../../../../assets/reactdiff01.gif "Exemple 3")

</td>
</tr>
</table>
