---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/pipeline-and-project-configuration/user-preferences-automating-setup.html"
breadcrumb-title: ''
description: Découvrez comment automatiser la configuration des préférences utilisateur dans Substance 3D Designer pour rationaliser le workflow.
helpx_creative_field: ""
helpx_description: Designer > Pipeline and Project Configuration > User Preferences - Automating Setup
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Préférences utilisateur - Automatisation de la configuration
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '656'
ht-degree: 0%

---


# Préférences utilisateur - Automatisation de la configuration

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Le fichier user\_preferences.xml contient tous les paramètres spécifiques à l&#39;utilisateur en dehors de ceux définis dans une [configuration de projet](../../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md). Ils concernent principalement des paramètres d’interface utilisateur et de performances spécifiques.

Le seul paramètre pertinent à modifier est le [fichier de configuration](../../pipeline-and-project-con/configuration-list-sbscfg/configuration-list-sbscfg.md) qui contient une liste de projets. Cela peut être fait de plusieurs façons, comme indiqué ci-dessous.

Vous pouvez également ignorer complètement la modification des préférences utilisateur et effectuer un remplacement basé sur la session du fichier SBSCFG à l’aide d’un argument de ligne de commande sur le raccourci Designer, voir ci-dessous.

</td>
<td width="25.00%" style="border: 0;" valign="top">

Icône ![Fichier XML](user-preferences-automating-setup.resources/user-preferences-automating-setup-01.png "Icône de fichier XML")

</td>
</tr>
</table>

## Permanent ou basé sur une session

Il existe deux façons différentes de configurer Designer pour utiliser un autre [fichier de configuration](../../pipeline-and-project-con/configuration-list-sbscfg/configuration-list-sbscfg.md) que le fichier par défaut, avec des avantages et des inconvénients :

* <b>Modification définitive du fichier user\_preferences.xml\
  </b>Ce fichier se trouve dans *~User\AppData\Local\Adobe\Adobe Substance 3D Designer* pour Windows. Si vous le modifiez, Designer utilisera toujours ce qui y est défini, indépendamment de la façon, du moment et de l’endroit où vous le démarrez. Apporter des modifications nécessite de modifier à nouveau le XML. Ces deux opérations sont décrites ci-dessous et ont tendance à être un peu complexes.
* <b>Définition temporaire de la session via un argument de ligne de commande\
  </b>Designer peut accepter un argument de ligne de commande au démarrage pour remplacer le fichier SBSCFG pour cette session (voir ci-dessous pour savoir comment procéder). Il s’agit d’une solution simple et élégante, qui permet de changer de projet beaucoup plus rapidement qu’en modifiant un fichier XML. Le danger est que si vous ouvrez via plusieurs raccourcis (par exemple, Menu Démarrer et Bureau sous Windows), vous pouvez obtenir des résultats différents sans que cela soit tout à fait évident. En outre, il n&#39;est pas aussi inviolable, car les utilisateurs peuvent supprimer, déplacer ou modifier leurs raccourcis beaucoup plus facilement que leur utilisateur\_preferences.xml.

## Modification XML

### Modification manuelle des préférences

S&#39;il n&#39;y a pas d&#39;installation automatisée, ou à des fins de test, vous pouvez accéder manuellement à <b>Modifier > Préférences...</b>, puis cliquer sur la section « <b>Projets</b> » sur la gauche.

![Paramètres du projet](user-preferences-automating-setup.resources/user-preferences-automating-setup-02.png "Paramètres du projet")

Le bouton marqué en rouge permet à l&#39;utilisateur de choisir un autre[fichier SBSCFG](../../pipeline-and-project-con/configuration-list-sbscfg/configuration-list-sbscfg.md).

### Modification via un script

Tout comme les fichiers de projet et de configuration, les préférences de l’utilisateur sont un XML structuré, avec le paramètre pertinent clairement identifiable. Plutôt que de modifier via un éditeur de texte comme le Bloc-notes++ ou le texte sublime, il est très bien adapté à la modification via une configuration par script externe.

L&#39;avantage du scripting est que l&#39;utilisateur n&#39;a rien d&#39;autre à faire que de cliquer sur un bouton, et si un système suffisamment compliqué est créé, il est possible de gérer et d&#39;échanger le projet facilement sans avoir besoin de gérer les fichiers et les paramètres manuellement.

La ligne correspondante ressemble à ceci :

```
  <configuration> 

   <configurationfile>file:///C:/Users/John/AppData/Local/Adobe/Adobe Substance 3D Designer/default_configuration.sbscfg</configurationfile> 

  </configuration>
```


