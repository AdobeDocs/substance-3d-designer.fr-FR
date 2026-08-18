---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/mask-builder.html"
breadcrumb-title: ''
description: Utilisez le nœud Concepteur de masque pour combiner plusieurs entrées de masque et créer des motifs de masque complexes pour des effets de matière.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Mask Builder
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Générateur de masques
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '741'
ht-degree: 0%

---


# Générateur de masques

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/mask-builder.png){width="128px"}

## Générateur de masques

**Entrée :** *Générateurs basés sur le maillage**/Générateurs de masques*

**Complexe**

</td>
<td style="border: 0;" valign="top">

## Description

Génère un masque noir et blanc en fonction des maps bakées et des paramètres utilisateur. Il s’agit de la version Designer de Painter Mask Builder.

Il s&#39;agit d&#39;un outil complexe conçu comme un constructeur de masques global, basé sur des maps bakées, des paramètres utilisateur et des modèles et cartes d&#39;usure/salissures. Il est principalement conçu comme un nœud très avancé et à contrôle total pour se fondre dans le dirt de pli et l&#39;usure des bords. Ce nœud est suffisamment puissant pour imiter tous les autres générateurs de masques.

Aucun frein n&#39;est explicitement requis, mais plus vous fournissez, plus ce nœud est capable de faire.

## Paramètres

### Entrées

* **Occlusion ambiante** : *Entrée en niveaux de gris*
* **Courbure** : *Entrée en niveaux de gris*
* **Espace universel normal** : *entrée de couleur*
* **Entrée Usure/salissures** : *Entrée Niveaux De Gris*
* **Entrée Usure/salissures 2** : *Entrée Niveaux De Gris*
* **Entrée Dispersion** :*Entrée Niveaux De Gris*\
  Tampon de dispersion personnalisé, requis pour utiliser les paramètres de Dispersion.
* **Masque (facultatif)** : *Entrée en niveaux de gris*\
  Emplacement de masque utilisé pour masquer les effets du nœud.
* **Position** : *Entrée Couleur*\
  Ce paramètre est utilisé pour les effets triplanaires et de haut en bas.

### Paramètres

* **Niveau** : *0.0 - 1.0*\
  Définit le niveau total de l’effet, qui s’affiche progressivement.
* **Contraste** : *0,0 - 1,0*\
  Règle le contraste du résultat.
* **Inverser** : *Faux/Vrai*\
  Inverse le résultat. Utile pour obtenir l’opposé du masque que vous créez.
* **Utiliser triplanaire** :*Faux/Vrai* Active la projection triplanaire, en évitant toute jointure avec les cartes usure/salissures.
* **Contraste de fusion triplanaire** : *0.0 - 1.0* définit le contraste de la fusion triplanaire.
* **Usure/salissures** : *0,0 - 1,0* définit la quantité d&#39;Usure/salissures à intégrer globalement.
* **Usure/salissures**
  * **Échelle** : *0 - 10* Définit l’échelle de l’Usure/salissures globale.
  * **Utiliser l&#39;Usure/salissures personnalisée** : *Faux/Vrai* Active l&#39;entrée d&#39;Usure/salissures personnalisée.
  * **Usure/salissures personnalisée secondaire** : *0.0 - 1.0* Active une deuxième entrée Usure/salissures personnalisée.
  * **Inverser** : *Faux/Vrai*\
    Inverse la courbe d’Usure/salissures.
* **AO** : *-1.0 - 1.0* Définit l&#39;étendue à laquelle l&#39;effet doit apparaître dans les zones AO occluses. Peut être modifié avec le groupe ci-dessous.
* **AO**
  * **Plage** : *0.0 - 1.0* Définit le seuil ou la plage pour l&#39;apparence du dirt.
  * **Contraste** : *0,0 - 1,0*\
    Règle le contraste de l’effet AOP.
  * **Bruit** :*0,0 - 1,0* Définit la quantité de bruit/usure/salissures à fusionner avec l&#39;effet AO.
  * **Échelle de bruit** : *0 - 10* définit l&#39;échelle du bruit/de l&#39;usure/salissures de l&#39;AO.
  * **Type de bruit** :*Taches, nuages, humidité, bruit blanc* bascule entre 4 types de bruit AO différents.
  * **Inverser** : *Faux/Vrai*\
    Inverse l’interprétation de la carte AO : le bruit apparaîtra dans les zones AO claires, et non dans les zones AO sombres.
