---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-poly-quadratic.html"
breadcrumb-title: ''
description: Utilisez le nœud Polyquadratique spline pour créer des splines quadratiques complexes avec plusieurs points de contrôle.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline (Poly Quadratic)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Spline (polyquadratique)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '1147'
ht-degree: 0%

---


# Spline (polyquadratique)

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icône de nœud](../../../../../../assets/spline-poly-quadratic-icon.png "Icône de nœud")

<b>Entrée :</b> Outils Spline Et Tracé > Outils spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Génère une spline sur plusieurs points. La quantité et les emplacements de ces points peuvent être arbitraires ou rassemblés à partir d&#39;un nœud [Liste de points](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/point-list/point-list.md).

</td>
</tr>
</table>

La trajectoire de la spline peut être lissée à partir de ses points intermédiaires, en ce sens que chaque point intermédiaire est le point de rencontre des tangentes « out » et « in » de ses voisins.

## Connecteurs d’entrée

<b>Aperçu</b> *Niveaux de gris* Aperçu des splines d&#39;entrée sous la forme d&#39;une image en niveaux de gris.

<b>Couleurs splines</b> *Couleur* Les coordonnées des points des splines d&#39;entrée codées dans les couches RVBA d&#39;une image couleur :\
<b> R</b> - Position X\
<b> G</b> - Position Y\
<b> B</b> - Height\
<b> A</b> - Données compressées :\
        * Signe : la spline est fermée (négative) ou ouverte (positive);\
        * Valeur absolue : Thickness + 1.

<b>Données splines</b> *Couleur* Données supplémentaires des splines d&#39;entrée codées dans les canaux RVBA d&#39;une image couleur.\
<b> R</b> - Tangentes X\
<b> G</b> - Tangentes Y\
<b> B</b> - Inutilisé\
<b> A</b> - Inutilisé

<b>Quantité de spline</b> *Nombre entier* Nombre de splines d&#39;entrée.

<b>Aperçu des points </b>*en niveaux de gris* Aperçu des points sous forme d’image en niveaux de gris.

<b>Liste des points d&#39;entrée</b> *Couleur* (disponible lorsque l&#39;option Utiliser la liste des points d&#39;entrée a la valeur True)\
Liste des points codés dans les couches RVBA d’une image couleur :\
    <b>R</b> - Position X\
    <b>G</b> - Position Y\
    <b>B</b> - Height\
    <b>A</b> - Données compressées :\
        * Partie entière : Smoothness ;\
        * Fraction : Thickness.

