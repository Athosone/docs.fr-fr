---
title: Schéma des paramètres d’application
ms.date: 03/30/2017
helpviewer_keywords:
- schema application settings
- application settings, schema [Windows Forms]
- Windows Forms, application settings schema
- configuration schema [.NET Framework], application settings
ms.assetid: 5797fcff-6081-4e8c-bebf-63d9c70cf14b
ms.openlocfilehash: a74716bcdf3c85c08d0ff3bf66407dce30ee91cc
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61705439"
---
# <a name="application-settings-schema"></a>Schéma des paramètres d’application

Paramètres d’application permettent à une application Windows Forms ou ASP.NET stocker et récupérer des paramètres de portée application et de portée utilisateur. Dans ce contexte, un *paramètre* est n’importe quel élément d’information qui peut-être être spécifiques à l’application ou spécifiques à l’utilisateur actuel, quoi que ce soit à partir d’une chaîne de connexion de base de données à l’utilisateur préféré par taille de fenêtre par défaut.

Par défaut, les paramètres d’application dans une application Windows Forms utilise le <xref:System.Configuration.LocalFileSettingsProvider> (classe), qui utilise le système de configuration .NET pour stocker les paramètres dans un fichier de configuration XML. Pour plus d’informations sur les fichiers utilisés par les paramètres de l’application, consultez [Application Settings Architecture](~/docs/framework/winforms/advanced/application-settings-architecture.md).

Paramètres de l’application définit les éléments suivants dans le cadre des fichiers de configuration qu’il utilise.

| Élément                    | Description                                                                           |
| -------------------------- | ------------------------------------------------------------------------------------- |
| **\<applicationSettings>** | Contient tous les  **\<paramètre >** balises spécifiques à l’application.                         |
| **\<userSettings>**        | Contient tous les  **\<paramètre >** balises spécifiques à l’utilisateur actuel.                        |
| **\<setting>**             | Définit un paramètre. Enfant de le  **\<applicationSettings >** ou  **\<userSettings >**. |
| **\<value>**               | Définit une valeur de paramètre. Enfant de  **\<paramètre >**.                                   |

## <a name="applicationsettings-element"></a>\<applicationSettings > élément

Cet élément contient tous les  **\<paramètre >** balises qui sont spécifiques à une instance de l’application sur un ordinateur client. Il ne définit aucun attribut.

## <a name="usersettings-element"></a>\<userSettings > élément

Cet élément contient tous les  **\<paramètre >** balises qui sont spécifiques à l’utilisateur qui utilise actuellement l’application. Il ne définit aucun attribut.

## <a name="setting-element"></a>\<définition > élément

Cet élément définit un paramètre. Il a les attributs suivants.

| Attribut        | Description |
| ---------------- | ----------- |
| **name**         | Obligatoire. ID unique du paramètre. Les paramètres créés via Visual Studio sont enregistrés avec le nom `ProjectName.Properties.Settings`. |
| **serializedAs** | Obligatoire. Le format à utiliser pour sérialiser la valeur en texte. Les valeurs valides sont les suivantes :<br><br>- `string`. La valeur est sérialisée comme une chaîne en utilisant un <xref:System.ComponentModel.TypeConverter>.<br>- `xml`. La valeur est sérialisée à l’aide de la sérialisation XML.<br>- `binary`. La valeur est sérialisée sous forme binaire texte encodé à l’aide de la sérialisation binaire.<br />- `custom`. Le fournisseur de paramètres a une connaissance inhérente de ce paramètre et sérialise et désérialise il. |

## <a name="value-element"></a>\<valeur > élément

Cet élément contient la valeur d’un paramètre.

## <a name="example"></a>Exemple

L’exemple suivant montre un fichier de paramètres d’application qui définit deux paramètres de portée application et deux paramètres de portée utilisateur :

```xml
<?xml version="1.0" encoding="utf-8" ?>
<configuration>
  <configSections>
    <sectionGroup name="applicationSettings" type="System.Configuration.ApplicationSettingsGroup, System, Version=2.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089">
      <section name="WindowsApplication1.Properties.Settings" type="System.Configuration.ClientSettingsSection, System, Version=2.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089" />
    </sectionGroup>
    <sectionGroup name="userSettings" type="System.Configuration.UserSettingsGroup, System, Version=2.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089">
      <section name="WindowsApplication1.Properties.Settings" type="System.Configuration.ClientSettingsSection, System, Version=2.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089" allowExeDefinition="MachineToLocalUser" />
    </sectionGroup>
  </configSections>
  <applicationSettings>
    <WindowsApplication1.Properties.Settings>
      <setting name="Cursor" serializeAs="String">
        <value>Default</value>
      </setting>
      <setting name="DoubleBuffering" serializeAs="String">
        <value>False</value>
      </setting>
    </WindowsApplication1.Properties.Settings>
  </applicationSettings>
  <userSettings>
    <WindowsApplication1.Properties.Settings>
      <setting name="FormTitle" serializeAs="String">
        <value>Form1</value>
      </setting>
      <setting name="FormSize" serializeAs="String">
        <value>595, 536</value>
      </setting>
    </WindowsApplication1.Properties.Settings>
  </userSettings>
</configuration>
```

## <a name="see-also"></a>Voir aussi

- [Vue d'ensemble des paramètres d'application](~/docs/framework/winforms/advanced/application-settings-overview.md)
- [Architecture des paramètres d'application](~/docs/framework/winforms/advanced/application-settings-architecture.md)
