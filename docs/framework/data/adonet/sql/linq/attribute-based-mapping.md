---
title: Mappage basé sur les attributs
ms.date: 03/30/2017
ms.assetid: 6dd89999-f415-4d61-b8c8-237d23d7924e
ms.openlocfilehash: d7d7c14ca12e40af643d164069cf7b0f3165fa20
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62032966"
---
# <a name="attribute-based-mapping"></a>Mappage basé sur les attributs
[!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] mappe une base de données SQL Server à un [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] modèle objet en appliquant des attributs ou en utilisant un fichier de mappage externe. Cette rubrique présente l'approche basée sur les attributs.  
  
 Dans sa forme de base, [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] mappe une base de données à un <xref:System.Data.Linq.DataContext>, une table à une classe, ainsi que des colonnes et des relations aux propriétés sur ces classes. Vous pouvez également utiliser des attributs pour mapper une hiérarchie d'héritage dans votre modèle objet. Pour plus d'informations, voir [Procédure : Générer le modèle objet en Visual Basic ou C# ](../../../../../../docs/framework/data/adonet/sql/linq/how-to-generate-the-object-model-in-visual-basic-or-csharp.md).  
  
 Les développeurs qui utilisent Visual Studio en général effectuent le mappage basé sur l’attribut à l’aide du [!INCLUDE[vs_ordesigner_long](../../../../../../includes/vs-ordesigner-long-md.md)]. Vous pouvez aussi utiliser l'outil en ligne de commande SQLMetal ou coder manuellement ces attributs. Pour plus d'informations, voir [Procédure : Générer le modèle objet en Visual Basic ou C# ](../../../../../../docs/framework/data/adonet/sql/linq/how-to-generate-the-object-model-in-visual-basic-or-csharp.md).  
  
> [!NOTE]
>  Vous pouvez également mapper à l'aide d'un fichier XML externe. Pour plus d’informations, consultez [mappage externe](../../../../../../docs/framework/data/adonet/sql/linq/external-mapping.md).  
  
 Les sections suivantes décrivent plus en détail le mappage basé sur les attributs. Pour plus d'informations, consultez l'espace de noms <xref:System.Data.Linq.Mapping>.  
  
## <a name="databaseattribute-attribute"></a>Attribut DatabaseAttribute  
 Utilisez cet attribut pour spécifier le nom par défaut de la base de données si la connexion n'a fourni aucun nom. Cet attribut est facultatif, mais si vous l'utilisez, vous devez appliquer la propriété <xref:System.Data.Linq.Mapping.DatabaseAttribute.Name%2A>, comme décrit dans le tableau suivant.  
  
|Propriété|Type|Par défaut|Description|  
|--------------|----------|-------------|-----------------|  
|<xref:System.Data.Linq.Mapping.DatabaseAttribute.Name%2A>|Chaîne|Voir <xref:System.Data.Linq.Mapping.DatabaseAttribute.Name%2A>|Utilisé avec sa propriété <xref:System.Data.Linq.Mapping.DatabaseAttribute.Name%2A>, spécifie le nom de la base de données.|  
  
 Pour plus d'informations, consultez <xref:System.Data.Linq.Mapping.DatabaseAttribute>.  
  
## <a name="tableattribute-attribute"></a>Attribut TableAttribute  
 Utilisez cet attribut pour désigner une classe comme classe d'entité associée à une table ou une vue de base de données. [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] traite les classes qui possèdent cet attribut comme des classes persistantes. Le tableau suivant décrit la propriété <xref:System.Data.Linq.Mapping.TableAttribute.Name%2A>.  
  
|Propriété|Type|Par défaut|Description|  
|--------------|----------|-------------|-----------------|  
|<xref:System.Data.Linq.Mapping.TableAttribute.Name%2A>|Chaîne|Même chaîne que le nom de la classe|Désigne une classe comme une classe d'entité associée à une table de base de données.|  
  
 Pour plus d'informations, consultez <xref:System.Data.Linq.Mapping.TableAttribute>.  
  
## <a name="columnattribute-attribute"></a>Attribut ColumnAttribute  
 Utilisez cet attribut pour désigner un membre d'une classe d'entité comme représentant d'une colonne d'une table de base de données. Vous pouvez appliquer cet attribut à n'importe quel champ ou propriété.  
  
 Seuls les membres que vous identifiez comme des colonnes sont récupérés et rendus persistants lorsque [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] enregistre les modifications dans la base de données. Il est supposé que les membres sans cet attribut sont non persistants et ne sont pas soumis aux insertions ou mises à jour.  
  
 Le tableau suivant décrit les propriétés de cet attribut.  
  
|Propriété|Type|Par défaut|Description|  
|--------------|----------|-------------|-----------------|  
|<xref:System.Data.Linq.Mapping.ColumnAttribute.AutoSync%2A>|AutoSync|Never|Indique au Common Language Runtime (CLR) de récupérer la valeur après une opération d'insertion ou de mise à jour.<br /><br /> Options : Always, Never, OnUpdate, OnInsert.|  
|<xref:System.Data.Linq.Mapping.ColumnAttribute.CanBeNull%2A>|Booléen|`true`|Indique qu'une colonne peut contenir des valeurs null.|  
|<xref:System.Data.Linq.Mapping.ColumnAttribute.DbType%2A>|Chaîne|Type déduit de colonne de base de données|Utilise des types et des modificateurs de base de données pour spécifier le type de la colonne de base de données.|  
|<xref:System.Data.Linq.Mapping.ColumnAttribute.Expression%2A>|Chaîne|Empty|Définit une colonne calculée dans une base de données.|  
|<xref:System.Data.Linq.Mapping.ColumnAttribute.IsDbGenerated%2A>|Booléen|`false`|Indique qu'une colonne contient des valeurs générées automatiquement par la base de données.|  
|<xref:System.Data.Linq.Mapping.ColumnAttribute.IsDiscriminator%2A>|Booléen|`false`|Indique que la colonne contient une valeur de discriminateur pour une hiérarchie d'héritage [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)].|  
|<xref:System.Data.Linq.Mapping.ColumnAttribute.IsPrimaryKey%2A>|Booléen|`false`|Spécifie que ce membre de classe représente une colonne qui est une clé primaire ou fait partie des clés primaire de la table.|  
|<xref:System.Data.Linq.Mapping.ColumnAttribute.IsVersion%2A>|Booléen|`false`|Identifie le type de colonne du membre comme horodatage ou numéro de version de base de données.|  
|<xref:System.Data.Linq.Mapping.ColumnAttribute.UpdateCheck%2A>|UpdateCheck|`Always`, à moins que <xref:System.Data.Linq.Mapping.ColumnAttribute.IsVersion%2A> ait la valeur `true` pour un membre|Spécifie l'approche de [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] concernant la détection de conflits d'accès concurrentiel optimiste.|  
  
 Pour plus d'informations, consultez <xref:System.Data.Linq.Mapping.ColumnAttribute>.  
  
> [!NOTE]
>  Les valeurs des propriétés AssociationAttribute et ColumnAttribute Storage respectent la casse. Assurez-vous, par exemple que les valeurs utilisées dans l'attribut de la propriété AssociationAttribute.Storage correspondent à la casse des noms de propriétés correspondants utilisés ailleurs dans le code. Cela s’applique à tous les langages de programmation .NET, y compris ceux qui ne sont pas généralement respecte la casse, y compris Visual Basic. Pour plus d'informations sur la propriété Storage, consultez <xref:System.Data.Linq.Mapping.DataAttribute.Storage%2A?displayProperty=nameWithType>.  
  
## <a name="associationattribute-attribute"></a>Attribut AssociationAttribute  
 Utilisez cet attribut pour désigner une propriété comment représentant une association dans la base de données, telle qu'une relation entre une clé étrangère et une clé primaire. Pour plus d’informations sur les relations, consultez [Comment : mapper des relations de base de données](../../../../../../docs/framework/data/adonet/sql/linq/how-to-map-database-relationships.md).  
  
 Le tableau suivant décrit les propriétés de cet attribut.  
  
|Propriété|Type|Par défaut|Description|  
|--------------|----------|-------------|-----------------|  
|<xref:System.Data.Linq.Mapping.AssociationAttribute.DeleteOnNull%2A>|Booléen|`false`|Placé sur une association dont tous les membres de clé étrangère sont non Nullable, supprime l'objet lorsque l'association a la valeur Null.|  
|<xref:System.Data.Linq.Mapping.AssociationAttribute.DeleteRule%2A>|Chaîne|Aucun.|Ajoute le comportement de suppression à une association.|  
|<xref:System.Data.Linq.Mapping.AssociationAttribute.IsForeignKey%2A>|Booléen|`false`|Si la valeur est true, désigne le membre comme clé étrangère dans une association qui représente une relation de base de données.|  
|<xref:System.Data.Linq.Mapping.AssociationAttribute.IsUnique%2A>|Booléen|`false`|Si la valeur est true, indique une contrainte d'unicité sur la clé étrangère.|  
|<xref:System.Data.Linq.Mapping.AssociationAttribute.OtherKey%2A>|Chaîne|ID de la classe connexe|Désigne un ou plusieurs membres de la classe d'entité cible comme valeurs de clés de l'autre côté de l'association.|  
|<xref:System.Data.Linq.Mapping.AssociationAttribute.ThisKey%2A>|Chaîne|ID de la classe conteneur|Désigne des membres de cette classe d'entité comme représentant les valeurs de clés sur ce côté de l'association.|  
  
 Pour plus d'informations, consultez <xref:System.Data.Linq.Mapping.AssociationAttribute>.  
  
> [!NOTE]
>  Les valeurs des propriétés AssociationAttribute et ColumnAttribute Storage respectent la casse. Assurez-vous, par exemple que les valeurs utilisées dans l'attribut de la propriété AssociationAttribute.Storage correspondent à la casse des noms de propriétés correspondants utilisés ailleurs dans le code. Cela s’applique à tous les langages de programmation .NET, y compris ceux qui ne sont pas généralement respecte la casse, y compris Visual Basic. Pour plus d'informations sur la propriété Storage, consultez <xref:System.Data.Linq.Mapping.DataAttribute.Storage%2A?displayProperty=nameWithType>.  
  
## <a name="inheritancemappingattribute-attribute"></a>Attribut InheritanceMappingAttribute  
 Utilisez cet attribut pour mapper une hiérarchie d'héritage.  
  
 Le tableau suivant décrit les propriétés de cet attribut.  
  
|Propriété|Type|Par défaut|Description|  
|--------------|----------|-------------|-----------------|  
|<xref:System.Data.Linq.Mapping.InheritanceMappingAttribute.Code%2A>|Chaîne|Aucun. La valeur doit être fournie.|Spécifie la valeur de code du discriminateur.|  
|<xref:System.Data.Linq.Mapping.InheritanceMappingAttribute.IsDefault%2A>|Booléen|`false`|Si la valeur est true, instancie un objet de ce type lorsqu'aucune valeur de discriminateur du magasin ne correspond à l'une des valeurs spécifiées.|  
|<xref:System.Data.Linq.Mapping.InheritanceMappingAttribute.Type%2A>|Type|Aucun. La valeur doit être fournie.|Spécifie le type de la classe dans la hiérarchie.|  
  
 Pour plus d'informations, consultez <xref:System.Data.Linq.Mapping.InheritanceMappingAttribute>.  
  
## <a name="functionattribute-attribute"></a>Attribut FunctionAttribute  
 Utilisez cet attribut pour désigner une méthode comme représentant une procédure stockée ou une fonction définie par l'utilisateur dans la base de données.  
  
 Le tableau suivant décrit les propriétés de cet attribut.  
  
|Propriété|Type|Par défaut|Description|  
|--------------|----------|-------------|-----------------|  
|<xref:System.Data.Linq.Mapping.FunctionAttribute.IsComposable%2A>|Booléen|`false`|Si la valeur est false, indique le mappage à une procédure stockée. Si la valeur est true, indique le mappage à une fonction définie par l'utilisateur.|  
|<xref:System.Data.Linq.Mapping.FunctionAttribute.Name%2A>|Chaîne|Même chaîne que le nom dans la base de données|Spécifie le nom de la procédure stockée ou de la fonction définie par l'utilisateur.|  
  
 Pour plus d'informations, consultez <xref:System.Data.Linq.Mapping.FunctionAttribute>.  
  
## <a name="parameterattribute-attribute"></a>Attribut ParameterAttribute  
 Utilisez cet attribut pour mapper des paramètres d'entrée sur les méthodes de procédure stockée.  
  
 Le tableau suivant décrit les propriétés de cet attribut.  
  
|Propriété|Type|Par défaut|Description|  
|--------------|----------|-------------|-----------------|  
|<xref:System.Data.Linq.Mapping.ParameterAttribute.DbType%2A>|Chaîne|Aucun.|Spécifie le type de base de données.|  
|<xref:System.Data.Linq.Mapping.ParameterAttribute.Name%2A>|Chaîne|Même chaîne qu'un nom de paramètre dans la base de données|Spécifie un nom pour le paramètre.|  
  
 Pour plus d'informations, consultez <xref:System.Data.Linq.Mapping.ParameterAttribute>.  
  
## <a name="resulttypeattribute-attribute"></a>Attribut ResultTypeAttribute  
 Utilisez cet attribut pour spécifier un type de résultat.  
  
 Le tableau suivant décrit les propriétés de cet attribut.  
  
|Propriété|Type|Par défaut|Description|  
|--------------|----------|-------------|-----------------|  
|<xref:System.Data.Linq.Mapping.ResultTypeAttribute.Type%2A>|Type|(Aucun)|Utilisé sur les méthodes mappées aux procédures stockées qui retournent <xref:System.Data.Linq.IMultipleResults>. Déclare les mappages de type valide ou attendu pour la procédure stockée.|  
  
 Pour plus d'informations, consultez <xref:System.Data.Linq.Mapping.ResultTypeAttribute>.  
  
## <a name="dataattribute-attribute"></a>Attribut DataAttribute  
 Utilisez cet attribut pour spécifier des noms et des champs de stockage privés.  
  
 Le tableau suivant décrit les propriétés de cet attribut.  
  
|Propriété|Type|Par défaut|Description|  
|--------------|----------|-------------|-----------------|  
|<xref:System.Data.Linq.Mapping.DataAttribute.Name%2A>|Chaîne|Identique au nom dans la base de données|Spécifie le nom de la table, de la colonne, etc.|  
|<xref:System.Data.Linq.Mapping.DataAttribute.Storage%2A>|Chaîne|Accesseurs publics|Spécifie le nom du champ de stockage sous-jacent.|  
  
 Pour plus d'informations, consultez <xref:System.Data.Linq.Mapping.DataAttribute>.  
  
## <a name="see-also"></a>Voir aussi

- [Référence](../../../../../../docs/framework/data/adonet/sql/linq/reference.md)
