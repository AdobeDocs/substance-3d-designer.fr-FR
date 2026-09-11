---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/tile-random-2.html"
breadcrumb-title: ''
description: Utilisez le nœud Mosaïque aléatoire 2 pour créer des motifs de mosaïque aléatoires avec des commandes de variation avancées dans Substance 3D Designer.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Tile Random 2
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Mosaïque aléatoire 2
user-guide-description: ''
user-guide-title: ''
source-git-commit: 79916cdb133abb1a43d11012c9d23c3c6d27b079
workflow-type: tm+mt
source-wordcount: '1308'
ht-degree: 0%

---


# Mosaïque aléatoire 2

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/tilerandom2.jpg){width="200px"}

<b>Entrée :</b> Générateurs De Textures > Motifs

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Le nœud **Tile Random 2** génère des carreaux adjacents de tailles aléatoires et de rapports height/largeur.

La grille peut être modifiée en *inclinant* de manière aléatoire les côtés des formes pour séparer les angles.

Les formes peuvent être ajustées avec des options de *mise à l&#39;échelle*, de *biseautage*, d&#39;*arrondi des angles*, ainsi que de *rotation déformée*.

Ces réglages peuvent être contrôlés par des *maps d&#39;entrée*.

Une sortie dédiée vous permet d&#39;entrer les **UV** de la forme en **Flood Fill à (...)** pour appliquer une variation supplémentaire.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Mappage aléatoire des tailles</b> <i>Niveaux de gris</i> | Image d&#39;entrée en niveaux de gris qui contrôle l’échelle aléatoire des formes.<br><br>Son impact est contrôlé par le paramètre <b>Multiplicateur de Map d&#39;entrée aléatoire</b>. |
| <b>Carte Inclinée Aléatoire</b> <i>Niveaux de gris</i> | Image d&#39;entrée en niveaux de gris qui contrôle l’inclinaison aléatoire des formes.<br><br>Son impact est contrôlé par le paramètre <b>Multiplicateur de Map d&#39;entrée oblique aléatoire</b>. |
| <b>Courbe De Rayon D&#39;Arrondi</b> <i>Niveaux de gris</i> | Image d&#39;entrée en niveaux de gris qui contrôle le rayon des angles arrondis des formes.<br><br>Son impact est contrôlé par le multiple de Map d&#39;entrée de rayon d&#39;<b>angles arrondis</b>. paramètre. |
| <b>Map distance en biseau</b> <i>Niveaux de gris</i> | Image d&#39;entrée en niveaux de gris qui contrôle le biseautage des formes.<br><br>Son impact est contrôlé par la <b>Map d&#39;entrée de distance en biseau Mult.</b> paramètre. |
| <b>Mappage de masque</b> <i>Niveaux de gris</i> | Image d&#39;entrée en niveaux de gris qui contrôle le masquage des formes.<br><br>Son impact est contrôlé par les paramètres <b>Début de l&#39;entrée de mappage de masque</b> et <b>Fin de l&#39;entrée de mappage de masque</b>. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Quantité X</b> <i>Entier</i> | Nombre de cellules sur l&#39;axe <b>X</b>. |
| <b>Quantité Y</b> <i>Entier</i> | Nombre de cellules sur l&#39;axe <b>Y</b>. |
| <b>Taille</b> |  |
| <b>Multiplicateur De Taille Aléatoire</b> <i>Flottant</i> | Applique un réglage <i>global</i> à l&#39;intensité de la mise à l&#39;échelle aléatoire. |
| <b>Multiplicateur De Map d&#39;entrée Aléatoire</b> <i>Flottant</i> | Règle l&#39;intensité de la mise à l&#39;échelle aléatoire à l&#39;aide des valeurs <i>échantillonnées</i> à partir de l&#39;entrée <b>Mappage de taille aléatoire</b>. |
| <b>Taille Aléatoire X</b> <i>Flottant</i> | Règle l&#39;intensité de la mise à l&#39;échelle aléatoire sur l&#39;axe <b>X</b> <i>uniquement</i>. |
| <b>Taille aléatoire Y</b> <i>Flottant</i> | Règle l&#39;intensité de la mise à l&#39;échelle aléatoire sur l&#39;axe <b>Y</b> <i>uniquement</i>. |
| <b>Distribution aléatoire des tailles</b> <i>Entier</i> | Contrôle la méthode de distribution des valeurs de mise à l&#39;échelle aléatoire :<br><br>- <i>Uniforme</i> : l&#39;échelle aléatoire est appliquée de <i>la même manière</i> sur toutes les cellules<br>- <i>Bruit bleu</i> : l&#39;échelle aléatoire est <i>ajustée</i> à l&#39;aide d&#39;un motif de bruit bleu |
| <b>Aspect de la forme - Transforme</b> |  |
| <b>Thickness d&#39;interstice</b> <i>Flottant</i> | Ajuste le thickness de l’espace entre les formes. Il est <i>égal pour toutes</i> formes. |
| <b>Multiplicateur De Position Aléatoire</b> <i>Flottant</i> | Applique un décalage de position aléatoire à la forme jusqu&#39;à ce qu&#39;elle <i>rencontre la bordure de sa cellule</i>. |
| <b>Rayon D&#39;Arrondi</b> <i>Flottant</i> | Ajuste le <i>rayon</i> des angles arrondis des formes. Une valeur de <b>0</b> signifie qu&#39;aucun arrondi n&#39;est appliqué.<br><br><i>Remarque</i> : cet effet ne peut pas être appliqué lorsque le paramètre <b>Activer par contrôle de biseau d&#39;Axe</b> est défini sur <i>Vrai</i>. |
| <b>Map d&#39;entrée de rayon d&#39;arrondi mult.</b> <i>Flottant</i> | Règle l&#39;intensité de l&#39;impact de la map d&#39;entrée de <b>courbe de transfert de rayon des angles arrondis</b> sur le rayon des angles arrondis.<br><br>La carte agit comme un multiplicateur <i>par pixel</i> pour le paramètre <b>Rayon d&#39;arrondi</b>.<br><br><i>Remarque</i> : cet effet ne peut pas être appliqué lorsque le paramètre <b>Activer par contrôle de biseau d&#39;Axe</b> est défini sur <i>Vrai</i>. |
| <b>Multiplicateur d&#39;échelle</b> <i>Flottant</i> | Ajuste la taille de chaque forme, en tant que proportion de la <i>zone de sa cellule</i>. |
| <b>Échelle aléatoire</b> <i>Flottant</i> | Règle l&#39;intensité selon laquelle une échelle aléatoire est appliquée à la forme <i>each</i>. |
| <b>Rotation</b> <i>Flottant</i> | Fait pivoter les formes dans leurs cellules en déplaçant chaque <i>coin</i> vers son <i>voisin</i> le long de la bordure de la cellule.<br><br>Cette méthode entraîne l&#39;application d&#39;une certaine quantité de <i>distorsion</i> et de <i>mise à l&#39;échelle</i> à la forme lors de sa rotation. |
| <b>Rotation aléatoire</b> <i>Flottant</i> | Règle l’intensité selon laquelle une rotation aléatoire est appliquée à chaque forme.<br><br>La méthode de rotation est décrite dans le paramètre <b>Rotation</b>. |
| <b>Position aléatoire des angles</b> <i>Flottant</i> | Déforme les formes en appliquant une quantité aléatoire de <i>décalage</i> à chacun de leurs <i>coins</i> le long de la bordure de leur cellule. |
| <b>Inclinaison</b> |  |
| <b>Multiplicateur aléatoire d&#39;inclinaison</b> <i>Flottant</i> | Applique un réglage <i>global</i> à l&#39;intensité de l&#39;inclinaison aléatoire. |
| <b>Multiplicateur aléatoire de Map d&#39;entrée d&#39;inclinaison</b> <i>Flottant</i> | Règle l&#39;intensité de l&#39;inclinaison aléatoire à l&#39;aide des valeurs <i>échantillonnées</i> à partir de l&#39;entrée <b>Courbe de l&#39;inclinaison aléatoire</b>. |
| <b>Inclinaison aléatoire X</b> <i>Flottant</i> | Règle l&#39;intensité de l&#39;inclinaison aléatoire sur l&#39;axe <b>X</b> <i>uniquement</i>. |
| <b>Inclinaison aléatoire Y</b> <i>Flottant</i> | Règle l&#39;intensité de l&#39;inclinaison aléatoire sur l&#39;axe <b>Y</b> <i>uniquement</i>. |
| <b>Distribution Aléatoire De L&#39;Inclinaison</b> <i>Entier</i> | Contrôle la méthode de distribution des valeurs d&#39;inclinaison aléatoires aléatoires :<br><br>- <i>Uniforme</i> : l&#39;inclinaison aléatoire est appliquée de <i>la même manière</i> sur toutes les cellules<br>- <i>Bruit bleu</i> : l&#39;inclinaison aléatoire est <i>ajustée</i> à l&#39;aide d&#39;un motif de bruit bleu |
| <b>Biseau</b> |  |
| <b>Mode de distance en biseau</b> <i>Entier</i> | Définit la méthode d&#39;<i>acquisition de la distance</i> selon laquelle les formes doivent être biseautées :<br><br>-<i>par rapport à la taille de Grille</i> : les formes sont biseautées selon la <i>proportion spécifiée de leur taille de grille</i><br>-<i>par rapport à la taille de forme</i> : les formes sont biseautées selon la <i>proportion spécifiée de leur taille</i><br>-<i>par rapport à la taille d&#39;image</i> : les formes sont biseautées selon la <i>proportion spécifiée de l&#39;image</i> |
| <b>Multiplicateur de distance en biseau</b> <i>Flottant</i> | Applique un réglage <i>global</i> à la distance du biseau. |
| <b>Map d&#39;entrée de distance en biseau multiple.</b> <i>Flottant</i> | Ajuste la distance du biseau à l&#39;aide de la map d&#39;entrée de <b>Map distance du biseau</b> sous la forme d&#39;un multiplicateur <i> par pixel</i>. |
| <b>Courbe Arrondie En Biseau</b> <i>Flottant</i> | Ajuste l&#39;intensité de l&#39;arrondi appliqué à l&#39;angle de biseau pour le rendre plus <i>convexe</i>. |
| <b>Activer le contrôle de biseau par Axe</b> <i>Booléen</i> | Lorsque <i>Vrai</i>, le biseautage peut être appliqué et ajusté <i>séparément</i> sur les axes <b>X</b> et <b>Y</b>.<br><br><i>Remarque</i> : cette <i>annulation</i> de l’effet <b>Arrondis</b>. |
| <b>Distance en biseau X</b> <i>Flottant</i> | Ajuste la distance du biseau sur l&#39;axe <b>X</b> <i>uniquement</i>. Cette distance dépend de la valeur du paramètre <b>Mode de distance du biseau</b>.<br><br><i>Remarque</i> : ce paramètre n&#39;est disponible que lorsque le paramètre <b>Activer par contrôle de biseau par Axe</b> est défini sur <i>Vrai</i>. |
| <b>Distance en biseau Y</b> <i>Flottant</i> | Ajuste la distance du biseau sur l&#39;axe <b>Y</b> <i>uniquement</i>. Cette distance dépend de la valeur du paramètre <b>Mode de distance du biseau</b>.<br><br><i>Remarque</i> : ce paramètre n&#39;est disponible que lorsque le paramètre <b>Activer par contrôle de biseau par Axe</b> est défini sur <i>Vrai</i>. |
| <b>Masquer</b> |  |
| <b>Inversion aléatoire du masque</b> <i>Booléen</i> | Inverse le masquage aléatoire des formes. |
| <b>Démarrage aléatoire du masque</b> <i>Flottant</i> | Pour une <b>valeur de départ aléatoire</b> donnée, le masquage pseudo-aléatoire est appliqué suivant un <i>ordre spécifique</i> d&#39;une forme de début à une forme de fin. Ce paramètre vous permet de <i>décaler l&#39;index</i> de la forme <i>début</i>.<br><br><i>Remarque</i> : cela détermine une limite d&#39;une <i>plage de valeurs</i> pour le masquage. La valeur peut donc être <i>supérieure</i> à la valeur <b>Fin aléatoire du masque</b>. |
| <b>Fin aléatoire du masque</b> <i>Flottant</i> | Pour une <b>valeur de départ aléatoire</b> donnée, le masquage pseudo-aléatoire est appliqué suivant un <i>ordre spécifique</i> d&#39;une forme de début à une forme de fin. Ce paramètre vous permet de <i>décaler l&#39;index</i> de la forme <i>fin</i>.<br><br><i>Remarque</i> : cela détermine une limite d&#39;une <i>plage de valeurs</i> pour le masquage. La valeur peut donc être <i>supérieure</i> à la valeur <b>Démarrage aléatoire du masque</b>. |
| <b>Inversion du masque par zone de cellule</b> <i>Booléen</i> | Inverse le masquage des formes par la zone de leurs cellules. |
| <b>Masquer par début de zone de cellule</b> <i>Flottant</i> | Ajuste le seuil d&#39;aire de la cellule <i>minimum</i> pour le masquage des formes.<br><br><i>Remarque</i> : détermine une limite d&#39;une <i>plage de valeurs</i> pour le masquage. La valeur peut donc être <i>supérieure</i> à la valeur <b>Masquer par fin de zone de cellule</b>. |
| <b>Masquer par fin de zone de cellule</b> <i>Flottant</i> | Ajuste le seuil d&#39;aire de la cellule <i>maximum</i> pour le masquage des formes.<br><br><i>Remarque</i> : détermine une limite d&#39;une <i>plage de valeurs</i> pour le masquage. La valeur peut donc être <i>inférieure</i> à la valeur <b>Masquer par début de zone de cellule</b>. |
| <b>Inversion de l&#39;entrée de mappage de masque</b> <i>Booléen</i> | Inverse le masquage des formes par la map d&#39;entrée <b>Mask Map</b>. |
| <b>Début de l&#39;entrée de mappage de masque</b> <i>Flottant</i> | Ajuste le seuil de <i>valeur de niveau de gris minimale</i> dans la map d&#39;entrée <b>Mask Map</b> pour le masquage des formes.<br><br><i>Remarque</i> : détermine une limite d&#39;une <i>plage de valeurs</i> pour le masquage. La valeur peut donc être <i>supérieure</i> à la valeur <b>Fin d&#39;entrée de mappage de masque</b>. |
| <b>Fin d&#39;entrée du mappage de masque</b> <i>Flottant</i> | Ajuste le seuil de <i>valeur de niveaux de gris maximale</i> dans la map d&#39;entrée <b>Mask Map</b> pour le masquage des formes.<br><br><i>Remarque</i> : détermine une limite d&#39;une <i>plage de valeurs</i> pour le masquage. La valeur peut donc être <i>inférieure</i> à la valeur <b>Début de l&#39;entrée de mappage de masque</b>. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/tilerandom2-variant.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/tilerandom2-variant2.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/tilerandom2-variant3.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/tilerandom2-inputs.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/tilerandom2-demo.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/tilerandom2-demo2.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/tilerandom2-node.png" />
        </td>
    </tr>
</table>
