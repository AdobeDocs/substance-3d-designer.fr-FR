---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/package-metadata.html"
breadcrumb-title: ''
description: Découvrez comment créer et gérer des métadonnées de pack dans Substance 3D Designer pour les bibliothèques de ressources organisées.
helpx_creative_field: ""
helpx_description: Designer > Package Metadata
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Métadonnées du package
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '729'
ht-degree: 0%

---


# Métadonnées du package

Les métadonnées de package sont un dictionnaire de valeurs de texte (chaînes) définies au niveau du package. Il est inclus dans le SBSAR lors de la publication, et il s&#39;agit d&#39;un stockage à usage général destiné à être utilisé par le script python.

## Affichage et modification des métadonnées via l’interface Designer

Si vous développez un plug-in Python, vous pouvez modifier les métadonnées manuellement à des fins de test et de débogage. Voici comment procéder :

1. Si vous double-cliquez sur un pack dans l’explorateur, le panneau Propriétés s’ouvre sur ce pack.

   ![Métadonnées du package](../assets/empty.png "Métadonnées du package")
1. Ici, vous avez une section dédiée « Métadonnées ». Il est probablement vide dans votre cas, comme dans la capture ci-dessus.

   Vous pouvez ajouter de nouvelles métadonnées en utilisant le bouton « plus ».

   ![Bouton Ajouter des métadonnées](../assets/hoveradd.png "Bouton Ajouter des métadonnées")
1. Un nouvel élément apparaît dans la section :

   ![Nouvelles métadonnées](../assets/newitem-1.png "Nouvelles métadonnées")
1. Il existe un champ « Clé » et un champ « Valeur ». Les deux peuvent être réglés sur tout ce qui convient à vos besoins. Le champ « Clé » doit avoir une valeur unique dans la liste.

   ![Nouvelle valeur de métadonnées](../assets/newitemfilled.png "Nouvelle valeur de métadonnées")
1. Vous pouvez également choisir le « Type » de l’élément. Pour le moment, il peut s’agir de « String » ou « URL » :

   ![Modifier le type de métadonnées](../assets/typecombo.png "Modifier le type de métadonnées")
1. Ici, le terme « URL » désigne une référence à une ressource incluse dans le package. Pour ce faire, sélectionnez un fichier sur votre disque dur, puis faites-le glisser sur le pack dans l’Explorateur. Il peut s’agir d’une ressource ordinaire, comme une image, ou de tout autre fichier, comme un fichier texte.

   ![Ressource générique dans le pack](../assets/resourceinpackage.png "Ressource générique dans le pack")
1. Le fichier apparaît comme une nouvelle ressource dans le package.

   Revenez maintenant au panneau Propriétés du package, créez une nouvelle métadonnée, attribuez-lui une clé appropriée et choisissez « URL » comme type. Sélectionnez ensuite le symbole « ... ». dans le champ « Valeur », et choisissez « De la ressource ». Enfin, choisissez le fichier que vous avez inclus juste avant et validez :

   ![Métadonnées d&#39;URL](../assets/urlmetadata.gif "Métadonnées d&#39;URL")
1. Vous pouvez maintenant voir que l&#39;URL de la ressource est stockée dans le champ Valeur.

   Vous pouvez également supprimer les métadonnées à l’aide du bouton « X » situé à droite de l’élément :

   ![Supprimer les métadonnées](../assets/hoverdelete.png "Supprimer les métadonnées")

>[!NOTE]
>
> Le déplacement ou la réorganisation des entrées de métadonnées est désactivé : l’ordre n’est pas significatif et ne sera pas conservé lors de la publication du package.

## Métadonnées dans les fichiers SBSAR publiés

Dans certains cas, vous pouvez récupérer les métadonnées que vous avez définies sur un package dans le SBSAR publié correspondant. Vous trouverez ci-dessous la manière dont les métadonnées sont transformées et stockées dans l&#39;archive, ainsi que la manière appropriée de les exploiter.

Les métadonnées sont stockées au format JSON dans un fichier nommé /assemblies/content/0000/metadata.json (le chemin est relatif à la racine de l’archive .sbsar).

Les métadonnées normales (chaîne) sont stockées telles quelles, par exemple « key » : « stringValue », une par ligne. Là encore, l&#39;ordre d&#39;origine des différentes clés n&#39;est pas conservé et sa mise en œuvre est définie. Ne vous fiez jamais à l&#39;ordre dans votre processus, comme avec les dicts Python réguliers !

Comme le but des métadonnées d&#39;URL est de permettre aux utilisateurs et aux plug-ins d&#39;inclure des fichiers étrangers dans l&#39;archive .sbsar, ils sont soumis à une transformation spécifique : Tout d&#39;abord, le fichier de la ressource correspondant à l&#39;URL stockée est copié dans l&#39;archive dans un emplacement défini par l&#39;implémentation (généralement dans un sous-dossier numéroté, qui contiendra uniquement ce fichier. Il s’agit d’éviter tout conflit de nom.) Le fichier conserve son nom d’origine (le nom de la ressource est ignoré à ce stade). Ainsi, au lieu de l’URL d’origine dans metadata.json, le chemin d’accès au fichier copié dans l’archive relatif à metadata.json est écrit.

Si nous exportons l’exemple de pack créé dans la section précédente (après avoir créé au moins un graphique avec certaines sorties), nous obtenons ce contenu d’archive :

```
myPackage.sbsar

|-- assemblies

        |-- content

            |-- 0000

                |-- New_Graph.sbsasm

                |-- New_Graph.xml

                |-- metadata.json

                |-- resources

                    |-- 0

                        |-- TEXT.txt
```


Et le contenu metadata.json est :

```
{

    "myResource": "resources/0/TEXT.txt",

    "myText": "This is a text"

}
```


À l&#39;heure actuelle, aucun outil spécifique n&#39;est fourni pour accéder aux métadonnées et aux ressources stockées dans l&#39;archive. La méthode recommandée est d’ouvrir l’archive avec le décodeur LZMA de votre choix et d’analyser le fichier metadata.json avec un analyseur JSON standard (si les clés ou les chaînes de valeurs contiennent des caractères fantaisie, ils seront échappés de la manière JSON).

>[!NOTE]
>
> Il ne reste aucune information sur le fait que chaque métadonnée soit une simple chaîne ou une URL, donc vous devez savoir ce que chaque clé que vous voulez lire est censée signifier.
