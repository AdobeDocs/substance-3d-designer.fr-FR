---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/pbr-render.html"
breadcrumb-title: ''
description: Utilisez le nœud Rendu PBR pour effectuer le rendu de matériaux basés physiquement avec un éclairage réaliste pour prévisualiser l’apparence du matériau.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > PBR Utilities > PBR Render
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Rendu PBR
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '1365'
ht-degree: 6%

---


# Rendu PBR

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](pbr-render.resources/pbr-render.png){width="250px"}

<b>Entrée :</b> Filtres de matériau > Utilitaires PBR

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Effectue le rendu d’un matériau PBR sur une sphère, un plan ou un cylindre à l’aide de l’éclairage basé sur l’image (IBL). Il s’agit d’un moteur de rendu à l’intérieur d’un nœud, qui peut être très utile pour générer des vignettes, des aperçus ou des ressources 2D. Il ne s’agit pas d’un rendu comme la vue 3D, mais d’une véritable texture générée dans votre graphique.

Ce nœud nécessite au moins un matériel PBR complet à brancher. Dans l’idéal, vous devez utiliser les modes de création de lien pour connecter le matériau au Rendu PBR. En outre, vous aurez besoin d’un environnement HDRI à enveloppe sphérique pour le rendu afin de calculer l’éclairage à partir de. Les matériaux à tester se trouvent sous Matériaux PBR, les cartes d&#39;environnement sous [Vue 3D dans la bibliothèque.](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/3d-view-library.md)

</td>
</tr>
</table>

>[!WARNING]
>
> **Moteur CPU (SSE2)**
> 
> Le nœud Rendu PBR est très lourd et ne fonctionne pas bien avec le moteur CPU de SSE2. Passez à un autre moteur en appuyant sur F9, si le nœud fonctionne extrêmement mal.

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Entrées de canal Matériau</b> | Plusieurs entrées de matériau sont utilisées pour effectuer le rendu du matériau sur la géométrie :<br><br>- Base color<br>- Normal<br>- Emissive<br>- Rugosité<br>- Métallique<br>- Specular level<br>- Height<br>- Ambient occlusion<br>- Masque d&#39;opacité<br>- Anisotropy level<br>- Anisotropy angle<br>- Translucency<br>- Échelle de distance de diffusion |
| <b>Carte de Dirt de l&#39;objectif</b> <i>Entrée en niveaux de gris</i> | Carte personnalisée du dirt sur l’objectif, qui apparaît lorsque les halos sont visibles. |
| <b>Carte d&#39;Ouverture de l&#39;objectif</b> <i>Entrée en niveaux de gris</i> | Peut être utilisé pour remplacer la forme Bokeh floue. Plus il est contrasté, plus il est visible. Gardez à l’esprit que seul un cercle de la texture est échantillonné, donc toute forme doit tenir dans un cercle. |
| <b>Entrée en arrière-plan</b> <i>Entrée de couleur</i> | Mappage personnalisé utilisé comme arrière-plan lorsque le paramètre <b>Mode arrière-plan</b> est défini sur <i>Entrée arrière-plan</i> |
| <b>Map d&#39;environnement</b> <i>Entrée couleur</i> | Carte d&#39;environnement utilisée pour calculer l&#39;éclairage. Doit être mappé sphériquement et en HDR. |

<a name="outputs"></a>

## Sorties

