---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/sphere-light.html"
breadcrumb-title: ''
description: Utilisez le nœud Lumière sphérique pour ajouter des sources de lumière sphériques aux environnements HDRI afin d’améliorer le contrôle de l’éclairage.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Sphere Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Lumière sphérique
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 0%

---


# Lumière sphérique

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/panorama-sphere-light.png){width="200px"}

## Lumière sphérique

**Entrée :** *Vue/Outils HDRI 3D*

**Complexe**

</td>
<td style="border: 0;" valign="top">

## Description

Génère une forme sphérique projetée. La transformation de sphère est pilotée par un gadget de transformation.

La Sphère lumineuse est très polyvalente et dispose d&#39;options qui lui permettent non seulement de générer de simples lumières rondes, mais aussi des planètes ou d&#39;autres corps célestes. Si vous n&#39;avez pas besoin des options d&#39;éclairage et de rotation plus avancées, consultez [Shape Light](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/hdri-tools/shape-light/shape-light.md) à la place.

## Entrées

* **Entrée image d&#39;arrière-plan** : *Entrée couleur* Arrière-plan facultatif sur lequel composer la lumière générée.
* **Entrée d’image de forme** : *Entrée de couleur* Image facultative à mapper sur la lumière Sphère. Utilisé uniquement lorsque le mode colorimétrique de la forme est défini sur Entrée image.

### Paramètres

* **Mode position** : *Distance avec l&#39;origine, position mondiale*\
  Choisissez entre deux modes de placement. La distance avec l&#39;origine est similaire aux coordonnées polaires, la sphère est définie par rapport au centre du panorama, la position universelle fonctionne comme les coordonnées 3D standard.
* **Coordonnées De Position**
  * **Vecteur Up** : *Z Up, Y Up*\
    En mode Position universelle uniquement, déterminez l&#39;orientation du repère.
  * **Position Sphère Mondiale** : *-2,0 - 2,0*\
    Le mode Position universelle permet uniquement de définir la position de la sphère dans l’espace univers.
  * **Position** :\
    Uniquement en mode Distance avec l&#39;origine. Définit la position par rapport au centre. Peut être manipulé dans la vue 2D.
  * **Distance avec l&#39;origine** : *0.0 - 20.0* Uniquement en mode Distance avec l&#39;origine. Définit la distance par rapport à l’origine et affecte la taille visible de la sphère.
* **Mode De Couleur De Forme** : *RGB, Température (Kelvin), Entrée D&#39;Image*\
  Choisissez la méthode à utiliser pour définir la couleur de la forme. Image Input permet d&#39;utiliser le deuxième emplacement d&#39;entrée.
* **Couleur** : *(valeur chromatique)*\
  Uniquement avec le mode colorimétrique de la forme défini sur RGB. Choisit la couleur de la forme.
* **Température de forme** : *800.0 - 20000.0*\
  Uniquement avec le mode Couleur de la forme réglé sur Température. Définit la valeur Kelvin pour la couleur de la forme.
* **Gamma d&#39;entrée d&#39;image sphère** : *sRVB, linéaire*\
  Uniquement avec le mode colorimétrique de la forme défini sur Entrée image. Déterminez comment interpréter l’entrée d’image de forme.
* **Rotation de la sphère** : *0.0 - 1.0*\
  Uniquement avec le mode colorimétrique de la forme défini sur Entrée image. Fait tourner la sphère autour de son centre pour orienter l’image mappée.
* **Exposition (EV)** : *0.0 - 10.0*\
  Définissez la valeur d’exposition de la forme générée, idéalement adaptée à la valeur d’exposition de l’image d’arrière-plan.
* **Rayon sphère** : *0,0 - 1,0*\
  Définit le rayon/la taille de la sphère.
* **Dureté de la sphère** : *0,0 - 1,0*\
  Définit la dureté/atténuation de la sphère.
* **Ombrage** :*Sans, Obscurcissement des membres, Lumière d&#39;Ombrage*\
  Définissez si un ombrage doit être appliqué à la sphère. Permet à la sphère de ne pas apparaître comme un objet solide non éclairé. L’obscurcissement des membres signifie qu’un léger obscurcissement apparaît sur les bords, l’éclairage Ombrage signifie que la sphère est éclairée par une lumière Ombrage facultative.
* **Position Mondiale Avec Ombrage Clair** : *-1,0 - 1,0*\
  Si l’option Ombrage est définie sur Lumière d’Ombrage, la position de la lumière sur la sphère est ici contrôlée.
* **Transparence Penombra** : *0.0 - 1.0*\
  Si l’option Ombrage est définie sur Lumière d’Ombrage, contrôle le retrait de l’ombrage.
* **Activer L&#39;Entrée En Arrière-Plan** : *Faux/Vrai*\
  Active/désactive l’utilisation d’une image d’arrière-plan facultative. Les composites ont généré de la lumière au-dessus de l’arrière-plan.
* **Couleur d&#39;arrière-plan** : *(valeur de couleur)*\
  Si l’entrée Arrière-plan n’est pas utilisée, définissez ici une valeur d’arrière-plan de couleur unie.
* **Gamma d&#39;arrière-plan** : *sRVB, linéaire* Si l&#39;entrée d&#39;arrière-plan est utilisée, définissez comment interpréter l&#39;entrée d&#39;arrière-plan.

## Exemples d’images

![](../../../../../../assets/sphere-light-ex.gif)

![](../../../../../../assets/spherelight-ex1.png)

</td>
</tr>
</table>
