---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/interface/3d-view/glslfx-shaders.html"
breadcrumb-title: ''
description: Utilisez les nuanceurs GLSLFX dans la vue 3D de Substance 3D Designer pour personnaliser le rendu des matériaux et les effets de prévisualisation.
helpx_creative_field: ""
helpx_description: Designer > Interface > 3D View > GLSLFX Shaders
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Shaders GLSLFX
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '3098'
ht-degree: 1%

---


# Shaders GLSLFX

Les fichiers GLSLFX font le pont entre l’application et les fichiers glsl shader.\
Il permet d&#39;utiliser n&#39;importe quel shader glsl sans avoir à modifier le code.

## Format de fichier

Le format GLSLFX est un fichier XML. Les commentaires sont pris en charge.

### En-tête et nœud racine

L&#39;élément de nœud racine XML est nommé <b>glslfx</b>.

```
<?xml version="1.0" encoding="UTF-8"?>

<glslfx version="1.0.0" author="allegorithmic.com">

    <!-- BODY -->

    <!-- ... -->

</glslfx>
```


### Corps

#### Technique

Elément XML décrivant une technique. Une technique est une variante du courant FX. Un fichier GLSLFX peut contenir plusieurs techniques, mais au moins une doit être définie.

Le rendu de la géométrie s’effectue selon l’une des techniques définies par l’application.

+++Définition d’élément XML
Technique <b>Name:</b>

<b>Attributs :</b>

* name : Toute chaîne utilisée pour nommer la technique

+++

L’élément XML peut avoir plusieurs enfants. Les éléments définis dans une technique remplacent les éléments définis globalement.

Par exemple, il est utilisé pour remplacer certaines valeurs d’uniforme et obtenir une variation FX pour cette technique.

#### Passe de rendu

Elément XML décrivant une passe de rendu. Une passe de rendu décrit le rendu de la géométrie.

Une technique peut contenir plusieurs passes de rendu exécutées de manière séquentielle. Une technique ne contenant aucune passe de rendu équivaut à une technique contenant une passe de rendu à l’écran.

Les éléments définis dans une passe de rendu remplacent les éléments définis dans la technique parent.

+++Définition d’élément XML
<b>Nom :</b> passe

<b>Attributs :</b>

* sortie

* hors écran : le rendu sera effectué en cibles de rendu définies par l’utilisateur

* à l’écran : le rendu est effectué dans la cible de rendu par défaut

+++

#### Shaders

Définissez les fichiers de nuanceur GLSL pour chaque type.

Définition d’élément XML :

+++Définition d’élément XML
Nuanceur <b>Name:</b>

<b>Attributs :</b>

* type : type d&#39;ombrage GLSL ;

* nom du fichier : chemin du fichier de nuanceur glsl. Peut être absolu ou relatif au fichier GLSLFX ;

* primitiveType : méthode de rendu de la primitive.


| Valeur &#39;type&#39; | Description |
| --- | --- |
| sommet | Ombrage de sommet |
| géométrie | Ombrage de géométrie |
| test\_control | Ombrage de contrôle de la facettisation |
| tess\_eval | Ombrage Évaluation de la facettisation |
| fragment | Nuanceur de fragments |



| Valeur « primitiveType » | Description |
| --- | --- |
| point | Rendu sous forme de points |
| boucle de ligne | Rendu en tant que boucle de ligne |
| patch[1..N] | Rendu sous forme de correctifs avec [1..N] sommets |


+++

#### Propriétés

Permet de configurer une partie de l’état OpenGL.

+++Définition d’élément XML
Propriété <b>Name:</b>

<b>Attributs :</b>

* name : Le nom de la propriété à définir. Le nom est basé sur la fonction OpenGL ou le nom glEnum :
  * Syntaxe des énumérations : sans le préfixe « GL\_ », en minuscules. Exemples : glEnable(GL\_BLEND\_ENABLE) => «  » », glDisable(GL\_CULL\_FACE) => «  » »
  * Syntaxe des fonctions : sans le préfixe « gl », en minuscules et avec tous les mots séparés par le caractère « \_ ». Exemple : glBlendFunc(GL\_SRC\_ALPHA, GL\_ONE\_MINUS\_SRC\_ALPHA) => «  »

* Syntaxe des énumérations : sans le préfixe « GL\_ », en minuscules. Exemples : glEnable(GL\_BLEND\_ENABLE) => «  » », glDisable(GL\_CULL\_FACE) => «  » »

* Syntaxe des fonctions : sans le préfixe « gl », en minuscules et avec tous les mots séparés par le caractère « \_ ». Exemple : glBlendFunc(GL\_SRC\_ALPHA, GL\_ONE\_MINUS\_SRC\_ALPHA) => «  »

* value : Valeur de la propriété.


