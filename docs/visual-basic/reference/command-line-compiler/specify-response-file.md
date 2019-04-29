---
title: '@ (spécifier un fichier réponse) (Visual Basic)'
ms.date: 03/13/2018
helpviewer_keywords:
- '@ (Specify Response File) compiler option [Visual Basic]'
ms.assetid: a6847eaa-e5f9-4303-9421-45b55484b9ca
ms.openlocfilehash: 6b993a6399eec4e203821109db153aadf246cbac
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61639020"
---
# <a name="-specify-response-file-visual-basic"></a>@ (spécifier un fichier réponse) (Visual Basic)
Spécifie un fichier qui contient les options du compilateur et les fichiers de code source à compiler.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
@response_file  
```  
  
## <a name="arguments"></a>Arguments  
 `response_file`  
 Obligatoire. Un fichier qui répertorie les options du compilateur ou les fichiers de code source à compiler. Placez le nom de fichier entre guillemets ( » «) s’il contient un espace.  
  
## <a name="remarks"></a>Notes  
 Le compilateur traite les options du compilateur et les fichiers de code source spécifiés dans un fichier réponse, comme s’ils avaient été spécifiés sur la ligne de commande.  
  
 Pour spécifier plusieurs fichiers réponse dans une compilation, spécifiez plusieurs options de fichier de réponse, telle que la suivante.  
  
```  
@file1.rsp @file2.rsp  
```  
  
 Dans une réponse du fichier, plusieurs options du compilateur et les fichiers de code source peuvent apparaître sur une seule ligne. Une spécification de l’option de compilateur unique doit apparaître sur une seule ligne (ne peut pas couvrir plusieurs lignes,). Fichiers réponse peuvent contenir des commentaires qui commencent par le `#` symbole.  
  
 Vous pouvez combiner les options spécifiées sur la ligne de commande avec les options spécifiées dans un ou plusieurs fichiers de réponse. Le compilateur traite les options de commande qu’il les rencontre. Par conséquent, les arguments de ligne de commande peuvent substituer des options précédemment affichées dans les fichiers réponse. À l’inverse, options dans un fichier réponse substituent les options affichées précédemment sur la ligne de commande ou dans d’autres fichiers de réponse.  
  
 Visual Basic fournit le fichier Vbc.rsp, qui se trouve dans le même répertoire que le fichier Vbc.exe. Le fichier Vbc.rsp est inclus par défaut, sauf si le `-noconfig` option est utilisée. Pour plus d’informations, consultez [- noconfig](../../../visual-basic/reference/command-line-compiler/noconfig.md).  
  
> [!NOTE]
>  Le `@` option n’est pas disponible dans l’environnement de développement Visual Studio ; il est disponible uniquement lors de la compilation à partir de la ligne de commande.  
  
## <a name="example"></a>Exemple  
 Les lignes suivantes sont à partir d’un exemple de fichier de réponse.  
  
```console
# build the first output file  
-target:exe   
-out:MyExe.exe  
source1.vb   
source2.vb  
```  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre comment utiliser le `@` option avec le fichier réponse nommé `File1.rsp`.  
  
```console
vbc @file1.rsp  
```  
  
## <a name="see-also"></a>Voir aussi

- [Compilateur de ligne de commande de Visual Basic](../../../visual-basic/reference/command-line-compiler/index.md)
- [-noconfig](../../../visual-basic/reference/command-line-compiler/noconfig.md)
- [Exemples de lignes de commande de compilation](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
