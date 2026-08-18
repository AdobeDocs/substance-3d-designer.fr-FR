---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/mdl-graphs/warnings-in-mdl-graphs.html"
breadcrumb-title: ''
description: Comprendre et résoudre les avertissements dans les graphiques MDL pour garantir une définition et un rendu de matériau corrects.
helpx_creative_field: ""
helpx_description: Designer > MDL graphs > Warnings in MDL graphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Avertissements dans les graphiques MDL
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '1001'
ht-degree: 0%

---


# Avertissements dans les graphiques MDL

Cette page répertorie les messages d&#39;avertissement et d&#39;erreur qui peuvent être déclenchés par les graphiques MDL dans [Substance 3D Designer](https://www.adobe.com/fr/products/substance3d-designer.html), et propose des étapes de dépannage courantes pour chacun d&#39;eux.

Les avertissements sont affichés dans l&#39;infobulle de l&#39;icône d&#39;avertissement pour la ressource de graphique dans le panneau [Explorateur](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/the-explorer-129368147.html), ainsi que dans le coin inférieur gauche de la [vue graphique](../../interface/the-graph-view/the-graph-view.md) si le graphique est chargé.

>[!NOTE]
>
> Les illustrations de cette section ont été enregistrées dans des <b>graphiques de Substances de données</b>, qui ont été *retirés* dans la version <b>13.0.0</b> de Substance 3D Designer. Cependant, ils s’appliquent également aux graphiques MDL.

## ![(erreur)](../../assets/error.svg) Aucun nœud de sortie défini

Aucun nœud de sortie n’est défini pour le graphique.

<b> ![(tick)](../../assets/check.svg) Solution</b>

Sélectionnez un nœud dans le graphique qui génère une valeur dont le type correspond au type attendu pour cette fonction, le cas échéant, puis cliquez sur RMB et sélectionnez l&#39;option <b>Définir comme racine</b> dans le menu contextuel ou double-cliquez sur LMB sur le nœud.\
Le nœud de sortie d&#39;un graphique de modèle de Substance est coloré en *orange*.

