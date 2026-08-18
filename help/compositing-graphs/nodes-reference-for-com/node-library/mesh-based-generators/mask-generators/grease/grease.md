---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/grease.html"
breadcrumb-title: ''
description: Utilisez le nœud Graisse pour générer des masques d'accumulation de graisse en fonction de la géométrie du maillage et des zones de contact.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Grease
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Graisse
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 2%

---


# Graisse

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/grease.png){width="128px"}

## Graisse

**Entrée :** *Générateurs basés sur le maillage**/Générateurs de masques*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Description

Génère un masque noir et blanc en fonction des maps bakées et des paramètres utilisateur. Similaires aux [masques dynamiques](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) dans [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Ce masque est spécialement conçu pour les visages de personnages et d’autres zones spécifiques. Génère un masque de type peau-graisse sur les zones à faible thickness.

## Paramètres

### Entrées

* **Thickness** : *Entrée en niveaux de gris*\
  Placage de Thickness cuit sur lequel repose l’ensemble de l’effet. Obligatoire !
* **Bruit** :*Entrée En Niveaux De Gris*\
  Carte Bruit en option pour remplacer l’usure/salissures de la graisse.
* **Masque (facultatif)** : *Entrée en niveaux de gris*\
  Emplacement de masque utilisé pour masquer les effets du nœud.

### Paramètres

* **Niveau** : *0.0 - 1.0*\
  Définit la quantité totale d’effet à afficher.
* **Contraste** : *0,0 - 1,0*\
  Règle le contraste du résultat.
* **Seuil de Thickness** : *0,0 - 1,0* Définit un thickness minimum auquel l&#39;effet doit apparaître. Tout aussi important que le niveau, ajustez-le en fonction de votre carte de Thickness.
* **Remplacer le bruit** : *Faux/Vrai* Définissez pour remplacer la carte d&#39;usure/salissures de graisse interne avec un emplacement d&#39;entrée personnalisé.

## Exemples d’images

![](../../../../../../assets/grease-ex.gif)

</td>
</tr>
</table>
