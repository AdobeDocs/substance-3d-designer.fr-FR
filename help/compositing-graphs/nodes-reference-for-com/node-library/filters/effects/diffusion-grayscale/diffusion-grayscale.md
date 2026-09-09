---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/diffusion-grayscale.html"
breadcrumb-title: ''
description: Utilisez le nœud Niveaux de gris de diffusion pour appliquer des effets de diffusion en niveaux de gris afin de créer des transitions et des mélanges de couleurs lisses.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Diffusion Grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Diffusion en niveaux de gris
user-guide-description: ''
user-guide-title: ''
source-git-commit: 07f136ebd89fbe737b6c042f1275bd348b2be514
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 3%

---


# Diffusion en niveaux de gris

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](diffusion-grayscale.resources/diffusion-grayscale-icon.png){width="200px"}

<b>Entrée :</b> Filtres > Effets

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Appliquez un processus de diffusion aux valeurs de l&#39;entrée d&#39;image **source** en fonction de l&#39;entrée d&#39;image **masque** fournie, en créant des dégradés lisses entre les valeurs.

Seules les valeurs des pixels correspondant au masque sont diffusées ; les autres pixels ne participent pas au résultat.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Source</b> <i>Niveaux de gris</i> | Image à diffuser. |
| <b>Masquer</b> <i>Niveaux de gris</i> | Masque de diffusion : les pixels blancs sont échantillonnés dans <i>Source</i> et diffusés dans les pixels noirs. L’image doit être en noir et blanc. Si le masque comprend des dégradés, la valeur de découpe est 0,5. |
| <b>Intensité</b> <i>Niveaux de gris</i> | Définit localement la force du processus de diffusion appliqué. Cette carte doit être <i>contrastée</i> pour un effet perceptible. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Itérations</b> <i>0.0 - 64.0</i> | Le nombre d&#39;itérations de diffusion à effectuer (plus le nombre est élevé, mieux c&#39;est, mais plus lentement). Les valeurs utiles sont comprises dans la plage [8, 48].<br>Notez que si vous ne recherchez pas l&#39;exactitude mathématique, les valeurs faibles conviennent ou sont même préférables. |
| <b>Distance</b> <i>0.0 - 1.0</i> | Ajuste la distance maximale de la diffusion. |
| <b>Activer le Dithering</b> <i>Vrai/Faux</i> | Contrôle la méthode d’échantillonnage de chaque passe. L’interpolation permet une convergence en moins de passes, mais introduit du bruit.<br>Sans cette option, chaque passe est plus rapide, mais davantage de passes sont nécessaires pour obtenir un résultat fluide sans artefacts de bande. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="diffusion-grayscale.resources/diffusion-grayscale-01-before.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="diffusion-grayscale.resources/diffusion-grayscale-01a-after.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="diffusion-grayscale.resources/diffusion-grayscale-01b-after.jpg" />
        </td>
    </tr>
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="diffusion-grayscale.resources/diffusion-grayscale-02-before.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="diffusion-grayscale.resources/diffusion-grayscale-02-after.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="diffusion-grayscale.resources/diffusion-grayscale-02-render.jpg" />
        </td>
    </tr>
</table>
