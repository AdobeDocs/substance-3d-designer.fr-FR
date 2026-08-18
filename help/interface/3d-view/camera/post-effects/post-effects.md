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
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '732'
ht-degree: 4%

---


# Effets de post-traitement

![Effets de post](../../../../assets/postEffects.png "Effets de post"){zoomable="yes"}

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
      <img src="../../../../assets/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXReinhard.jpg" alt="PostFXReinhard">
      <br><i>Après</i>
    </td>
  </tr>
</table>



![PostFXDisabled](../../../../assets/PostFXDisabled.jpg "PostFXDisabled")

![PostFXReinhard](../../../../assets/PostFXReinhard.jpg "PostFXReinhard")

+++

+++Atan


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXAtan.jpg" alt="PostFXAtan">
      <br><i>Après</i>
    </td>
  </tr>
</table>



![PostFXDisabled](../../../../assets/PostFXDisabled.jpg "PostFXDisabled")

![PostFXAtan](../../../../assets/PostFXAtan.jpg "PostFXAtan")

+++

+++Exp


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXExp.jpg" alt="PostFXExp">
      <br><i>Après</i>
    </td>
  </tr>
</table>



![PostFXDisabled](../../../../assets/PostFXDisabled.jpg "PostFXDisabled")

![PostFXExp](../../../../assets/PostFXExp.jpg "PostFXExp")

+++

+++Journal


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXLog.jpg" alt="PostFXLog">
      <br><i>Après</i>
    </td>
  </tr>
</table>



![PostFXDisabled](../../../../assets/PostFXDisabled.jpg "PostFXDisabled")

![PostFXLog](../../../../assets/PostFXLog.jpg "PostFXLog")

+++

+++Aces


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXAces.jpg" alt="PostFXAces">
      <br><i>Après</i>
    </td>
  </tr>
</table>



![PostFXDisabled](../../../../assets/PostFXDisabled.jpg "PostFXDisabled")

![PostFXAces](../../../../assets/PostFXAces.jpg "PostFXAces")

+++

+++Hejl


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXHejl.jpg" alt="PostFXHel">
      <br><i>Après</i>
    </td>
  </tr>
</table>



![PostFXDisabled](../../../../assets/PostFXDisabled.jpg "PostFXDisabled")

![PostFXHejl](../../../../assets/PostFXHejl.jpg "PostFXHejl")

+++

+++Neutre


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXNeutral.jpg" alt="PostFXNeutral">
      <br><i>Après</i>
    </td>
  </tr>
</table>



![PostFXDisabled](../../../../assets/PostFXDisabled.jpg "PostFXDisabled")

![PostFXNeutral](../../../../assets/PostFXNeutral.jpg "PostFXNeutral")

+++

+++Agx


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXAgx.jpg" alt="PostFXAgx">
      <br><i>Après</i>
    </td>
  </tr>
</table>



![PostFXDisabled](../../../../assets/PostFXDisabled.jpg "PostFXDisabled")

![PostFXAgx](../../../../assets/PostFXAgx.jpg "PostFXAgx")

+++

+++Pbr neutre


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXPbrNeutral.jpg" alt="PostFXPbrNeutral">
      <br><i>Après</i>
    </td>
  </tr>
</table>



![PostFXDisabled](../../../../assets/PostFXDisabled.jpg "PostFXDisabled")

![PostFXPbrNeutral](../../../../assets/PostFXPbrNeutral.jpg "PostFXPbrNeutral")

+++

## Flou lumineux

Simule l’effet produit par l’appareil photo de franges de lumières se vidant des zones très lumineuses vers l’extérieur sur les zones recevant moins de lumière.

L’effet est influencé par l’éclairage de la scène, l’exposition de l’appareil photo et les matériaux émissifs.

+++Seuil
Valeur de luminance au-dessus de laquelle la floraison doit être visible.

*Gauche : 1,0 / Droite : 4,0*



