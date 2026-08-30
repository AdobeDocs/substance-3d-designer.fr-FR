---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/text.html"
breadcrumb-title: ''
description: Utilisez le nœud Texte pour générer des textures de texte avec des polices et des styles personnalisables afin de créer des motifs textuels.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Text
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Texte
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 1%

---


# Texte

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nœud atomique : Texte](text.resources/comp_text_1.png "Nœud atomique : Texte"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Le nœud Texte permet d’insérer du texte créé par l’utilisateur dans vos graphiques. Les utilisateurs peuvent également sélectionner des paramètres tels que la police, l’alignement et la rotation pour personnaliser l’emplacement du texte.

Le nœud Texte est très puissant et constitue le seul moyen de placer facilement du texte. Cela peut être un peu difficile à utiliser en raison du placement qui se produit toujours sur une zone de travail carrée et limitée et parce que les polices sont pilotées par une liste externe définie par le système.

</td>
</tr>
</table>

Seules les polices Truetype (.ttf) et certaines polices Opentype sont prises en charge. Si des polices sont absentes de la liste, il s’agit probablement de la raison. <b>Les polices ne peuvent pas être affichées en tant que paramètre.</b>

Lorsqu’un graphique utilisant du texte est publié sur sbsar, la police est incorporée dans le package, comme pour les bitmaps et autres ressources, afin de garantir son bon fonctionnement sur tous les systèmes et applications.

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">



</td>
<td width="83.33%" style="border: 0;" valign="top">



</td>
<td width="100.00%" style="border: 0;" valign="top">



</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Connecteurs de sortie

</td>
<td style="border: 0;" valign="top">

### Exemples

</td>
</tr>
</table>

## Paramètres

|  |  |
| --- | --- |
| <b>Mode colorimétrique</b> *Booléen* | Permet de basculer entre une image en niveaux de gris et une image en couleur. |
| <b>Texte</b> *Chaîne* | Détermine la description du texte. |
| <b>Police</b> *Chaîne* | Ressource de police utilisée pour le rendu du texte. |
| <b>Taille de police</b> *Flotter* | Taille de police du texte, en points. |
| <b>Alignement</b> *Nombre entier* | Définit l’alignement du texte à gauche, au centre (par défaut) ou à droite. |
| <b>Transformation</b> *Float4* | Matrice de transformation 2x2 appliquée au texte rendu. |
| <b>Position</b> *Float2* | Position du texte dans l’image de sortie. |
| <b>Arrière-plan</b> *Float/Float4* | Couleur d’arrière-plan de l’image de sortie. |
| <b>Couleur de la police</b> *Float/Float4* | Couleur du texte. |

## Connecteurs d’entrée

|  |  |
| --- | --- |
| <b>Arrière-plan</b> *Niveaux de gris/Couleur* PRINCIPAL | Couleur d’arrière-plan de l’image de sortie. |

## Connecteurs de sortie

|  |  |
| --- | --- |
| <b>Sortie</b> *Niveaux de gris/Couleur* |  |

## Exemples

*Bientôt disponible.*
