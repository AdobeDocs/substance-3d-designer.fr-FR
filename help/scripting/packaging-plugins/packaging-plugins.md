---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/scripting/packaging-plugins.html"
breadcrumb-title: ''
description: Découvrez comment créer des packs de plug-ins Python pour Substance 3D Designer à des fins de distribution et d’installation.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Packaging plugins
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Assemblage de plug-ins
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 3%

---


# Assemblage de plug-ins

## Contenu du pack de plug-ins

Les packages sont un fichier unique, en interne une archive zip, contenant un fichier **pluginInfo.json** avec des métadonnées sur le plug-in,

le code du plug-in et tous les autres fichiers ou ressources nécessaires au fonctionnement du plug-in.

**Entrées PluginInfo.json :**

| Entrée | Description | Valeur par défaut | Notes |
| --- | --- | --- | --- |
| metadata\_format\_version | Format du fichier de métadonnées. | 1 | Obligatoire.Actuellement doit être défini sur 1. |
| nom | Nom du plug-in. |  | Obligatoire. Doit correspondre au nom du module Python contenant le code du plug-in |
| version | Version du plug-in. |  | Facultatif. |
| auteur | Auteur du plug-in. |  | Facultatif. |
| e-mail | Adresse e-mail de l’auteur du plug-in. |  | Facultatif. |
| min\_designer\_version | Version minimale de l’application requise par le plug-in pour fonctionner. | 2019.2 | Facultatif. |
| plate-forme | Plate-forme sur laquelle le plug-in s’exécute. | tout | Facultatif. Pour les plug-ins contenant du code compilé, cette entrée peut être utilisée pour désactiver le plug-in sur des plateformes non prises en charge.Valeurs possibles : win, linux, osx, any. |

## Création d’un projet de pack de plug-ins

Nous fournissons un projet de modèle [Cookiecutter](https://cookiecutter.readthedocs.io/en/latest/) pour simplifier la création de projets de pack de plug-ins.

Vous pouvez l’utiliser directement ou le modifier selon vos propres besoins.

Le modèle se trouve dans le répertoire de l&#39;application, sous <b>plugins/tools/pkgplugintemplate</b>.

1. <b>Installez Python s&#39;il n&#39;est pas déjà installé sur votre système</b>

   Cookiecuter est compatible avec Python 2 et Python 3
1. <b>Installez Cookiecutter si ce n&#39;est pas déjà fait</b>

   Habituellement, cela peut être fait en utilisant pip :

   ```
   pip install cookiecutter
   ```


   Pour d&#39;autres méthodes d&#39;installation de Cookiecutter ou pour plus d&#39;informations sur Cookiecutter, consultez la documentation à l&#39;adresse <https://cookiecutter.readthedocs.io/en/latest/installation.html>
1. <b>Créer un projet de pack de plug-ins</b>

   Dans une exécution de fenêtre de terminal :

   ```
   cookiecutter path/to/pkgplugintemplate -o path/to/new/project
   ```


   Renseignez les informations requises. Le nouveau projet sera créé dans le répertoire spécifié.
1. <b>Créez un pack pour votre plug-in une fois le développement terminé</b>

   Dans une exécution de fenêtre de terminal :

   ```
   python makepackage.py
   ```

1. Le pack de plug-ins sera généré dans le répertoire de build
