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
source-git-commit: ca90755a159a7e0297bb26d1e3522b0cfeb6f2ac
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 6%

---


# Matériau de base

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/pbr-base-material.png){width="128px"}

<b>Entrée :</b> Filtres de matériau > Utilitaires PBR

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Le moyen le plus rapide et le plus simple de créer un matériau multicanal dans [Adobe Substance 3D Designer](https://www.adobe.com/fr/products/substance3d-designer.html). Ce nœud renvoie une matière complète groupée basée sur des valeurs et des paramètres de couleur unie simples. Vous pouvez ensuite l’utiliser comme pseudo-élément ou l’affiner pour obtenir un matériau complexe.

Le nœud est très utile pour texturer des accessoires complets et fusionner plusieurs matériaux. En fait, vous pouvez démarrer chaque matériau à partir de ce nœud, sans jamais avoir besoin d&#39;une base de matériaux complexe.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
|  | Entrées facultatives pour chaque canal qui peut être basculé avec les commutateurs dans « Entrées définies par l&#39;utilisateur ». |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Workflow PBR</b> <i>Métal - Rugosité, Specular - Brillance</i> | Définit le modèle PBR utilisé. |
| <b>Paramètre prédéfini de matériau</b> <i>Personnalisé, Diélectrique, Or, Argent, Aluminium, Fer, Cuivre, Titane, Nickel, Cobalt, Platine</i> | Raccourci rapide pour créer certains métaux. Désactive les options non pertinentes. |
| <b>Couleur de base</b> <i>(valeur de couleur)</i> | Couleur unie utilisée pour la Base color. |
| <b>Métallique</b> <i>(valeur Niveaux de gris)</i> | Valeur solide utilisée pour Métallique. |
| <b>Couleur Diffuse</b> <i>(valeur de couleur)</i> | Couleur unie utilisée pour le Diffuse. |
| <b>Specular</b> <i>(valeur de couleur)</i> | Couleur unie utilisée pour le Specular. |
| <b>Paramètres prédéfinis Specular</b> <i>Plastique, Bois, Pierre, Brique, Sable, Béton, Tissu, Métal Rouillé, Eau, Glace, Verre</i> | Paramètres prédéfinis rapides facultatifs pour définir des valeurs de Specular PBR correctes. |
| <b>Plage de Specular</b> <i>0.0 - 1.0</i> | Règle la plage de Specular. |
| <b>Rugosité - Brillance</b> |  |
| <b>Valeur de Rugosité</b> <i>(valeur Niveaux de gris)</i> | Définissez la valeur de rugosité de base globale si la couche est active. |
| <b>Valeur de Brillance</b> <i>(valeur Niveaux de gris)</i> | Couleur unie utilisée pour la Brillance, si la couche est active. |
| <b>Quantité Usure/salissures</b> <i>0.0 - 1.0</i> | Degré de fusion de l’entrée de mappage Usure/salissures facultative dans les options Lustre ou Rugosité. |
| <b>Répétition Usure/salissures</b> <i>1 - 16</i> | Étendue de mosaïque de la carte Usure/salissures facultative par. |
| <b>Entrée Usure/salissures personnalisée</b> <i>Faux/Vrai</i> | Active ou désactive le mappage Usure/salissures personnalisé facultatif . |
| <b>Normal</b> |  |
| <b>Normal à partir de l&#39;intensité de l&#39;Height</b> <i>0.0 - 16.0</i> | Convertit éventuellement le calque de hauteur personnalisé en calque normal et le renvoie comme calque de hauteur par matériau. |
| <b>Height</b> |  |
| <b>Position Height</b> <i>0.0 - 1.0</i> | Valeur solide utilisée pour la sortie Height. |
| <b>Plage d&#39;Height</b> <i>0.0 - 1.0</i> | Définit l’influence de la carte de hauteur définie par l’utilisateur, si cette option est activée. |
| <b>Cartes Définies Par L&#39;Utilisateur</b> | Active ou désactive toutes les cartes définies par l&#39;utilisateur, renvoyant ces dernières au lieu des valeurs unies. |
