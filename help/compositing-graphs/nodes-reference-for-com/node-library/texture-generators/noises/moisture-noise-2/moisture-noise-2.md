---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/moisture-noise-2.html"
breadcrumb-title: ''
description: Utilisez le nœud Bruit d'humidité 2 pour générer des motifs d'humidité organiques pour des textures de surface réalistes.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Moisture noise 2
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Bruit d'humidité 2
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 1%

---


# Bruit d&#39;humidité 2

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Bruit d&#39;humidité 2 - Icône](moisture-noise-2.resources/moisture_noise_2.png "Bruit d&#39;humidité 2 - Icône"){width="200px"}

<b>Entrée :</b> Générateurs de textures > Bruits

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Une variante des bruits riches et spongieux de l&#39;<b>humidité</b>.

Disques de dureté et de taille variables et dispersés et additionnés ou soustraits de la couleur ci-dessous, à partir d&#39;un gris de base.

Voir aussi : [Bruit d&#39;humidité 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/moisture-noise/moisture-noise.md)

</td>
</tr>
</table>

<a name="outputs"></a>

## Sorties

|  |  |
|:---|:---|
| <b>Sortie</b> <i>Niveaux de gris</i> | Le bruit généré est une image bitmap en niveaux de gris. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Échelle</b> <i>Nombre entier</i> | Subdivision de la grille utilisée pour générer les carreaux de bruit.    Plus la valeur est élevée, plus le nombre de carreaux dessinés est important et plus le bruit est dense. |
| <b>Désordre</b> <i>Flotter</i> | Déplace les ingrédients du bruit.    Cela peut être utilisé pour animer le bruit. |
| <b>Désorganiser la vitesse</b> <i>Flotter</i> | Ajuste la distance de displacement appliquée par le paramètre <b>Désordre</b>.    Cela permet de contrôler la vitesse du displacement lors de l’animation du bruit. |
| <b>Désorganiser l&#39;anisotropie</b> <i>Flotter</i> | Contrôle l&#39;étendue des directions du displacement appliqué par le paramètre <b>Désordre</b>, où une valeur plus élevée entraîne une direction plus étroite et plus définie.    La direction est contrôlée par le paramètre <b>Désorganiser l&#39;angle d&#39;anisotropie</b>. |
| <b>Désorganiser l&#39;anisotropy angle</b> <i>Flotter</i> | Contrôle la direction du displacement appliqué par le paramètre <b>Disorder</b>, lorsque le paramètre <b>Disorder anisotropie</b> n&#39;est pas nul. |
| <b>Taille du motif</b> <i>Float2</i> | Multiplicateur de la taille d’un motif diffusé. , où 1,0 correspond à la taille de diffusion d’origine. |
| <b>Angle du motif</b> <i>Flotter</i> | Angle utilisé pour définir la direction du motif diffusé, en nombre de tours et à partir de l’horizontale vers la droite. |
| <b>Angle aléatoire du motif</b> <i>Flotter</i> | Quantité maximale de variation aléatoire appliquée à la valeur <b>Angle du motif</b>, en nombre de tours. |
| <b>Opacité globale</b> <i>Flotter</i> | Opacité de tous les ingrédients du bruit, où 0,0 donne un gris plat de base et 1,0 est le résultat de l&#39;addition ou de la soustraction complète appliquée par les ingrédients. |
| <b>Décalage de mosaïque</b> <i>Float2</i> | Définit la position de la partie du plan infini utilisée pour le rendu du bruit. |
| <b>Expansion non carrée</b> <i>Booléen</i> | Dans les images non carrées, la mosaïque générée reste carrée et étend la génération de bruit aux limites de l’image. |

## Exemples

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Bruit d&#39;humidité 2 - Exemple 1](moisture-noise-2.resources/moisture_noise_2_1.png "Bruit d&#39;humidité 2 - Exemple 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Bruit d&#39;humidité 2 - Exemple 2](moisture-noise-2.resources/noise_moisture_noise_2_speed0.6_aniso0.gif "Bruit d&#39;humidité 2 - Exemple 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Bruit d&#39;humidité 2 - Exemple 3](moisture-noise-2.resources/noise_moisture_noise_2_speed0.6_aniso1.gif "Bruit d&#39;humidité 2 - Exemple 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Bruit d&#39;humidité 2 - Exemple 4](moisture-noise-2.resources/noise_moisture_noise_2_speed0.3_aniso0.6.gif "Bruit d&#39;humidité 2 - Exemple 4"){zoomable="yes"}

</td>
</tr>
</table>
