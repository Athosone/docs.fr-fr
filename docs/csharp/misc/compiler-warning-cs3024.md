---
title: Avertissement du compilateur CS3024
ms.date: 07/20/2015
f1_keywords:
- CS3024
helpviewer_keywords:
- CS3024
ms.assetid: fef9db31-9a7f-42d5-ad37-3e7faf661f95
ms.openlocfilehash: 7515fdd7bc8f57890e3f1aac6303ed4607cc2249
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61688252"
---
# <a name="compiler-warning-cs3024"></a>Avertissement du compilateur CS3024
Le type de contrainte 'type' n’est pas conforme CLS  
  
 Le compilateur émet cet avertissement, car l’utilisation d’un type non conforme CLS comme contrainte de type générique peut empêcher le code écrit dans certains langages de consommer votre classe générique.  
  
### <a name="to-eliminate-this-warning"></a>Pour supprimer cet avertissement  
  
1. Utilisez un type conforme CLS pour la contrainte de type.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant génère l’avertissement CS3024 à plusieurs emplacements :  
  
```csharp  
// cs3024.cs  
// Compile with: /target:library  
 [assembly: System.CLSCompliant(true)]  
  
[type: System.CLSCompliant(false)]  
public class TestClass // CS3024  
{  
    public ushort us;  
}  
[type: System.CLSCompliant(false)]  
public interface ITest // CS3024  
{}  
public interface I<T> where T : TestClass  
{}  
public class TestClass_2<T> where T : ITest  
{}  
public class TestClass_3<T> : I<T> where T : TestClass  
{}  
public class TestClass_4<T> : TestClass_2<T> where T : ITest  
{}  
public class Test  
{  
    public static int Main()  
    {  
        return 0;  
    }  
}  
```  
  
## <a name="see-also"></a>Voir aussi

- [Contraintes sur les paramètres de type](../../csharp/programming-guide/generics/constraints-on-type-parameters.md)
