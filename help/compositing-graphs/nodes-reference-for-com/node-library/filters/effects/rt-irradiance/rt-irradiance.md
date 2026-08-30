---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/rt-irradiance.html"
breadcrumb-title: ''
description: Utilisez le nœud Irradiance RT pour calculer les informations d'irradiance en temps réel à partir de la géométrie pour des calculs d'éclairage réalistes.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > RT Irradiance
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Irradiance RT
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 4%

---


# Irradiance RT

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](rt-irradiance.resources/rt-irradiance.png){width="128px"}

<b>Entrée :</b> Filtres > Effets

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Génère une irradiance par lancer de rayons sur une entrée de carte d&#39;height générée à partir d&#39;une carte d&#39;environnement et d&#39;une carte émissive. Peut être utilisé pour « transformer » l’éclairage en texture à l’intérieur d’un graphique. Utilisé pour de faux éclairages et lueurs globaux.Ce nœud ne doit pas être utilisé en combinaison avec le moteur CPU (SSE) en raison du temps de calcul. Renvoie deux cartes : une sortie d&#39;irradiance où l&#39;irradiance est appliquée aux entrées de matière, une carte d&#39;irradiance brute contenant uniquement les valeurs d&#39;irradiance calculées.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Height</b> <i>Entrée en niveaux de gris</i> | L&#39;Height est la seule entrée requise de l&#39;emplacement de matériau. Sans lui, le nœud ne fonctionnera pas bien. |
| <b>Émissif</b> <i>Entrée de couleur</i> | L’Emissive doit être dans un format où le noir pur n’émet aucune lumière, toute autre valeur colorée émettant de la lumière. Alpha ignoré. Une connexion à cet emplacement ou à l&#39;emplacement de l&#39;environnement est requise pour voir le résultat. |
| <b>Environnement</b> <i>Entrée couleur</i> | Environnement d’éclairage HDR pour calculer l’irradiance avec. Une connexion à cet emplacement, ou à l&#39;emplacement Emissive, est requise pour voir le résultat. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Échelle d&#39;Height</b> <i>0.0 - 1.0</i> | Redimensionnez pour interpréter l’height à. Affecte l’aspect de toute la scène. |
| <b>Qualité</b> <i>32 rayons, 64 rayons, 128 rayons</i> | Détermine la qualité du résultat, mais affecte également les performances. Moins de rayons signifie plus de bruit. |
| <b>Calculer les rebonds</b> <i>Faux/Vrai</i> | Activer/désactiver le calcul des rebonds. Affecte la qualité et la vitesse. |
| <b>Rotation de l&#39;environnement</b> <i>0.0 - 1.0</i> | Faites pivoter l&#39;environnement autour. |
| <b>Exposition à l&#39;environnement (EV)</b> <i>-4.0 - 4.0</i> | Valeur d’exposition à utiliser pour l’environnement, qui affecte la luminosité totale de l’effet. |
| <b>Intensité émissive</b> <i>0.0 - 20.0</i> | Multiplicateur pour l&#39;entrée émissive, affecte la force d&#39;irradiation de l&#39;entrée émissive. |
| <b>Espace colorimétrique Emissive</b> <i>sRVB, linéaire</i> | Espace colorimétrique utilisé pour interpréter l’entrée Intensive. |
| <b>Ombres IBL dans l&#39;Alpha d&#39;irradiation brute</b> <i>Faux/Vrai</i> | Activez/désactivez l’option Ajouter des ombres au masque |
| <b>Biais LOD Emissive</b> <i>-1.0 - 1.0</i> | Affinez la qualité de l&#39;irradiance emissive. Une valeur faible signifie plus de bruit. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="rt-irradiance.resources/rt-irr-03-1.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="rt-irradiance.resources/rt-irr-01-1.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="rt-irradiance.resources/rt-irr-02-1.jpg" />
        </td>
    </tr>
</table>
