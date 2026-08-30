---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/technical-issues/application-does-not-start.html"
breadcrumb-title: ''
description: Résolvez les problèmes qui empêchent Substance 3D Designer de démarrer et trouvez des solutions pour lancer l’application.
helpx_creative_field: ""
helpx_description: Designer > Technical issues > Application does not start
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: L’application ne démarre pas
user-guide-description: ''
user-guide-title: ''
source-git-commit: 70bcf76fbb7c055ba9aa0b61e6975c266c8dd652
workflow-type: tm+mt
source-wordcount: '828'
ht-degree: 1%

---


# L’application ne démarre pas

Cette page répertorie les causes courantes d’échec du démarrage de Substance 3D Designer et propose des étapes de dépannage pour chacune d’elles, regroupées par système d’exploitation :

[Designer 15.0 et versions ultérieures](#version-15-0)

[Windows 10/11](#windows-10-11)

[Windows 7/8/8.1](#windows-7-8)

[Linux](#linux)

## Designer 15.0 et versions ultérieures

<b>[(erreur)](application-does-not-start.resources/error.svg) Problème</b>

Les versions 15.0 et ultérieures de Designer ne peuvent pas démarrer sur les systèmes disposant à la fois d’un GPU intégré (iGPU) et d’un GPU distinct (dGPU).

<b>[(coche)](application-does-not-start.resources/check.svg) Étapes recommandées</b>

Mettez à jour les pilotes graphiques de l’iGPU. Vous trouverez les derniers pilotes ici : [Intel](https://downloadcenter.intel.com/product/80939/Graphics-Drivers)  | [AMD](https://www.amd.com/en/support/download/drivers.html)

## Windows 10/11

**![(erreur)](application-does-not-start.resources/error.svg) Problème**

Substance 3D Designer ne démarre pas sur les systèmes utilisant Windows 10 ou Windows 11.

**![(coche)](application-does-not-start.resources/check.svg) Étapes recommandées**

Les anciennes versions de Designer peuvent ne pas démarrer sous Windows 10 ou Windows 11 en raison d&#39;une bibliothèque *obsolète* `libeay32.dll` utilisée dans le processus de validation de licence.

Vous pouvez essayer de remplacer la bibliothèque par une *version mise à jour*, telle que celle distribuée [ici](https://support.networkoptix.com/hc/en-us/articles/115015730007-Nx-Software-crashes-due-to-libeay32-dll-on-Windows) (sélectionnez le fichier pour Windows 32 bits), en procédant comme suit :

1. Localisez le fichier `libeay32.dll` dans le répertoire d&#39;installation de Designer
1. Sauvegardez le fichier dans un emplacement sûr si vous devez le restaurer à l’avenir
1. Remplacer le fichier par la version mise à jour
1. Démarrer Designer

>[!WARNING]
>
> Configurations non prises en charge
> 
> Windows 10 n’est pas pris en charge. Pour en savoir plus, consultez la page [Configuration requise](../../getting-started/system-requirements/system-requirements.md).
> 
> Les versions de Designer qui ont dépassé leur période de maintenance ne sont pas prises en charge. Ces versions peuvent ne plus fonctionner de manière fiable si des modifications importantes sont apportées au système, telles que des mises à niveau du système d’exploitation.

## Windows 7/8/8.1

**![(erreur)](application-does-not-start.resources/error.svg) Problème**

Substance 3D Designer ne démarre pas sur les systèmes utilisant Windows 7, Windows 8 ou Windows 8.1.

**![(coche)](application-does-not-start.resources/check.svg) Étapes recommandées**

Dans le cadre de la mise à jour de la version **11.3.0**, nous avons mis à niveau plusieurs bibliothèques, outils et SDK qui *n&#39;étaient plus compatibles* avec les versions de Windows antérieures à Windows 10.

Nous *recommandons vivement* la mise à niveau vers Windows 10, car Microsoft ne prend plus en charge les versions précédentes de Windows pour une utilisation grand public (voir [ici](https://www.microsoft.com/en-us/windows/windows-7-end-of-life-support-information) et [ici](https://docs.microsoft.com/en-us/lifecycle/faq/windows#windows-8.1)). Par conséquent, l&#39;utilisation continue de ces versions présente un *problème de sécurité*.\
Si la mise à niveau vers Windows 10 n&#39;est pas possible, *ne mettez pas à jour* votre installation de Designer *version antérieure* **11.2.2**.

>[!WARNING]
>
> Configurations non prises en charge
> 
> Veuillez noter que Windows 7, Windows 8 et Windows 8.1 ne sont *pas officiellement pris en charge*. Pour en savoir plus, consultez la page [Configuration requise](../../getting-started/system-requirements/system-requirements.md).

## Linux

<b>[(erreur)](application-does-not-start.resources/error.svg) Problème</b>

Blocage lors de la fermeture de l’écran d’accueil et de l’affichage de la fenêtre principale.

<b>[(coche)](application-does-not-start.resources/check.svg) Étapes recommandées</b>

Designer ne parvient pas à charger les composants Python, car il charge la bibliothèque <b>libffi.so</b> du système au lieu de la sienne.

Pour vous assurer que Designer charge sa propre bibliothèque, utilisez cette commande dans le répertoire d’installation de Designer, en remplaçant `%command%` par votre commande pour exécuter Designer :

```
LD_PRELOAD=./plugins/pythonsdk/lib/python3.11/lib-dynload/libffi.so.6 %command%
```


Veuillez noter que le numéro de version de Python dépend de la version de Designer exécutée :

* Inférieur à 14.0.0 : python3.9
* Inférieur à 12.1.0 : python3.7

+++Options de lancement de Steam
Les utilisateurs Linux qui démarrent Designer à partir de Steam peuvent définir la commande LD\_PRELOAD dans les options de lancement de Designer, comme indiqué ci-dessous.

Une fois cela fait, Designer peut être démarré à partir de Steam normalement pour toutes les sessions futures.

![Options de lancement de vapeur](application-does-not-start.resources/steam_linux_launch_option.jpg "Options de lancement de vapeur")



+++

**![(erreur)](application-does-not-start.resources/error.svg) Problème**

L’édition Steam de Designer ne démarre pas avec et ne produit aucun message d’erreur.

**![(coche)](application-does-not-start.resources/check.svg) Étapes recommandées**

Vous pouvez obtenir des messages d&#39;erreur en enregistrant l&#39;application Steam à la place.

Comme recommandé [ici](https://github.com/ValveSoftware/steam-for-linux/issues/7114#issuecomment-629634260), fermez complètement Steam, puis exécutez la commande suivante à partir d&#39;un terminal (ou créez un raccourci pour cette commande) :

```
steam 2>&1 | tee /path/to/logfile
```


<b>![(erreur)](application-does-not-start.resources/error.svg) Issu</b><b>e</b>

Impossible de charger le plug-in `<b>xcb</b>`. Le message suivant s’affiche dans la ligne de commande :

```
qt.qpa.plugin: Could not load the Qt platform plugin "xcb" in "" even though it was found. 

This application failed to start because no Qt platform plugin could be initialized. Reinstalling the application may fix this problem. 

 

Available platform plugins are: minimal, offscreen, xcb. 

 

Aborted (core dumped)
```


**![(coche)](application-does-not-start.resources/check.svg) Étapes recommandées**

Certains packages requis sont manquants. Exécutez la commande suivante à partir du répertoire d’installation de Designer :

```
ldd libQt5XcbQpa.so.5
```


Recherchez dans la liste imprimée tous les packages signalés comme `not found`, puis exécutez la commande suivante pour chacun de ces packages manquants :

```
apt-get install <package-name>
```


E.g.

```
apt-get install libxcb-xinput0
```


<b>![(erreur)](application-does-not-start.resources/error.svg) Problème</b>

Cette erreur se produit lors du démarrage de Designer :

```
error while loading shared libraries: libcrypt.so.1: cannot open shared object file: No such file or directory
```


Une bibliothèque système chargée par Designer n&#39;est pas compatible avec la bibliothèque <b>libcrypto.so.1.1</b> de Designer.

<b>![(coche)](application-does-not-start.resources/check.svg) Étapes recommandées</b>

Supprimez la bibliothèque <b>`libcrypto.so.1.1`</b> du répertoire d&#39;installation de Designer afin que la bibliothèque du système soit utilisée à la place.

>[!NOTE]
>
> Cette solution fonctionne uniquement lorsque le système dispose de sa propre bibliothèque libcrypto.so.1. Sur les distributions récentes, un package de compatibilité tel que <b>libxcrypt-compat</b> doit peut-être être installé.

<b>![(erreur)](application-does-not-start.resources/error.svg) Problème</b>

Substance 3D Designer ne démarre pas sur les systèmes utilisant des distributions Linux *basées sur Arch*.

**![(coche)](application-does-not-start.resources/check.svg) Étapes recommandées *(![(avertissement)](application-does-not-start.resources/warning.svg) instables, GPU AMD uniquement !)***

Essayez d&#39;installer **progl** (qui fait partie des pilotes [AMDGPU-PRO](https://wiki.archlinux.org/title/AMDGPU_PRO)) et démarrez Designer. Pour ce faire, vous pouvez utiliser le préfixe `progl` dans la commande de lancement de l&#39;application :

```
progl <designer-application-path>
```


N&#39;oubliez pas que `progl` peut être instable. Il convient donc de tenter cette opération en *dernier recours*.

>[!WARNING]
>
> Veuillez noter que les distributions basées sur Arch de Linux ne sont *pas prises en charge*. Pour en savoir plus, consultez la page [Configuration requise](../../getting-started/system-requirements/system-requirements.md).
