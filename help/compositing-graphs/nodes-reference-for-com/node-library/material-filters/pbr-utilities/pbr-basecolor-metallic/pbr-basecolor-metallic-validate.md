---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/pbr-basecolor-metallic-validate.html"
breadcrumb-title: ''
description: Utilisez le nœud Validation Métallique de la couleur de base PBR pour valider et corriger la couleur de base et les valeurs métalliques pour les matériaux PBR.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > PBR Utilities > PBR BaseColor  Metallic Validate
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Validation Métallique de la couleur de base PBR
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 1%

---


# PBR BaseColor / Metallic Validate

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](pbr-basecolor-metallic-validate.resources/pbr-basecolor-metallic-validate-01.png){width="128px"}

<b>Entrée :</b> Filtres de matériau > Utilitaires PBR

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Nœud d&#39;utilitaire qui génère une « carte thermique » de bonne à mauvaise dont les valeurs sont correctes ou incorrectes selon les normes PBR.

Il est très utile comme outil d&#39;apprentissage pour la PBR, car il fournit un retour visuel très clair sur les erreurs et où elles peuvent être trouvées.

N’utilisez pas cet outil comme outil final, mais assurez-vous de toujours comprendre clairement pourquoi vous enfreignez les règles mises en évidence par cet outil.

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Mode de validation</b> <i>Albédo , Métal, Combiné</i> | Permet de sélectionner uniquement le mode Albédo, Métal ou les deux en mode Présentation. |
| <b>Seuil de plage d&#39;obscurité Albédo</b> <i>50 sRVB, 30 sRVB</i> | Définit la limite inférieure d’Albédo à 50 ou 30 sRVB. Peut diminuer ou augmenter la tolérance pour les zones rouges. |
| <b>Plage de réflectance du métal</b> <i>Réflexion 70-100 %, Réflexion 60-100 %</i> | Modifications de la plage Métallique à considérer comme correctes. Peut diminuer ou augmenter la tolérance pour les zones rouges. |
| <b>Mappage d&#39;incrustation</b> <i>Faux/Vrai</i> | Le mode de débogage rapide pour superposer les maps d&#39;entrée permet un suivi plus rapide des zones problématiques. |
