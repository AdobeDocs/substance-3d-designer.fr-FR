---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/voronoi.html"
breadcrumb-title: ''
description: Utilisez le nœud Voronoi pour générer des motifs Voronoi afin de créer des textures cellulaires et des effets de matériau organique.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Voronoi
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Voronoi
user-guide-description: ''
user-guide-title: ''
source-git-commit: db5ad9a6ad1d03fedcc3d760cc8886501d16b87f
workflow-type: tm+mt
source-wordcount: '610'
ht-degree: 0%

---


# Voronoi

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](voronoi.resources/voronoi.png){width="200px"}

<b>Entrées :</b> Générateurs de Textures > Bruits

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Le nœud **Voronoi** génère un bruit 3D Voronoi mappé à une image 2D à l&#39;aide d&#39;une projection orthographique *Z-down*.

Ce nœud peut être testé avec [Cube GBuffers](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d-gbuffers/cube-3d-gbuffers.md) en entrée au lieu d&#39;une map bakée réelle (comme illustré dans l&#39;exemple ci-dessous).

>[!WARNING]
>
> Ce bruit est destiné à être utilisé avec le *moteur GPU uniquement* (c&#39;est-à-dire **Direct** ou **OpenGL**). Accédez à **Outils > Changer de moteur...** ou appuyez sur la touche **F9** pour sélectionner le moteur souhaité.

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Inverser</b> <i>Booléen</i> | Inverse l’image de sortie. |
| <b>Échelle</b> <i>Flottant</i> | Contrôle l&#39;échelle du bruit Voronoi.<br><br>*Remarque* : lorsque la **Répétition** est activée sur *n&#39;importe quel axe*, l&#39;ajustement de l&#39;échelle est *gradué*. C&#39;est ce qui est attendu. |
| <b>Taille</b> <i>Flottant3</i> | Contrôle la taille du bruit Voronoi dans les axes **X**, **Y** et **Z**. Les valeurs non uniformes entraînent un effet de *étiré ou d&#39;écrasement*.<br><br>*Remarque* : lorsque la **Répétition** est activée sur *n&#39;importe quel axe*, le réglage de la taille est *par paliers*. C&#39;est ce qui est attendu. |
| <b>Décalage</b> <i>Flottant3</i> | Applique un décalage à la *position* du bruit Voronoi dans les axes **X**, **Y** et **Z**. |
| <b>Désordre</b> <i>Flottant3</i> | Intensité du *décalage aléatoire* appliqué à chaque point du bruit dans les axes **X**, **Y** et **Z**. |
| <b>Intensité de la Distorsion</b> <i>Flottant</i> | Contrôle l&#39;intensité d&#39;un *effet de déformation* appliqué sur le bruit Voronoi. |
| <b>Multiplicateur d&#39;échelle de Distorsion</b> <i>Flottant</i> | Contrôle l&#39;échelle du *motif de déformation* utilisé dans l&#39;effet de déformation contrôlé par l&#39;**intensité de la Distorsion**. |
| <b>Courbe Arrondie</b> <i>Flottant</i> | Arrondit la *pente* autour de chaque point du bruit pour le rendre *convexe*.<br><br>*Remarque* : ce paramètre n&#39;est pas disponible lorsque le paramètre **Style** est défini sur *Edge*. |
| <b>Échelle de distance</b> <i>Flottant</i> | Ajuste la *distance du dégradé* autour de chaque point du bruit. |
| <b>Mode Distance</b> <i>Entier</i> | Définit la méthode pour *calculer le gradient de distance* autour de chaque point du bruit :<br><br>- *euclidien*<br>- *Manhattan*<br>- *Tchebychev*<br>- *Minkowski* |
| <b>Nombre de Minkowski</b> <i>Flottant</i> | Ordre *p* de la distance de Minkowski. Si nous divisons le gradient de distance en quadrants, ce nombre a un impact sur ces quadrants comme suit :<br><br>- p est *exactement* 1 : droit<br>- p est *inférieur* à 1 : concave<br>- p est *supérieur* à 1 : convexe<br><br>valeurs intéressantes :<br><br>- *1.0* : distance de Manhattan<br>- *2.0* : distance euclidienne<br>- *Infini* : distance de Tchebychev <br><br>*Remarque* : ce paramètre est uniquement disponible lorsque le paramètre **Mode de distance** est défini sur *Minkowski*. |
| <b>Style</b> <i>Entier</i> | Définit la méthode *de rendu des données* du bruit de Voronoi, en tenant compte du fait que le bruit est fondé sur un ensemble de points dans l&#39;espace :<br><br>- *F1* : la distance au *point le plus proche* dans l&#39;espace<br>- *F2* : la distance au *deuxième point le plus proche* dans l&#39;espace<br>- *F2-F1*<br>- *F1\* F2 *<br>-* F1/F2 *<br>-* Bord *: le* bord entre chaque cellule *du bruit dans l&#39;espace<br>-* Couleur aléatoire *: attribuez une* couleur plate aléatoire* à chaque cellule du bruit dans l&#39;espace |
| <b>Thickness Edge</b> <i>Flottant</i> | Ajuste le thickness des contours détectés entre les cellules du bruit Voronoi. Les arêtes sont détectées dans les axes X, Y et Z. Certaines épaisseurs peuvent donc augmenter plus rapidement que d&#39;autres en fonction de la *profondeur* des cellules.<br><br>*Remarque* : ce paramètre n&#39;est disponible que lorsque le paramètre **Style** est défini sur *Arête*. |
| <b>Mode générateur de couleurs aléatoire</b> <i>Entier</i> | Définit la méthode d&#39;*acquisition* de la valeur de départ aléatoire pour le choix de couleur par cellule :<br><br>-*Valeur de départ aléatoire globale* : utilisez la valeur de départ *héritée* par le nœud<br>-*Valeur de départ manuelle* : utilisez une valeur de départ *discrète*<br><br>*Remarque* : ce paramètre n&#39;est disponible que lorsque le paramètre **Style** est défini sur *Couleur aléatoire*. |
| <b>Générateur aléatoire de couleurs</b> <i>Entier</i> | Valeur de départ aléatoire discrète qui doit être utilisée pour le choix de couleur par cellule.<br><br>*Remarque* : ce paramètre n&#39;est disponible que lorsque le paramètre **Style** est défini sur *Couleur aléatoire* et le paramètre **Mode de valeur de départ aléatoire** sur ***Valeur de départ manuelle***. |
| <b>Extension non carrée</b> <i>Booléen</i> | Active la compensation de la courbure et de la étire avec des proportions non carrées. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="voronoi.resources/voronoi-variant2.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="voronoi.resources/voronoi-variant3.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="voronoi.resources/voronoi-variant5.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="voronoi.resources/voronoi-variant.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="voronoi.resources/voronoi-variant4.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="voronoi.resources/voronoi-variant6.jpg" />
        </td>
    </tr>
</table>
