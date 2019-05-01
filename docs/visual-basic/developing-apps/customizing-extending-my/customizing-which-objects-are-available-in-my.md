---
title: Personnalisation de la disponibilité ou non des objets dans My (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- My namespace [Visual Basic], customizing
- My namespace
ms.assetid: 4e8279c2-ed5b-4681-8903-8a6671874000
ms.openlocfilehash: c0b47521c6a62071466ae4193cd8553bdfb3dcde
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62014230"
---
# <a name="customizing-which-objects-are-available-in-my-visual-basic"></a>Personnalisation de la disponibilité ou non des objets dans My (Visual Basic)

Cette rubrique décrit comment vous pouvez contrôler qui `My` objets sont activés par configuration de votre projet `_MYTYPE` constante de compilation conditionnelle. L’environnement de développement intégré de Visual Studio (IDE) conserve la `_MYTYPE` constante de compilation conditionnelle pour un projet synchronisé avec le type du projet.  
  
## <a name="predefined-mytype-values"></a>Prédéfinies \_MYTYPE valeurs  

Vous devez utiliser le `/define` option du compilateur pour définir le `_MYTYPE` constante de compilation conditionnelle. Lorsque vous spécifiez votre propre valeur pour le `_MYTYPE` constante, vous devez placer la valeur de chaîne dans la barre oblique inverse/guillemets (\\») séquences. Par exemple, vous pouvez utiliser :  
  
```  
/define:_MYTYPE=\"WindowsForms\"  
```  
  
 Ce tableau montre à quoi le `_MYTYPE` constante de compilation conditionnelle a la valeur pour plusieurs types de projet.  
  
|Type de projet|\_Valeur MYTYPE|  
|------------------|--------------------|  
|Bibliothèque de classes|« Windows »|  
|Application console|« Console »|  
|Web|« Web »|  
|Bibliothèque de contrôles Web|« WebControl »|  
|Application Windows|"WindowsForms"|  
|Application Windows, lors du démarrage avec personnalisé `Sub Main`|"WindowsFormsWithCustomSubMain"|  
|Bibliothèque de contrôles Windows|« Windows »|  
|Service Windows|« Console »|  
|Empty|« Vide »|  
  
> [!NOTE]
> Toutes les comparaisons de chaînes de la compilation conditionnelle respectent la casse, quel que soit la façon dont le `Option Compare` instruction est définie.  
  
## <a name="dependent-my-compilation-constants"></a>Dépendants \_mon constantes de Compilation  

Le `_MYTYPE` constante de compilation conditionnelle, contrôle à son tour, les valeurs de plusieurs autres `_MY` constantes de compilation :  
  
|\_MYTYPE|\_MYAPPLICATIONTYPE|\_MYCOMPUTERTYPE|\_MYFORMS|\_MYUSERTYPE|\_MYWEBSERVICES|  
|--------------|-------------------------|----------------------|---------------|------------------|---------------------|  
|« Console »|« Console »|« Windows »|Undefined|« Windows »|TRUE|  
|« Custom »|Undefined|Undefined|Undefined|Undefined|Undefined|  
|« Vide »|Undefined|Undefined|Undefined|Undefined|Undefined|  
|« Web »|Undefined|« Web »|FALSE|« Web »|FALSE|  
|« WebControl »|Undefined|« Web »|FALSE|« Web »|TRUE|  
|« Windows » ou « »|« Windows »|« Windows »|Undefined|« Windows »|TRUE|  
|"WindowsForms"|"WindowsForms"|« Windows »|TRUE|« Windows »|TRUE|  
|"WindowsFormsWithCustomSubMain"|« Console »|« Windows »|TRUE|« Windows »|TRUE|  
  
 Par défaut, les constantes de compilation conditionnelle non définis se résolvent en `FALSE`. Vous pouvez spécifier des valeurs pour les constantes non définis lors de la compilation de votre projet pour remplacer le comportement par défaut.  
  
> [!NOTE]
> Lorsque `_MYTYPE` a la valeur « Personnalisé », le projet contient le `My` espace de noms, mais il ne contient aucun objet. Toutefois, l’affectation `_MYTYPE` à « Vide » empêche le compilateur d’ajouter le `My` espace de noms et ses objets.  
  
 Ce tableau décrit les effets des valeurs prédéfinies de le `_MY` constantes de compilation.  
  
|Constante|Signification|  
|--------------|-------------|  
|`_MYAPPLICATIONTYPE`|Permet de `My.Application`, si la constante est « Console », Windows, » ou « WindowsForms » :<br /><br /> -La version « Console » dérive <xref:Microsoft.VisualBasic.ApplicationServices.ConsoleApplicationBase>. et a moins de membres que la version « Windows ».<br />-La version « Windows » dérive <xref:Microsoft.VisualBasic.ApplicationServices.ApplicationBase>.et a moins de membres que la version « WindowsForms ».<br />-La version « WindowsForms » de `My.Application` dérive <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase>. Si le `TARGET` constante est définie comme étant « winexe », puis la classe inclut un `Sub Main` (méthode).|  
|`_MYCOMPUTERTYPE`|Permet de `My.Computer`, si la constante est « Web » ou « Windows » :<br /><br /> -La version « Web » dérive <xref:Microsoft.VisualBasic.Devices.ServerComputer>, et a moins de membres que la version « Windows ».<br />-La version « Windows » du `My.Computer` dérive <xref:Microsoft.VisualBasic.Devices.Computer>.|  
|`_MYFORMS`|Permet de `My.Forms`, si la constante est `TRUE`.|  
|`_MYUSERTYPE`|Permet de `My.User`, si la constante est « Web » ou « Windows » :<br /><br /> -La version « Web » de `My.User` est associé à l’identité de l’utilisateur de la requête HTTP actuelle.<br />-La version « Windows » du `My.User` est associé au principal actuel du thread.|  
|`_MYWEBSERVICES`|Permet de `My.WebServices`, si la constante est `TRUE`.|  
|`_MYTYPE`|Permet de `My.Log`, `My.Request`, et `My.Response`, si la constante est « Web ».|  
  
## <a name="see-also"></a>Voir aussi

- <xref:Microsoft.VisualBasic.ApplicationServices.ApplicationBase>
- <xref:Microsoft.VisualBasic.Devices.Computer>
- <xref:Microsoft.VisualBasic.Logging.Log>
- <xref:Microsoft.VisualBasic.ApplicationServices.User>
- [Comment My dépend du type de projet](../../../visual-basic/developing-apps/development-with-my/how-my-depends-on-project-type.md)
- [Compilation conditionnelle](../../../visual-basic/programming-guide/program-structure/conditional-compilation.md)
- [/define (Visual Basic)](../../../visual-basic/reference/command-line-compiler/define.md)
- [My.Forms (objet)](../../../visual-basic/language-reference/objects/my-forms-object.md)
- [My.Request (objet)](../../../visual-basic/language-reference/objects/my-request-object.md)
- [My.Response (objet)](../../../visual-basic/language-reference/objects/my-response-object.md)
- [My.WebServices (objet)](../../../visual-basic/language-reference/objects/my-webservices-object.md)