| Valeurs &#39;name&#39; | Valeurs &#39;value&#39; | Description |
| --- | --- | --- |
| blend\_enabled | booléen | Activation/désactivation du mode de fusion |
|  | vrai |  |
|  | faux |  |
| blend\_func | chaîne, chaîne | Définition des fonctions de fusion source et cible |
|  | zéro | pour OpenGL enum GL\_ZERO |
|  | un | pour OpenGL enum GL\_ONE |
|  | src\_color | pour OpenGL enum GL\_SRC\_COLOR |
|  | one\_minus\_src\_color | pour l’énumération OpenGL GL\_ONE\_MINUS\_SRC\_COLOR |
|  | dst\_color | pour OpenGL enum GL\_DST\_COLOR |
|  | one\_minus\_dst\_color | pour l’énumération OpenGL GL\_ONE\_MINUS\_DST\_COLOR |
|  | src\_alpha | pour OpenGL enum GL\_SRC\_ALPHA |
|  | one\_minus\_src\_alpha | pour l’énumération OpenGL GL\_ONE\_MINUS\_SRC\_ALPHA |
|  | dst\_alpha | pour OpenGL enum GL\_DST\_ALPHA |
|  | one\_minus\_dst\_alpha | pour l’énumération OpenGL GL\_ONE\_MINUS\_DST\_ALPHA |
|  | constante\_color | pour OpenGL enum GL\_CONSTANT\_COLOR |
|  | one\_minus\_constant\_color | pour l’énumération OpenGL GL\_ONE\_MINUS\_CONSTANT\_COLOR |
|  | constante\_alpha | pour OpenGL enum GL\_CONSTANT\_ALPHA |
|  | one\_minus\_constant\_alpha | pour l’énumération OpenGL GL\_ONE\_MINUS\_CONSTANT\_ALPHA |
|  | src\_alpha\_saturate | pour l’énumération OpenGL GL\_SRC\_ALPHA\_SATURATE |
|  | src1\_color | pour OpenGL enum GL\_SRC1\_COLOR |
|  | one\_minus\_src1\_color | pour l’énumération OpenGL GL\_ONE\_MINUS\_SRC1\_COLOR |
|  | src1\_alpha | pour OpenGL enum GL\_SRC1\_ALPHA |
|  | one\_minus\_src1\_alpha | pour l’énumération OpenGL GL\_ONE\_MINUS\_SRC1\_ALPHA |
| cull\_face\_enabled | booléen | Activation/désactivation de l’abattage du visage |
|  | vrai |  |
|  | faux |  |
| cull\_face\_mode | chaîne | Définir le mode d&#39;abattage du visage |
|  | avant | pour OpenGL enum GL\_FRONT |
|  | envers | pour OpenGL enum GL\_BACK |
|  | avant\_et\_arrière | pour l’énumération OpenGL GL\_FRONT\_AND\_BACK |
| profondeur\_func | chaîne | Définition de la fonction de comparaison des profondeurs |
|  | jamais | pour OpenGL enum GL\_NEVER |
|  | moins | pour OpenGL enum GL\_LESS |
|  | égal | pour OpenGL enum GL\_LEQUAL |
|  | égal à | pour OpenGL enum GL\_EQUAL |
|  | notequal | pour OpenGL enum GL\_NOTEQUAL |
|  | égaler | pour OpenGL enum GL\_GEQUAL |
|  | supérieur | pour OpenGL enum GL\_GREATER |
|  | toujours | pour OpenGL enum GL\_ALWAYS |


+++

#### Uniformes

Permet de remplacer certains uniformes définis globalement ou dans la technique parent. Cela permet de modifier le comportement du shader pour cette technique ou passe de rendu.

Voir la section <b>Uniformes</b> ci-dessous pour plus de détails sur leur définition.

+++Exemple


+++

## Cibles de rendu

Pour les passes de rendu hors écran, les cibles de rendu doivent être définies dans la passe de rendu.

+++Définition d’élément XML
Sortie <b>Name:</b>

<b>Attributs :</b>

* attachment : point d’attache OpenGL, inspiré des noms OpenGL :\
  GL\_COLOR\_ATTACHMENT[0..3] => &#39;color[0..3]&#39;\
  GL\_PROFONDEUR\_ATTACHMENT => &#39;profondeur&#39;

attachment : point d’attache OpenGL, inspiré des noms OpenGL :\
GL\_COLOR\_ATTACHMENT[0..3] => &#39;color[0..3]&#39;\
GL\_PROFONDEUR\_ATTACHMENT => &#39;profondeur&#39;

* nom : nom de la cible de rendu.\
  Il peut être utilisé lors d’une passe de rendu ultérieure pour lier cette cible de rendu en tant qu’échantillonneur.

nom : nom de la cible de rendu.\
Il peut être utilisé lors d’une passe de rendu ultérieure pour lier cette cible de rendu en tant qu’échantillonneur.

* format : format interne de la cible de rendu.

format : format interne de la cible de rendu.

* clear : attribut facultatif qui définit une valeur clear.\
  Si elle est présente, la cible de rendu sera effacée à cette valeur au début de la passe de rendu.\
  S’il est manquant, la cible de rendu conservera son contenu précédent.

+++

>[!NOTE]
>
> Les cibles de rendu couleur sont interdites dans une passe de rendu à l’écran, mais une cible de rendu de profondeur peut être partagée avec n’importe quelle passe de rendu (mais elle risque de rompre le rendu lors du mélange de plusieurs matières dans la scène).

<b>À propos des formats</b>

Pour les formats de profondeur, tous les formats OpenGL de profondeur seule (sans pochoir) sont pris en charge :

* GL\_PROFONDEUR\_COMPONENT16 => &#39;profondeur 26&#39;
* GL\_PROFONDEUR\_COMPONENT24 => &#39;profondeur 34&#39;
* GL\_PROFONDEUR\_COMPONENT32 => &#39;profondeur 42&#39;
* GL\_PROFONDEUR\_COMPONENT32F => &#39;profondeur 42f&#39;

Pour les formats de couleur, le nom est basé sur les noms d’énumération OpenGL, sans le préfixe « GL\_ », en minuscules.\
Trois formats de canal (RGB) ne sont pas pris en charge. Utilisez plutôt un format RVBA.\
Nombre de bits par pixel par canal pris en charge :

* Entier non signé normalisé : 8, 16
* Point flottant : 16, 32

Une exception à ces règles est le format GL\_R11F\_G11F\_B10F qui est pris en charge. :

