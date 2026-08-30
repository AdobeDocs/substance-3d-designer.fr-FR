---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/interface/3d-view/camera/post-effects.html"
breadcrumb-title: ''
description: Appliquez des effets de post-traitement à la caméra de vue 3D pour un aperçu et une visualisation améliorés des matériaux.
helpx_creative_field: ""
helpx_description: Designer > Interface > 3D view > Camera > Post effects
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Effets de post-traitement
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '732'
ht-degree: 4%

---


# Effets de post-traitement

![Effets de post](post-effects.resources/postEffects.png "Effets de post"){zoomable="yes"}

Dans les propriétés de caméra, vous pouvez activer les effets de post-traitement pour améliorer les rendus ou vérifier des propriétés de matériau spécifiques.

Ces effets sont développés en interne et ne sont disponibles que pour le pixelliseur et les [rendus](../../../../interface/3d-view/3d-renderers/3d-renderers.md) Pathtracer GPU.

Tout effet de post-publication activé au moment de l&#39;enregistrement des [ressources de scène 3D](../../../../resources/3d-scene-resource/3d-scene-resource.md) ou des [fichiers d&#39;état de scène](../../../../working-with-3d-scenes/working-with-3d-scenes.md) sera enregistré dans le cadre de l&#39;état de la scène.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Mappage de tons

</td>
<td style="border: 0;" valign="top">

### Flou lumineux

</td>
<td style="border: 0;" valign="top">

### Profondeur de champ

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

## Mappage de tons

Remappe les couleurs du rendu en fonction d’algorithmes et/ou de tables de correspondance (LUT) spécifiques.

Cela vous permet d’améliorer la cohérence des couleurs entre les applications. Par exemple, le mappeur de tonalité AgX est également disponible dans Blender.

+++Reinhard


<table>
  <tr>
    <td>
      <img src="post-effects.resources/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="post-effects.resources/PostFXReinhard.jpg" alt="PostFXReinhard">
      <br><i>Après</i>
    </td>
  </tr>
</table>



![PostFXDisabled](post-effects.resources/PostFXDisabled.jpg "PostFXDisabled")

![PostFXReinhard](post-effects.resources/PostFXReinhard.jpg "PostFXReinhard")

+++

+++Atan


<table>
  <tr>
    <td>
      <img src="post-effects.resources/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="post-effects.resources/PostFXAtan.jpg" alt="PostFXAtan">
      <br><i>Après</i>
    </td>
  </tr>
</table>



![PostFXDisabled](post-effects.resources/PostFXDisabled.jpg "PostFXDisabled")

![PostFXAtan](post-effects.resources/PostFXAtan.jpg "PostFXAtan")

+++

+++Exp


<table>
  <tr>
    <td>
      <img src="post-effects.resources/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="post-effects.resources/PostFXExp.jpg" alt="PostFXExp">
      <br><i>Après</i>
    </td>
  </tr>
</table>



![PostFXDisabled](post-effects.resources/PostFXDisabled.jpg "PostFXDisabled")

![PostFXExp](post-effects.resources/PostFXExp.jpg "PostFXExp")

+++

+++Journal


<table>
  <tr>
    <td>
      <img src="post-effects.resources/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="post-effects.resources/PostFXLog.jpg" alt="PostFXLog">
      <br><i>Après</i>
    </td>
  </tr>
</table>



![PostFXDisabled](post-effects.resources/PostFXDisabled.jpg "PostFXDisabled")

![PostFXLog](post-effects.resources/PostFXLog.jpg "PostFXLog")

+++

+++Aces


<table>
  <tr>
    <td>
      <img src="post-effects.resources/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="post-effects.resources/PostFXAces.jpg" alt="PostFXAces">
      <br><i>Après</i>
    </td>
  </tr>
</table>



![PostFXDisabled](post-effects.resources/PostFXDisabled.jpg "PostFXDisabled")

![PostFXAces](post-effects.resources/PostFXAces.jpg "PostFXAces")

+++

+++Hejl


<table>
  <tr>
    <td>
      <img src="post-effects.resources/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="post-effects.resources/PostFXHejl.jpg" alt="PostFXHel">
      <br><i>Après</i>
    </td>
  </tr>
</table>



![PostFXDisabled](post-effects.resources/PostFXDisabled.jpg "PostFXDisabled")

![PostFXHejl](post-effects.resources/PostFXHejl.jpg "PostFXHejl")

+++

+++Neutre


<table>
  <tr>
    <td>
      <img src="post-effects.resources/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="post-effects.resources/PostFXNeutral.jpg" alt="PostFXNeutral">
      <br><i>Après</i>
    </td>
  </tr>
</table>



![PostFXDisabled](post-effects.resources/PostFXDisabled.jpg "PostFXDisabled")

