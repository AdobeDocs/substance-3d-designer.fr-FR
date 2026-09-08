---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/diffusion-uv.html"
breadcrumb-title: ''
description: Utilisez l’UV Diffusion pour appliquer des effets de diffusion dans l’espace UV afin de créer des transitions et des mélanges de couleurs lisses.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Diffusion UV
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: UV de diffusion
user-guide-description: ''
user-guide-title: ''
source-git-commit: a4ccdbff5343e3ece0312bd9b3318fb236f07308
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 2%

---


# UV de diffusion

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-uv-icon.png){width="200px"}

<b>Entrée :</b> Filtres > Effets

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Appliquez un processus de diffusion aux coordonnées UV dans l&#39;entrée d&#39;image **source** en fonction de l&#39;entrée d&#39;image **masque** fournie, en interpolant les coordonnées entre les valeurs de **source**.

Seuls les UV des pixels correspondant au masque sont diffusés ; les autres pixels ne participent pas au résultat.

Veuillez noter que la répétition est gérée de manière spéciale : lorsque la répétition est *activée* (ce qui est le cas par défaut), les coordonnées voisines peuvent être moyennées au-delà de la limite 0/1.

Par exemple, si la valeur de la coordonnée U est de 0,1 sur un pixel et de 0,8 sur un autre, la valeur moyenne sera de 0,95 au lieu de 0,45, car la *répétition des coordonnées est supposée*. Cela est indépendant de la position réelle des pixels : les valeurs des coordonnées sont traitées de la même manière sur toute l’image.

Cela peut entraîner des résultats indésirables lors de l&#39;utilisation de ce filtre pour la *déformation de la texture*. Si cela se produit, assurez-vous que votre masque définit des « courbes/points de contrôle » espacés de *demi-texture maximum*.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Source</b> <i>Couleur</i> | Les UV à diffuser. Veuillez noter que les répétitions sont traitées de manière spéciale dans ce filtre (voir <i>Description</i>). |
| <b>Masquer</b> <i>Niveaux de gris</i> | Masque de diffusion : les pixels blancs sont échantillonnés dans <i>Source</i> et diffusés dans les pixels noirs. L’image doit être en noir et blanc. Si le masque comprend des dégradés, la valeur de découpe est 0,5. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Itérations</b> <i>0.0 - 64.0</i> | Le nombre d&#39;itérations de diffusion à effectuer (plus le nombre est élevé, mieux c&#39;est, mais plus lentement). Les valeurs utiles sont comprises dans la plage [8, 48].<br>Notez que si vous ne recherchez pas l&#39;exactitude mathématique, les valeurs faibles conviennent ou sont même préférables. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/diffusion-uv-01a-before.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/diffusion-uv-01a-after.jpg" />
        </td>
    </tr>
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/diffusion-uv-01b-before.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/diffusion-uv-01b-after.jpg" />
        </td>
    </tr>
</table>