<b>Numéro De Point</b> *Nombre entier* (disponible lorsque l&#39;option Utiliser la liste des points d&#39;entrée a la valeur True)\
Nombre de points.

>[!IMPORTANT]
>
> Les connecteurs <b>Liste de points</b> et <b>Numéro de point</b> ne sont *pas compatibles* avec les connecteurs <b>Cordon spline</b>, <b>Données spline</b> et <b>Quantité spline</b>, car ils reposent sur des données différentes.

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

<b>Quantité De Points</b> *Nombre entier* Nombre arbitraire de points utilisés pour construire la spline.

<b>Mode de connexion Spline d&#39;entrée</b> *Entier* Méthode utilisée pour connecter les splines d&#39;entrée :\
*- Auto:* La fin de la dernière spline d&#39;entrée est connectée au début de la spline générée, et la fin de la spline générée est connectée au début de la première spline d&#39;entrée ;\
*- Manuel :* Vous pouvez spécifier quelles splines d&#39;entrée doivent être connectées aux extrémités de la spline générée et où ces connexions doivent atterrir sur les splines d&#39;entrée.

<b>Fermer la spline</b> *Booléen* Contrôle si le point d&#39;extrémité de la spline doit être connecté à son point de départ.\
Le lissage appliqué à la spline aux points de départ et d&#39;arrivée est spécifié par les valeurs de Smoothness de ces points.

<b>Inverser la direction</b> *Booléen*\
Inverse la direction de la spline.

<b>Utiliser la liste des points d&#39;entrée</b> *Booléen* Utilisez la liste de points fournie pour les connecteurs d&#39;entrée Liste de points d&#39;entrée et Numéro de point au lieu d&#39;une liste arbitraire de points.\
La liste de points peut être fournie par un nœud [Liste de points](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/point-list/point-list.md).

<b>Connecter le démarrage à la spline d&#39;entrée</b> *Booléen* Lorsque la valeur est True, le début de la spline générée est connecté au dernier point de la dernière spline dans les splines d&#39;entrée.

<b>Démarrer l&#39;index spline de connexion</b> *Nombre entier* (disponible lorsque le mode de connexion de spline d&#39;entrée est défini sur Manuel et le mode de connexion Démarrer sur spline d&#39;entrée est défini sur Vrai) L&#39;index de la spline d&#39;entrée qui doit être connectée au début de la spline générée.

<b>Démarrer la position de connexion</b> *Flottant* (disponible lorsque le mode de connexion de spline d&#39;entrée est défini sur Manuel et que le mode de connexion Démarrer sur spline d&#39;entrée est défini sur Vrai)Position sur la spline d&#39;entrée sélectionnée où la connexion au début de la spline générée doit atterrir.\
Cette valeur correspond à la longueur normalisée de la spline d&#39;entrée sélectionnée.

<b>Connecter la fin à la spline d&#39;entrée</b> *Booléen* Lorsque la valeur est True, l&#39;extrémité de la spline générée est connectée au premier point de la première spline dans les splines d&#39;entrée.

<b>Fin de l&#39;index spline de connexion</b> *Nombre entier* (disponible lorsque le mode de connexion de la spline d&#39;entrée est défini sur Manuel et le mode de connexion Fin à la spline d&#39;entrée est défini sur Vrai)Index de la spline d&#39;entrée qui doit être connectée à la fin de la spline générée.

<b>Terminer la position de connexion</b> *Flottant* (disponible lorsque le mode de connexion de spline d&#39;entrée est défini sur Manuel et que le mode de connexion Fin à spline d&#39;entrée est défini sur Vrai) Position sur la spline d&#39;entrée sélectionnée où la connexion à l&#39;extrémité de la spline générée doit atterrir.\
Cette valeur correspond à la longueur normalisée de la spline d&#39;entrée sélectionnée.

<b>Distribution uniforme</b> *Booléen*\
Lorsque la valeur est True, les points de la spline sont régulièrement espacés du début à la fin.

<b>Ajouter une spline d&#39;entrée</b> *Booléen*\
Ajoute la spline générée à la fin de la liste des splines connectées aux entrées de <b>spline</b>.

<b>Correction non carrée </b>*Booléenne* Ajustez la position et le thickness des points pour conserver la forme de spline dans des résolutions non carrées.\
Cela a également un impact sur la distribution uniforme.

<b>Ajustement du Smoothness global</b> *Flottant* Applique un décalage uniforme à la valeur de smoothness de tous les points.\
La valeur de smoothness résultante est fixée à la plage [0;1].

+++Propriétés des points
<b>p# Propriétés</b> *Float3* Définit les propriétés du point p#.\
*- Height :* ajuste l&#39;height du point où une valeur inférieure signifie un emplacement plus bas ou plus profond ;\
*- Smoothness :* décale le début du lissage de la spline à p#, où une valeur de 0 entraîne une trajectoire dure et 1 une trajectoire entièrement lisse ;\
*- Thickness :* ajuste le thickness de la spline à p#. Le thickness est utilisé par des nœuds Spline spécifiques.

+++

+++Coordonnées des points
<b>p#</b> *Float2* Définit la position du point p# dans l’espace de texture.

+++

+++Prévisualiser
<b>Afficher les tangentes</b> *Booléen* Affiche les tangentes des points p1 et p3 à p2 dans la sortie d’aperçu.

<b>Afficher l&#39;assistant de direction</b> *Booléen* Affiche un point au début de la spline et une flèche à sa fin dans la sortie Aperçu.

<b>Afficher l&#39;enveloppe de Thickness</b> *Booléen*\
Affiche des lignes supplémentaires sur les thickness de la spline.

<b>Afficher le libellé des points</b> *Booléen*\
Pour chaque point, affiche le nom du point en regard de celui-ci dans la sortie « Aperçu ».

<b>Taille de l&#39;étiquette des points</b> *Float* (disponible lorsque « Afficher l&#39;étiquette des points » est défini sur « Vrai »)\
Taille du libellé de chaque point dans l’espace de la texture, où 0,1 correspond à un dixième de la largeur de la texture.

<b>Afficher les points</b> *Booléen*\
Affiche les points de contrôle de la spline.

<b>Taille Des Points</b> *Float* (disponible lorsque « Afficher les points » est défini sur « Vrai »)\
Rayon des points dans l’espace de la texture, où 0,1 correspond à un dixième de la largeur de la texture.

<b>Quantité de segments</b> *Nombre entier* Ajuste le nombre de segments utilisés pour dessiner la visualisation de la spline dans la sortie d&#39;aperçu.\
Plus la valeur est élevée, plus la ligne est lisse.

<b>Thickness (px)</b> *Flottant* Ajuste le thickness de la visualisation de la spline en pixels dans la sortie d&#39;aperçu.

+++

## Exemples

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplinePolyQuadratic-Variant1-Before.jpg" alt="SplinePolyQuadrique-Variant1-Before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplinePolyQuadratic-Variant1-After.jpg" alt="SplinePolyQuadrique-Variant1-After">
      <br><i>Après</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![Exemple de nœud 2](../../../../../../assets/SplinePolyQuadratic-Demo.gif "Exemple de nœud 2")

</td>
</tr>
</table>

</td>
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
