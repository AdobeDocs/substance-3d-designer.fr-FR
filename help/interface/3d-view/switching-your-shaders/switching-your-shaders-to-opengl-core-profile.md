---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/3d-view/switching-your-shaders-to-opengl-core-profile.html"
breadcrumb-title: ''
description: Découvrez comment passer des ombrages au profil OpenGL Core dans la vue 3D de Substance 3D Designer pour plus de compatibilité et de performances.
helpx_creative_field: ""
helpx_description: Designer > Interface > 3D View > Switching your shaders to OpenGL Core Profile
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Passage de vos shaders à OpenGL Core Profile
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 0%

---


# Passage de vos shaders à OpenGL Core Profile

Depuis la version 2018.2.0, la fenêtre d’affichage 3D utilise OpenGL Core Profile.\
À cette occasion, nous avons mis à jour certains shaders que nous fournissons avec l&#39;application de GLSL version 120 à GLSL version 330.

Vous pouvez mettre à jour vos propres shaders pour tirer parti des nouvelles fonctions GLSL disponibles, ou pour rendre votre code GLSL plus moderne. Veuillez noter que sur MacOS, les anciens nuanceurs peuvent ne plus fonctionner.\
Pour obtenir une vue d’ensemble complète des nouvelles fonctionnalités, nous vous recommandons vivement de consulter la documentation officielle d’OpenGL. Vous pouvez par exemple consulter la [spécification de langage d&#39;Ombrage OpenGL 3.30](https://www.khronos.org/registry/OpenGL/specs/gl/GLSLangSpec.3.30.pdf).\
Sinon, voici un guide rapide qui vous aidera à convertir vos shaders GLSL 1.20 en GLSL 3.30 :

## Mise à jour du numéro de version

Tout d&#39;abord, remplacez (ou ajoutez-le en haut de votre fichier si vous ne l&#39;avez pas encore) votre directive `#version` précédente par `#version 330`.

### Remplacez votre « attribut » et « variant » par « in » ou « out »

Désormais, les variables `attribute` et `varying` sont explicitement déclarées en tant que `in` ou `out` en fonction de l’étape de nuanceur :

Dans l&#39;ombrage de sommets, `attribute` s des sommets sont déclarés comme `in`, tandis que `varying` s à passer à l&#39;ombrage de fragments sont déclarés comme `out`.\
Par exemple :

```
## version 120



attribute vec3 vertexPosition;

attribute vec3 vertexNormal;

attribute vec2 vertexUV;



varying vec3 fragmentNormal;

varying vec2 fragmentUV;
```


devient :

```
## version 330



in vec3 vertexPosition;

in vec3 vertexNormal;

in vec2 vertexUV;



out vec3 fragmentNormal;

out vec2 fragmentUV;
```


De même, dans l’ombrage de fragments, l’option variable apparaît. Vous devez également déclarer une variable de sortie qui remplacera gl\_FracColor (qui n’est plus intégrée) :

```
## version 120



varying vec3 fragmentNormal;

varying vec2 fragmentUV;



void main() {

...

gl_FragColor = vec4(myColor.rgb, 1.0);

}
```


devient :

```
## version 330



in vec3 fragmentNormal;

in vec2 fragmentUV;



out vec4 outColor; //you could choose any name you want here



void main() {

...

outColor = vec4(myColor.rgb, 1.0);

}
```


### Utilisation de nouvelles fonctions de recherche de texture

Avec la nouvelle version du langage ombrage, l’API de recherche de texture a été à la fois simplifiée et améliorée.

Les fonctions `texture1D()`, `texture2D()`, `texture3D()` et `textureCube()` deviennent toutes des surcharges de `texture()`.\
De même, `texture2DLod()` devient `textureLod()`, `texture2DGrad()` devient `textureGrad()` et ainsi de suite.

Vous avez également désormais accès à des fonctions utiles telles que `textureSize()` (pour interroger la taille de l’échantillonneur dans texel), `textureOffset()` (pour échantillonner les voisins de l’emplacement cible), `textureFetch()` (pour fournir un emplacement d’échantillon en pixels), et plus encore.
