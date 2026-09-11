---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/uniform-color.html"
breadcrumb-title: ''
description: Utilisez le nœud Couleur uniforme pour générer des textures de couleur uniforme afin de créer des remplissages de couleur unie et des calques de base.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Uniform color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Couleur uniforme
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9aaf135d4c336ea0cff865524ad1ccd5dcc225bd
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 8%

---


# Couleur uniforme

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Noeud atomique : Couleur uniforme](uniform-color.resources/comp_uniform_1.png "Noeud atomique : Couleur uniforme"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Génère une valeur constante de niveau de gris ou de couleur.

Il s’agit d’un nœud simple, très souvent utilisé comme point de départ pour l’ajout de couleurs ou la création de valeurs spécifiques.

</td>
</tr>
</table>

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

>[!TIP]
>
> Optimisation des performances
> 
> Ces deux réglages réduisent le temps de calcul et l&#39;empreinte mémoire du nœud :
> 
> * Si une valeur de niveaux de gris est nécessaire, assurez-vous de basculer le [mode colorimétrique](#parameters) du nœud sur « Niveaux de gris ».
> * La sortie du nœud étant une couleur plate, vous pouvez utiliser la résolution la plus basse possible. Définissez le paramètre « [Taille de sortie](../../../../compositing-graphs/output-size/output-size.md) » du nœud pour utiliser la [méthode d&#39;héritage](../../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) « absolue » et une résolution de 16x16 pixels.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Paramètres

</td>
<td style="border: 0;" valign="top">

### Connecteurs de sortie

</td>
<td style="border: 0;" valign="top">

### Exemples

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

## Paramètres

|  |  |
| --- | --- |
| <b>Mode colorimétrique</b> *Booléen* | Permet de basculer entre une image en niveaux de gris et une image en couleur. |
| <b>Couleur de sortie</b> *Flottant/Flottant 4* | Sélectionne la couleur plate à utiliser dans l’image de sortie.   Lors de l’utilisation du mode colorimétrique Couleur, le Canal Alpha est utilisé pour l’opacité, où 0 est entièrement transparent et 1 entièrement opaque. |

## Connecteurs de sortie

|  |  |
| --- | --- |
| <b>Sortie</b> *Couleur/Niveaux De Gris* |  |

## Exemples

*Bientôt disponible.*
