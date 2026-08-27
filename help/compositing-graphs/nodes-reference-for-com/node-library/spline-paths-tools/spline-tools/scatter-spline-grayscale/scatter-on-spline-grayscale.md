---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/scatter-on-spline-grayscale.html"
breadcrumb-title: ''
description: Utilisez le nœud Dispersion sur niveaux de gris spline pour répartir les éléments en niveaux de gris le long des tracés splines pour les motifs procéduraux.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Scatter on Spline Grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Dispersion sur niveaux de gris spline
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '2812'
ht-degree: 0%

---


# Dispersion sur niveaux de gris spline

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icône de nœud](../../../../../../assets/scatter-on-spline-grayscale-icon.png "Icône de nœud")

<b>Entrée :</b> Outils Spline Et Tracé > Outils spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Trace le ou les motifs spécifiés le long des splines d&#39;entrée sur l&#39;arrière-plan d&#39;entrée.

</td>
</tr>
</table>

Le nœud offre des options de personnalisation avancées pour contrôler la façon dont les motifs sont dispersés.

Certains aspects de la diffusion peuvent être contrôlés à l&#39;aide d&#39;images provenant d&#39;autres nœuds dans le graphique afin de renforcer l&#39;aspect dynamique du résultat.

>[!NOTE]
>
> Voir aussi [Dispersion sur la couleur de la spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/scatter-on-spline-color/scatter-on-spline-color.md).

## Connecteurs d’entrée

<b>Arrière-plan </b>*en niveaux de gris* (principal)Image en niveaux de gris sur laquelle les splines doivent être dessinées.

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

<b>Entrée de motif #</b> *Niveaux de gris* Le(s) motif(s) qui doivent être dispersés le long des splines.

<b>Mappage d&#39;échelle</b> *Niveaux de gris* La carte contrôlant l&#39;échelle des motifs dispersés. L’effet de cette carte est contrôlé par le paramètre Multiplicateur d’entrée de carte d’échelle et est combiné aux autres paramètres du groupe Taille.

<b>Mappage de l&#39;Height</b> *Niveaux de gris* La carte contrôlant l&#39;height des motifs dispersés. L’effet de cette courbe est contrôlé par le paramètre Multiplicateur d’entrée Height et est associé aux autres paramètres Couleur du groupe Couleur.

<b>Mappage de masque</b> *Niveaux de gris* La carte contrôlant le masquage des motifs dispersés. L’effet de cette courbe est contrôlé par le paramètre Seuil de la courbe de transfert du masque et est combiné aux autres paramètres Masque dans le groupe Couleur.

## Connecteurs de sortie

<b>Sortie</b> *Niveaux de gris* Image représentant le ou les motifs dispersés le long de la ou des splines d&#39;entrée sur l&#39;arrière-plan d&#39;entrée.

## Paramètres

<b>Entrée spline</b> *Entier* Méthode de sélection des splines à utiliser pour les motifs de diffusion :
* *Toutes les splines* : utilisez toutes les splines dans la liste d&#39;entrée ;
* *Spline unique* : utilisez uniquement la spline spécifiée à partir de la liste d&#39;entrée ;
* *Plage de splines* : utilisez uniquement les splines de la plage spécifiée à partir de la liste d&#39;entrée.