![&#39;Aucune solution de nœud de sortie définie&#39;](../../assets/warnings-model-output.gif "&#39;Aucune solution de nœud de sortie définie&#39;")

### ![(erreur)](../../assets/error.svg) Au moins une valeur d&#39;entrée a été rejetée

La valeur fournie pour un paramètre n&#39;entraîne pas un calcul valide du nœud.

<b> ![(tick)](../../assets/check.svg) Solution</b>

Ajustez la valeur afin qu’elle soit logique pour le paramètre cible.

![&#39;Au moins une valeur d&#39;entrée a été rejetée&#39; solution](../../assets/warnings-model-rejected-value.gif "&#39;Au moins une valeur d&#39;entrée a été rejetée&#39; solution")

### ![(erreur)](../../assets/error.svg) Aucune valeur d&#39;entrée

Une valeur d&#39;entrée attendue par un nœud pour effectuer son calcul n&#39;est pas fournie.

<b> ![(tick)](../../assets/check.svg) Solution</b>

Certains paramètres de nœud ne peuvent pas revenir à une valeur par défaut lorsqu&#39;aucune donnée n&#39;est fournie à leur connecteur d&#39;entrée. C’est souvent le cas pour les entrées Scène.

Connectez les entrées de nœud au connecteur de sortie d&#39;un autre nœud de type correspondant.

![&#39;Aucune valeur d&#39;entrée&#39; solution](../../assets/warnings-model-no-input-value.gif "&#39;Aucune valeur d&#39;entrée&#39; solution")

### Le nœud ![(erreur)](../../assets/error.svg) n&#39;a pas été calculé

Les informations fournies au nœud sont incomplètes ou non valides, le nœud n&#39;a donc pas pu effectuer ses calculs.

<b> ![(tick)](../../assets/check.svg) Solution</b>

Montez en amont dans le graphique et recherchez les avertissements déclenchés par des problèmes qui empêchent les nœuds de fournir une sortie valide.

![&#39;Le nœud n&#39;était pas calculé&#39; solution](../../assets/warnings-model-no-input-value.gif "&#39;Le nœud n&#39;était pas calculé&#39; solution")

### ![(erreur)](../../assets/error.svg) Les données référencées comportent des avertissements

La ressource référencée par un nœud comporte un ou plusieurs avertissements. Voici quelques nœuds référençant une ressource :

* Un nœud d&#39;instance de graphe référence un graphe
* Un nœud de ressource Scène référence une ressource de scène 3D bitmap

<b> ![(tick)](../../assets/check.svg) Solution</b>

Dans le panneau Explorateur, recherchez la ressource référencée et résolvez tous les avertissements déclenchés par la ressource :

* Pour les graphiques, reportez-vous aux autres éléments de cette page
* Pour tout autre type de ressource, reportez-vous à la page Avertissements des dépendances

![&#39;Les données référencées ont la solution de certains avertissements](../../assets/warnings-model-referenced-data.gif "&#39;Les données référencées ont la solution de certains avertissements")

### ![(erreur)](../../assets/error.svg) ressource référencée introuvable

La ressource référencée par un nœud est introuvable au chemin d&#39;accès enregistré dans le fichier Substance 3D (SBS). Voici quelques nœuds référençant une ressource :

* Un nœud d&#39;instance de graphe référence un graphe
* Un nœud de ressource Scène référence une ressource de scène 3D bitmap

<b> ![(tick)](../../assets/check.svg) Solution</b>

Pour les nœuds d’instance de graphe

Vérifiez que le graphique source existe dans le package situé au chemin enregistré dans leur attribut <b>Package</b>.\
Si ce n&#39;est pas le cas, supprimez le nœud d&#39;instance et remplacez-le par un nœud d&#39;instance référençant un package valide. Vous pouvez également recréer le package et le graphique référencés par le nœud d&#39;instance, puis recharger le package hôte en cliquant sur *RMB* dans le panneau [Explorateur](https://substance3d.adobe.com/documentation/display/DRAFTDESIGNER/.The+Explorer+window+vDraftVersion) et en sélectionnant l&#39;option <b>Recharger</b> dans le menu contextuel.

Pour les nœuds de ressource Scène

Recherchez les ressources référencées dans le panneau [Explorateur](https://substance3d.adobe.com/documentation/display/DRAFTDESIGNER/.The+Explorer+window+vDraftVersion) et vérifiez qu&#39;elles existent à l&#39;emplacement enregistré dans leur attribut <b>Chemin d&#39;accès</b>.\
Si ce n&#39;est pas le cas, cliquez sur *RMB* sur l&#39;élément de ressource dans l&#39;Explorateur et sélectionnez <b>Déplacer...Option </b> dans le menu contextuel pour définir un nouveau fichier cible valide pour cette ressource.

![&#39;Ressource référencée introuvable&#39; solution](../../assets/warnings-model-referenced-resource.gif "&#39;Ressource référencée introuvable&#39; solution")

### ![(erreur)](../../assets/error.svg) La plage souple ne contient pas la valeur

La valeur par défaut d&#39;un paramètre exposé n&#39;est pas incluse dans la plage paramétrée définie pour ce paramètre.

<b> ![(tick)](../../assets/check.svg) Solution</b>

Ajustez la valeur par défaut ou la plage adoucie afin d’inclure la première dans la seconde.

>[!NOTE]
>
> Cet avertissement ne peut pas être déclenché via l&#39;interface utilisateur, car il *ajuste automatiquement* la plage souple pour inclure la valeur par défaut. Seule la modification des données dans le fichier Substance 3D (SBS) *directement* peut déclencher cet avertissement.

La plage souple ![ ne contient pas la valeur « solution ](../../assets/warnings-model-ranges.gif " » La plage souple ne contient pas la valeur « solution ") »

### ![(erreur)](../../assets/error.svg) La plage souple est hors de la plage fixe

La plage paramétrée et le paramètre exposé ne sont pas entièrement inclus dans la plage fixe définie pour ce paramètre.

<b> ![(tick)](../../assets/check.svg) Solution</b>

Ajustez la plage souple ou la plage stricte de sorte que la première soit entièrement incluse dans la seconde.

>[!NOTE]
>
> Cet avertissement ne peut pas être déclenché via l&#39;interface utilisateur, car il *ajuste automatiquement* la plage souple pour qu&#39;elle soit entièrement incluse dans la plage dure. Seule la modification des données dans le fichier Substance 3D (SBS) *directement* peut déclencher cet avertissement.

![&#39;La plage souple est hors de la plage dure&#39; solution](../../assets/warnings-model-ranges.gif "&#39;La plage souple est hors de la plage dure&#39; solution")

### ![(erreur)](../../assets/error.svg) La valeur est hors limites

La valeur par défaut d&#39;un paramètre exposé n&#39;est pas incluse dans la plage fixe définie pour ce paramètre.

<b> ![(tick)](../../assets/check.svg) Solution</b>

Ajustez la valeur par défaut ou la plage fixe de manière à inclure la première dans la seconde.

>[!NOTE]
>
> Cet avertissement ne peut pas être déclenché via l&#39;interface utilisateur, car il *ajuste automatiquement* la valeur par défaut à inclure dans la plage fixe. Seule la modification des données dans le fichier Substance 3D (SBS) *directement* peut déclencher cet avertissement.

![&#39;La valeur est hors plage&#39; solution](../../assets/warnings-model-ranges.gif "&#39;La valeur est hors plage&#39; solution")
