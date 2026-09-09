---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/technical-issues/cannot-create-load-a-project.html"
breadcrumb-title: ''
description: Résolvez les problèmes de création ou de chargement de projets dans Substance 3D Designer et trouvez des solutions.
helpx_creative_field: ""
helpx_description: Designer > Technical issues > Cannot createload a project
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Impossible de charger un projet
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '1105'
ht-degree: 0%

---


# Impossible de créer ou charger un projet

Cette page répertorie les causes courantes d’échec de la création ou du chargement de projets dans Substance 3D Designer et propose des étapes de dépannage pour chacune d’elles.

## L’application est trop ancienne pour ouvrir l’URL

**![(erreur)](../../assets/error.svg) Problème**

Le fichier **Substance 3D (SBS)** est chargé par une version de Substance 3D Designer qui *ne prend pas en charge son format*. Le fichier Substance 3D a probablement été *enregistré dans une version plus récente* du logiciel qui utilise un format mis à jour pour ces fichiers.

**![(coche)](../../assets/check.svg) Étapes recommandées**

Le format de fichier Substance 3D (SBS) évolue au même rythme que Substance 3D Designer. Le plus souvent, une nouvelle version du logiciel devra *mettre à jour vos fichiers* afin qu&#39;ils puissent prendre en charge les dernières fonctionnalités.

Vous *êtes invité* à effectuer cette mise à jour lors du *chargement du fichier pour la première fois* dans une nouvelle version.

>[!WARNING]
>
> Si le fichier est enregistré *après* l&#39;application de la mise à jour, sa version de format change également. À ce stade, il ne peut *plus être chargé dans les versions précédentes* de Substance 3D Designer.
> 
> Cette limitation s&#39;applique également à la [Substance Player](https://helpx.adobe.com/substance-3d-player/home.html).

Vérifiez d’abord que vous utilisez la dernière version de Substance 3D Designer autorisée par votre licence actuelle. Voici les points d&#39;accès aux mises à jour pour chaque édition :

