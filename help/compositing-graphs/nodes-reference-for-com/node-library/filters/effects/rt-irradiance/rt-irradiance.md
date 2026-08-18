---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/rt-irradiance.html"
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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 1%

---


# Irradiance RT

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/rt-irradiance.png){width="128px"}

**Entrée :** *Filtres/Effets*

**Complexe**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Description

Génère une irradiance par lancer de rayons sur une entrée de carte d&#39;height générée à partir d&#39;une carte d&#39;environnement et d&#39;une carte émissive. Peut être utilisé pour « transformer » l’éclairage en texture à l’intérieur d’un graphique. Utilisé pour de faux éclairages et lueurs globaux.Ce nœud ne doit pas être utilisé en combinaison avec le moteur CPU (SSE) en raison du temps de calcul. Renvoie deux cartes : une sortie d&#39;irradiance où l&#39;irradiance est appliquée aux entrées de matière, une carte d&#39;irradiance brute contenant uniquement les valeurs d&#39;irradiance calculées.

</td>
</tr>
</table>

## Paramètres

### Entrées

* **Height :** *Entrée en niveaux de gris* L&#39;Height est la seule entrée requise à partir de l&#39;emplacement Matériau. Sans lui, le nœud ne fonctionnera pas bien.
* **Émissif :** *L&#39;entrée de couleur*&#x200B;Émissif doit être dans un format où le noir pur n&#39;émet pas de lumière, toute autre valeur colorée émet de la lumière. Alpha ignoré. Une connexion à cet emplacement ou à l&#39;emplacement de l&#39;environnement est requise pour voir le résultat.
* **Environnement** : *Entrée Couleur*\
  Environnement d’éclairage HDR pour calculer l’irradiance avec. Une connexion à cet emplacement, ou à l&#39;emplacement Emissive, est requise pour voir le résultat.

### Paramètres

* **Échelle D&#39;Height** : *0.0 - 1.0*\
  Redimensionnez pour interpréter l’height à. Affecte l’aspect de toute la scène.
* **Qualité** : *32 rayons, 64 rayons, 128 rayons*\
  Détermine la qualité du résultat, mais affecte également les performances. Moins de rayons signifie plus de bruit.
* **Rebonds de calcul** : *Faux/Vrai*\
  Activer/désactiver le calcul des rebonds. Affecte la qualité et la vitesse.
* **Rotation de l&#39;environnement** : *0.0 - 1.0*\
  Faites pivoter l&#39;environnement autour.
* **Exposition à l’environnement (EV)** : *-4.0 - 4.0*\
  Valeur d’exposition à utiliser pour l’environnement, qui affecte la luminosité totale de l’effet.
* **Intensité émissive** : *0.0 - 20.0*\
  Multiplicateur pour l&#39;entrée émissive, affecte la force d&#39;irradiation de l&#39;entrée émissive.
* **Espace colorimétrique émissif** : *sRVB, linéaire*\
  Espace colorimétrique utilisé pour interpréter l’entrée Intensive.
* **Ombres IBL dans l&#39;Alpha d&#39;irradiation brute** : *Faux/Vrai*\
  Activez/désactivez l’option Ajouter des ombres au masque
* **Biais de charge émissive** : *-1.0 - 1.0* Qualité du réglage de l&#39;irradiance émissive. Une valeur faible signifie plus de bruit.

## Exemples d’images

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/rt-irr-03-1.jpg" width="300px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c1_image" src="../../../../../../assets/rt-irr-01-1.jpg" width="300px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c2_image" src="../../../../../../assets/rt-irr-02-1.jpg" width="300px"/></div> |
| --- | --- | --- |
|  |  |  |