* GL\_RGBA8 => &#39;rgba8&#39;
* GL\_RGBA16F => &#39;rgba16f&#39;
* GL\_SRGB8\_ALPHA 8 => &#39;srgb8\_alpha8&#39;
* GL\_R11F\_G11F\_B10F => &#39;r11f\_g11f\_b10f&#39;
* GL\_RG16 => « rg16 »

### Échantillonnages

Autorisez le remplacement de certains échantillonnages définis globalement, car ils ne peuvent pas être définis dans une technique. Cela permet de définir une utilisation d’échantillonnage pour cette passe de rendu ou de lire à partir d’une cible de rendu d’une passe de rendu précédente.

Voir la section <b>Échantillonneurs</b> pour plus de détails sur leur définition.

+++Exemple


+++

## Format des sommets d’entrée

Cela permet de définir la sémantique de chaque attribut défini dans l&#39;ombrage de sommet.

<b>Définition d&#39;élément XML :</b>

Nom : &#39;vertexformat&#39;

Attributs :

* &#39;name&#39; : Le nom de l&#39;attribut tel que défini dans l&#39;ombrage de sommet.
* &#39;sémantique&#39; : Sémantique de l&#39;attribut.

| Valeur sémantique | Description |
| --- | --- |
| position | Position du sommet (float3) |
| normal | Vertex normal (float3) |
| texcoord[0..N] | Tampon de coordonnées de texture de sommet N (float2) |
| tangente[0..N] | Tampon de tangente de sommet N (float4) |
| binormal[0..N] | Tampon binormal de sommet N (float4) |

Exemple :

```
<?xml version="1.0" encoding="UTF-8"?>

<glslfx version="1.0.0" author="allegorithmic.com">

     <!-- BODY -->

     <!-- ... -->



     <!-- INPUT VERTEX FORMAT -->

     <vertexformat name="iVS_Position" semantic="position"/>

     <vertexformat name="iVS_Normal" semantic="normal"/>

     <vertexformat name="iVS_UV" semantic="texcoord0"/>

     <vertexformat name="iVS_Tangent" semantic="tangent0"/>

     <vertexformat name="iVS_Binormal" semantic="binormal0"/>

</glslfx>
```


## Échantillonnages

Cela permet de définir l&#39;utilisation de chaque échantillonneur.\
Il est utilisé par l&#39;application pour déterminer la texture à définir dans les échantillonneurs spécifiés.

<b>Définition d&#39;élément XML :</b>

Nom : &#39;sampler&#39;

Attributs :

* &#39;name&#39; : Le nom de la variable d&#39;échantillonnage dans le fichier shader.
* &#39;usage&#39; : Utilisation de l&#39;échantillonneur. Elle correspond à l’utilisation spécifiée dans le nœud Sortie du graphique.

| Valeur &#39;usage&#39; | Description |
| --- | --- |
| diffuse | Diffuse map |
| opacité | Mappage d’opacité |
| émissif | Carte émissive |
| occlusion ambiante | Carte d’occlusion ambiante |
| ambiant | Carte d&#39;ambiance |
| masque | Mappage de masque |
| detailnormal | Détailler la carte de normales |
| normal | Map normal |
| choc | Carte de relief |
| hauteur | table des Heights |
| displacement | plan de displacement |
| niveau spéculatif | plan de specular level |
| spécularcolor | table des couleurs specular |
| spéculaire | carte du specular |
| brillance | Carte de brillance |
| rugosité | Courbe de transfert de rugosité |
| niveau d&#39;anisotropie | Carte des niveaux d&#39;anisothropie |
| anisotropyangle | Carte d&#39;angle d&#39;anisothropie |
| transmissif | Carte de transmission |
| réflexion | Carte de réflexion |
| réfraction | Carte de réfraction |
| environnement | Mappage d&#39;environnement (mappage de cube) |
| panorama | Carte de panorama (carte de latitude/longitude) |
| masque bleu | Texture de tramage 256 x 256 |

* Plusieurs utilisations sont prises en charge.
  * Exemple :

```
   <!-- SAMPLERS -->

    <sampler name="baseColorMap" usage="basecolor,diffuse"/>

     <!-- ... -->
```


&#39;isHidden&#39; : Booléen qui indique si l&#39;échantillonneur doit apparaître dans l&#39;interface utilisateur graphique

* Exemple :

```
     <!-- SAMPLERS -->

    <sampler name="bluenoiseMask" usage="bluenoisemask" ishidden="true"/>

     <!-- ... -->
```


Mode d’habillage :

<table data-preserve-html="true"><tbody><tr><th>Nom</th><th>Valeur</th></tr><tr><td rowspan="4">texture_wrap_s, texture_wrap_t, texture_wrap_r<br/><br/><br/></td><td>clamp_to_edge</td></tr><tr><td>clamp_to_border</td></tr><tr><td colspan="1">mirrored_repeat</td></tr><tr><td colspan="1">répéter<br/><br/></td></tr></tbody></table>

Filtre de texture

<table data-preserve-html="true"><tbody><tr><th>Nom</th><th>Valeur</th></tr><tr><td rowspan="6">texture_min_filter, texture_mag_filter<br/><br/><br/></td><td>le plus proche</td></tr><tr><td>linéaire</td></tr><tr><td colspan="1">nearest_mipmap_nearest</td></tr><tr><td colspan="1">linear_mipmap_nearest</td></tr><tr><td colspan="1">nearest_mipmap_linear</td></tr><tr><td colspan="1">linear_mipmap_linear</td></tr></tbody></table>

Exemple :