<b>Index Spline</b> *Nombre entier* (disponible lorsque l&#39;option Entrée spline est définie sur Spline unique) L&#39;index de liste de la spline qui doit être utilisé pour les motifs de diffusion.

<b>Plage de splines</b> *Entier2* (disponible lorsque l&#39;option Entrée spline est définie sur Plage spline)Plage d&#39;index de liste comprenant les splines qui doivent être utilisées pour les motifs de diffusion.

<b>Mode Dispersion</b> *Entier* Méthode de diffusion des motifs le long des splines, qui a un impact sur la quantité de motifs sur chaque spline :
* Quantité de forme : la quantité spécifiée de motifs à espacement régulier est dispersée ;
* Espacement des formes : le nombre de motifs est automatiquement ajusté pour s’adapter à l’espacement régulier spécifié.\
  Dans les deux cas, le premier et le dernier motif se trouvent exactement au début et à la fin de chaque spline respectivement.

<b>Quantité de forme</b> *Nombre entier* (disponible lorsque le mode Dispersion est défini sur Quantité de forme) Quantité de motifs régulièrement espacés le long de chaque spline.

<b>Répartition De La Forme Le Long De La Spline</b> *Nombre entier* (disponible lorsque le mode Dispersion est défini sur Quantité de forme)Méthode de répartition des motifs le long d&#39;une spline :
* *Source* : l&#39;espacement des motifs est influencé par les tangentes des points de spline, où les formes sont plus éloignées à proximité des points avec de longues tangentes ;
* *Uniforme* : les motifs sont régulièrement espacés le long de la spline, quelles que soient ses tangentes et sa trajectoire.

<b>Espacement des formes</b> *Flottant* (disponible lorsque le mode Dispersion est défini sur Espacement de forme ) Distance minimale le long d&#39;une spline selon laquelle les motifs doivent être espacés, tout en atterrissant toujours le premier et le dernier motif respectivement au début et à la fin de chaque spline.

<b>Démarrer</b> *Flottant*<span id="_Hlk135680521"></span> Décale le point à partir du début d&#39;une spline où commence la diffusion. La valeur est la longueur normalisée de chaque spline.

<b>Fin</b> *Flottant* Décale le point à partir du début d&#39;une spline à l&#39;endroit où la diffusion se termine. La valeur est la longueur normalisée de chaque spline.

<b>Pivot De Forme</b> *Float2* Décale le pivot du motif X et Y dans l&#39;espace tangent de la spline.\
En considérant que le pivot est ce qui est placé sur la spline, cela décale efficacement les motifs le long ou perpendiculairement à la spline.\
Remarque : la position des pivots a un impact sur l’effet des paramètres « Échelle » et « Rotation (pivot) ».

+++Motif
<b>Motif</b> *Nombre entier* Le motif qui doit être dispersé le long des splines :\
*- Entrée de motif* : utilisez les motifs fournis pour les entrées « Entrée de motif # » ;\
*- Carré ;
* Disque ;
* Paraboloïde ;
* Bell;
* gaussien ;
* Épine ;
* Pyramide ;
* Brique ;
* Gradation ;
* Vagues ;
* Demi-cloche ;
* Cloche à dorsale;
* Croissant ;
* Capsule ;
* Cône ;
* Graduation w. offset ;
* Hémisphère.*

<b>Numéro d&#39;entrée de motif</b> *Nombre entier* (disponible lorsque « Pattern » est défini sur « Pattern Input »)Sélectionne l&#39;index du motif d&#39;entrée qui doit être diffusé.

<b>Distribution d&#39;entrée de motif</b> *Nombre entier* (disponible lorsque « Pattern » est défini sur « Pattern Input »)Méthode utilisée pour sélectionner lequel des motifs d&#39;entrée doit être dispersé sur une spline donnée :\
*- Aléatoire* : un motif est sélectionné de manière aléatoire ;\
*- le long de la spline* : l&#39;index de motif augmente progressivement le long de la spline ;\
*- Index de motif* : boucle sur l&#39;index des motifs d&#39;entrée le long de chaque spline ;\
*- Index de spline* : passe en boucle sur l&#39;index des motifs d&#39;entrée d&#39;une spline à la suivante dans la liste des splines d&#39;entrée.

<b>Variation de distribution</b> *Flottant* (disponible lorsque l&#39;option Distribution d&#39;entrée de motif est définie sur le long de la spline) augmente ou diminue de manière aléatoire l&#39;index sélectionné des motifs sur la spline.

<b>Remplacer le premier motif</b> *Booléen* Sélectionnez manuellement l&#39;index du motif qui doit être placé au début de chaque spline.

<b>Premier index d&#39;entrée de motif</b> *Nombre entier* (disponible lorsque l&#39;option Remplacer le premier motif est définie sur Vrai) L&#39;index du motif qui doit être placé au début de chaque spline.

<b>Remplacer le dernier motif</b> *Booléen* Sélectionnez manuellement l&#39;index du motif qui doit être placé à l&#39;extrémité de chaque spline.

<b>Dernier index d&#39;entrée de motif</b> *Nombre entier* (disponible lorsque l&#39;option Remplacer le dernier motif est définie sur Vrai)Index du motif qui doit être placé à la fin de chaque spline.

+++

+++Doublons
<b>Mode de distribution</b> *Entier* Méthode utilisée pour placer les motifs dupliqués :\
*- Linéaire* : les doublons sont espacés de manière régulière le long de la normale de la spline à partir de l&#39;emplacement d&#39;origine du motif ;\
*- Circulaire* : les copies sont disposées le long d&#39;un cercle virtuel centré sur la spline à l&#39;emplacement d&#39;origine du motif.

<b>Quantité de doublons</b> *Nombre entier* Nombre de motifs dupliqués.

<b>Décalage</b> *Float2* (disponible lorsque le mode Distribution est défini sur Linéaire)Applique un décalage aux positions des duplicatas le long de la tangente (parallèle) et de la normale (perpendiculaire) de la spline.\
Les copies situées sur les côtés opposés de la spline sont déplacées dans des directions opposées.

<b>Décalage au centre</b> *Float2* (disponible lorsque le mode de distribution est défini sur Linéaire)Applique un décalage aux copies le long de la spline sur X (parallèle) et Y (perpendiculaire).

<b>Angle de répartition</b> *Flotter* (disponible lorsque le mode de distribution est défini sur Circulaire)Arc du cercle virtuel le long duquel les doublons sont distribués, comme l&#39;angle de cet arc où 1 est le cercle entier.

<b>Distance de décalage</b> *Flottant* (disponible lorsque le « Mode de distribution » est défini sur « Circulaire »)Le rayon du cercle virtuel le long duquel les doublons sont distribués.

<b>Rotation</b> *Flottant* Fait pivoter le cercle virtuel le long duquel les doublons sont distribués.

<b>Atténuation Du Début/Fin Du Décalage</b> *Float2* Tient compte de la distance entre le milieu et le début et la fin de la spline lors de l&#39;application de décalages aux duplicatas.\
Cela signifie que les décalages sont réduits pour les doublons situés plus près des extrémités d&#39;une spline.

<b>Décaler l&#39;atténuation par Thickness</b> *Variation* Les facteurs dans le thickness de la spline lors de l&#39;application de décalages à des doublons.\
Cela signifie que les décalages sont réduits pour les doublons sur une partie d&#39;une spline avec un thickness inférieur.

+++

+++Taille
<b>Mode Taille</b> *Entier* Méthode de définition de la taille des motifs diffusés :\
*- Normal* : la taille est contrôlée uniformément à l&#39;aide d&#39;un paramètre « Scale » global ;\
*- Utiliser le Thickness de la spline* : la taille dépend du thickness de la spline.

<b>Le Thickness Affecte</b> *Nombre entier* (disponible lorsque le mode Taille est défini sur Utiliser le Thickness de la spline)Spécifie quel axe de l&#39;échelle d&#39;un motif doit être piloté par le thickness de la spline :
* X &amp; Y : le Thickness est multiplié par rapport à la taille dans les axes X et Y ;\
  <span id="_Hlk135741125"></span>- X : le Thickness est multiplié par rapport à la taille sur l&#39;axe X uniquement ;
* Y : le Thickness est multiplié par rapport à la taille sur l’axe Y uniquement.\
  Lorsqu’elle n’est pas multipliée, l’échelle d’origine du motif correspond à la totalité de l’image.\
  Cela signifie qu’en mode « X », la taille sur l’axe Y correspond à l’intégralité de l’image et doit être modifiée à l’aide du paramètre Taille. Il en est de même pour la taille sur l’axe X lors de l’utilisation du mode Y.

<b>Taille</b> *Float2* Taille d’origine des motifs en X et en Y avant que d’autres réglages ne soient effectués par d’autres paramètres.

<b>Taille aléatoire</b> *Flottant 2* Applique un multiplicateur aléatoire jusqu&#39;à la valeur spécifiée pour réduire la taille des motifs dans X et Y.

<b>Échelle de Thickness</b> *Flottant* (disponible lorsque le mode Taille est défini sur Utiliser le Thickness de la spline)Multiplicateur supplémentaire pour l&#39;échelle des motifs lorsque le thickness de la spline le pilote.

<b>Échelle</b> *Flottant* (disponible lorsque le mode Taille est défini sur Normal) Contrôle global de la taille de tous les motifs, où 1 correspond à la plage complète de l’image.\
La mise à l’échelle est appliquée par rapport au pivot d’un motif. La position de pivot peut être décalée à l’aide du paramètre « Shape Pivot ».

<b>Échelle aléatoire</b> *Flottant* Applique un multiplicateur aléatoire jusqu&#39;à la valeur spécifiée pour réduire la taille des motifs.

<b>Multiplicateur d&#39;entrée de mappage d&#39;échelle</b> *Flottant* Contrôle l’intensité de l’entrée de la carte d’échelle. Cette carte agit comme un multiplicateur pour la taille actuelle des motifs.\
L’effet de cette carte est combiné aux autres paramètres du groupe Taille.

<b>Mode D&#39;Échantillonnage D&#39;Entrée À L&#39;Échelle</b> *Espace de texture* La méthode de mappage des valeurs de la carte d&#39;échelle aux splines :\
*- Espace de texture* : les valeurs sont appliquées aux splines où elles se trouveraient si elles étaient placées dans une texture à l&#39;aide des coordonnées UV de la texture. Cela applique effectivement la valeur aux cannelures « en place »;\
*- Horizontal le long de la spline* : les valeurs sont appliquées directement aux coordonnées des splines codées (voir Entrée des cordons de spline), où chaque ligne est appliquée à une spline différente de haut en bas ;\
*- Heure. le long de la spline (rand. offset X)* : les valeurs sont appliquées directement aux coordonnées des splines codées (voir entrée Spline Coords), avec un décalage horizontal aléatoire dans la carte d&#39;échelle pour chaque spline (c&#39;est-à-dire chaque ligne dans Spline Coords);\
*- Heure. le long de la spline (rand. décalage Y)* : les valeurs sont appliquées directement aux coordonnées des splines codées (voir Entrée des cœurs de spline), avec un décalage vertical aléatoire dans la carte d&#39;échelle pour chaque spline (c&#39;est-à-dire chaque ligne dans les cœurs de spline).

<b>Atténuation Début/Fin</b> *Float2* Tient compte de la distance entre le milieu de la spline et ses extrémités lors de la mise à l&#39;échelle des motifs.\
Cela signifie que la taille est réduite pour les motifs situés plus près des extrémités d’une spline.

+++

+++Position
<b>Décalage local</b> *Float2* Applique un décalage aux positions des motifs le long de la tangente (parallèle) et de la normale (perpendiculaire) de la spline.

<b>Décalage local aléatoire</b> *Float2* Applique un décalage aléatoire supplémentaire aux positions des motifs le long de la tangente (parallèle) et de la normale (perpendiculaire) de la spline.

<b>Décalage local au centre aléatoire</b> *Float2* Décale le centre du décalage aléatoire appliqué par le paramètre Aléatoire de décalage local le long de la tangente (parallèle) et de la normale (perpendiculaire) de la spline.

<b>Atténuation du début/de la fin du décalage local</b> *Float2* Tient compte de la distance entre le milieu et le début et la fin de la spline lors de l&#39;application de décalages de position aux motifs.\
Cela signifie que les décalages sont réduits pour les motifs situés plus près des extrémités d’une spline.

<b>Atténuation du décalage local par Thickness</b> *Variation* Les facteurs dans le thickness de la spline lors de l&#39;application de décalages aux motifs.\
Cela signifie que les décalages sont réduits pour les doublons sur une partie d&#39;une spline avec un thickness inférieur.

<b>Décalage sur la spline</b> *Flottant* Applique un décalage de position aux motifs le long des splines.

<b>Décalage aléatoire sur la spline</b> *Flottant* Applique un décalage de position supplémentaire aux motifs le long des splines.

+++

+++Rotation
<b>Aligner avec la tangente</b> *Booléen* Fait pivoter les motifs pour qu&#39;ils correspondent à la direction de la spline à leur emplacement.

<b>Rotation (Pivot)</b> *Flottant* Fait pivoter les motifs autour de leurs pivots.\
La position de pivot peut être décalée à l’aide du paramètre « Shape Pivot ».

<b>Rotation Aléatoire (Pivot)</b> *Flottant* Applique une rotation aléatoire supplémentaire aux motifs autour de leurs pivots.\
La position de pivot peut être décalée à l’aide du paramètre « Shape Pivot ».

<b>Rotation aléatoire au centre (pivot)</b> L&#39;option *Flotter* Fait pivoter autour des pivots du motif le centre des rotations aléatoires appliquées par le paramètre Rotation aléatoire.

<b>Rotation (au centre)</b> *Flottant* Fait pivoter les motifs autour de leur centre.

<b>Rotation aléatoire (au centre)</b> *Flottant* Applique une rotation aléatoire supplémentaire aux motifs autour de leur centre.

<b>Centre aléatoire de rotation (centre)</b> *Flottant* Fait pivoter autour du centre du motif le centre des rotations aléatoires appliquées par le paramètre Rotation aléatoire.

+++

+++Couleur
<b>Mode de fusion</b> *Entier* Méthode de fusion des couleurs des motifs avec à la fois l’arrière-plan et d’autres motifs qui se chevauchent :\
*- Max* : utilisez la couleur la plus lumineuse ;\
*- Ajouter* : ajoutez les couleurs ensemble.

<b>Couleur de base de la forme</b> *Flottant* La couleur de base des motifs.

<b>Multiplicateur de couleur de base de la forme</b> *Flottant* L’intensité de la couleur de base de la forme des motifs.\
Remarque : la couleur de sortie est le résultat pondéré de tous les multiplicateurs de couleurs.

<b>Multiplicateur de Thickness spline</b> *Variable* Intensité par laquelle la couleur de chaque motif est multipliée par rapport au thickness de la spline à son emplacement.\
Remarque : la couleur de sortie est le résultat pondéré de tous les multiplicateurs de couleurs.

<b>Multiplicateur d&#39;index de forme</b> *Variable* Intensité par laquelle la couleur de chaque motif est multipliée par rapport à son index normalisé.\
Remarque : la couleur de sortie est le résultat pondéré de tous les multiplicateurs de couleurs.

<b>Mode Height Hémisphère</b> *Nombre entier* (disponible lorsque « Motif » est défini sur « Hémisphère »)Effet de l&#39;height de la spline sur un motif hémisphérique dispersé sur celle-ci :\
*- Décalage* : l&#39;height spline est ajouté à l&#39;height de l&#39;hémisphère ;\
*- Échelle* : l&#39;height de la spline est multiplié par rapport à l&#39;height de l&#39;hémisphère.

<b>Multiplicateur d&#39;Height spline</b> *Variable* Intensité par laquelle la couleur de chaque motif est multipliée par rapport à l&#39;height de la spline à son emplacement.\
Remarque : la couleur de sortie est le résultat pondéré de tous les multiplicateurs de couleurs.

<b>Multiplicateur d&#39;échelle de forme</b> *Variable* Intensité par laquelle la couleur de chaque motif est multipliée par rapport à son échelle.\
Remarque : la couleur de sortie est le résultat pondéré de tous les multiplicateurs de couleurs.

<b>Luminance aléatoire</b> *Flottant* Applique un multiplicateur aléatoire jusqu&#39;à la valeur spécifiée pour diminuer la luminance des motifs.\
Remarque : la couleur de sortie est le résultat pondéré de tous les multiplicateurs de couleurs.

<b>Multiplicateur d&#39;entrée Height</b> *Flottant* Contrôle l&#39;intensité de l&#39;entrée de la carte d&#39;Height. Cette map agit comme un multiplicateur pour la luminance actuelle des motifs.\
L’effet de cette courbe est combiné aux autres paramètres du groupe « Couleur ».\
Remarque : la couleur de sortie est le résultat pondéré de tous les multiplicateurs de couleurs.

<b>Mode d&#39;échantillonnage d&#39;entrée de mappage d&#39;Height</b> *Entier* Méthode de mappage des valeurs de l&#39;Height Mapper sur les splines :\
*- Espace de texture* : les valeurs sont appliquées aux splines où elles se trouveraient si elles étaient placées dans une texture à l&#39;aide des coordonnées UV de la texture. Cela applique effectivement la valeur aux cannelures « en place »;\
*- Horizontal le long de la spline* : les valeurs sont appliquées directement aux coordonnées des splines codées (voir Entrée des cordons de spline), où chaque ligne est appliquée à une spline différente de haut en bas ;\
*- Heure. le long de la spline (rand. offset X)* : les valeurs sont appliquées directement aux coordonnées des splines codées (voir entrée Spline Coords), avec un décalage horizontal aléatoire dans la carte d&#39;échelle pour chaque spline (c&#39;est-à-dire chaque ligne dans Spline Coords);\
*- Heure. le long de la spline (rand. décalage Y)* : les valeurs sont appliquées directement aux coordonnées des splines codées (voir Entrée des cœurs de spline), avec un décalage vertical aléatoire dans la carte d&#39;échelle pour chaque spline (c&#39;est-à-dire chaque ligne dans les cœurs de spline).

<b>Masquer aléatoirement</b> *Flottant* Ajuste la plage du masquage aléatoire des motifs, où 0 signifie qu’aucun motif n’est masqué et 1 signifie que tous les motifs le sont.

<b>Seuil de mappage de masque</b> Les valeurs *flottantes* du mappage de masque inférieures à cette valeur seuil sont traitées en noir, tandis que les valeurs supérieures au seuil sont traitées en blanc.\
Cela signifie que tous les motifs dans les zones de la carte de masque situées en dessous de cette valeur seront masqués.

<b>Mode D&#39;Échantillonnage D&#39;Entrée De Mappage De Masque</b> *Nombre entier* Méthode de mappage des valeurs de la carte de masque aux splines :\
*- Espace de texture* : les valeurs sont appliquées aux splines où elles se trouveraient si elles étaient placées dans une texture à l&#39;aide des coordonnées UV de la texture. Cela applique effectivement la valeur aux cannelures « en place »;\
*- Horizontal le long de la spline* : les valeurs sont appliquées directement aux coordonnées des splines codées (voir Entrée des cordons de spline), où chaque ligne est appliquée à une spline différente de haut en bas ;\
*- Heure. le long de la spline (rand. offset X)* : les valeurs sont appliquées directement aux coordonnées des splines codées (voir entrée Spline Coords), avec un décalage horizontal aléatoire dans la carte d&#39;échelle pour chaque spline (c&#39;est-à-dire chaque ligne dans Spline Coords);\
*- Heure. le long de la spline (rand. décalage Y)* : les valeurs sont appliquées directement aux coordonnées des splines codées (voir Entrée des cœurs de spline), avec un décalage vertical aléatoire dans la carte d&#39;échelle pour chaque spline (c&#39;est-à-dire chaque ligne dans les cœurs de spline).

<b>Inverser la carte de masque</b> *Booléen* Inverse les valeurs de la carte de masque à l&#39;aide d&#39;une opération « Une moins » (1 - x).

<b>Inversion de masque</b> *Booléen* Inverse le masquage des motifs.

+++

<b>Correction Non Carrée</b> *Booléen* Ajustez la position des points pour conserver la forme de la spline dans des résolutions autres que carrées.

## Exemples

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/ScatterOnSplineGrayscale-Variant1-Before.jpg" alt="ScatterOnSplineGrayscale-Variant1-Before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="../../../../../../assets/ScatterOnSplineGrayscale-Variant1-After.jpg" alt="ScatterOnSplineGrayscale-Variant1-After">
      <br><i>Après</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/ScatterOnSplineGrayscale-Variant2-Before.jpg" alt="ScatterOnSplineGrayscale-Variant2-Before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="../../../../../../assets/ScatterOnSplineGrayscale-Variant2-After.jpg" alt="ScatterOnSplineGrayscale-Variant2-After">
      <br><i>Après</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Exemple de nœud 2](../../../../../../assets/ScatterOnSplineGrayscale-Demo.gif "Exemple de nœud 2")

</td>
<td style="border: 0;" valign="top">

![Démonstration de nœud 2](../../../../../../assets/ScatterOnSplineGrayscale-Demo2.gif "Démonstration de nœud 2")

</td>
</tr>
</table>
