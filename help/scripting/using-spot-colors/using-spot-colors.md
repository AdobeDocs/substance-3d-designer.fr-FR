---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/scripting/using-spot-colors.html"
breadcrumb-title: ''
description: Découvrez comment utiliser les tons directs dans les scripts Substance 3D Designer Python pour les workflows de couleurs spécialisés.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Using spot colors
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Utilisation des tons directs
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 0%

---


# Utilisation des tons directs

La classe </b>SDSpotColorLibrary<b>, accessible depuis la classe <b>SDApplication</b>, contient des informations sur les bibliothèques de tons directs incluses dans Designer.

Cette classe permet de répertorier les catalogues de couleurs et les tons directs et de rechercher des tons directs spécifiques ou le ton direct le plus proche d’une couleur RGB donnée.

Les tons directs ne sont *pas disponibles* dans Designer lorsque vous utilisez <b>OpenColorIO</b>. Dans ce cas, app.getSpotColorLibrary() renvoie <b>Aucun</b>.

>[!IMPORTANT]
>
> Les tons directs ne sont *pas disponibles* dans Designer lorsque vous utilisez <b>OpenColorIO</b>. Dans ce cas, app.getSpotColorLibrary() renvoie <b>Aucun</b>.

```
import sd 

 

ctx = sd.getContext() 

app = ctx.getSDApplication() 

spotLib = app.getSpotColorLibrary() 

 

## Find a color by color book and color name.

col = spotLib.findSpotColorByName( 

    spotColorBookName="PANTONE+ Solid Coated", 

    spotColorName="PANTONE Yellow 012 C" 

) 

 

print(col) 

print(col.get()) 

 

print(spotLib.getSpotColorBookName(col)) 

print(spotLib.getSpotColorName(col)) 

 

## Find the closest spot color in a specific book, to an RGB color.

## The RGB color is specified in the working color space currently used by Designer.

col = spotLib.findClosestSpotColor( 

    spotColorBookName="PANTONE+ Solid Coated", 

    r=88 / 255.0, 

    g=132 / 255.0, 

    b=167 / 255.0 

) 

 

print(col) 

print(col.get()) 

print(spotLib.getSpotColorBookName(col)) 

print(spotLib.getSpotColorName(col))
```


Les tons directs peuvent être récupérés et définis dans les propriétés des nœuds.

```
import sd 

from sd.api.sdbasetypes import * 

from sd.api.sdvaluecolorrgba import SDValueColorRGBA 

from sd.api.sdvaluespotcolor import SDValueSpotColor 

 

ctx = sd.getContext() 

app = ctx.getSDApplication() 

uiMgr = app.getUIMgr() 

spotLib = app.getSpotColorLibrary() 

 

node = uiMgr.getCurrentGraphSelection()[0] 

 

## Set RGBA color in node property.

rgbaColor = SDValueColorRGBA.sNew(ColorRGBA(0.7, 0.5, 0.2, 1)) 

node.setInputPropertyValueFromId("outputcolor", rgbaColor) 

 

## Set spot color in node property.

spotColor = spotLib.findSpotColorByName( 

    spotColorBookName="PANTONE+ Solid Coated", 

    spotColorName="PANTONE Yellow 012 C" 

) 

node.setInputPropertyValueFromId("outputcolor", spotColor) 

 

## Get color from node property (could be a SDValueColorRGBA or a SDValueSpotColor)

anyColor = node.getInputPropertyValueFromId("outputcolor") 

 

## Print the RGBA components of the color.

print(anyColor.get()) 

 

## Check if the color is a spot color.

if isinstance(anyColor, SDValueSpotColor): 

## Print the spot color information of the color.

    print(spotLib.getSpotColorBookName(anyColor)) 

    print(spotLib.getSpotColorName(anyColor)) 

 
```
