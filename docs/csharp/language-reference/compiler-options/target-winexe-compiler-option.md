---
title: -target:winexe (Options du compilateur C#)
ms.date: 07/20/2015
f1_keywords:
- /target:winexe
helpviewer_keywords:
- /target compiler options [C#], /target:winexe
- -target compiler options [C#], /target:winexe
- target compiler options [C#], /target:winexe
ms.assetid: b5a0619c-8caa-46a5-a743-1cf68408ad7a
ms.openlocfilehash: 3c16bf8aed0d281b2b5a3f9c6ae06f343b1eff7c
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59307304"
---
# <a name="-targetwinexe-c-compiler-options"></a>-target:winexe (Options du compilateur C#)
L’option **-target:winexe** indique au compilateur de créer un programme Windows exécutable (EXE).  
  
## <a name="syntax"></a>Syntaxe  
  
```console  
-target:winexe  
```  
  
## <a name="remarks"></a>Remarques  
 Le fichier exécutable est créé avec l’extension .exe. Un programme Windows est un programme qui fournit une interface utilisateur à partir de la bibliothèque .NET Framework ou avec les API Windows.  
  
 Utilisez [-target:exe](../../../csharp/language-reference/compiler-options/target-exe-compiler-option.md) pour créer une application console.  
  
 À moins que l’option [-out](../../../csharp/language-reference/compiler-options/out-compiler-option.md) spécifie autre chose, le fichier de sortie prend le nom du fichier d’entrée qui contient la méthode [Main](../../../csharp/programming-guide/main-and-command-args/index.md).  
  
 Quand ils sont spécifiés dans la ligne de commande, tous les fichiers jusqu’à l’option **-out** ou [-target](../../../csharp/language-reference/compiler-options/target-compiler-option.md) suivante sont utilisés pour créer le programme Windows.  
  
 Une seule et unique méthode **Main** est requise dans les fichiers de code source qui sont compilés dans un fichier .exe. L’option [-main](../../../csharp/language-reference/compiler-options/main-compiler-option.md) vous permet de spécifier la classe contenant la méthode **Main**, au cas où votre code possède plusieurs classes avec une méthode **Main**.  
  
### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Pour définir cette option du compilateur dans l'environnement de développement Visual Studio  
  
1. Ouvrez la page **Propriétés** du projet.  
  
2. Cliquez sur la page de propriétés **Application**.  
  
3. Modifiez la propriété **Type de sortie**.  
  
 Pour plus d’informations sur la définition de cette option du compilateur par programmation, consultez <xref:VSLangProj80.ProjectProperties3.OutputType%2A>.  
  
## <a name="example"></a>Exemple  
 Compilez `in.cs` en un programme Windows :  
  
```console  
csc -target:winexe in.cs  
```  
  
## <a name="see-also"></a>Voir aussi

- [-target (Options du compilateur C#)](../../../csharp/language-reference/compiler-options/target-compiler-option.md)
- [Options du compilateur C#](../../../csharp/language-reference/compiler-options/index.md)
