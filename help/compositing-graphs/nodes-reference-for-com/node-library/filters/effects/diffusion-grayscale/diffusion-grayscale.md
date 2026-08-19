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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 1%

---


# Diffusion en niveaux de gris

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-grayscale-icon.png){width="200px"}

**Entrée :** *Filtres/Effets*

**Intermédiaire**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Description

Appliquez un processus de diffusion aux valeurs de l&#39;entrée d&#39;image **source** en fonction de l&#39;entrée d&#39;image **masque** fournie, en créant des dégradés lisses entre les valeurs.

Seules les valeurs des pixels correspondant au masque sont diffusées ; les autres pixels ne participent pas au résultat.

</td>
</tr>
</table>

## Paramètres

* **Itérations** : *0,0 - 64,0* le nombre d&#39;itérations de diffusion à effectuer (plus le nombre est élevé, mieux c&#39;est, mais plus le nombre est lent). Les valeurs utiles sont comprises dans la plage [8, 48].\
  Veuillez noter que si vous ne recherchez pas l&#39;exactitude mathématique, les valeurs faibles sont correctes ou même meilleures.\
  **Distance** : **0,0 - 1,0** ajuste la distance maximale de diffusion.
* **Activer l&#39;interpolation** : *Vrai/Faux* contrôle la méthode d&#39;échantillonnage de chaque passe. L’interpolation permet une convergence en moins de passes, mais introduit du bruit.\
  Sans lui, chaque passe est plus rapide, mais davantage de passes sont nécessaires pour obtenir un résultat lisse sans artefacts de bande.

## Entrées

* **Source** *Niveaux de gris*\
  Image à diffuser.
* **Masquer** *En Niveaux De Gris*\
  Masque de diffusion : les pixels blancs sont échantillonnés dans *Source* et diffusés dans les pixels noirs. L’image doit être en noir et blanc. Si le masque comprend des dégradés, la valeur de découpe est 0,5.
* **Intensité** *Niveaux de gris*\
  Définit localement la force du processus de diffusion appliqué. Cette carte doit être *contrastée* pour un effet perceptible.

## Exemples d’images

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-grayscale-01-before.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-grayscale-01a-after.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-grayscale-01b-after.jpg){width="256px"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-grayscale-02-before.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-grayscale-02-after.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-grayscale-02-render.jpg){width="512px"}

</td>
</tr>
</table>
