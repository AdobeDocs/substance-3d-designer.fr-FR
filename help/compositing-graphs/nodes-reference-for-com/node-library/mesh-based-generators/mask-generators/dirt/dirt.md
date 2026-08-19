---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/dirt.html"
breadcrumb-title: ''
description: Utilisez le nœud Dirt pour générer des masques d’accumulation de dirts en fonction de la courbure, de la position et de l’occlusion du maillage.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Dirt
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Saleté
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 2%

---


# Saleté

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/dirt.png){width="128px"}

## Saleté

**Entrée :** *Générateurs basés sur le maillage**/Générateurs de masques*

**Intermédiaire**

</td>
<td style="border: 0;" valign="top">

## Description

Génère un masque noir et blanc en fonction des maps bakées et des paramètres utilisateur. Similaires aux [masques dynamiques](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) dans [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Ce masque représente les dirts des bords et des coins occultés et enfoncés, en fonction de l&#39;AO et de la courbure cuits.

## Paramètres

### Entrées

* **Courbure** : *Entrée en niveaux de gris*\
  Map bakée utilisée pour les effets internes et le masquage. Obligatoire !
* **Occlusion ambiante** : *Entrée en niveaux de gris*\
  Map bakée utilisée pour les effets internes et le masquage. Obligatoire !
* **Entrée Usure/salissures** : *Entrée niveaux de gris*\
  Entrée de mappage usure/salissures personnalisée, facultative, activée par le paramètre.
* **Masque (facultatif)** : *Entrée en niveaux de gris*\
  Emplacement de masque utilisé pour masquer les effets du nœud.
* **Espace universel normal** : *entrée de couleur*\
  Utilisé uniquement pour le format triplanaire.
* **Position** : *Entrée Couleur*\
  Utilisé uniquement pour le format triplanaire.

### Paramètres

* **Niveau de Dirt** : *0,0 - 1,0* Contrôle principal du montant du dirt.
* **Contraste du Dirt** :*0.0 - 1.0* contrôle le contraste principal du dirt dans le masque.
* **Quantité d&#39;Usure/salissures** : *0.0 - 1.0* Définit le degré de granulosité du dirt. Réglez la valeur sur 0 pour obtenir un dirt parfaitement lisse.
* **Masquage des bords** : *0,0 - 1,0* quantité de dirt à supprimer des bords relevés (en fonction de la courbe de référence).
* **Utiliser l&#39;Usure/salissures personnalisée** : *Faux/Vrai* Active l&#39;utilisation de l&#39;entrée de mappage usure/salissures personnalisée au lieu de l&#39;Usure/salissures intégrée.
* **Échelle d&#39;Usure/salissures** : *1 - 16* définit l&#39;échelle de mosaïque des détails d&#39;Usure/salissures.
* **Utiliser la projection triplanaire** : *Faux/Vrai* Utiliser la [projection triplanaire](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/utilities-mesh-based-gen/tri-planar/tri-planar.md) pour le mappage Usure/salissures, supprime les coutures.
* **Contraste de fusion triplanaire** : *0.001 - 1.0* définit le contraste de la projection triplanaire.

## Exemples d’images

![](../../../../../../assets/dirt-ex.gif)

</td>
</tr>
</table>