<table>
  <tr>
    <td>
      <img src="../../../../assets/bloomThreshold1.jpg" alt="bloomThreshold1">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="../../../../assets/bloomThreshold4.jpg" alt="bloomThreshold4">
      <br><i>Après</i>
    </td>
  </tr>
</table>



![bloomThreshold1](../../../../assets/bloomThreshold1.jpg "bloomThreshold1")

![bloomThreshold4](../../../../assets/bloomThreshold4.jpg "bloomThreshold4")

+++

+++Atténuation
Dégradé d&#39;atténuation de la floraison, où une valeur plus faible réduit le rayon de la floraison.

*Gauche : 1,0 / Droite : 0,6*



<table>
  <tr>
    <td>
      <img src="../../../../assets/bloomFalloff1.jpg" alt="bloomFalloff1">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="../../../../assets/bloomFalloff0-6.jpg" alt="bloomFalloff0-6">
      <br><i>Après</i>
    </td>
  </tr>
</table>



![bloomFalloff1](../../../../assets/bloomFalloff1.jpg "bloomFalloff1")

![bloomFalloff0-6](../../../../assets/bloomFalloff0-6.jpg "bloomFalloff0-6")

+++

+++Niveau
L&#39;intensité de la floraison. Plus la valeur est élevée, plus les franges de lumière sont claires et marquées.

*Gauche : 8.0 / Droite : 2.0*



<table>
  <tr>
    <td>
      <img src="../../../../assets/bloomLevel8.jpg" alt="bloomLevel8">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="../../../../assets/bloomLevel2.jpg" alt="bloomLevel2">
      <br><i>Après</i>
    </td>
  </tr>
</table>



![bloomLevel8](../../../../assets/bloomLevel8.jpg "bloomLevel8")

![bloomLevel2](../../../../assets/bloomLevel2.jpg "bloomLevel2")

+++

+++Changement de couleur
Décale la teinte des zones affectées par la floraison vers des couleurs plus chaudes.

*Gauche : 0,0 / Droite : 0,8*



<table>
  <tr>
    <td>
      <img src="../../../../assets/bloomColorShift0.jpg" alt="bloomColorShift0">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="../../../../assets/bloomColorShift0-8.jpg" alt="bloomColorShift0-8">
      <br><i>Après</i>
    </td>
  </tr>
</table>



![bloomColorShift0](../../../../assets/bloomColorShift0.jpg "bloomColorShift0")

![bloomColorShift0-8](../../../../assets/bloomColorShift0-8.jpg "bloomColorShift0-8")

+++

## Profondeur de champ

Simule le phénomène optique provoqué par les objectifs de l’appareil photo lorsque des objets plus proches et plus éloignés que la distance focale sont flous.

L’effet est affecté par les paramètres « F-Stop » et « Distance de mise au point » de l’appareil photo.

>[!TIP]
>
> Pour régler rapidement la mise au point de l’appareil photo, placez le curseur sur l’emplacement d’une scène que vous souhaitez mettre au point et appuyez sur les touches Ctrl + LMB (Windows) ou Cmd + LMB (macOS) pour définir automatiquement la distance de mise au point sur cet emplacement.

+++Rayon max.
Rayon maximal de l’effet de flou.

*Gauche : 32,0 / Droite : 4,0*



<table>
  <tr>
    <td>
      <img src="../../../../assets/depthOfFieldMaxRadius32.jpg" alt="depthOfFieldMaxRadius32">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="../../../../assets/depthOfFieldMaxRadius4.jpg" alt="depthOfFieldMaxRadius4">
      <br><i>Après</i>
    </td>
  </tr>
</table>



![depthOfFieldMaxRadius32](../../../../assets/depthOfFieldMaxRadius32.jpg "depthOfFieldMaxRadius32")

![depthOfFieldMaxRadius4](../../../../assets/depthOfFieldMaxRadius4.jpg "depthOfFieldMaxRadius4")

+++

+++Force composite
Ampleur de l’effet de flou à partir de la distance focale vers l’extérieur.

*Gauche : 0,2 / Droite : 0,05*