|  |  |
|:---|:---|
| <b>Beauté</b> | Le rendu final |
| <b>Irradiance brute</b> | Données d&#39;irradiance de la Map opacity <br><br><i>Alpha:</i> du rendu final |
| <b>Specular Brut</b> | Les données de specular du rendu final<br><br><i>Alpha :</i> carte des ombres de Specular |
| <b>Espace monde normal</b> | Les données de normale de l&#39;espace monde de la map height d&#39;Alpha <br><br><i>du rendu final :</i> d&#39;Espace monde |
| <b>Repère tangent normal</b> | Les données des normales de l&#39;espace de tangente de l&#39;Alpha de rendu final <br><br><i> :</i> map height de l&#39;espace de Tangente |
| <b>UV</b> | Les données d&#39;UV de la Map opacity <br><br><i>Alpha :</i> du rendu final |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Forme</b> <i>Sphère, Plan, Cylindre</i> | Définit la forme utilisée pour le rendu. Les formes personnalisées ne sont pas possibles. |
| <b>Intensité du Displacement</b> <i>0.0 - 0.5</i> | Définissez l’intensité du displacement à partir de l’height. |
| <b>Rotation de l&#39;environnement</b> <i>0.0 - 1.0</i> | Fait pivoter l’environnement d’éclairage. Pré-rotation par rapport au déplacement de la caméra. |
| <b>Mode Arrière-plan</b> <i>Entrée Couleur, Environnement, Ambiant, Arrière-Plan</i> | Définissez ce qui s’affiche en arrière-plan. La couleur est une couleur unie, l’environnement est la carte que vous avez connectée avec un flou facultatif. Ambiant est une version très floue de l&#39;environnement. |
| <b>Couleur d&#39;arrière-plan</b> <i>(valeur de couleur)</i> | Disponible uniquement lorsque le mode Arrière-plan est défini sur Couleur. |
| <b>Flou d&#39;arrière-plan de l&#39;environnement</b> <i>0.0 - 1.0</i> | Disponible uniquement lorsque le mode Arrière-plan est défini sur Environnement. |
| <b>Forme</b> |  |
| <b>Échelle</b> <i>0.0 - 2.0</i> | Définissez l’échelle de la sphère. |
| <b>Taille du plan</b> <i>0.0 - 1.0</i> | Définissez l’échelle du plan. |
| <b>Rayon du cylindre</b> <i>0.0 - 1.0</i> | Définissez le rayon du cylindre. |
| <b>Longueur du cylindre</b> <i>0.0 - 1.0</i> | Définissez la longueur du cylindre. |
| <b>Rotation</b> <i>0.0 - 1.0</i> | Fait pivoter la forme sans faire pivoter l’éclairage. |
| <b>Direction de la rotation</b> <i>0.0 - 1.0</i> | Définit l’axe de rotation en 2D. |
| <b>Rotation Autour De La Direction</b> <i>0.0 - 1.0</i> | Forme en rotation sur l’axe de rotation. |
| <b>Position de la forme</b> <i>-1.0 - 1.0</i> | Déplace les formes. |
| <b>UV</b> <i>1.0 - 6.0</i> | Définit la quantité d’UV-Répétition. |
| <b>Échelle UV Sphère</b> <i>0.0 - 4.0</i> | Définit l&#39;échelle des UV sur la sphère. |
| <b>Échelle UV plane</b> <i>1.0 - 4.0</i> | Définit l&#39;échelle des UV sur le plan. |
| <b>Échelle UV de cylindre</b> <i>1.0 - 6.0</i> | Définit l&#39;échelle des UV sur le cylindre. |
| <b>Décalage des UV</b> <i>0.0 - 1.0</i> | UV de décalage |
| <b>Inclinaison des UV</b> <i>Faux/Vrai</i> | Inclinaison l’UV de 45° pour la sphère. |
| <b>Appareil photo</b> |  |
| <b>Exposition</b> <i>-4.0 - 4.0</i> | Définissez l’exposition de la caméra. |
| <b>Mappeur de tonalité</b> <i>Linear, ACE, Filmic Hejl</i> | Définissez la solution de mappage de tonalité à utiliser pour l’image finale. |
| <b>Mode Caméra</b> <i>Perspective, Orthographique</i> | Permutez la caméra entre deux modes de projection. |
| <b>Champ de vision</b> <i>0.01 - 100.0</i> | Définissez l’angle FOV de la caméra. |
| <b>Distance</b> <i>0.0 - 4.0</i> | Définissez la distance entre la caméra et le centre de l’objet. |
| <b>Intensité du vignetage</b> <i>0.0 - 1.0</i> | Définissez l’intensité de l’effet de vignette. |
| <b>Rayon de vignetage</b> <i>0.0 - 1.0</i> | Définissez le rayon de l’effet de vignette. |
| <b>Position à l&#39;écran</b> | Déplace la caméra autour de l’objet. Cette option peut également être modifiée à l’aide d’un objet dans la vue 2D. |
| <b>Profondeur de champ</b> |  |
| <b>Rayon D&#39;Ouverture</b> <i>0.0 - 0.1</i> | Définit le rayon de l’ouverture. Des valeurs élevées signifient que les zones floues deviennent plus floues (bokeh). |
| <b>Lames d&#39;Ouverture</b> <i>3 - 9</i> | Définit la forme du flou bokeh. |
| <b>Bague D&#39;Ouverture</b> <i>0.0 - 1.0</i> | Ajoute un dégradé interne à la forme bokeh. |
| <b>Difraction Ouverture</b> <i>0.0 - 2.0</i> | Ajoute une aberration chromatique au bokeh. |
| <b>Bokeh tourbillonnant</b> <i>0.0 - 1.0</i> | Ajoute un effet de tourbillon ou de rotation aux zones floues bokeh floues floues. |
| <b>Mode Focus</b> <i>Auto, Point</i> | Définissez si le focus est prédéterminé ou défini par l’utilisateur. La mise au point vous permet de déplacer un point dans la vue 2D pour déterminer la distance de mise au point. |
| <b>Point De Mise Au Point</b> | Si le focus est défini sur Point, vous pouvez déplacer ce point. dispose d’un widget de vue 2D. |
| <b>Décalage de mise au point</b> <i>-0.5 - 0.5</i> | Si le focus est défini sur Auto, vous permet de le déplacer d’avant en arrière. |
| <b>Utiliser le mappage d&#39;Ouverture personnalisé</b> <i>Faux/Vrai</i> | Remplace les paramètres d’ouverture ci-dessus et utilise l’entrée de courbe d’ouverture pour déterminer la forme bokeh. Nécessite une entrée. |
| <b>Effets postérieurs</b> |  |
| <b>Activer les Effets de post-traitement</b> <i>Faux/Vrai</i> | Active/désactive les post-effets <i>tous</i> dans le rendu final. |
| <b>Intensité de la floraison</b> <i>0.0 - 2.0</i> | Définit la force de l’effet de floraison. |
| <b>Seuil de floraison</b> <i>0.0 - 2.0</i> | Définit le seuil d’apparition de la floraison. |
| <b>Décalage chromatique de la floraison</b> <i>0.0 - 1.0</i> |  |
| <b>Intensité du halo de l&#39;objectif</b> <i>0.0 - 1.0</i> | Définit l’intensité de l’effet de halo. |
| <b>Intensité des Halos</b> <i>0.0 - 1.0</i> | Définit l’intensité du halo. Assurez-vous que la lumière de l’arrière-plan de votre environnement est bien visible pour voir correctement cet effet. |
| <b>Intensité du Dirt de l&#39;objectif</b> <i>0.0 - 1.0</i> | Définit l’effet de la texture dirt de l’objectif sur les Halos. |
| <b>Paramètres de rendu</b> |  |
| <b>Qualité de Diffuse</b> <i>16 Échantillons, 32 Échantillons, 64 Échantillons, 128 Échantillons</i> | Basculez entre les niveaux de qualité pour la carte de diffusion. |
| <b>Multiplicateur Diffuse</b> <i>0.0 - 1.0</i> | Contrôle la contribution des parties émissives à l&#39;irradiation. |
| <b>Intensité de l&#39;ombre du Diffuse</b> <i>0.0 - 1.0</i> | Contrôle l’intensité des ombres diffuses. |
| <b>Dithering Specular</b> <i>0.0 - 1.0</i> | Définissez la quantité de tramage pour le specular. |
| <b>Multiplicateur d&#39;ombre de Specular</b> <i>0.0 - 1.0</i> | Contrôle l’intensité des ombres dans les reflets specular. |
| <b>Mode Opacité</b> <i>Test d&#39;Alpha tramé, Fusion d&#39;Alpha simple</i> | Contrôle la méthode d’application de la transparence. Le mode de fusion <i>Alpha simple</i> est plus visible sur des arrière-plans uniformes. |
| <b>Intensité de l&#39;Ambient occlusion</b> <i>0.0 - 1.0</i> | Définit l’intensité des ombres de l’occlusion ambiante. |
| <b>Réglages de matière</b> |  |
| <b>Recalculer les normales</b> <i>Faux/Vrai</i> | Les normales seront recalculées à partir de la carte d&#39;height en fonction de l&#39;intensité du displacement. |
| <b>Format normal</b> <i>DirectX, OpenGL</i> | Basculer entre différents Formats de map normaux (inverse la couche verte) |
| <b>Entrée F0 diélectrique</b> <i>Valeur constante, entrée de Specular level</i> | Définissez ce qui détermine les valeurs F0. Entrée de specular level signifie qu&#39;il sera piloté par un mappage d&#39;entrée. |
| <b>Diélectrique F0</b> <i>0.0 - 0.08</i> | Si l’option Valeur constante est choisie pour Entrée diélectrique F0, ce curseur vous permet de définir la valeur globale. |
| <b>Pelage transparent</b> |  |
| <b>Activer le pelage transparent</b> <i>Faux/Vrai</i> | Permet d’ajouter un calque de revêtement transparent simple et supplémentaire sur le matériau d’entrée. |
| <b>Épaisseur de pelage nette</b> <i>0.0 - 1.0</i> | Définit l’intensité ou l’intensité du calque clearcoat. |
| <b>Effacer le Coat specular level</b> <i>0.0 - 1.0</i> | Définit la rugosité du calque clearcoat. |
| <b>Hériter de la normale à partir du calque de base</b> <i>Faux/Vrai</i> | Définissez cette option si clearcoat ignore ou utilise les normales du matériau de base. |
| <b>Émissif</b> |  |
| <b>Activer l&#39;éclairage Emissive</b> <i>Vrai/Faux</i> | Active/désactive la contribution diffuse de l’éclairage emissive. |
| <b>Intensité émissive</b> <i>0.0 - 10.0</i> | Définit le multiplicateur global pour la carte émissive. |
| <b>Subsurface scattering</b> |  |
| <b>Activer la Subsurface scattering</b> <i>Vrai/Faux</i> | Active/désactive la subsurface scattering dans le rendu final.<br><br><i>Remarque :</i> la Subsurface scattering nécessite que la valeur d&#39;entrée <b>Translucency</b> soit <i>supérieure à 0,0</i> |
| <b>Distance de diffusion</b> <i>0.0 - 1.0</i> | Ajuste la distance maximale de l&#39;effet de diffusion.<br><br><i>Remarque :</i> cette valeur est multipliée par rapport à la valeur d&#39;entrée <i> de l&#39;<b>échelle de distance de diffusion</b> par couche de couleur</i>. |
| <b>Décalage Rouge</b> <i>0.0 - 1.0</i> | Règle l’intensité de l’effet de décalage du rouge dans la diffusion. |
| <b>Rayleigh</b> <i>0.0 - 1.0</i> | Règle l’intensité de l’effet Rayleigh dans la diffusion. |

## Exemples

Toutes les images ont été générées directement à l&#39;intérieur de Designer, dans la fenêtre d&#39;affichage 2D, à l&#39;aide des matériaux de la bibliothèque [Ressources Substance 3D](https://substance3d.adobe.com/assets).

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="pbr-render.resources/pbr-render-v2.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="pbr-render.resources/sphere-thermal-insulation-panel.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="pbr-render.resources/sphere-ominous-obsidian.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="pbr-render.resources/sphere-forest-gravel-1.jpg" />
        </td>
    </tr>
    <tr style="border: 0; background: transparent">
        <td style="border: 0; background: transparent">
            <img src="pbr-render.resources/sphere-chesterfield-1.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="pbr-render.resources/sphere-carbon-fiber.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="pbr-render.resources/plane-inclined-lumber-tiles.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="pbr-render.resources/cylinder-medieval-leaded-glass-window.jpg" />
        </td>
    </tr>
</table>
