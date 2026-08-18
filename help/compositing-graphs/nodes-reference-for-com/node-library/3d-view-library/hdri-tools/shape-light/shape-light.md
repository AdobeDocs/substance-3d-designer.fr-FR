---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/shape-light.html"
breadcrumb-title: ''
description: Utilisez le nœud Shape Light pour ajouter des sources lumineuses de forme personnalisée aux environnements HDRI afin d’obtenir des effets d’éclairage créatifs.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Shape Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Shape Light
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---


# Shape Light

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/panorama-shape.png){width="200px"}

## Shape Light

**Entrée :** *Vue/Outils HDRI 3D*

**Complexe**

</td>
<td style="border: 0;" valign="top">

## Description

Génère une forme rectangulaire projetée sphériquement. La transformation de forme est pilotée par un gadget de transformation.

## Entrées

* **Entrée image d&#39;arrière-plan** : *Entrée couleur* Arrière-plan facultatif sur lequel composer la lumière générée.
* **Entrée d’image de forme** : *Entrée de couleur* Image facultative à mapper sur la lumière Sphère. Utilisé uniquement lorsque le mode colorimétrique de la forme est défini sur Entrée image.

## Paramètres

* **Matrice de forme**
  * **Matrice** : *(Matrice De Transformation)*\
    Contrôle de la transformation du résultat. Le résultat peut être modifié en interagissant directement avec la zone de travail.
  * **Décalage** : *-2.0 - 2.0*\
    Déplace ou traduit le résultat. Le résultat peut être modifié en interagissant directement avec la zone de travail.
* **Forme** : *Rectangle, Disque*\
  Choisissez la forme à placer.
* **Mode De Couleur De Forme** : *RGB, Température (Kelvin), Entrée D&#39;Image*\
  Choisissez la méthode à utiliser pour définir la couleur de la forme. Image Input permet d&#39;utiliser le deuxième emplacement d&#39;entrée.
* **Couleur** : *(valeur chromatique)*\
  Uniquement avec le mode colorimétrique de la forme défini sur RGB. Choisit la couleur de la forme.
* **Température de forme** : *800.0 - 20000.0*\
  Uniquement avec le mode Couleur de la forme réglé sur Température. Définit la valeur Kelvin pour la couleur de la forme.
* **Gamma d&#39;entrée d&#39;image de forme** : *sRVB, linéaire*\
  Uniquement avec le mode colorimétrique de la forme défini sur Entrée image. Déterminez comment interpréter l’entrée d’image de forme.
* **Exposition de forme (EV)** : *0.0 - 10.0*\
  Définissez la valeur d’exposition de la forme générée, idéalement adaptée à la valeur d’exposition de l’image d’arrière-plan.
* **Dureté de la forme** : *0.0 - 1.0*\
  Définissez la dureté des bords de la forme.
* **Exposition aux zones réactives (EV)** : *0.0 - 10.0*\
  Définissez l’exposition de la zone réactive centrale. Notez que ce n’est pas très visible en mode RGB.
* **Taille de la zone réactive** : *0.0 - 1.0*\
  Taille de la zone réactive centrale.
* **Suppression de la zone réactive** : *0.0 - 1.0*\
  Atténuation de la zone réactive centrale.
* **Position de la zone réactive** : *0.0 - 1.0*\
  Position X et Y de la zone réactive centrale.
* **Activer L&#39;Entrée En Arrière-Plan** : *Faux/Vrai*\
  Active/désactive l’utilisation d’une image d’arrière-plan facultative. Les composites ont généré de la lumière au-dessus de l’arrière-plan.
* **Couleur d&#39;arrière-plan** : *(valeur de couleur)*\
  Si l’entrée Arrière-plan n’est pas utilisée, définissez ici une valeur d’arrière-plan de couleur unie.
* **Gamma d&#39;arrière-plan** : *sRVB, linéaire* Si l&#39;entrée d&#39;arrière-plan est utilisée, définissez comment interpréter l&#39;entrée d&#39;arrière-plan.

## Exemples d’images

![](../../../../../../assets/shape-light-ex.gif)

</td>
</tr>
</table>
