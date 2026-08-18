---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-ridged-noise-fractal.html"
breadcrumb-title: ''
description: Utilisez le nœud Fractal de bruit strié 3D pour générer des motifs de bruit fractal strié dans l’espace 3D afin de créer des textures de type montagne.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Ridged Noise Fractal
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Bruit 3D ridgé fractal
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 0%

---


# Bruit 3D ridgé fractal

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/3dridgednoisefractal.png){width="200px"}

**Entrée :** *Générateurs De Texture**/Bruits*

**Intermédiaire**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Description

Le nœud Fractal de **bruit structuré 3D** génère un bruit structuré *fractal* dans l&#39;espace 3D en fonction de l&#39;entrée **Carte de position**.

Ce nœud peut être testé avec [Cube 3D GBuffers](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d-gbuffers/cube-3d-gbuffers.md) en entrée au lieu d&#39;une map bakée réelle (comme illustré dans l&#39;exemple ci-dessous).

>[!WARNING]
>
> Ce bruit est destiné à être utilisé avec le *moteur GPU uniquement* (c&#39;est-à-dire **Direct3D** ou **OpenGL**). Accédez à **Outils > Changer de moteur...** ou appuyez sur la touche **F9** pour sélectionner le moteur souhaité.

</td>
</tr>
</table>

## Paramètres

* **Inverser** *Booléen*\
  Inverse l’image de sortie.
* **Échelle** *Flottant*\
  Contrôle l’échelle du bruit fractal 3D avec arête.
* **Taille** *Float3*\
  Contrôle la taille du bruit fractal 3D avec arête sur les axes **X**, **Y** et **Z**. Les valeurs non uniformes entraînent un effet d&#39;*étirement ou de compression*.
* **Décalage** *Float3*\
  Applique un décalage à la *position* du bruit fractal en 3D sur les axes **X**, **Y** et **Z**.
* **Intensité de la Distorsion** *Flottant*\
  Contrôle l&#39;intensité d&#39;un *effet de déformation* appliqué sur le bruit fractal 3D Ridged.
* **Multiplicateur D&#39;Échelle De Distorsion** *Flottant*\
  Contrôle l&#39;échelle du *motif de déformation* utilisé dans l&#39;effet de déformation contrôlé par l&#39;**intensité de la Distorsion**.
* **Niveau Min** *Nombre Entier*\
  *niveau minimum de répétition* utilisé dans le motif fractal. Une plage minimale/maximale plus large donne un motif *plus riche* avec une variation sur davantage de plages de fréquences.
* **Niveau Max** *Nombre Entier*\
  *niveau de répétition* maximum utilisé dans le motif fractal. Une plage minimale/maximale plus large donne un motif *plus riche* avec une variation sur davantage de plages de fréquences.
* **Rugosité** *Flotter*\
  Contrôle l&#39;*équilibre* entre les *niveaux de répétition* bas et élevés dans le motif fractal.\
  *Remarque* : une valeur de **0** entraîne une sortie *non conforme* à d&#39;autres valeurs faibles qui la suivent. C&#39;est ce qui est attendu.
* **Lacunarité** *Flottant*\
  Contrôle la façon dont le motif fractal appliqué *remplit l&#39;espace*. Une valeur *plus élevée* entraîne *moins d&#39;espaces* dans le motif et un bruit *plus dense*.
* **Opacité globale** *Flottant*\
  Contrôle la *plage* des valeurs de bruit fractal 3D avec arête *autour* de la **valeur de base**.
* **Ligne De Base** *Flotter*\
  Applique un *décalage* à la valeur de base de *luminance* pour la distribution de la valeur de bruit 3D Ridged.
* **Contraste** *Flottant*\
  Règle le contraste du bruit 3D avec arête.
* **Activer les limites** *booléennes*\
  Règle le bruit 3D avec arête de sorte que le motif résultant *se répète* sur les axes X, Y et Z.

## Exemples d’images

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dridgednoisefractal-variant.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dridgednoisefractal-variant2.jpg){width="256px"}

</td>
</tr>
</table>