![PostFXNeutral](post-effects.resources/PostFXNeutral.jpg "PostFXNeutral")

+++

+++Agx


<table>
  <tr>
    <td>
      <img src="post-effects.resources/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="post-effects.resources/PostFXAgx.jpg" alt="PostFXAgx">
      <br><i>Après</i>
    </td>
  </tr>
</table>



![PostFXDisabled](post-effects.resources/PostFXDisabled.jpg "PostFXDisabled")

![PostFXAgx](post-effects.resources/PostFXAgx.jpg "PostFXAgx")

+++

+++Pbr neutre


<table>
  <tr>
    <td>
      <img src="post-effects.resources/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="post-effects.resources/PostFXPbrNeutral.jpg" alt="PostFXPbrNeutral">
      <br><i>Après</i>
    </td>
  </tr>
</table>



![PostFXDisabled](post-effects.resources/PostFXDisabled.jpg "PostFXDisabled")

![PostFXPbrNeutral](post-effects.resources/PostFXPbrNeutral.jpg "PostFXPbrNeutral")

+++

## Flou lumineux

Simule l’effet de caméra de franges de lumières qui se saignent vers l’extérieur à partir de zones très lumineuses vers des zones recevant moins de lumière.

L’effet dépend de l’éclairage de la scène, de l’exposition de la caméra et des matériaux d’emissive.

+++Seuil
Valeur de luminance au-dessus de laquelle la floraison doit être visible.

*Gauche : 1,0 / Droite : 4,0*



<table>
  <tr>
    <td>
      <img src="post-effects.resources/bloomThreshold1.jpg" alt="bloomThreshold1">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="post-effects.resources/bloomThreshold4.jpg" alt="bloomThreshold4">
      <br><i>Après</i>
    </td>
  </tr>
</table>



![bloomThreshold1](post-effects.resources/bloomThreshold1.jpg "bloomThreshold1")

![bloomThreshold4](post-effects.resources/bloomThreshold4.jpg "bloomThreshold4")

+++

+++Atténuation
Dégradé d&#39;atténuation de la floraison, où une valeur plus faible réduit le rayon de la floraison.

*Gauche : 1,0 / Droite : 0,6*



<table>
  <tr>
    <td>
      <img src="post-effects.resources/bloomFalloff1.jpg" alt="bloomFalloff1">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="post-effects.resources/bloomFalloff0-6.jpg" alt="bloomFalloff0-6">
      <br><i>Après</i>
    </td>
  </tr>
</table>



![bloomFalloff1](post-effects.resources/bloomFalloff1.jpg "bloomFalloff1")

![bloomFalloff0-6](post-effects.resources/bloomFalloff0-6.jpg "bloomFalloff0-6")

+++

+++Niveau
L&#39;intensité de la floraison. Plus la valeur est élevée, plus les franges de lumière sont claires et marquées.

*Gauche : 8.0 / Droite : 2.0*



<table>
  <tr>
    <td>
      <img src="post-effects.resources/bloomLevel8.jpg" alt="bloomLevel8">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="post-effects.resources/bloomLevel2.jpg" alt="bloomLevel2">
      <br><i>Après</i>
    </td>
  </tr>
</table>



![bloomLevel8](post-effects.resources/bloomLevel8.jpg "bloomLevel8")

![bloomLevel2](post-effects.resources/bloomLevel2.jpg "bloomLevel2")

+++

+++Changement de couleur
Décale la teinte des zones affectées par la floraison vers des couleurs plus chaudes.

*Gauche : 0,0 / Droite : 0,8*



<table>
  <tr>
    <td>
      <img src="post-effects.resources/bloomColorShift0.jpg" alt="bloomColorShift0">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="post-effects.resources/bloomColorShift0-8.jpg" alt="bloomColorShift0-8">
      <br><i>Après</i>
    </td>
  </tr>
</table>



![bloomColorShift0](post-effects.resources/bloomColorShift0.jpg "bloomColorShift0")

![bloomColorShift0-8](post-effects.resources/bloomColorShift0-8.jpg "bloomColorShift0-8")

+++

## Profondeur de champ

Simule le phénomène optique provoqué par les objectifs de caméra où les objets plus proches et plus éloignés que la distance focale sont flous.

L&#39;effet est affecté par les paramètres « F-Stop » et « Distance de mise au point » de la caméra.

>[!TIP]
>
> Pour régler rapidement la mise au point de la caméra, placez le curseur sur l’emplacement d’une scène que vous souhaitez mettre au point et appuyez sur Ctrl + LMB (Windows) ou Cmd + LMB (macOS) pour définir automatiquement la distance de mise au point sur cet emplacement.

+++Rayon max.
Rayon maximal de l’effet de flou.

*Gauche : 32,0 / Droite : 4,0*



