---
title: <remove>, élément de schemeSettings (paramètres d’URI)
ms.date: 03/30/2017
ms.assetid: 4095ba51-de20-4f87-b562-018abe422c91
ms.openlocfilehash: f29ee86deaa150324b40f4fac12ead152553e50d
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61674439"
---
# <a name="remove-element-for-schemesettings-uri-settings"></a>\<Supprimer >, élément de schemeSettings (paramètres d’Uri)
Supprime un paramètre de schéma pour un nom de schéma.  
  
 \<configuration>  
\<uri>  
\<schemeSettings>  
\<remove>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<remove
  name="http|https"
/>
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|name|Le nom du schéma pour lequel ce paramètre s’applique. Les seules valeurs prises en charge sont nom = « http » et le nom = « https ».|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<schemeSettings, élément (paramètres d’Uri)](../../../../../docs/framework/configure-apps/file-schema/network/schemesettings-element-uri-settings.md)|Spécifie la façon dont un <xref:System.Uri> est analysé pour les schémas spécifiques.|  
  
## <a name="remarks"></a>Notes  
 Par défaut, le <xref:System.Uri?displayProperty=nameWithType> % n’échappe pas de classe encodé délimiteurs de chemin d’accès avant d’exécuter la compression de chemin d’accès. Ceci était implémenté comme un mécanisme de sécurité contre les attaques comme suit :  
  
 `http://www.contoso.com/..%2F..%2F/Windows/System32/cmd.exe?/c+dir+c:\`  
  
 Si cet URI est passé à des modules ne gère ne pas % caractères encodés correctement, cela peut entraîner la commande suivante en cours d’exécution par le serveur :  
  
 `c:\Windows\System32\cmd.exe /c dir c:\`  
  
 Pour cette raison, <xref:System.Uri?displayProperty=nameWithType> première délimiteurs de chemin d’accès n’échappe pas de classe, puis applique la compression de chemin d’accès. Le résultat du passage de l’URL malveillante ci-dessus à <xref:System.Uri?displayProperty=nameWithType> classe les résultats de constructeur dans l’URI suivant :  
  
 `http://www.microsoft.com/Windows/System32/cmd.exe?/c+dir+c:\`  
  
 Ce comportement par défaut peut être modifié pour ne pas les délimiteurs de chemin d’accès codé en pourcentage échapper à l’aide de l’option de configuration schemeSettings pour un modèle spécifique.  
  
## <a name="configuration-files"></a>Fichiers de configuration  
 Cet élément peut être défini dans le fichier de configuration de l'application ou dans le fichier de configuration de l'ordinateur (Machine.config).  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre une configuration utilisée par la <xref:System.Uri> classe qui supprime les paramètres de schéma pour le schéma http.  
  
```xml  
<configuration>  
  <uri>  
    <schemeSettings>  
      <remove name="http"/>  
    </schemeSettings>  
  </uri>  
</configuration>  
```  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Configuration.SchemeSettingElement?displayProperty=nameWithType>
- <xref:System.Configuration.SchemeSettingElementCollection?displayProperty=nameWithType>
- <xref:System.Configuration.UriSection?displayProperty=nameWithType>
- <xref:System.Configuration.UriSection.SchemeSettings%2A?displayProperty=nameWithType>
- <xref:System.GenericUriParserOptions?displayProperty=nameWithType>
- <xref:System.Uri?displayProperty=nameWithType>
- [Schéma des paramètres réseau](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
