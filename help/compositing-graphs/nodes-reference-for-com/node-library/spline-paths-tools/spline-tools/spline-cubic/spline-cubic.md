---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-cubic.html"
breadcrumb-title: ''
description: Utilisez le nœud Cubique spline pour créer des splines cubiques lisses avec quatre points de contrôle pour les tracés courbes.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline (Cubic)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Spline (Cubique)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '772'
ht-degree: 0%

---


# Spline (Cubique)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icône de nœud](../../../../../../assets/spline-cubic-icon.png "Icône de nœud")

<b>Entrée :</b> Outils Spline Et Tracé > Outils spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Génère une spline unique entre deux points <b>p1 </b> et <b>p2</b> à des emplacements arbitraires.

La trajectoire de la spline est contrôlée par la tangente « out » de <b>p1</b> et la tangente « in » de <b>p2</b>.

</td>
</tr>
</table>

## Connecteurs d’entrée

<b>Aperçu</b> *Niveaux de gris* Aperçu des splines d&#39;entrée sous la forme d&#39;une image en niveaux de gris.

<b>Couleurs splines</b> *Couleur* Les coordonnées des points des splines d&#39;entrée codées dans les couches RVBA d&#39;une image couleur :\
<b> R</b> - Position X\
<b> G</b> - Position Y\
<b> B</b> - Height\
<b>A</b> - Données compressées :\
* Signe : la spline est fermée (négative) ou ouverte (positive);\
* Valeur absolue : Thickness + 1.

<b>Données splines</b> *Couleur* Données supplémentaires des splines d&#39;entrée codées dans les canaux RVBA d&#39;une image couleur.\
<b> R</b> - Tangentes X\
<b> G</b> - Tangentes Y\
<b> B</b> - Inutilisé\
<b> A</b> - Inutilisé

<b>Quantité de spline</b> *Nombre entier* Nombre de splines d&#39;entrée.

## Connecteurs de sortie

<b>Aperçu</b> *Niveaux de gris* L’aperçu des splines de sortie sous forme d’image en niveaux de gris.

<b>Couleurs splines</b> *Couleur* Les coordonnées des points splines de sortie sont codées dans les couches RVBA d&#39;une image couleur.\
<b>R</b> - Position X\
<b>G</b> - Position Y\
<b>B</b> - Height\
<b>A</b> - Données compressées :\
* Signe : la spline est fermée (négative) ou ouverte (positive);\
* Valeur absolue : Thickness + 1.

<b>Données splines</b> *Couleur* Données supplémentaires des splines de sortie codées dans les canaux RVBA d&#39;une image couleur.\
<b>R</b> - Tangentes X\
<b>G</b> - Tangentes Y\
<b>B</b> - Inutilisé\
<b>A</b> - Inutilisé

<b>Quantité de spline</b> *Nombre entier* Nombre de splines de sortie.

## Paramètres

<b>Inverser la direction</b> *Booléen*\
Inverse la direction de la spline.

<b>Ajouter une spline d&#39;entrée</b> *Booléen*\
Ajoute la spline générée à la fin de la liste des splines connectées aux entrées de <b>spline</b>.

<b>Correction non carrée </b>*Booléenne* Ajustez la position et le thickness des points pour conserver la forme de spline dans des résolutions non carrées.\
Cela a également un impact sur la distribution uniforme.

+++Hauteur
<b>Height de démarrage</b> *Flottant* Ajuste l&#39;height du point p1 où une valeur inférieure signifie un emplacement plus bas ou plus profond.\
Cela a un impact sur l&#39;height de la spline en p1.

<b>Height final</b> *Flottant* Ajuste l&#39;height du point p2 où une valeur inférieure signifie un emplacement plus bas ou plus profond.\
Cela a un impact sur le thickness de la spline à p2.

<b>Height de tangence automatique</b> *Booléen* définit automatiquement l&#39;height des tangentes de spline à interpoler linéairement de l&#39;Height Début à l&#39;Height Fin.