<table>
  <tr>
    <td>
      <img src="post-effects.resources/depthOfFieldMaxRadius32.jpg" alt="depthOfFieldMaxRadius32">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="post-effects.resources/depthOfFieldMaxRadius4.jpg" alt="depthOfFieldMaxRadius4">
      <br><i>Après</i>
    </td>
  </tr>
</table>



![depthOfFieldMaxRadius32](post-effects.resources/depthOfFieldMaxRadius32.jpg "depthOfFieldMaxRadius32")

![depthOfFieldMaxRadius4](post-effects.resources/depthOfFieldMaxRadius4.jpg "depthOfFieldMaxRadius4")

+++

+++Force composite
Ampleur de l’effet de flou à partir de la distance focale vers l’extérieur.

*Gauche : 0,2 / Droite : 0,05*



<table>
  <tr>
    <td>
      <img src="post-effects.resources/depthOfFieldCompositeStrength0-2.jpg" alt="depthOfFieldCompositeStrength0-2">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="post-effects.resources/depthOfFieldCompositeStrength0-05.jpg" alt="depthOfFieldCompositeStrength0-05">
      <br><i>Après</i>
    </td>
  </tr>
</table>



![depthOfFieldCompositeStrength0-2](post-effects.resources/depthOfFieldCompositeStrength0-2.jpg "depthOfFieldCompositeStrength0-2")

![depthOfFieldCompositeStrength0-05](post-effects.resources/depthOfFieldCompositeStrength0-05.jpg "depthOfFieldCompositeStrength0-05")

+++

+++Aberration longitudinale
Intensité de l&#39;aberration se produisant à distance de la distance focale.

L’aberration simule comment différentes longueurs d’onde de la lumière ont des distances focales légèrement différentes, ce qui donne l’impression que les couleurs sont décalées et présentent des différences subtiles de mise au point.

*Gauche : 0,0 / Droite : 1,0*



<table>
  <tr>
    <td>
      <img src="post-effects.resources/depthOfFieldLongitudinalAberration0.jpg" alt="depthOfFieldLongitudinalAberration0">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="post-effects.resources/depthOfFieldLongitudinalAberration1.jpg" alt="depthOfFieldLongitudinalAberration1">
      <br><i>Après</i>
    </td>
  </tr>
</table>



![depthOfFieldLongitudinalAberration0](post-effects.resources/depthOfFieldLongitudinalAberration0.jpg "depthOfFieldLongitudinalAberration0")

![depthOfFieldLongitudinalAberration1](post-effects.resources/depthOfFieldLongitudinalAberration1.jpg "depthOfFieldLongitudinalAberration1")

+++

+++Aberration achromatique
Indique si l’aberration doit être achromatique, ce qui signifie que certaines couleurs ou toutes ont la même distance focale.

Ainsi, l’effet de flou semble être réparti de manière plus égale.

*À Gauche : Vrai/À Droite : Faux*



<table>
  <tr>
    <td>
      <img src="post-effects.resources/depthOfFieldAchromaticAberrationYes.jpg" alt="depthOfFieldAchromaticAberrationYes">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="post-effects.resources/depthOfFieldAchromaticAberrationNo.jpg" alt="depthOfFieldAchromaticAberrationNo">
      <br><i>Après</i>
    </td>
  </tr>
</table>



![depthOfFieldAchromaticAberrationYes](post-effects.resources/depthOfFieldAchromaticAberrationYes.jpg "depthOfFieldAchromaticAberrationYes")

![depthOfFieldAchromaticAberrationNo](post-effects.resources/depthOfFieldAchromaticAberrationNo.jpg "depthOfFieldAchromaticAberrationNo")

+++

+++Œil de chat
Active l’effet d’œil de chat dans la scène. Ce dernier simule comment la lumière pénétrant à un angle oblique ne pénètre pas dans un disque, mais dans un ovale irrégulier, ce qui provoque une distorsion.

Cet effet est plus prononcé aux ouvertures supérieures, c&#39;est-à-dire aux valeurs F-Stop plus faibles.

*À Gauche : Vrai/À Droite : Faux*



<table>
  <tr>
    <td>
      <img src="post-effects.resources/depthOfFieldAchromaticCatsEyeYes.jpg" alt="depthOfFieldAchromaticCatsEyeYes">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="post-effects.resources/depthOfFieldAchromaticCatsEyeNo.jpg" alt="depthOfFieldAchromaticCatsEyeNo">
      <br><i>Après</i>
    </td>
  </tr>
</table>



![depthOfFieldAchromaticCatsEyeYes](post-effects.resources/depthOfFieldAchromaticCatsEyeYes.jpg "depthOfFieldAchromaticCatsEyeYes")

![depthOfFieldAchromaticCatsEyeNo](post-effects.resources/depthOfFieldAchromaticCatsEyeNo.jpg "depthOfFieldAchromaticCatsEyeNo")

+++