* <b>Abonnement Substance 3D Adobe :</b> accédez à la section Mises à jour de l&#39;onglet Applications dans l&#39;application [Adobe Creative Cloud pour poste de travail](https://creativecloud.adobe.com/en/apps/download/creative-cloud)
* Abonnement <b>[Substance 3d.com](http://Substance3d.com) :</b> effectuez la mise à jour lorsque vous y êtes invité dans Substance 3D Designer, ou téléchargez le dernier programme d&#39;installation dans la section [Mes licences](https://store.substance3d.com/user) du site web [Substance 3d.com](http://substance3d.com)
* <b>Flux :</b> l&#39;application se mettra à jour automatiquement par défaut. Vous pouvez déclencher manuellement la mise à jour en démarrant Substance 3D Designer ou en accédant à l’écran Téléchargements

>[!WARNING]
>
> Assurez-vous que vous n&#39;aurez pas besoin de charger vos fichiers dans une version précédente de Substance 3D Designer *avant d&#39;enregistrer* un fichier qui a été mis à jour.
> 
> Vous pouvez également *faire une copie* de votre fichier *avant* de le charger dans une nouvelle version de Substance 3D Designer, afin de toujours avoir un fichier vers lequel revenir si vous devez utiliser une version précédente du logiciel.

## Blocage lors de la création ou du chargement d’un projet

<b> ![(error)](../../assets/error.svg) Problème</b>

Un crash lors de la création ou du chargement d&#39;un projet est souvent causé par une erreur lors de l&#39;initialisation de la [Vue 3D](../../interface/3d-view/3d-view.md), qui se produit lors de la configuration de l&#39;espace de travail.

Si le système est un ordinateur portable, une application tierce peut appliquer un *plan de gestion de l&#39;alimentation* qui empêche la vue 3D d&#39;utiliser le GPU du système. Cela peut entraîner un crash si aucun autre périphérique GPU ne peut effectuer la tâche à sa place.

Un crash peut également se produire lorsque la configuration ou la mise à l&#39;échelle *d&#39;affichage* a été modifiée entre les sessions, de sorte que l&#39;image de rendu de la vue 3D est créée à des coordonnées non valides.

<b> ![(tick)](../../assets/check.svg) Étapes recommandées</b>

Compte tenu des multiples causes possibles de ce blocage, nous vous suggérons de suivre les étapes de dépannage suivantes dans l’ordre :

Mettre à jour les pilotes graphiques

Tout d’abord, vérifiez que les pilotes graphiques sont à jour. Vous pouvez trouver la dernière version de votre GPU [ici](https://www.nvidia.com/Download/index.aspx?lang=en-us) (NVIDIA), [ici](https://www.amd.com/en/support) (AMD) ou [ici](https://downloadcenter.intel.com/product/80939/Graphics-Drivers) (Intel).

Forcer les meilleures performances

Recherchez tout logiciel qui gère la *formule d&#39;alimentation* de votre système (par exemple, ASUS Armory Crate), en particulier lorsque le système est un ordinateur portable.

Certaines applications de gestion de l’alimentation peuvent limiter l’accès d’autres applications au GPU du système ou nuire aux performances du GPU, ce qui peut entraîner des blocages. Si une application de gestion de l&#39;alimentation existe et est active, passez au mode qui offre les meilleures performances.

Forcer l’utilisation d’un GPU discret

Si votre système dispose de *cartes graphiques commutables*, envisagez d’imposer l’utilisation du GPU distinct (dGPU) pour les applications Substance 3D.

Dans la plupart des cas, cela est réalisé dans une application dédiée qui contrôle les paramètres GPU. Par exemple, pour les GPU NVIDIA, vous pouvez le faire dans l’application « Panneau de configuration NVIDIA ».

Réinitialiser l’interface utilisateur enregistrée dans le registre

Si le blocage est dû à une modification de la configuration d’affichage ou de la mise à l’échelle, vous pouvez tenter de supprimer les entrées de registre de Designer pour réinitialiser entièrement l’interface utilisateur, entre autres paramètres.

La procédure permettant d’effectuer cette réinitialisation par système d’exploitation est décrite ci-dessous :

+++Windows
* Fermer Designer

Fermer Designer

* Ouvrez l&#39;application <b>Invite de commandes</b>

Ouvrez l&#39;application <b>Invite de commandes</b>

* Entrez la commande suivante et appuyez sur <b>Entrée</b> :

  <b>Creative Cloud Desktop</b>

  ```
  reg delete "HKEY_CURRENT_USER\Software\Adobe\Adobe Substance 3D Designer" /f
  ```


  <b>Édition vapeur/Substance</b>

  ```
  reg delete "HKEY_CURRENT_USER\Software\Allegorithmic\Substance Designer" /f
  ```


Entrez la commande suivante et appuyez sur <b>Entrée</b> :

<b>Creative Cloud Desktop</b>

<b>Édition vapeur/Substance</b>

* Déconnectez le deuxième moniteur de votre système et reconnectez-le (ignorez cette étape si *plusieurs écrans ne sont pas* connectés)

Déconnectez le deuxième moniteur de votre système et reconnectez-le (ignorez cette étape si *plusieurs écrans ne sont pas* connectés)

* Démarrez Designer, mais ne *créez ou n’ouvrez aucun projet*

Démarrez Designer, mais ne *créez ou n’ouvrez aucun projet*

* Dans la barre supérieure, ouvrez le menu <b>Windows</b> et sélectionnez l&#39;option <b>Nouvelle vue 3D</b>

Dans la barre supérieure, ouvrez le menu <b>Windows</b> et sélectionnez l&#39;option <b>Nouvelle vue 3D</b>

* Vérifiez que la <b>vue 3D</b> est correctement initialisée et essayez différents maillages d&#39;aperçu dans le menu <b>Scène</b> de la barre supérieure du panneau

Vérifiez que la <b>vue 3D</b> est correctement initialisée et essayez différents maillages d&#39;aperçu dans le menu <b>Scène</b> de la barre supérieure du panneau

* Création ou ouverture d’une matière

Création ou ouverture d’une matière

+++

+++macOS
* Fermer Designer

Fermer Designer

* Ouvrez l&#39;application <b>Terminal</b>

Ouvrez l&#39;application <b>Terminal</b>

* Entrez la commande suivante et appuyez sur <b>Entrée</b> :

  <b>Creative Cloud Desktop</b>

  ```
  rm ~/Library/Preferences/com.adobe.Adobe\ Substance\ 3D\ Designer.plist
  ```


  <b>Édition vapeur/Substance</b>

  ```
  rm ~/Library/Preferences/com.allegorithmic.Substance\ Designer.plist
  ```


Entrez la commande suivante et appuyez sur <b>Entrée</b> :

<b>Creative Cloud Desktop</b>

<b>Édition vapeur/Substance</b>

* Déconnectez le deuxième moniteur de votre système et reconnectez-le (ignorez cette étape si *plusieurs écrans ne sont pas* connectés)

Déconnectez le deuxième moniteur de votre système et reconnectez-le (ignorez cette étape si *plusieurs écrans ne sont pas* connectés)

* Démarrez Designer, mais ne *créez ou n’ouvrez aucun projet*

Démarrez Designer, mais ne *créez ou n’ouvrez aucun projet*

* Dans la barre supérieure, ouvrez le menu <b>Windows</b> et sélectionnez l&#39;option <b>Nouvelle vue 3D</b>

Dans la barre supérieure, ouvrez le menu <b>Windows</b> et sélectionnez l&#39;option <b>Nouvelle vue 3D</b>

* Vérifiez que la <b>vue 3D</b> est correctement initialisée et essayez différents maillages d&#39;aperçu dans le menu <b>Scène</b> de la barre supérieure du panneau

Vérifiez que la <b>vue 3D</b> est correctement initialisée et essayez différents maillages d&#39;aperçu dans le menu <b>Scène</b> de la barre supérieure du panneau

* Création ou ouverture d’une matière

Création ou ouverture d’une matière

+++
