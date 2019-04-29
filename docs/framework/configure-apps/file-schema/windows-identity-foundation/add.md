---
title: <add>
ms.date: 03/30/2017
ms.assetid: 4712a888-f154-4395-8887-ef14a88a6497
author: BrucePerlerMS
ms.openlocfilehash: 34643d10ef1ed2e87152e5013634e62859e0594e
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61791766"
---
# <a name="add"></a>\<add>
Ajoute le Gestionnaire de jetons de sécurité spécifié à la collection de gestionnaires de jetons.  
  
 \<system.identityModel>  
\<identityConfiguration>  
\<securityTokenHandlers>  
\<add>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <securityTokenHandlers>  
      <add type=xs:string>  
        <optionalConfigurationElement>  
        </optionalConfigurationElement>  
      </add>  
    </securityTokenHandlers>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|type|Le nom de type CLR de gestionnaire de jetons à ajouter. Pour plus d’informations sur la façon de spécifier le `type` d’attribut, consultez [références de Type personnalisé](https://docs.microsoft.com/previous-versions/windows-identity-foundation/gg638728(v=msdn.10)#custom-type-references).|  
  
### <a name="child-elements"></a>Éléments enfants  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<samlSecurityTokenRequirement>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/samlsecuritytokenrequirement.md)|Fournit une configuration pour le <xref:System.IdentityModel.Tokens.SamlSecurityTokenHandler> (classe), la <xref:System.IdentityModel.Tokens.Saml2SecurityTokenHandler> classe ou une classe dérivée d’un de ces classes.|  
|[\<sessionTokenRequirement>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/sessiontokenrequirement.md)|Fournit une configuration pour la <xref:System.IdentityModel.Tokens.SessionSecurityTokenHandler> classe ou les classes dérivées.|  
|[\<userNameSecurityTokenHandlerRequirement>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/usernamesecuritytokenhandlerrequirement.md)|Fournit une configuration pour la <xref:System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler> classe ou les classes dérivées.|  
|[\<x509SecurityTokenHandlerRequirement>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/x509securitytokenhandlerrequirement.md)|Fournit une configuration facultative pour le <xref:System.IdentityModel.Tokens.X509SecurityTokenHandler> classe ou les classes dérivées.|  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<securityTokenHandlers>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/securitytokenhandlers.md)|Spécifie une collection de gestionnaires de jetons de sécurité qui sont inscrits avec le point de terminaison.|  
  
## <a name="remarks"></a>Notes  
 Le `<add>` élément peut prendre un seul élément enfant qui spécifie la configuration pour le Gestionnaire de jetons. Cela dépend de la classe de gestionnaire référencée ou non par le biais du `type` attribut de la `<add>` élément prend en charge cette fonctionnalité. Les classes de gestionnaire de jetons qui fournissent cette fonctionnalité doivent exposer un constructeur qui accepte un <xref:System.Xml.XmlElement> objet.  
  
```  
public class CustomTokenHandler : Microsoft.IdentityModel.Tokens.SecurityTokenHandler  
{  
    public CustomTokenHandler( XmlElement customConfig )  
    {  
    }  
}  
```  
  
 Plusieurs des classes de gestionnaire de jetons de sécurité intégrés ne fournissent pas cette fonctionnalité. Ces classes sont <xref:System.IdentityModel.Tokens.SamlSecurityTokenHandler>, <xref:System.IdentityModel.Tokens.Saml2SecurityTokenHandler>, <xref:System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler>, <xref:System.IdentityModel.Tokens.X509SecurityTokenHandler>, et <xref:System.IdentityModel.Tokens.SessionSecurityTokenHandler>.  
  
> [!IMPORTANT]
>  La collection de gestionnaires de jetons ne peut contenir qu’un seul gestionnaire de tout type donné. Cela signifie, par exemple, que si vous souhaitez ajouter un gestionnaire qui est dérivé de la <xref:System.IdentityModel.Tokens.Saml2SecurityTokenHandler> classe à la collection, vous devez d’abord supprimer la <xref:System.IdentityModel.Tokens.Saml2SecurityTokenHandler>, qui n’est présent par défaut, à partir de la collection. Vous pouvez utiliser la [ \<Supprimer >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/remove.md) élément à supprimer un gestionnaire unique à partir de la collection ou utilisez le [ \<Effacer >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/clear.md) élément à supprimer tous les gestionnaires de la collection.  
  
 Les paramètres spécifiés sur un gestionnaire de remplacent les paramètres équivalents spécifiés sur la collection de gestionnaires de jetons sous le [ \<securityTokenHandlerConfiguration >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/securitytokenhandlerconfiguration.md) élément et ceux spécifiés au niveau du service sous le [ \<identityConfiguration >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md) élément.  
  
## <a name="example"></a>Exemple  
 Le code XML suivant illustre l’utilisation de la `<add>` et `<remove>` éléments pour remplacer le Gestionnaire de jetons de session par défaut par un gestionnaire de jetons de session personnalisée. Le code XML provient de la `ClaimsAwareWebFarm` exemple.  
  
```xml  
<securityTokenHandlers>  
  <remove type="System.IdentityModel.Tokens.SessionSecurityTokenHandler, System.IdentityModel, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089" />  
  <add type="System.IdentityModel.Services.Tokens.MachineKeySessionSecurityTokenHandler, System.IdentityModel.Services, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089" />  
</securityTokenHandlers>  
```
