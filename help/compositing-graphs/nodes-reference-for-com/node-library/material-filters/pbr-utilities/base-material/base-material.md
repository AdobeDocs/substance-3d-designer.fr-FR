---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/base-material.html"
breadcrumb-title: ''
description: Utilisez le nœud Matériau de base pour créer des propriétés de matériau de base afin de créer de toutes pièces des matériaux physiques.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > PBR Utilities > Base Material
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Matériau de base
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 4%

---


# Matériau de base

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/pbr-base-material.png){width="128px"}

## Matériau de base

**Entrée :** *Filtres de matériaux/Utilitaires PBR*

**Intermédiaire**

</td>
<td style="border: 0;" valign="top">

## Description

Le moyen le plus rapide et le plus simple de créer un matériau multicanal dans [Adobe Substance 3D Designer](https://www.adobe.com/fr/products/substance3d-designer.html). Ce nœud renvoie une matière complète groupée basée sur des valeurs et des paramètres de couleur unie simples. Vous pouvez ensuite l’utiliser comme pseudo-élément ou l’affiner pour obtenir un matériau complexe.

Le nœud est très utile pour texturer des accessoires complets et fusionner plusieurs matériaux. En fait, vous pouvez démarrer chaque matériau à partir de ce nœud, sans jamais avoir besoin d&#39;une base de matériaux complexe.

## Paramètres

### Entrées

* Entrées facultatives pour chaque canal qui peut être basculé avec les commutateurs dans « Entrées définies par l&#39;utilisateur ».

### Paramètres

* **Workflow PBR** :*Métal - Rugosité, Specular - Brillance* définit le modèle PBR utilisé.
* **Paramètre prédéfini de matériau** :*Personnalisé, Diélectrique, Or, Argent, Aluminium, Fer, Cuivre, Titane, Nickel, Cobalt, Platine* Raccourci rapide pour créer certains métaux. Désactive les options non pertinentes.
* **Couleur de base** : *(Valeur de couleur)*Couleur unie utilisée pour la couleur de base.
* **Métallique** : *(Valeur Niveaux de gris)*Valeur solide utilisée pour Métallique.
* **Couleur diffuse** : *(Valeur de couleur)*Couleur unie utilisée pour Diffuse.
* **Specular** : *(Valeur chromatique)*Couleur unie utilisée pour le Specular.
* **Paramètres prédéfinis de Specular** :*plastique, bois, pierre, brique, sable, béton, tissu, métal rouillé, eau, glace, verre* Des paramètres prédéfinis rapides facultatifs pour définir des valeurs de Specular correctes pour le PBR.
* **Plage de Specular** : *0,0 - 1,0* ajuste la plage de Specular.
* **Rugosité - Brillance**
  * **Valeur de la rugosité** : *(valeur Niveaux de gris)*Définissez la valeur de rugosité de base globale, si la couche est active.
  * **Valeur de brillance** : *(valeur Niveaux de gris)*Couleur unie utilisée pour le brillant, si la couche est active.
  * **Quantité d&#39;Usure/salissures** : *0.0 - 1.0* Degré de fusion de l&#39;entrée de mappage d&#39;Usure/salissures facultative vers le brillant ou la rugosité.
  * **Limites d&#39;Usure/salissures** : *1 - 16*&#x200B;Étendue de la mosaïque de mappage d&#39;Usure/salissures facultative par.
  * **Entrée Usure/salissures personnalisée** : *Faux/Vrai* Active ou désactive le mappage Usure/salissures personnalisé facultatif .
* **Normal**
  * **Normale à partir de l&#39;intensité de l&#39;Height** : *0.0 - 16.0* Convertit éventuellement la courbe de hauteur personnalisée en courbe normale et la renvoie en tant que courbe de normale du matériau.
* **Height**
  * **Position de l&#39;Height** : *0.0 - 1.0* Valeur solide utilisée pour la sortie Height.
  * **Plage d&#39;Height** : *0.0 - 1.0* Définit l&#39;influence de la carte de hauteur définie par l&#39;utilisateur, si elle est activée.
* **Cartes Définies Par L&#39;Utilisateur**
  * Active ou désactive toutes les cartes définies par l&#39;utilisateur, renvoyant ces dernières au lieu des valeurs unies.

## Exemples d’images

|  |
| --- |
| Aucune image n&#39;est jointe à cette page. |

</td>
</tr>
</table>
