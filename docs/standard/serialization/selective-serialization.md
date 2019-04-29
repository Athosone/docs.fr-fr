---
title: Sérialisation sélective
ms.date: 08/07/2017
dev_langs:
- CSharp
helpviewer_keywords:
- serialization, selective serialization
- binary serialization, selective serialization
ms.assetid: 39c56635-95d2-4afd-aff1-b022e7649bb3
ms.openlocfilehash: af608031a661037b89c9783ac2451a6b536f9cd4
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61712484"
---
# <a name="selective-serialization"></a>Sérialisation sélective
Une classe contient souvent des champs qui ne doivent pas être sérialisés. Par exemple, supposez qu'une classe stocke un ID de thread dans une variable membre. Quand la classe est désérialisée, il se peut que le thread stocké pour l’ID au moment de la sérialisation de la classe ne s’exécute plus. La sérialisation de cette valeur est donc inutile. Vous pouvez empêcher des variables membres d’être sérialisées en les marquant avec l’attribut [NonSerialized](xref:System.NonSerializedAttribute) comme suit.  
  
```csharp  
[Serializable]  
public class MyObject   
{  
  public int n1;  
  [NonSerialized] public int n2;  
  public String str;  
}  
```

Si possible, faites en sorte qu'un objet pouvant contenir des données de sécurité sensibles soit non sérialisable. Si l’objet doit être sérialisé, appliquez l’attribut `NonSerialized` aux champs spécifiques qui stockent des données sensibles. Si vous n’excluez pas ces champs de la sérialisation, notez que les données qu’ils stockent sont exposées à tout code autorisé à sérialiser. Pour plus d’informations sur l’écriture de code de sérialisation sécurisé, consultez [Sécurité et sérialisation](../../../docs/framework/misc/security-and-serialization.md).

[!INCLUDE [binary-serialization-warning](../../../includes/binary-serialization-warning.md)]
  
## <a name="see-also"></a>Voir aussi

- [Sérialisation binaire](binary-serialization.md)
- [Sérialisation XML et SOAP](xml-and-soap-serialization.md)
- [Sécurité et sérialisation](../../../docs/framework/misc/security-and-serialization.md)
