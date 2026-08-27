---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/scripting/using-color-management.html"
breadcrumb-title: ''
description: Découvrez comment utiliser les fonctionnalités de gestion des couleurs dans les scripts Substance 3D Designer Python pour obtenir des couleurs précises.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Using color management
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Utilisation de la gestion des couleurs
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 0%

---


# Utilisation de la gestion des couleurs

La classe </b>SDColorManagementEngine<b>, accessible à partir de la classe <b>SDApplication</b>, contient des informations sur les *paramètres de gestion des couleurs actuels*.

## Accès et interrogation du moteur de gestion des couleurs

```
import sd 

 

ctx = sd.getContext() 

app = ctx.getSDApplication() 

 

## Access the color management engine.

cm = app.getColorManagementEngine() 

 

## Currently getName can return "legacy", "ace" or "ocio"

## depending on the color management settings in the preferences.

cmName = cm.getName()  

print(cmName) 

 

print(cm.getWorkingColorSpaceName()) 

print(cm.getRawColorSpaceName()) 

 

if cmName == "ocio": 

## If OpenColorIO is enabled, print the config file name.

    print(cm.getOCIOConfigFileName()) 

 

## List all color spaces.

colorSpaces = cm.getColorSpaces() 

for cs in colorSpaces: 

    print(cs.get())
```


En outre, il est possible d&#39;*attribuer des espaces colorimétriques* aux ressources bitmap à partir de Python.

### Définition des espaces colorimétriques sur les ressources bitmap

```
import sd 

import sd 

from sd.api.sdproperty import * 

from sd.api.sdresourcebitmap import SDResourceBitmap 

from sd.api.sdvaluestring import SDValueString 

from sd.api.sdvaluebool import SDValueBool 

 

ctx = sd.getContext() 

app = ctx.getSDApplication() 

pkgMgr = app.getPackageMgr() 

cm = app.getColorManagementEngine() 

 

colorSpaces = cm.getColorSpaces() 

 

## Get all the resources in the first package.

pkg = pkgMgr.getPackages()[0] 

resources = pkg.getChildrenResources(isRecursive=True) 

 

for res in resources: 

 if isinstance(res, SDResourceBitmap): 

  props = res.getProperties(SDPropertyCategory.Annotation) 

 

## Print the current color space for the resource.

  p0 = res.getPropertyFromId("bitmap_color_space", SDPropertyCategory.Annotation) 

  cs = res.getAnnotationPropertyValueFromId("bitmap_color_space") 

  print(cs.get()) 

 

## Print the current premultiplied alpha setting for the resource.

  p1 = res.getPropertyFromId("bitmap_premultiplied_alpha", SDPropertyCategory.Annotation) 

  cs = res.getAnnotationPropertyValueFromId("bitmap_premultiplied_alpha") 

  print(cs.get()) 

 

## Assign new values for the color space and premultiplied alpha properties.

  res.setPropertyValue(p0, colorSpaces[2]) 

  res.setPropertyValue(p1, SDValueBool.sNew(False))
```


## Écriture de textures SDT avec des conversions d’espace colorimétrique

La méthode **save** de la classe **SDTexture** accepte désormais un paramètre facultatif **outputColorSpace**. Une fois spécifiée, la conversion de l&#39;espace colorimétrique sera *appliquée avant d&#39;enregistrer l&#39;image*.

Si le mode de gestion des couleurs prend en charge les profils ICC incorporés *et* le format de fichier de destination les prend également en charge, le profil ICC d&#39;espace colorimétrique sera *incorporé dans le fichier image obtenu*.
