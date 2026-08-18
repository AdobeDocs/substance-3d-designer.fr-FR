---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-circle.html"
breadcrumb-title: ''
description: Utilisez le nœud Cercle spline pour créer des splines circulaires afin de générer des motifs et des formes arrondis.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Circle
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Cercle spline
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '671'
ht-degree: 0%

---


# Cercle spline

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icône de nœud](../../../../../../assets/spline-circle-icon.png "Icône de nœud")

<b>Entrée :</b> Outils Spline Et Tracé > Outils spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Génère une spline unique en forme de cercle.

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

<b>Rayon du cercle</b> *Flotter*\
Ajuste le rayon du cercle dans l’espace de la texture.

<b>Pré-Rotation Du Cercle</b> *Flotter*\
Applique une rotation au cercle de base avant l’application de la propriété Taille.

<b>Taille du cercle</b> *Float2*\
Ajuste la taille horizontale (X) et verticale (Y) du cercle.

<b>Après-Rotation Du Cercle</b> *Flotter*\
Applique une rotation au cercle de base après l’application de la propriété Taille.

<b>Position du cercle</b> *Float2*\
Définit la position du centre du cercle dans l’espace de la texture.

<b>Démarrer le Thickness</b> *Flottant* Ajuste le thickness du point de départ du cercle.\
Ce thickness est interpolé le long de la spline jusqu&#39;au Thickness d&#39;extrémité.\
Remarque : Thickness est utilisé par des nœuds Spline spécifiques.

<b>Fin de Thickness</b> *Flottant* Ajuste le thickness de l’extrémité du cercle.\
Ce thickness est interpolé le long de la spline jusqu&#39;au Thickness Début.\
Remarque : Thickness est utilisé par des nœuds Spline spécifiques.

<b>Height de démarrage</b> *Flottant* Ajuste l’height du point de départ du cercle, où une valeur inférieure signifie un emplacement plus bas ou plus profond.\
Cet height est interpolé le long de la spline jusqu&#39;à l&#39;Height Fin.

<b>Height final</b> *Flottant* Ajuste l’height du point d’extrémité du cercle, où une valeur plus faible signifie un emplacement plus bas ou plus profond.\
Cet height est interpolé le long de la spline à partir de l&#39;Height Début.

<b>Rogner</b> *Float2* Décale les points de départ et d&#39;arrivée de la spline le long du cercle.\
Ces valeurs sont normalisées.

<b>Spirale</b> *Flottant* Déplace le point de départ du cercle de son rayon à son centre.\
La distance depuis le centre est ensuite interpolée le long de la spline jusqu&#39;à l&#39;extrémité de la spline.\
Cette valeur est normalisée.

<b>Virages en spirale</b> *Flottant* Définit le nombre de tours effectués par la spirale autour de son centre.

<b>Puissance en spirale</b> *Flottant* Applique une courbe de puissance à la distance par rapport au centre utilisée pour dessiner la spirale.\
Une valeur supérieure à un signifie qu&#39;une plus grande partie de la spirale reste proche du centre.

<b>Inverser la direction</b> *Booléen*\
Inverse la direction de la spline.

<b>Distribution uniforme</b> *Booléen*\
Lorsque la valeur est True, les points de la spline sont régulièrement espacés du début à la fin.

<b>Ajouter une spline d&#39;entrée</b> *Booléen*\
Ajoute la spline générée à la fin de la liste des splines connectées aux entrées de <b>spline</b>.

<b>Correction non carrée </b>*Booléenne* Ajustez la position et le thickness des points pour conserver la forme de spline dans des résolutions non carrées.\
Cela a également un impact sur la distribution uniforme.

+++Prévisualiser
<b>Afficher l&#39;assistant de direction</b> *Booléen* Affiche un point au début de la spline et une flèche à sa fin dans la sortie Aperçu.

<b>Afficher l&#39;enveloppe de Thickness</b> *Booléen*\
Affiche des lignes supplémentaires sur les thickness de la spline.

<b>Quantité de segments</b> *Nombre entier* Ajuste le nombre de segments utilisés pour dessiner la visualisation de la spline dans la sortie d&#39;aperçu.\
Plus la valeur est élevée, plus la ligne est lisse.

<b>Thickness (px)</b> *Flottant* Ajuste le thickness en pixels de la visualisation de la spline dans la sortie Aperçu.

+++

## Exemples

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Exemple de nœud 1](../../../../../../assets/SplineCircle-Variant1.jpg "Exemple de nœud 1")

</td>
<td style="border: 0;" valign="top">

![Exemple de nœud 2](../../../../../../assets/SplineCircle-Demo.gif "Exemple de nœud 2")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Exemple 3](../../../../../../assets/SplineCircle-Variant2.jpg "Exemple 3")

</td>
<td style="border: 0;" valign="top">

![Exemple 4](../../../../../../assets/SplineCircle-Variant3.jpg "Exemple 4")

</td>
</tr>
</table>
