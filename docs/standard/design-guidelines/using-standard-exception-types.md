---
title: Utilisation de types d'exceptions standard
ms.date: 10/22/2008
ms.technology: dotnet-standard
helpviewer_keywords:
- throwing exceptions, standard types
- catching exceptions
- exceptions, catching
- exceptions, throwing
ms.assetid: ab22ce03-78f9-4dca-8824-c7ed3bdccc27
author: KrzysztofCwalina
ms.openlocfilehash: b947c7cce057c060b1ab5054d1227f5703ccbf89
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62026334"
---
# <a name="using-standard-exception-types"></a>Utilisation de types d'exceptions standard
Cette section décrit les exceptions standard fournies par le Framework et les détails de leur utilisation. La liste n’est en aucun cas exhaustive. Reportez-vous à la documentation de référence du .NET Framework pour l’utilisation d’autres types d’exception de Framework.  
  
## <a name="exception-and-systemexception"></a>Exception et SystemException  
 **X DO NOT** lever <xref:System.Exception?displayProperty=nameWithType> ou <xref:System.SystemException?displayProperty=nameWithType>.  
  
 **X DO NOT** catch `System.Exception` ou `System.SystemException` dans le code d’infrastructure, sauf si vous souhaitez lever de nouveau.  
  
 **X AVOID** interception `System.Exception` ou `System.SystemException`, sauf dans les gestionnaires d’exceptions de niveau supérieur.  
  
## <a name="applicationexception"></a>ApplicationException  
 **X DO NOT** lever ou dériver de <xref:System.ApplicationException>.  
  
## <a name="invalidoperationexception"></a>InvalidOperationException  
 **✓ DO** lever un <xref:System.InvalidOperationException> si l’objet est dans un état inapproprié.  
  
## <a name="argumentexception-argumentnullexception-and-argumentoutofrangeexception"></a>ArgumentException, ArgumentNullException et ArgumentOutOfRangeException  
 **✓ DO** lever <xref:System.ArgumentException> ou l’un de ses sous-types si des arguments incorrects sont passés à un membre. Préférer le type plus dérivé d’exception, le cas échéant.  
  
 **✓ DO** définir le `ParamName` propriété lors de la levée d’une des sous-classes de `ArgumentException`.  
  
 Cette propriété représente le nom du paramètre ayant provoqué l’exception levée. Notez que la propriété peut être définie à l’aide d’une des surcharges de constructeur.  
  
 **✓ DO** utiliser `value` pour le nom du paramètre de valeur implicite d’accesseurs Set de propriété.  
  
## <a name="nullreferenceexception-indexoutofrangeexception-and-accessviolationexception"></a>NullReferenceException, IndexOutOfRangeException, and AccessViolationException  
 **X DO NOT** autoriser API pouvant être appelées publiquement à lever explicitement ou implicitement <xref:System.NullReferenceException>, <xref:System.AccessViolationException>, ou <xref:System.IndexOutOfRangeException>. Ces exceptions sont réservées et levée par le moteur d’exécution et, dans que la plupart des cas indiquent un bogue.  
  
 Effectuer la vérification d’arguments pour éviter de lever ces exceptions. Lever ces exceptions expose des détails d’implémentation de votre méthode peut changer au fil du temps.  
  
## <a name="stackoverflowexception"></a>StackOverflowException  
 **X DO NOT** lever explicitement <xref:System.StackOverflowException>. L’exception doit être levée explicitement uniquement par le CLR.  
  
 **X DO NOT** catch `StackOverflowException`.  
  
 Il est quasiment impossible d’écrire du code managé qui reste cohérent en présence de débordements de pile arbitraire. Les parties non managés du CLR restent cohérentes à l’aide de sondes pour déplacer les débordements de pile à des endroits bien définis, plutôt que par sauvegarde à partir de débordements de pile arbitraire.  
  
## <a name="outofmemoryexception"></a>OutOfMemoryException  
 **X DO NOT** lever explicitement <xref:System.OutOfMemoryException>. Cette exception est levée uniquement par l’infrastructure CLR.  
  
## <a name="comexception-sehexception-and-executionengineexception"></a>ComException et SEHException ExecutionEngineException  
 **X DO NOT** lever explicitement <xref:System.Runtime.InteropServices.COMException>, <xref:System.ExecutionEngineException>, et <xref:System.Runtime.InteropServices.SEHException>. Ces exceptions doivent être levée uniquement par l’infrastructure CLR.  
  
 *Portions © 2005, 2009 Microsoft Corporation. Tous droits réservés.*  
  
 *Réimprimé avec l’autorisation de Pearson éducation, Inc. à partir de [instructions de conception Framework : Conventions, les idiomes et les modèles pour les bibliothèques .NET réutilisable, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) Krzysztof Cwalina et Brad Abrams, publié le 22 octobre 2008 par Addison-Wesley Professional dans le cadre de la série de développement de Microsoft Windows.*  
  
## <a name="see-also"></a>Voir aussi

- [Règles de conception de .NET Framework](../../../docs/standard/design-guidelines/index.md)
- [Instructions de conception pour les exceptions](../../../docs/standard/design-guidelines/exceptions.md)