#### Exemple Python

Voici un exemple simple de fonction Python 2.7 pour Windows qui modifie le fichier user\_preferences.xml pour un autre fichier de configuration. La valeur est alors modifiée de façon permanente jusqu’à ce qu’elle soit rétablie. La fonction SetConfigurationFile peut ensuite être appelée avec le chemin de votre fichier sbscfg personnalisé comme paramètre.

Un script Python permet un code puissant et propre, et peut être facilement intégré ailleurs, mais l&#39;inconvénient est que pour qu&#39;un utilisateur puisse l&#39;exécuter, il doit être compilé en un exécutable, ou l&#39;utilisateur a besoin d&#39;un déploiement Python.

```
import xml.etree.ElementTree as ElementTree 

import os 

 

##Example Python script for changing Substance 3D Designer user preference file## 

 

def SetConfigurationFile(p_ConfigPath): 

## Check is the path passed as parameter exists.

    if(os.path.isfile(p_ConfigPath)): 

## replace backslashes by forwardslahes to ensure consistency

        p_ConfigPath = p_ConfigPath.replace("\", "/") 

## get Local Appadata path from Environment variables, construct full path to user_preferences.xml and check if it exists.

        m_AppDataPath = os.environ.get('LOCALAPPDATA') 

        if m_AppDataPath != None: 

            m_UserPrefsPath = os.path.join(m_AppDataPath, str("Adobe/Adobe Substance 3D Designer/user_preferences.xml")) 

            if(os.path.isfile(m_UserPrefsPath)): 

## read XML elementtree from file, find correct element until we get to the actual line that defines the configurationfile path

                m_PrefsTree = ElementTree.parse(m_UserPrefsPath) 

                m_PrefsRoot = m_PrefsTree.getroot() 

                m_PrefsElement = m_PrefsRoot.find("preferences") 

                m_XMLError = True 

                if(m_PrefsElement != None): 

                    m_ConfigElement = m_PrefsElement.find("configuration") 

                    if(m_ConfigElement != None): 

                        m_ConfigFileElement = m_ConfigElement.find("configurationfile") 

                        if(m_ConfigFileElement != None): 

                            m_XMLError = False 

## Check if path is already set, to avoid double work

                            if m_ConfigFileElement.text.replace("file:///","") == p_ConfigPath: 

                                print "configurationfile is already set to desired path. Aborting." 

                                return True 

                            else: 

## construct correctly formatted path, insert into elementtree

                                m_ConfigPath = str("file:///" + p_ConfigPath) 

                                m_ConfigFileElement.text = m_ConfigPath 

 

## Write to file

                                m_XMLString = str("<?xml version="1.0" encoding="UTF-8"?>n") + ElementTree.tostring(m_PrefsRoot, 'utf-8') 

                                m_File = open(m_UserPrefsPath,'w') 

                                m_File.write(m_XMLString) 

                                m_File.close() 

                                print "configuration file path succesfully changed!" 

                                return True 

                if m_XMLError: 

## if this flag was not set to false, we can assume something was missing or went wrong when walking through the XML

                    print("Error: malformed content in user_preferences.xml!") 

                    return False 

            else: 

                print "Error: user_preferences.xml does not exist, try starting Substance 3D Designer first!" 

                return False 

        else: 

            print "Error: LocalAppData path returned None" 

            return False 

    else: 

        print "Error: Invalid Configuration File path!" 

        return False
```


## Raccourci d’argument de ligne de commande

De manière beaucoup plus simple, il est possible d’indiquer à Designer d’utiliser un SBSCFG spécifique au démarrage à l’aide de l’argument « —config-file » (facultatif).

### Configuration manuelle

Bien qu&#39;il ne soit pas recommandé d&#39;utiliser une méthode manuelle dans un environnement de production, cela peut être fait assez rapidement à des fins de test si vous avez déjà configuré votre fichier SBSCFG.

1. Ajouter un espace
1. Ajoutez —config-file après le chemin d’accès au concepteur dans la section Target.
1. Ajouter un autre espace
1. Ajoutez votre chemin, *entouré de guillemets* pour éviter les problèmes d’espaces dans votre chemin
1. Le résultat devrait être le suivant :

   *« C:\Program Files\Adobe\Adobe Substance 3D Designer\Adobe Substance 3D Designer.exe » —config-file « C:\Dev\Substance\custom\_configuration.sbscfg«*

![Entrée du fichier de configuration dans les propriétés du fichier exécutable](user-preferences-automating-setup.resources/user-preferences-automating-setup-03.jpg "Entrée du fichier de configuration dans les propriétés du fichier exécutable")