```
<?xml version="1.0" encoding="UTF-8"?>

<glslfx version="1.0.0" author="allegorithmic.com">

     <!-- BODY -->

     <!-- ... -->



     <!-- SAMPLERS -->

     <sampler name="baseColorMap" usage="basecolor,diffuse"/>

     <sampler name="heightMap" usage="height"/>

     <sampler name="normalMap" usage="normal"/>

     <sampler name="detailNormalMap" usage="detailNormal"/>

     <sampler name="environmentMap" usage="environment"/>

     <sampler name="bluenoiseMask" usage="bluenoisemask" ishidden="true"/>

     <sampler name="sssDiffuseMap" usage="sssDiffuse"/>

</glslfx>
```


## Uniformes

Cela vous permet d&#39;ajouter des informations supplémentaires sur chaque uniforme de shader.

<b>Définition d&#39;élément XML :</b>

Nom : &#39;uniforme&#39;

Attributs :

&#39;name&#39; : Le nom de l&#39;uniforme dans le fichier shader.

| Valeur sémantique | Description |
| --- | --- |
| monde | Matrice mondiale (float16) |
| worldinversetranspose | Matrice de transposition inverse universelle (float16) |
| worldviewprojection | Matrice de projection Vue du monde (float16) |
| viewinverse | Matrice inverse mondiale (float16) |
| vision du monde | Matrice Vue du monde (float16) |
| modelview | Matrice de la vue du modèle (float16) |
| projection | Matrice de projection (float16) |
| ambiant | Couleur ambiante de la scène (float3) |
| lightposition[0..N] | Position de la nième lumière de la scène (float3) |
| lightcolor[0..N] | Couleur de la nième lumière de la scène (float3) |
| lightintensity[0..N] | Intensité de la N ième lumière de la scène (float) |
| globaltime | Heure actuelle en secondes (float) |
| résolution | Résolution de la fenêtre d’affichage (int2) |
| souris | Position de la souris (int2) |
| samplespostablesize | Nombre d’échantillons à utiliser pour calculer l’éclairage de l’environnement (int) |
| irradianceshcoefs | La gamme de vecteurs d&#39;harmoniques sphériques (float3[10]) |
| panoramamipmapheight | Nombre de niveaux du mipmap dans la carte du panorama (float) |
| panorama | Angle Angle de rotation de la carte du panorama (flottant) |
| intensité du panorama | Intensité de la carte du panorama (flottant) |
| computebinormalinfragmentshader | Le binormal est-il calculé par fragment ? (sinon, par sommet) (bool) |
| isdirectxnormal | Le format de map normal est-il DirectX ? (bool) |
| uvwscale | Valeurs d’échelle de u, v, w (float3) |
| renderuvtile | Rendu d’une seule mosaïque UV ? (bool) |
| uvtilecoords | Coordonnées de la mosaïque UV pour le rendu (int2) |

« sémantique » : sémantique de l&#39;uniforme. (Toutes les matrices sont float16).

Exemple :

```
<?xml version="1.0" encoding="UTF-8"?>

<glslfx version="1.0.0" author="allegorithmic.com">

     <!-- BODY -->

     <!-- ... -->



     <!-- MATRICES -->

     <uniform name="worldMatrix" semantic="world"/>

     <uniform name="worldViewProjMatrix" semantic="worldviewprojection"/>

     <uniform name="worldViewMatrix" semantic="worldview"/>

     <uniform name="worldInverseTransposeMatrix" semantic="worldinversetranspose"/>

     <uniform name="viewInverseMatrix" semantic="viewinverse"/>

     <uniform name="modelViewMatrix" semantic="modelview"/>

     <uniform name="projectionMatrix" semantic="projection"/>

</glslfx>
```


Exemple :

```
<?xml version="1.0" encoding="UTF-8"?>

<glslfx version="1.0.0" author="allegorithmic.com">

    <!-- BODY -->

    <!-- ... -->



    <!-- SCENE PARAMETERS -->

    <uniform name="AmbiColor" semantic="ambient"/>

    <uniform name="Lamp0Pos" semantic="lightposition0"/>

    <uniform name="Lamp0Color" semantic="lightcolor0"/>

    <uniform name="Lamp1Pos" semantic="lightposition1"/>

    <uniform name="Lamp1Color" semantic="lightcolor1"/>

</glslfx>
```


### Autres paramètres

D&#39;autres renseignements supplémentaires peuvent être ajoutés à chaque uniforme pour :

* définir la valeur par défaut
* valeurs de pince
* contrôler la façon dont l’uniforme sera affiché dans l’application :
* définir le libellé
* définissez les informations de widget utilisées pour modifier la valeur dans l’application :
* nom du widget, min, max, étape d’incrémentation/décrémentation
* groupes d’uniformes dans des widgets de groupe

Comme les uniformes peuvent être remplacés pour chaque technique, cela permet d&#39;afficher une configuration d&#39;interface graphique spécifique pour chaque technique.

<b>Définition d&#39;élément XML :</b>

Nom : &#39;uniforme&#39;

Attributs :

* &#39;name&#39; : Le nom de l&#39;uniforme dans le fichier shader.
* &#39;default&#39; : la valeur par défaut uniforme
* &#39;min&#39; : la valeur min de la plage de validité
* &#39;max&#39; : la valeur maximale de la plage de validité
* &#39;guiName&#39; : nom de l&#39;uniforme dans l&#39;interface graphique de l&#39;application
* &#39;guiGroup&#39; : nom du groupe pour placer l&#39;uniforme dans l&#39;interface graphique de l&#39;application
* &#39;guiWidget&#39; : nom du widget utilisé pour modifier la valeur uniforme dans l&#39;interface graphique de l&#39;application

| Valeur « guiWidget » | Description |
| --- | --- |
| coulissant | Widget de curseur pour floatN |
| angle | Widget Angle pour flotteur |
| couleur | Widget de couleur pour float3, float4 color |
| case à cocher | Widget Case à cocher pour bool |