* **Courbure** : *0.0 - 1.0* Définit l’effet qui doit apparaître sur les bords de courbure ; il peut être à la fois convexe et concave. Modifiez ceci avec le groupe ci-dessous.
* **Courbure**
  * **Plage de convexité** : *-1.0 - 1.0* Définit l&#39;effet à appliquer sur les bords de courbure convexes (clairs).
  * **Contraste convexe** : *0.0 - 1.0* définit le contraste de l&#39;effet convexe.
  * **Inversion convexe** :*Faux/Vrai* Inverse l&#39;interprétation des bords convexes.
  * **Plage concave** : *-1.0 - 1.0* Définit l’effet à appliquer sur les bords de courbure concaves (sombres).
  * **Contraste concave** : *0.0 - 1.0* définit le contraste de la plage concave.
  * **Inversion concave** :*Faux/Vrai* Inverse l&#39;interprétation des bords concaves.
  * **Smoothness** : *0,0 - 16,0* Niveau de flou et de lissage à appliquer aux bords de courbure.
  * **Amplification de niveau** : *0,0 - 1,0* amplification supplémentaire si l’effet n’est pas assez visible.
  * **Bruit** :*0.0 - 1.0* définit l’influence du bruit/de l’usure/salissures sur l’effet Courbure.
  * **Échelle de bruit** : *0 - 10* définit l’échelle du bruit.
  * **Type de bruit** :*Taches, nuages, humidité, bruit blanc* Choisissez entre 4 types de bruit différents.
* **Dégradé de haut en bas** : *-1.0 - 1.0* Fusionne ou masque avec un dégradé de haut en bas en fonction du mappage de position. Les valeurs positives éclaircissent les choses, tandis que les valeurs négatives masquent les effets existants.
* **Dégradé**
  * **Plage** : *0,0 - 1,0* définit la position du dégradé.
  * **Contraste** : *0,0 - 1,0*\
    Règle le contraste du dégradé.
  * **Inverser** : *Faux/Vrai*\
    Inverse le dégradé. Permute efficacement le bas et le haut.
* **Espace universel normal** :*0,0 - 1,0* similaire au dégradé de haut en bas, mais avec la carte de position et dans six directions, semblable à un faux éclairage. Les valeurs positives s’éclaircissent, les valeurs négatives s’assombrissent.
* **Espace universel normal**
  * **Intensité supérieure** : *-1,0 - 1,0*
  * **Intensité inférieure** : *-1,0 - 1,0*
  * **Intensité avant** : *-1,0 - 1,0*
  * **Intensité du dos** : *-1,0 - 1,0*
  * **Intensité correcte** : *-1,0 - 1,0*
  * **Intensité gauche** : *-1,0 - 1,0*
* **Scratches** : *-1.0 - 1.0* Mélange les rayures dans les zones blanches.
* **Scratches**
  * **Quantité** : *0 - 4096* Définit la quantité totale de rayures.
  * **Échelle** : *0.0 - 1.0* Définit l’échelle de chaque rayure.
* **Dispersion** : *-1.0 - 1.0* Dispersion un tampon personnalisé dans les zones blanches.
* **Dispersion**
  * **Échelle** : *0 - 50*&#x200B;Échelle totale de l’effet.
  * **Densité** : *0.0 - 1.0* Contrôle de la densité de diffusion, valeur qui doit apparaître.
  * **Taille** : *0,0 - 4,0* Taille du tampon dispersé.
  * **Variation de taille** : *0.0 - 1.0* Variation dans la taille du tampon.
  * **Variation d’opacité** : *0.0 - 1.0* Variation dans l’opacité du tampon.

## Exemples d’images

|  |
| --- |
| Aucune image n&#39;est jointe à cette page. |

</td>
</tr>
</table>