<table>
  <tr>
    <td>
      <img src="../../../../assets/depthOfFieldCompositeStrength0-2.jpg" alt="depthOfFieldCompositeStrength0-2">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="../../../../assets/depthOfFieldCompositeStrength0-05.jpg" alt="depthOfFieldCompositeStrength0-05">
      <br><i>Après</i>
    </td>
  </tr>
</table>



![depthOfFieldCompositeStrength0-2](../../../../assets/depthOfFieldCompositeStrength0-2.jpg "depthOfFieldCompositeStrength0-2")

![depthOfFieldCompositeStrength0-05](../../../../assets/depthOfFieldCompositeStrength0-05.jpg "depthOfFieldCompositeStrength0-05")

+++

+++Aberration longitudinale
Intensité de l&#39;aberration se produisant à distance de la distance focale.

L’aberration simule comment différentes longueurs d’onde de la lumière ont des distances focales légèrement différentes, ce qui donne l’impression que les couleurs sont décalées et présentent des différences subtiles de mise au point.

*Gauche : 0,0 / Droite : 1,0*



<table>
  <tr>
    <td>
      <img src="../../../../assets/depthOfFieldLongitudinalAberration0.jpg" alt="depthOfFieldLongitudinalAberration0">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="../../../../assets/depthOfFieldLongitudinalAberration1.jpg" alt="depthOfFieldLongitudinalAberration1">
      <br><i>Après</i>
    </td>
  </tr>
</table>



![depthOfFieldLongitudinalAberration0](../../../../assets/depthOfFieldLongitudinalAberration0.jpg "depthOfFieldLongitudinalAberration0")

![depthOfFieldLongitudinalAberration1](../../../../assets/depthOfFieldLongitudinalAberration1.jpg "depthOfFieldLongitudinalAberration1")

+++

+++Aberration achromatique
Indique si l’aberration doit être achromatique, ce qui signifie que certaines couleurs ou toutes ont la même distance focale.

Ainsi, l’effet de flou semble être réparti de manière plus égale.

*À Gauche : Vrai/À Droite : Faux*



<table>
  <tr>
    <td>
      <img src="../../../../assets/depthOfFieldAchromaticAberrationYes.jpg" alt="depthOfFieldAchromaticAberrationYes">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="../../../../assets/depthOfFieldAchromaticAberrationNo.jpg" alt="depthOfFieldAchromaticAberrationNo">
      <br><i>Après</i>
    </td>
  </tr>
</table>



![depthOfFieldAchromaticAberrationYes](../../../../assets/depthOfFieldAchromaticAberrationYes.jpg "depthOfFieldAchromaticAberrationYes")

![depthOfFieldAchromaticAberrationNo](../../../../assets/depthOfFieldAchromaticAberrationNo.jpg "depthOfFieldAchromaticAberrationNo")

+++

+++Œil de chat
Active l’effet d’œil de chat dans la scène. Ce dernier simule comment la lumière pénétrant à un angle oblique ne pénètre pas dans un disque, mais dans un ovale irrégulier, ce qui provoque une distorsion.

Cet effet est plus prononcé aux ouvertures supérieures, c&#39;est-à-dire aux valeurs F-Stop plus faibles.

*À Gauche : Vrai/À Droite : Faux*



<table>
  <tr>
    <td>
      <img src="../../../../assets/depthOfFieldAchromaticCatsEyeYes.jpg" alt="depthOfFieldAchromaticCatsEyeYes">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="../../../../assets/depthOfFieldAchromaticCatsEyeNo.jpg" alt="depthOfFieldAchromaticCatsEyeNo">
      <br><i>Après</i>
    </td>
  </tr>
</table>



![depthOfFieldAchromaticCatsEyeYes](../../../../assets/depthOfFieldAchromaticCatsEyeYes.jpg "depthOfFieldAchromaticCatsEyeYes")

![depthOfFieldAchromaticCatsEyeNo](../../../../assets/depthOfFieldAchromaticCatsEyeNo.jpg "depthOfFieldAchromaticCatsEyeNo")

+++
