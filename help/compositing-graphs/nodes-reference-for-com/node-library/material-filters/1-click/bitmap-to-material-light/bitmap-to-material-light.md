---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/1-click/bitmap-to-material-light.html"
breadcrumb-title: ''
description: Utilisez le nœud Bitmap en Matériau de lumière pour convertir rapidement des images bitmap en matériaux avec un éclairage optimisé pour des workflows rapides.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > 1-Click > Bitmap to Material Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Bitmap en lumière Matériau
user-guide-description: ''
user-guide-title: ''
source-git-commit: caf740432682ed82eb55ad2f84bc9dd6ed15ad14
workflow-type: tm+mt
source-wordcount: '517'
ht-degree: 11%

---


# Bitmap en lumière Matériau

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](bitmap-to-material-light.resources/b2m-light.png)

<b>Entrée :</b> Filtres de matériau > En un clic

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Ce nœud convertit une seule entrée Diffuse/Couleur de base en un matériau complet. En tant que version simple et « légère » du Matériau Bitmap2 d’[Allegorithmic à part entière, qui peut être acheté séparément](https://www.allegorithmic.com/products/bitmap2material), elle vous donne un aperçu de la version complète. Cela peut bien fonctionner dans les cas les plus simples.

Bien qu&#39;il ne soit pas garanti que les matériaux soient parfaits et corrects pour le PBR, c&#39;est un bon moyen rapide de commencer si vous n&#39;avez qu&#39;une seule image et que vous voulez un matériau complet.

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Canaux</b> | Active et désactive les canaux de matériau dans ce groupe, par exemple lors de l’utilisation de cartes de Specular/Brillance au lieu de cartes Métallique/Rugosité. |
| <b>Global</b> |  |
| <b>Balance des Profondeurs</b> <i>-1.0 - 1.0</i> | Définit un biais/décalage pour la carte de hauteur. |
| <b>Diffuse</b> |  |
| <b>Netteté</b> <i>0.0 - 1.0</i> | Ajoute de la netteté au résultat de diffusion. |
| <b>Teinte</b> <i>0.0 - 1.0</i> | Les Tint diffusent avec un décalage de teinte sélectionné par l’utilisateur. |
| <b>Saturation</b> <i>0.0 - 1.0</i> | Modifie la saturation du résultat du Diffuse. |
| <b>Luminosité</b> <i>0.0 - 1.0</i> | Règle la luminosité du résultat du Diffuse. |
| <b>Contraste</b> <i>-1.0 - 1.0</i> | Règle le contraste du résultat. |
| <b>Relief</b> | Le groupe Relief contrôle les sorties Normal et Height. |
| <b>Format Normal De Sortie</b> <i>DirectX, OpenGL</i> | Bascule entre les formats normaux (bascule en vert). |
| <b>Inverser le Relief généré</b> <i>Faux/Vrai</i> | Inverse l&#39;interprétation de l&#39;height. |
| <b>Force normale</b> <i>0.0 - 20.0</i> | Définit la force du mappage normal généré. |
| <b>Égaliseur de Reliefs</b> <i>0.0 - 1.0</i> | Définit les soldes de conversion pour différentes échelles de détail. |
| <b>Intensité du pincement</b> <i>0.0 - 1.0</i> | Rend les transitions normales plus nettes. Ajoute un filtre de netteté avant de passer à la normale, ce qui rend les contours plus prononcés. |
| <b>Netteté normale</b> <i>0.0 - 1.0</i> | Accentue la texture normale après la conversion, fait ressortir les détails. |
| <b>Adoucissement normal</b> <i>0.0 - 1.0</i> | Adoucit Normalmap après la conversion, masque les détails. |
| <b>Specular</b> |  |
| <b>Influence du Specular</b> <i>0.0 - 1.0</i> | Définit l’influence de la diffusion sur le Specular. Affecte également la Brillance et les sorties de Rugosité. |
| <b>Saturation du Specular</b> <i>0.0 - 1.0</i> | Modifie la saturation de la sortie Specular. |
| <b>Netteté Specular</b> <i>0.0 - 1.0</i> | Accentue la netteté de la sortie Specular. |
| <b>Speculars level entrants</b> <i>0.0 - 1.0</i> | Définit les niveaux d’entrée pour l’interprétation du Specular. |
| <b>Speculars level sortants</b> <i>0.0 - 1.0</i> | Modifie les niveaux de sortie du Specular. |
| <b>Influence Métallique du Specular</b> <i>0.0 - 1.0</i> | Détermine l’influence de l’entrée Métallique facultative sur le mappage Specular. |
| <b>Brillance</b> |  |
| <b>Niveaux De Brillance Dans</b> <i>0.0 - 1.0</i> | Définit les niveaux d’entrée pour l’interprétation des Brillances. |
| <b>Niveaux De Brillance Sortants</b> <i>0.0 - 1.0</i> | Modifie les niveaux de sortie de la Brillance. |
| <b>Influence Métallique de la Brillance</b> <i>0.0 - 1.0</i> | Détermine l&#39;influence de l&#39;entrée Métallique facultative sur la carte de Brillance. |
| <b>Rugosité</b> |  |
| <b>Niveaux De Rugosité Dans</b> <i>0.0 - 1.0</i> | Définit les niveaux d’entrée pour l’interprétation des Rugosités. |
| <b>Niveaux De Rugosité Sortants</b> <i>0.0 - 1.0</i> | Modifie les niveaux de sortie de la Rugosité. |
| <b>Influence de la Métallique rugosité</b> <i>0.0 - 1.0</i> | Détermine l&#39;influence de l&#39;entrée Métallique facultative sur la carte de Brillance. |
| <b>Ambient occlusion</b> |  |
| <b>Ambient occlusion Dans Diffuse</b> <i>0.0 - 1.0</i> | Fusions dans l’AO généré dans la sortie de Diffuse. |
| <b>Planche Ambient occlusion</b> <i>0.0 - 1.0</i> | Définit la distance de propagation de l’IA générée. |
| <b>Distance De Lumière De L&#39;Ambient occlusion</b> <i>0.0 - 1.0</i> | Définit l’interprétation de la « profondeur » AO. A moins d’influence lorsqu’il existe une Planche importante. |
| <b>Angle de lumière Ambient occlusion</b> <i>0.0 - 1.0</i> | Définit l’angle de convertit AO du faux éclairage. Peut être utilisé pour compenser tout AO directionnel déjà présent dans le Diffuse, s’il est défini sur un angle opposé. |
| <b>Niveaux D&#39;Ambient occlusion</b> <i>0.0 - 1.0</i> | Modifie les niveaux de sortie AO. |