* &#39;guiMin&#39; : valeur min du widget
* &#39;guiMax&#39; : valeur maximale du widget

## Exemple : Crénelage/Parallaxe

### Fichier Parallax Vertex Shader

Situé dans .\tessellation\_parallax\parallax\vs.glsl

Contenu :

> #version 120

attribute vec4 iVS\_Position ;\
attribute vec4 iVS\_Normal ;\
attribute vec2 iVS\_UV ;\
attribute vec4 iVS\_Tangent ;\
attribute vec4 iVS\_Binormal ;

variable vec3 iFS\_Normal ;\
variable vec2 iFS\_UV ;\
variable vec3 iFS\_Tangent ;\
variable vec3 iFS\_Binormal ;\
variable vec3 iFS\_PointWS ;

mat4 worldMatrix uniforme ;\
mat4 worldViewProjMatrix uniforme ;

void main()\
&lbrace;\
gl\_Position = worldViewProjMatrix \&#42; iVS\_Position ;\
iFS\_Normal = iVS\_Normal.xyz ;\
iFS\_UV = iVS\_UV ;\
iFS\_Tangent = iVS\_Tangent.xyz ;\
iFS\_Binormal = iVS\_Binormal.xyz ;\
iFS\_PointWS = (worldMatrix \&#42; iVS\_Position).xyz ;\
&rbrace;

### Fichier de nuanceur de sommets de pavage

Situé dans .\tessellation\_parallax\tessellation\vs.glsl

Contenu :

&#x200B;>> 

&#x200B;#version 120

attribute vec4 iVS\_Position ;\
attribute vec4 iVS\_Normal ;\
attribute vec2 iVS\_UV ;\
attribute vec4 iVS\_Tangent ;\
attribute vec4 iVS\_Binormal ;

variable vec4 oVS\_Normal ;\
variation de vec2 oVS\_UV ;\
variable vec4 oVS\_Tangent ;\
variable vec4 oVS\_Binormal ;

void main()\
&lbrace;\
gl\_Position = iVS\_Position ;\
oVS\_Normal = iVS\_Normal ;\
oVS\_UV = iVS\_UV ;\
oVS\_Tangent = iVS\_Tangent ;\
oVS\_Binormal = iVS\_Binormal ;\
&rbrace;

### Fichier Shader de contrôle de la pavage

Situé dans .\tessellation\_parallax\tessellation\tcs.glsl

Contenu :

&#x200B;>> 

&#x200B;#version 400 core\
&#x200B;#extension GL\_ARB\_tessellation\_shader : enable

layout(vertices = 3) out ;

in vec4 oVS\_Normal[];\
in vec2 oVS\_UV[];\
in vec4 oVS\_Tangent[];\
in vec4 oVS\_Binormal[];

out vec4 oTCS\_Normal[];\
out vec2 oTCS\_UV[];\
out vec4 oTCS\_Tangent[];\
out vec4 oTCS\_Binormal[];

facteur de tessellation uniforme du flotteur ;

void main()\
&lbrace;\
gl\_TessLevelOuter[0] = tessellationFactor ;\
gl\_TessLevelOuter[1] = tessellationFactor ;\
gl\_TessLevelOuter[2] = tessellationFactor ;\
gl\_TessLevelInner[0] = tessellationFactor ;\
gl\_out[gl\_InvocationID].gl\_Position = gl\_in[gl\_InvocationID].gl\_Position ;

oTCS\_Normal[gl\_InvocationID] = oVS\_Normal[gl\_InvocationID];\
oTCS\_UV[gl\_InvocationID] = oVS\_UV[gl\_InvocationID];\
oTCS\_Tangent[gl\_InvocationID] = oVS\_Tangent[gl\_InvocationID];\
oTCS\_Binormal[gl\_InvocationID] = oVS\_Binormal[gl\_InvocationID];\
&rbrace;

### Fichier de nuanceur d&#39;évaluation de la facettisation

Situé dans .\tessellation\_parallax\tessellation\tcs.glsl

Contenu :

&#x200B;>> 

&#x200B;#version 400 core

layout(triangles, equal\_spacing, ccw) in ;

in vec4 oTCS\_Normal[];\
in vec2 oTCS\_UV[];\
in vec4 oTCS\_Tangent[];\
in vec4 oTCS\_Binormal[];

mat4 worldMatrix uniforme ;\
mat4 worldViewProjMatrix uniforme ;

sampler2D heightMap uniforme ;

carrelage flottant uniforme = 1,0f ;\
uniformise float heightMapScale = 1.0f ;

out vec3 iFS\_Normal ;\
out vec2 iFS\_UV ;\
out vec3 iFS\_Tangent ;\
out vec3 iFS\_Binormal ;\
out vec3 iFS\_PointWS ;

vec3 interpolate3D(vec3 v0, vec3 v1, vec3 v2, vec3 uvw)\
&lbrace;\
return uvw.x \&#42; v0 + uvw.y \&#42; v1 + uvw.z \&#42; v2 ;\
&rbrace;

vec2 interpolate2D(vec2 v0, vec2 v1, vec2 v2, vec3 uvw)\
&lbrace;\
return uvw.x \&#42; v0 + uvw.y \&#42; v1 + uvw.z \&#42; v2 ;\
&rbrace;

void main()\
&lbrace;\
vec3 uvw = gl\_TessCoord.xyz ;

vec3 newPos = interpolate3D(gl\_in[0].gl\_Position.xyz, gl\_in[1].gl\_Position.xyz, gl\_in[2].gl\_Position.xyz, uvw);\
vec3 newNormal = normalize(interpolate3D(oTCS\_Normal[0].xyz, oTCS\_Normal[1].xyz, oTCS\_Normal[2].xyz, uvw);\
vec3 newTangent = normalize(interpolate3D(oTCS\_Tangent[0].xyz, oTCS\_Tangent[1].xyz, oTCS\_Tangent[2].xyz, uvw));\
vec3 newBinormal = normalize(interpolate3D(oTCS\_Binormal[0].xyz, oTCS\_Binormal[1].xyz, oTCS\_Binormal[2].xyz, uvw));\
vec2 newUV = interpolate2D(oTCS\_UV[0], oTCS\_UV[1], oTCS\_UV[2], uvw);

float heightTexSample = texture(heightMap, newUV \&#42; tiling).x \&#42; 2.0 - 1.0 ;\
newPos += newNormal \&#42; heightTexSample \&#42; heightMapScale ;

vec4 obj\_pos = vec4(newPos, 1);\
gl\_Position = worldViewProjMatrix \&#42; obj\_pos ;

iFS\_UV = newUV \&#42; mosaïque ;\
iFS\_Tangent = newTangent ;\
iFS\_Binormal = newBinormal ;\
iFS\_Normal = newNormal ;\
iFS\_PointWS = (worldMatrix \&#42; obj\_pos).xyz ;\
&rbrace;

### Fichier Fragment Shader

Situé dans .\tessellation\_parallax\fs.glsl

Contenu :

&#x200B;>> 

&#x200B;#version 120

// #define ALG\_NORMAL\_DIRECTX\
&#x200B;#define ALG\_NORMAL\_OPENGL

&#x200B;#ifdef ALG\_NORMAL\_DIRECTX\
// #define FLIP\_NORMAL\_X\
SYMÉTRIE #define\_NORMALE\_Y\
// #define FLIP\_NORMAL\_Z\
&#x200B;#endif //#ifdef ALG\_NORMAL\_DIRECTX

&#x200B;#ifdef ALG\_NORMAL\_OPENGL\
// #define FLIP\_NORMAL\_X\
SYMÉTRIE #define\_NORMALE\_Y\
// #define FLIP\_NORMAL\_Z\
&#x200B;#endif //#ifdef ALG\_NORMAL\_OPENGL

variable vec3 iFS\_Normal ;\
variable vec2 iFS\_UV ;\
variable vec3 iFS\_Tangent ;\
variable vec3 iFS\_Binormal ;\
variable vec3 iFS\_PointWS ;

uniforme vec3 Lamp0Pos = vec3(0.0f,0.0f,70.0f);\
uniforme vec3 Lamp0Color = vec3(1.0f,1.0f,1.0f);\
uniforme vec3 Lamp1Pos = vec3(70.0f,0.0f,0.0f);\
uniforme vec3 Lamp1Color = vec3(0.198f,0.198f,0.198f);\
bool uniforme flipNormal = true ;\
Uniform float TilingDetail = 3.0f ;\
SpecExpon = 50,0 ;\
flotteur uniforme Ks = 1,0 ;\
uniforme int parallax\_mode = 0 ;\
facteur de tessellation uniforme du flotteur = 4,0 ;\
uniformise float heightMapScale = 1.0f ;\
profondeur uniforme du flotteur\_detail = 0.5f ;\
flotteur uniforme Kr = 0,5 f ;\
int uniforme KF\_on = 1 ;\
KFs flottants uniformes = 1,0f ;\
uniforme vec3 AmbiColor = vec3(0.07f,0.07f,0.07f);\
carrelage flottant uniforme = 1,0f ;\
uniforme int enableTilingInFS = 0 ;

sampler2D heightMap uniforme ;\
sampler2D normalMap uniforme ;\
sampler2D detailNormalMap uniforme ;\
sampler2D emissiveMap uniforme ;\
sampler2D diffuseMap uniforme ;\
specularMap de sampler2D uniforme ;\
opacityMap sampler2D uniforme ;\
samplerCube environmentMap uniforme ;

mat4 worldMatrix uniforme ;\
mat4 worldInverseTransposeMatrix uniforme ;\
mat4 viewInverseMatrix uniforme ;

vec4 litFct(float NdotL, float NdotH, float specExp)\
&lbrace;\
flottant ambiant = 1,0 ;\
diffusion flottante = max(NdotL, 0,0);\
specular flottant = step(0.0, NdotL) \&#42; pow(max(0.0, NdotH), specExp);\
return vec4(ambiante, diffuse, specular, 1,0);\
&rbrace;

vec3 lerpFct(vec3 v0, vec3 v1, float percent)\
&lbrace;\
return v0 + (v1-v0) \&#42; %;\
&rbrace;

// Phong Ombrage\
void phong\_ombrage(\
dans vec3 LightColor,\
dans vec3 normalWS,\
dans vec3 pointToLightDirWS,\
dans vec3 pointToCameraDirWS,\
inout vec3 DiffuseContrib,\
inout vec3 SpecularContrib)\
&lbrace;\
vec3 Hn = normalize(pointToCameraDirWS + pointToLightDirWS);\
vec4 litV = litFct(dot(normalWS, pointToLightDirWS), dot(normalWS, Hn), SpecExpon);\
DiffuseContrib = litV.y \&#42; LightColor ;\
SpecularContrib = litV.y \&#42; litV.z \&#42; Ks \&#42; LightColor ;\
&rbrace;

vec3 fixNormalSample(vec3 v)\
&lbrace;\
vec3 résultat = v - vec3(0.5,0.5,0.5);

SYMÉTRIE #ifdef\_NORMALE\_X\
result.x = -result.x ;\
&#x200B;#endif // ifdef FLIP\_NORMAL\_X\
SYMÉTRIE #ifdef\_NORMALE\_Y\
result.y = -result.y ;\
&#x200B;#endif // ifdef FLIP\_NORMAL\_Y\
SYMÉTRIE #ifdef\_NORMALE\_Z\
result.z = -result.z ;\
&#x200B;#endif // ifdef FLIP\_NORMAL\_Z

résultat du retour ;\
&rbrace;

vec3 normalVecOSToWS(vec3 normal)\
&lbrace;\
retour normal ;\
&rbrace;

void main()\
&lbrace;\
vec3 cameraPosWS = viewInverseMatrix[3].xyz ;\
vec3 pointToLight0DirWS = normalize(Lamp0Pos - iFS\_PointWS);\
vec3 pointToLight1DirWS = normalize(Lamp1Pos - iFS\_PointWS);\
vec3 pointToCameraDirWS = normalize(cameraPosWS);\
vec3 normalOS = normalize(iFS\_Normal);\
vec3 tangentOS = normalize(iFS\_Tangent);\
vec3 binormalOS = normalize(iFS\_Binormal);

// ------------------------------------------\
// S&#39;assurer que le TBN est orthonormé\
binormalOS = normalize(cross(normalOS, tangentOS));\
tangentOS = normalize(cross(binormalOS, normalOS));

vec3 cumulatedNormalOS = normalOS;

// ------------------------------------------\
// Mettre à jour les UV\
float a = dot(normalOS,-pointToCameraDirWS);\
vec3 s = vec3(dot(pointToCameraDirWS,tangentOS), dot(pointToCameraDirWS,binormalOS), a);\
vec2 uv = enableTilingInFS == 0 ? iFS\_UV : (iFS\_UV \&#42; mosaïque);\
float height = texture2D(heightMap,uv).x \&#42; 2.0 - 1.0 ;\
float parallax = parallax\_mode == 0 ? (tessellationFactor / 100000.f + heightMapScale / 500.f) : (heightMapScale / 50.f);\
+= uv (height \&#42; s.xy \&#42; parallaxe) ;

// ------------------------------------------\
// Ajouter la normale à partir de normalMap\
vec3 normalTS = texture2D(normalMap,uv).xyz ;\
normalTS = fixNormalSample(normalTS);\
vec3 normalMapOS = normalTS.x\&#42;tangentOS + normalTS.y\&#42;binormalOS ;\
cumulatedNormalOS = cumulatedNormalOS + normalMapOS;\
cumulatedNormalOS = normalize(cumulatedNormalOS);

// ------------------------------------------\
// Ajouter un mappage normal détaillé\
vec3 normalDetailTS = texture2D(detailNormalMap,uv\&#42;TilingDetail).xyz ;\
normalDetailTS = fixNormalSample(normalDetailTS);\
vec3 variableNormalDetailTS = lerpFct(vec3(0.0,0.0,0.5),normalDetailTS,Profondeur\_detail);\
vec3 normalDetailOS = variableNormalDetailTS.x\&#42;tangentOS + variableNormalDetailTS.y\&#42;binormalOS ;\
cumulatedNormalOS = cumulatedNormalOS + normalDetailOS ;\
cumulatedNormalOS = normalize(cumulatedNormalOS);

if (length(normalTS)&lt;0.0001)\
cumulatedNormalOS = normalOS;

vec3 cumulatedNormalWS = normalVecOSToWS(cumulatedNormalOS);

// ------------------------------------------\
// Calculer diffusion et Specular

// Contribution Light 0\
vec3 diffContrib = vec3(0, 0, 0);\
vec3 specContrib = vec3(0, 0, 0);\
phong\_ombrage(Lamp0Color, cumulatedNormalWS, pointToLight0DirWS, pointToCameraDirWS, diffContrib, specContrib);

// Contribution Light 1\
vec3 diffContrib2 = vec3(0, 0, 0);\
vec3 specContrib2 = vec3(0, 0, 0);\
phong\_ombrage(Lamp1Color, cumulatedNormalWS, pointToLight1DirWS, pointToCameraDirWS, diffContrib2, specContrib2);

diffContrib += diffContrib2 ;\
specContrib += specContrib2 ;

vec4 diffuseColor = texture2D(diffuseMap,uv);

vec3 specularColor = texture2D(specularMap,uv).rgb ;\
vec3 R = reflect(pointToCameraDirWS, cumulatedNormalWS);\
vec3 reflColor = Kr \&#42; textureCube(environmentMap,R.xyz).bgr ;

float FallofRefl ;

if (KFs >= 0,0)\
FallofRefl = max((1-dot(pointToCameraDirWS/(KFs),cumulatedNormalWS)),0)\&#42;KF\_on ;\
else\
FallofRefl = (1-max(((1-dot(pointToCameraDirWS/(-KFs),cumulatedNormalWS))),0))\&#42;KF\_on ;

if (KF\_on == 0)\
FallofRefl=1,0 ;

vec3 Ambiant\_final = diffuseColor.rgb\&#42;AmbiColor ;

// ------------------------------------------\
vec3 emissive = texture2D(emissiveMap,uv).xyz ;

vec3 finalcolor = Ambiant\_final\
&#x200B;+ specularColor\&#42;specContrib\
&#x200B;+ diffuseColor.rgb\&#42;diffContrib\
&#x200B;+ (reflColor\&#42;specularColor\&#42;FallofRefl)\
&#x200B;+ émissif ;

// Couleur finale\
vec4 finalColor4 = vec4(finalcolor, texture2D(opacityMap,uv));

gl\_FragColor = finalColor4 ;\
&rbrace;

### Fichier GLSLFX

Le fichier glslfx définit deux techniques de rendu de la géométrie :

* On utilise la technique de tessellation matérielle
* L’autre se base sur un effet de parallaxe qui sera utilisé comme solution de secours si le matériel de l’utilisateur ne prend pas en charge la facettisation.

Situé dans .\tessellation\_parallax\fs.glsl

Contenu :

```
<?xml version="1.0" encoding="UTF-8"?>

<!DOCTYPE sbsbatchnode SYSTEM "glslfx.dtd">

<glslfx version="1.0.0" author="allegorithmic.com">



    <!-- TECHNIQUES -->

    <technique name="Tesselation">

        <!-- PROPERTIES -->

        <property name="blend_enabled" value="true"/>

        <property name="blend_func" value="src_alpha,one_minus_src_alpha"/>

        <property name="cull_face_enabled" value="true"/>

        <property name="cull_face_mode" value="back"/>



        <!-- SHADERS -->

        <shader type="vertex" filename="tessellation_parallax/tessellation/vs.glsl" primitiveType="patch4"/>

        <shader type="tess_control" filename="tessellation_parallax/tessellation/tcs.glsl"/>

        <shader type="tess_eval" filename="tessellation_parallax/tessellation/tes.glsl"/>

        <shader type="fragment" filename="tessellation_parallax/fs.glsl"/>



        <!-- UNIFORMS -->

        <uniform name="parallax_mode" guiName="Parallax Mode" min="0" max="0" />

        <uniform name="enableTilingInFS" guiName="Tiling Enabled In FS" min="0" max="0" />

        <uniform name="tessellationFactor" guiName="Tessellation Factor" default="4" min="1" max="64" guiStep="1" guiWidget="slider"/>

    </technique>



    <technique name="Parallax">

        <!-- PROPERTIES -->

        <property name="blend_enabled" value="true"/>

        <property name="blend_func" value="src_alpha,one_minus_src_alpha"/>

        <property name="cull_face_enabled" value="true"/>

        <property name="cull_face_mode" value="back"/>



        <!-- SHADERS -->

        <shader type="vertex" filename="tessellation_parallax/parallax/vs.glsl"/>

        <shader type="fragment" filename="tessellation_parallax/fs.glsl"/>



        <!-- UNIFORMS -->

        <uniform name="parallax_mode" guiName="Parallax Mode" min="1" max="1" />

        <uniform name="enableTilingInFS" guiName="Tiling Enabled In FS" min="1" max="1" />



    </technique>



    <!-- INPUT VERTEX FORMAT -->

    <vertexformat name="iVS_Position" semantic="position"/>

    <vertexformat name="iVS_Normal" semantic="normal"/>

    <vertexformat name="iVS_UV" semantic="texcoord0"/>

    <vertexformat name="iVS_Tangent" semantic="tangent0"/>

    <vertexformat name="iVS_Binormal" semantic="binormal0"/>



    <!-- SAMPLERS -->

    <sampler name="diffuseMap" usage="diffuse"/>

    <sampler name="heightMap" usage="height"/>

    <sampler name="normalMap" usage="normal"/>

    <sampler name="detailNormalMap" usage="detailNormal"/>

    <sampler name="emissiveMap" usage="emissive"/>

    <sampler name="specularMap" usage="specular"/>

    <sampler name="opacityMap" usage="opacity"/>

    <sampler name="environmentMap" usage="environment"/>



    <!-- MATRICES -->

    <uniform name="worldMatrix" semantic="world"/>

    <uniform name="worldViewProjMatrix" semantic="worldviewprojection"/>

    <uniform name="worldViewMatrix" semantic="worldview"/>

    <uniform name="worldInverseTransposeMatrix" semantic="worldinversetranspose"/>

    <uniform name="viewInverseMatrix" semantic="viewinverse"/>

    <uniform name="modelViewMatrix" semantic="modelview"/>

    <uniform name="projectionMatrix" semantic="projection"/>



    <!-- SCENE PARAMETERS -->

    <uniform name="AmbiColor" semantic="ambient"/>

    <uniform name="Lamp0Pos" semantic="lightposition0"/>

    <uniform name="Lamp0Color" semantic="lightcolor0"/>

    <uniform name="Lamp1Pos" semantic="lightposition1"/>

    <uniform name="Lamp1Color" semantic="lightcolor1"/>



    <!-- UNIFORMS -->

    <uniform name="tiling" guiName="Tiling" default="1" min="1" guiWidget="slider" guiMax="10"/>

    <uniform name="heightMapScale" guiGroup="Height" guiName="Scale" default="1" min="0" guiWidget="slider" guiMin="-50" guiMax="50" />

    <uniform name="TilingDetail" guiGroup="Detail Normal" guiName="Tiling" default="3" min="1" guiWidget="slider" guiMax="10"/>

    <uniform name="Depth_detail" guiGroup="Detail Normal" guiName="Intensity" default="0.5" min="0" max="1" guiStep="0.05" guiWidget="slider"/>

    <uniform name="SpecExpon" guiGroup="Specular" guiName="Power" default="50" min="1" guiWidget="slider" guiMax="128"/>

    <uniform name="Ks" guiGroup="Specular" guiName="Intensity" default="1" min="0" guiWidget="slider" guiMax="3"/>

    <uniform name="Kr" guiGroup="Reflection" guiName="Intensity" default="0.5" min="0" max="1" guiStep="0.01" guiWidget="slider"/>

    <uniform name="KF_on" guiGroup="Reflection" guiName="Falloff" default="1" min="0" max="1" guiStep="1" guiWidget="slider"/>

    <uniform name="KFs" guiGroup="Reflection" guiName="Falloff Size" default="1" min="-1" max="1" guiStep="0.05" guiWidget="slider"/>



</glslfx>
```
