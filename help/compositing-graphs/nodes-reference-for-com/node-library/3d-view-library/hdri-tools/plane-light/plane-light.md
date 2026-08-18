---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/plane-light.html"
breadcrumb-title: ''
description: Utilisez le nœud Lumière plane pour ajouter des sources lumineuses planes aux environnements HDRI afin de contrôler l’éclairage directionnel.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Plane Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Éclairage plan
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '631'
ht-degree: 0%

---


# Éclairage plan

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/panorama-plane-light.png){width="200px"}

## Éclairage plan

**Entrée :** *Vue/Outils HDRI 3D*

**Complexe**

</td>
<td style="border: 0;" valign="top">

## Description

Génère une forme plane projetée sphériquement. Le plan peut être placé et orienté en 3D à l’aide des paramètres d’entrée.

Elle diffère de la [lumière de forme](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/hdri-tools/shape-light/shape-light.md) plus simple en ce sens qu&#39;elle offre des options de placement plus avancées en dehors de la projection de Distance avec l&#39;origine plus simple, et que davantage de motifs et de masques peuvent être appliqués, tout comme la [lumière de ligne](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/hdri-tools/line-light/line-light.md).

## Entrées

* **Entrée d&#39;image d&#39;arrière-plan** : *Entrée de couleur*\
  Arrière-plan facultatif sur lequel composer la lumière générée.
* **Entrée d&#39;image de forme** : *Entrée de couleur*\
  Image facultative à plaquer sur l’éclairage linéaire. Utilisé uniquement lorsque le mode colorimétrique de la forme est défini sur Entrée image.
* **Entrée d&#39;image de motif** : *Entrée en niveaux de gris*\
  Image de motif personnalisée, utilisée lorsque le paramètre « Motif » est défini sur « Entrée image ».

## Paramètres

* **Mode Position** : *Sol/Plafond, Distance avec l&#39;origine, Positions Dans Le Monde*\
  Choisissez parmi trois modes de placement différents. Manipulation de la prise en charge du sol/plafond et de la Distance avec l&#39;origine dans la vue 2D, les positions universelles ne peuvent être modifiées que par le biais des propriétés, mais prennent en charge un placement plus exact.
* **Afficher la grille au sol** :*Faux/Vrai*\
  Fonction d&#39;aide permettant de dessiner une grille de mise à la terre de débogage. Permet d’estimer la position des lignes dans l’espace.
* **Coordonnées De Position**
  * **Vecteur Up** : *Z Up, Y Up*\
    En mode Position universelle uniquement, déterminez l&#39;orientation du repère.
  * **Position UV dans le plan** :\
    Seulement avec sol / plafond et Distance avec l&#39;origine. Définit la position du plan dans l’espace UV.
  * **Position Planétaire En Plan** : *-2,0 - 2,0*\
    Uniquement avec le mode Positions universelles. Définit la position du plan dans l’espace universel. Aucune interaction de vue 2D prise en charge.
  * **Height absolu du plan** : *0.0 - 1.0*\
    Uniquement avec le mode Position sol/plafond, définit l&#39;height absolu à partir du plafond. Utilisez Afficher la grille au sol pour mieux estimer la position.
  * **Distance avec l&#39;origine** : *0.0 - 1.0*\
    Uniquement avec le mode Position de la Distance avec l&#39;origine. Définit la distance entre les deux points du panorama.
* **Mode De Couleur De Forme** : *RGB, Température (Kelvin), Entrée D&#39;Image*\
  Choisissez la méthode à utiliser pour définir la couleur de la forme. Image Input permet d&#39;utiliser le deuxième emplacement d&#39;entrée.
* **Couleur** : *(valeur chromatique)*\
  Uniquement avec le mode colorimétrique de la forme défini sur RGB. Choisit la couleur de la forme.
* **Température** : *800.0 - 20000.0*\
  Uniquement avec le mode Couleur de la forme réglé sur Température. Définit la valeur Kelvin pour la couleur de la forme.
* **Mode UV de l’image de forme** : *Étirer, Étirer au milieu uniquement, Répéter + Espacement*\
  Uniquement avec le mode colorimétrique de la forme défini sur Entrée image. Définit la façon dont l’image est appliquée à la forme de trait et détermine le comportement de répétition UV.
* **Espacement de répétition d&#39;image de forme** : *0.0 - 1.0*\
  Uniquement avec le mode colorimétrique de la forme défini sur Entrée image et avec le mode UV défini sur Répétition + Espacement. Définit l’espacement lorsque l’image se répète le long de la ligne.
* **Gamma d&#39;image de forme** : *sRVB, linéaire*\
  Uniquement avec le mode colorimétrique de la forme défini sur Entrée image. Déterminez comment interpréter l’entrée d’image de forme.
* **Exposition (EV)** : *0.0 - 10.0*\
  Définissez la valeur d’exposition de la forme générée, idéalement adaptée à la valeur d’exposition de l’image d’arrière-plan.
* **Échelle de plan** : *0.0 - 1.0*\
  Définissez une échelle uniforme pour la forme Plan.
* **Taille du plan** : *0.0 - 1.0*\
  Définissez une taille non uniforme de la forme Plan.
* **Rotation du plan** : *0.0 - 1.0*\
  Faire pivoter le plan le long de son axe central.
* **Motif** : *Carré Lisse, Carré Net, Cône, Hémisphère, Entrée D&#39;Image*\
  Sélectionnez la forme de motif à utiliser.
* **Dureté du motif** : *0.0 - 1.0*\
  Définissez la dureté/le contraste du motif.
* **Mode UV du motif** : *Étirer, Étirer au milieu uniquement*\
  Définissez comment utiliser le masque de motif secondaire, appliqué au-dessus de l’image de forme.
* **Activer L&#39;Écrêtage Au Sol** : *Faux/Vrai*\
  Activez cette option si le plan peut être écrêté par un plan au sol ou s’il est toujours affiché en dessous. Utilisez l’option Afficher la grille au sol pour mieux l’estimer.
* **Height au sol** : *-2.0 - 0.0*\
  Réglez l’height au sol pour l’écrêtage.
* **Activer L&#39;Entrée En Arrière-Plan** : *Faux/Vrai*\
  Active/désactive l’utilisation d’une image d’arrière-plan facultative. Les composites ont généré de la lumière au-dessus de l’arrière-plan.
* **Couleur d&#39;arrière-plan** : *(valeur de couleur)*\
  Si l’entrée Arrière-plan n’est pas utilisée, définissez ici une valeur d’arrière-plan de couleur unie.
* **Gamma d&#39;arrière-plan** : *sRVB, linéaire* Si l&#39;entrée d&#39;arrière-plan est utilisée, définissez comment interpréter l&#39;entrée d&#39;arrière-plan.

## Exemples d’images

![](../../../../../../assets/plane-light-ex.gif)

</td>
</tr>
</table>
