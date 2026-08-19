---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/getting-started/activation-and-licenses.html"
breadcrumb-title: ''
description: Découvrez comment activer Substance 3D Designer et gérer les licences pour accéder à toutes les fonctionnalités et capacités.
helpx_creative_field: ""
helpx_description: Designer > Getting started > Activation and licenses
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Activation et licences
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '434'
ht-degree: 1%

---


# Processus d’activation par type d’application

Le processus d’activation dépend de l’endroit où vous avez acheté ou accédé à Designer :

| Edition | Processus d’activation |
| --- | --- |
| Application pour poste de travail Creative Cloud | Voir la page dédiée dans la [documentation HelpX](https://helpx.adobe.com/fr/support/substance-3d-designer.html). En cas de problème, la [documentation du Creative Cloud](https://helpx.adobe.com/fr/creative-cloud/user-guide.html) peut fournir des réponses supplémentaires. |
| Vapeur | Lancez le produit directement depuis votre bibliothèque Steam. |
| Substance (autonome) | Voir le processus d’activation décrit ci-dessous. |

## Étapes d’activation (édition Substance)

### UTILISATION DE L’ASSISTANT D’ACTIVATION

Trois choix s&#39;offrent à vous :

* <b>Évaluer ce produit</b> : les versions d&#39;évaluation héritées ne sont plus disponibles. Vous pouvez à la place commencer une version d&#39;essai de 30 jours pour chaque application Substance 3D [ici](https://www.adobe.com/creativecloud/3d-augmented-reality.html) ou avec Creative Cloud Desktop. Chaque version d’essai est indépendante des autres applications Substance 3D, vous pouvez donc les tester une par une ou toutes à la fois.
* <b>Activer à l&#39;aide d&#39;un fichier de licence</b> : activez le produit avec un fichier de licence (<b>\*.key</b>) téléchargé à partir de la page de votre compte sur le [site web Substance 3D](https://store.substance3d.com/user) avant le 30 septembre 2022.
* <b>Activer à l&#39;aide de votre compte</b> : les comptes Substance hérités ne peuvent plus être utilisés pour l&#39;activation. [Plus d&#39;informations sur les comptes de Substance de données sont disponibles ici](https://helpx.adobe.com/fr/substance-3d/unlisted/faq-end-of-life-accounts.html).

>[!IMPORTANT]
>
> Pour installer le fichier de licence avec l’Assistant d’activation, assurez-vous d’exécuter Designer en tant qu’administrateur et de désactiver temporairement votre antivirus.

![Assistant d&#39;activation](../../assets/activation-wizard.png "Assistant d&#39;activation")

### Activation manuelle

Vous pouvez activer manuellement Designer en plaçant le fichier license.key dans le dossier suivant :

<table data-preserve-html="true">
<colgroup> <col/> <col/> <col/> <col/> </colgroup><tbody><tr><th style="text-align: left;">Plateforme</th>
<th style="text-align: left;">Version</th>
<th colspan="2" style="text-align: left;">Chemin</th>
</tr><tr><td rowspan="4" style="text-align: left;"><b>Windows</b></td>
<td rowspan="2" style="text-align: left;"><b>11.2</b> ou version ultérieure</td>
<td style="text-align: left;">AppData &gt; Local</td>
<td style="text-align: left;">C:\Users\[nom d’utilisateur]\AppData\Local\Adobe\Adobe Substance 3D Designer</td>
</tr><tr><td style="text-align: left;">AppData &gt; Itinérance</td>
<td style="text-align: left;">C:\Users\[nom d’utilisateur]\AppData\Roaming\Adobe\Adobe Substance 3D Designer</td>
</tr><tr><td rowspan="2" style="text-align: left;"><b>11.1</b> ou version antérieure</td>
<td style="text-align: left;">AppData &gt; Local</td>
<td style="text-align: left;">C:\Users\[nom d’utilisateur]\AppData\Local\Allegorithmic\Substance Designer</td>
</tr><tr><td style="text-align: left;">AppData &gt; Itinérance</td>
<td style="text-align: left;">C:\Users\[nom d’utilisateur]\AppData\Roaming\Allegorithmic\Substance Designer</td>
</tr><tr><td rowspan="2" style="text-align: left;"><b>Mac</b></td>
<td style="text-align: left;"><b>11.2</b> ou version ultérieure<br/>
</td>
<td colspan="2" style="text-align: left;">/Users/[nom d’utilisateur]/Library/Application Support/Adobe/Adobe Substance 3D Designer</td>
</tr><tr><td style="text-align: left;"><b>11.1</b> ou version antérieure<br/>
</td>
<td colspan="2" style="text-align: left;">/Users/[nom d’utilisateur]/Library/Application Support/Allegorithmic/Substance Designer</td>
</tr><tr><td rowspan="2" style="text-align: left;"><b>Linux</b></td>
<td style="text-align: left;"><b>11.2</b> ou version ultérieure</td>
<td colspan="2" style="text-align: left;">/home/[nom d’utilisateur]/.local/share/Adobe/Adobe Substance 3D Designer</td>
</tr><tr><td style="text-align: left;"><b>11.1</b> ou version antérieure<br/>
</td>
<td colspan="2" style="text-align: left;">/home/[nom d’utilisateur]/.local/share/Allegorithmic/Substance Designer</td>
</tr></tbody></table>

>[!NOTE]
>
> Certains des répertoires dans les chemins mentionnés ci-dessus peuvent être masqués par défaut. Saisissez le chemin manuellement dans l’explorateur de fichiers ou affichez les fichiers masqués pour les afficher.

>[!IMPORTANT]
>
> Assurez-vous que le fichier s&#39;appelle **license.key**, sinon l&#39;application ne pourra pas le trouver.

### VARIABLE D’ENVIRONNEMENT

Vous pouvez remplacer l&#39;emplacement que Designer recherche pour le fichier <b>license.key</b> par une [variable d&#39;environnement](../../pipeline-and-project-con/environment-variables/environment-variables.md).
