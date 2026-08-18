---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/nadir-patch.html"
breadcrumb-title: ''
description: Utilisez le nœud Nadir patch pour appliquer des correctifs à la zone nadir des panoramas HDRI afin de corriger les artefacts de fond dans les cartes d’environnement.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Nadir Patch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Nadir patch
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 1%

---


# Nadir patch

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/panorama-nadir-patch.png){width="200px"}

## Nadir patch

**Entrée :** *Vue/Outils HDRI 3D*

**Complexe**

</td>
<td style="border: 0;" valign="top">

## Description

Ce nœud fournit une fonctionnalité permettant de corriger le point au sol central (nadir) d&#39;une image mappée de manière sphérique. Il peut être utilisé pour masquer ou « cloner » un vilain nadir, ou un appareil photo ou un trépied visible. Cela fonctionne comme un [patch de duplication](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md), mais avec des réglages pour les images mappées de manière sphérique. L’utilisateur sélectionne un point ailleurs dans l’image, c’est-à-dire le clone et le mélange au nadir. Le traitement ne nécessite aucune autre entrée externe qu’une seule HDRI, mais un masque externe peut être utilisé comme alpha pour l’effet de pièce.

L&#39;effet peut être rapidement vérifié et validé avec [Nadir extract](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/hdri-tools/nadir-extract/nadir-extract.md).

## Entrées

* **Entrée** : *Entrée Couleur*
* **Entrée de masque** :*Entrée en niveaux de gris*\
  Emplacement de masque facultatif utilisé pour masquer le correctif. Fonctionne comme un alpha.

## Paramètres

* **Activer** : *Faux/Vrai*\
  Activez ou désactivez l’effet de correction.
* **Assistant Afficher les images** : *Faux/Vrai*\
  Afficher ou masquer les lignes d&#39;assistant, à des fins de débogage.
* **Thickness d’images** : *0.0 - 1.0*\
  Thickness des lignes auxiliaires.
* **Échelle De Correctif** : *0.0 - 1.0*\
  Échelle globale et uniforme du correctif. Affecte la source et la cible.
* **Taille du correctif** : *0.0 - 1.0*\
  Taille non uniforme du patch.
* **Rotation du correctif** : *0.0 - 1.0*\
  Rotation du patch. Affecte la source et la cible.
* **Alpha De La Pièce** : *Entrée Carré Lisse, Gaussienne, Masque*\
  Définissez le paramètre alpha à utiliser pour fusionner le patch avec l’arrière-plan.
* **Dureté du correctif** : *0.0 - 1.0*\
  Définissez la dureté/le contraste alpha.
* **Décalage de rotation source** : *0,0 - 1,0*\
  Rotation uniquement pour la source du correctif.
* **Coordonnées De Position**
  * **Position source** :\
    Position de la source. Possède un handle en vue 2D.
  * **Position du correctif** :\
    Position de la cible. Possède un handle en vue 2D.

## Exemples d’images

![](../../../../../../assets/nadir-patch-ex.gif)

</td>
</tr>
</table>
