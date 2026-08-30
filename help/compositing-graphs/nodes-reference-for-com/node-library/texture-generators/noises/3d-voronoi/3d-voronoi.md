---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-voronoi.html"
breadcrumb-title: ''
description: Utilisez le nœud Voronoi 3D pour générer des motifs Voronoi basés sur la position mondiale 3D afin de créer des textures cellulaires volumétriques.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Voronoi
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D Voronoi
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '539'
ht-degree: 0%

---


# 3D Voronoi

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-voronoi.resources/3dvoronoi.png){width="200px"}

<b>Entrées :</b> Générateurs de Textures > Bruits

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Le nœud <b>Voronoi 3D</b> génère un bruit Voronoi dans l&#39;espace 3D en fonction de l&#39;entrée <b>Carte de position</b>.

Ce nœud peut être testé avec [Cube 3D GBuffers](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d-gbuffers/cube-3d-gbuffers.md) en entrée au lieu d&#39;une map bakée réelle (comme illustré dans l&#39;exemple ci-dessous).

</td>
</tr>
</table>

>[!WARNING]
>
> Ce bruit est destiné à être utilisé avec le <i>moteur GPU uniquement</i> (c&#39;est-à-dire <b>Direct3D</b> ou <b>OpenGL</b>). Accédez à <b>Outils > Changer de moteur...</b> ou appuyez sur la touche <b>F9</b> pour sélectionner le moteur souhaité.

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Inverser</b> <i>Booléen</i> | Inverse l’image de sortie. |
| <b>Échelle</b> <i>Flotter</i> | Contrôle l&#39;échelle du bruit 3D Voronoi.<br><br><i>Remarque</i> : lorsque la <b>Répétition</b> est activée sur <i>n&#39;importe quel axe</i>, l&#39;ajustement de l&#39;échelle est <i>gradué</i>. C&#39;est ce qui est attendu. |
| <b>Taille</b> <i>Float3</i> | Contrôle la taille du bruit de Voronoï 3D sur les axes <b>X</b>, <b>Y</b> et <b>Z</b>. Les valeurs non uniformes entraînent un effet de <i>étiré ou d&#39;écrasement</i>.<br><br><i>Remarque</i> : lorsque la <b>Répétition</b> est activée sur <i>n&#39;importe quel axe</i>, le réglage de la taille est <i>par paliers</i>. C&#39;est ce qui est attendu. |
| <b>Décalage</b> <i>Float3</i> | Applique un décalage à la <i>position</i> du bruit de Voronoï 3D sur les axes <b>X</b>, <b>Y</b> et <b>Z</b>. |
| <b>Désordre</b> <i>Float3</i> | Intensité du <i>décalage aléatoire</i> appliqué à chaque point du bruit dans les axes <b>X</b>, <b>Y</b> et <b>Z</b>. |
| <b>Intensité de la Distorsion</b> <i>Flotter</i> | Contrôle l&#39;intensité d&#39;un <i>effet de déformation</i> appliqué sur le bruit Voronoi 3D. |
| <b>Multiplicateur d&#39;échelle de Distorsion</b> <i>Flotter</i> | Contrôle l&#39;échelle du <i>motif de déformation</i> utilisé dans l&#39;effet de déformation contrôlé par l&#39;<b>intensité de la Distorsion</b>. |
| <b>Courbe Arrondie</b> <i>Flotter</i> | Arrondit la <i>pente</i> autour de chaque point du bruit pour le rendre <i>convexe</i>.<br><br><i>Remarque</i> : ce paramètre n&#39;est pas disponible lorsque le paramètre <b>Style</b> est défini sur <i>Edge</i>. |
| <b>Échelle de distance</b> <i>Flotter</i> | Ajuste la <i>distance du dégradé</i> autour de chaque point du bruit. |
| <b>Mode Distance</b> <i>Nombre entier</i> | Définit la méthode pour <i>calculer le gradient de distance</i> autour de chaque point du bruit :<br><br>- <i>euclidien</i><br>- <i>Manhattan</i><br>- <i>Tchebychev</i><br>- <i>Minkowski</i> |
| <b>Nombre de Minkowski</b> <i>Flotter</i> | Ordre <i>p</i> de la distance de Minkowski. Si nous divisons le gradient de distance en quadrants, ce nombre a un impact sur ces quadrants comme suit :<br><br>- p est <i>exactement</i> 1 : droit<br>- p est <i>inférieur</i> à 1 : concave<br>- p est <i>supérieur</i> à 1 : convexe<br><br>valeurs intéressantes :<br>- <i>1.0</i> : distance de Manhattan<br>- <i>2.0</i> : distance euclidienne<br>- <i>Infini</i> : distance de Tchebychev<br><br><i>Remarque</i> : ce paramètre est uniquement disponible lorsque le paramètre <b>Mode de distance</b> est défini sur <i>Minkowski</i>. |
| <b>Style</b> <i>Nombre entier</i> | Définit la méthode <i>de rendu des données</i> du bruit 3D de Voronoi, en tenant compte du fait que le bruit est fondé sur un ensemble de points dans l&#39;espace 3D :<br><br>- <i>F1</i> : distance jusqu&#39;au <i>point le plus proche</i> dans l&#39;espace 3D<br>- <i>F2</i> : distance jusqu&#39;au <i>deuxième point le plus proche</i> dans l&#39;espace 3D<br>- <i>F2-F1</i><br>- <i>F1\*F2</i><br>- <i>F1/F2</i><br>- <i>Bord</i> : le <i>bord entre chaque cellule</i> du bruit dans l&#39;espace 3D<br>- <i>Couleur aléatoire</i> : attribuez une <i>couleur plate aléatoire</i> à chaque cellule du bruit dans l&#39;espace 3D |
| <b>Thickness Edge</b> <i>Flotter</i> | Ajuste le thickness des contours détectés entre les cellules du bruit Voronoi 3D. Les arêtes sont détectées dans les axes X, Y et Z. Certaines épaisseurs peuvent donc augmenter plus rapidement que d&#39;autres en fonction de la <i>profondeur</i> des cellules.<br><br><i>Remarque</i> : ce paramètre n&#39;est disponible que lorsque le paramètre <b>Style</b> est défini sur <i>Arête</i>. |
| <b>Activer la Répétition</b> <i>Booléen</i> | Ajuste le bruit de Voronoï 3D de sorte que son motif résultant <i>se répète</i> sur les axes X, Y et Z. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-voronoi.resources/3dvoronoi-variant.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-voronoi.resources/3dvoronoi-variant5.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-voronoi.resources/3dvoronoi-variant2.jpg" />
        </td>
    </tr>
    <tr style="border: 0; background: transparent">
        <td style="border: 0; background: transparent">
            <img src="3d-voronoi.resources/3dvoronoi-variant4.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-voronoi.resources/3dvoronoi-variant3.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-voronoi.resources/3dvoronoi-variant6.jpg" />
        </td>
    </tr>
</table>
