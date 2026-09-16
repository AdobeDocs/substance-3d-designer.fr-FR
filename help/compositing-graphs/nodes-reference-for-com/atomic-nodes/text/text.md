---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/text.html"
breadcrumb-title: ""
description: Utilisez le nœud Texte pour générer des textures de texte avec des polices et des styles personnalisables afin de créer des modèles textuels.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Text
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Texte
user-guide-description: ""
user-guide-title: ""
source-git-commit: 0cb0df528e7f0eb6f3c2d51e35302744952718d5
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 1%
---

# Texte

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Noeud atomique : Texte](text.resources/comp_text_1.png "Noeud atomique : Texte")

</td>
<td style="border: 0;" valign="top">

Le nœud Texte fournit un moyen de placer du texte créé par l’utilisateur dans vos graphes. Les utilisateurs peuvent également sélectionner des paramètres tels que la police, l’alignement et la rotation pour personnaliser l’emplacement du texte.

Le nœud Texte est très puissant et constitue le seul moyen de placer facilement du texte. Cela peut être un peu difficile à utiliser en raison du placement qui se produit toujours sur une zone de travail carrée et limitée et parce que les polices sont pilotées par une liste externe définie par le système.

</td>
</tr>
</table>

<div data-preserve-html="true" style="text-align: center;"><img src="text.resources/text-tooltip.gif" alt="info-bulle de texte" /></div>

Seules les polices Truetype (.ttf) et certaines polices Opentype sont prises en charge. Si des polices sont absentes de la liste, il s’agit probablement de la raison. <b>Les polices ne peuvent pas être exposées en tant que paramètre.</b>

Lorsqu’un Graphe utilisant du texte est publié sur sbsar, la police est incorporée dans le package, tout comme les bitmaps et autres ressources, pour s’assurer qu’elle fonctionne sur tous les systèmes et applications.



## Paramètres

|  |  |
| --- | --- |
| <b>Mode colorimétrique</b> *Booléen* | Permet de basculer entre une image en niveaux de gris et une image en couleur. |
| <b>Texte</b> *Chaîne* | Détermine la description du texte. |
| <b>Police</b> *Chaîne* | Ressource de police utilisée pour le rendu du texte. |
| <b>Taille de police</b> *Flottant* | Taille de police du texte, en points. |
| <b>Alignement</b> *Entier* | Définit l’alignement du texte à gauche, au centre (par défaut) ou à droite. |
| <b>Transformation</b> *Flottant4* | Matrice de transformation 2x2 appliquée au texte rendu. |
| <b>Position</b> *Flottant 2* | Position du texte dans l’image de sortie. |
| <b>Arrière-plan</b> *Flottant/Flottant 4* | Couleur d’arrière-plan de l’image de sortie. |
| <b>Couleur de la police</b> *Flottant/Flottant 4* | Couleur du texte. |

## Connecteurs d’entrée

|  |  |
| --- | --- |
| <b>Arrière-plan</b> *Niveaux de gris/Couleur* PRINCIPAL | Couleur d’arrière-plan de l’image de sortie. |


## Exemples

*Bientôt disponible.*