<b>Height tangent p1</b> *Flottant* (disponible lorsque « Height de tangente automatique » a la valeur True)\
Règle l’height de la tangente de « sortie » du point p1 où une valeur inférieure signifie un emplacement plus bas ou plus profond.\
Cela a un impact sur l&#39;height le long de la spline lorsqu&#39;il s&#39;éloigne de p1.

<b>Height tangent p2</b> *Flottant* (disponible lorsque « Height de tangente automatique » a la valeur True)\
Règle l’height de la tangente « entrée » du point p2 où une valeur inférieure signifie un emplacement plus bas ou plus profond.\
Cela a un impact sur l&#39;height le long de la spline lorsqu&#39;il s&#39;éloigne de p2.

+++

+++Épaisseur
<b>Démarrer le Thickness</b> *Flottant* Ajuste le thickness du point p1.\
Cela a un impact sur le thickness de la spline à p1.\
Remarque : Thickness est utilisé par des nœuds Spline spécifiques.

<b>Fin de Thickness</b> *Flottant* Ajuste le thickness du point p2.\
Cela a un impact sur le thickness de la spline à p2.\
Remarque : Thickness est utilisé par des nœuds Spline spécifiques.

<b>Thickness tangent automatique</b> *Booléen* Définit automatiquement le thickness des tangentes de spline à interpoler linéairement du Thickness de début au Thickness de fin.\
Remarque : Thickness est utilisé par des nœuds Spline spécifiques.

<b>Thickness tangent p1</b> *Flottant* (disponible lorsque « Thickness de tangente automatique » a la valeur True)\
Ajuste le thickness de la tangente de sortie du point p1.\
Cela a un impact sur le thickness le long de la spline lorsqu&#39;il s&#39;éloigne de p1.\
Remarque : Thickness est utilisé par des nœuds Spline spécifiques.

<b>Thickness tangent p2</b> *Flottant* (disponible lorsque « Thickness de tangente automatique » a la valeur True)\
Règle le thickness de la tangente « entrée » du point p2.\
Cela a un impact sur le thickness le long de la spline lorsqu&#39;il s&#39;éloigne de p2.\
Remarque : Thickness est utilisé par des nœuds Spline spécifiques.

+++

+++Coordonnées des points
<b>p1</b> *Float2* Définit la position du point p1 dans l’espace de texture.

<b>p1 Tangente</b> *Float2* Définit la position de la poignée de tangente de sortie du point p1 dans l’espace de texture.

<b>p2</b> *Float2* Définit la position du point p2 dans l’espace de texture.

<b>p2 tangente</b> *Float2* Définit la position de la poignée de tangente « d’entrée » du point p2 dans l’espace de texture.

+++

+++Prévisualiser
<b>Afficher les tangentes</b> *Booléen* Affiche la tangente de sortie du point p1 et la tangente d’entrée du point p2 dans la sortie Aperçu.

<b>Afficher l&#39;assistant de direction</b> *Booléen* Affiche un point au début de la spline et une flèche à sa fin dans la sortie Aperçu.

<b>Quantité de segments</b> *Nombre entier* Ajuste le nombre de segments utilisés pour dessiner la visualisation de la spline dans la sortie d&#39;aperçu.\
Plus la valeur est élevée, plus la ligne est lisse.

<b>Thickness (px)</b> *Flottant* Ajuste le thickness en pixels de la visualisation de la spline dans la sortie Aperçu.

+++

## Exemples

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Exemple de nœud 1](../../../../../../assets/SplineCubic-Variant1.jpg "Exemple de nœud 1")

</td>
<td style="border: 0;" valign="top">

![Exemple de nœud 2](../../../../../../assets/SplineCubic-Variant2.jpg "Exemple de nœud 2")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Exemple de nœud 3](../../../../../../assets/SplineCubic-Demo.gif "Exemple de nœud 3")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
