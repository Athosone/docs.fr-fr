---
title: -out (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- /out compiler option [Visual Basic]
- -out compiler option [Visual Basic]
- out compiler option [Visual Basic]
ms.assetid: 9f148c15-0909-4cb8-a2db-777f8a8b45ae
ms.openlocfilehash: 5dcf9dc5cc0987e965aba7fd2b8821252e19a655
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58815990"
---
# <a name="-out-visual-basic"></a>-out (Visual Basic)
Spécifie le nom du fichier de sortie.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
-out:filename  
```  
  
## <a name="arguments"></a>Arguments  
  
|Terme|Définition|  
|---|---|  
|`filename`|Obligatoire. Le nom du fichier de sortie que le compilateur crée. Si le nom de fichier contient un espace, placez le nom entre guillemets ( » «).|  
  
## <a name="remarks"></a>Notes  
 Spécifiez le nom complet et l’extension de fichier à créer. Si vous ne le faites pas, le fichier .exe tire son nom de fichier de code source contenant le `Sub Main` procédure et le fichier .dll tire son nom du premier fichier de code source.  
  
 Si vous spécifiez un nom de fichier sans extension .exe ou .dll, le compilateur ajoute automatiquement l’extension pour vous, en fonction de la valeur spécifiée pour le `-target` option du compilateur.  
  
|Pour définir - out dans l’environnement de développement intégré Visual Studio|  
|---|  
|1.  Sélectionnez un projet dans l' **Explorateur de solutions**. Dans le menu **Projet**, cliquez sur **Propriétés**. <br />2.  Cliquez sur l’onglet **Application** .<br />3.  Modifiez la valeur dans le **nom de l’Assembly** boîte.|  
  
## <a name="example"></a>Exemple  
 Le code suivant compile `T2.vb` et crée le fichier de sortie `T2.exe`.  
  
```console
vbc t2.vb -out:t3.exe  
```  
  
## <a name="see-also"></a>Voir aussi

- [Compilateur de ligne de commande de Visual Basic](../../../visual-basic/reference/command-line-compiler/index.md)
- [-target (Visual Basic)](../../../visual-basic/reference/command-line-compiler/target.md)
- [Exemples de lignes de commande de compilation](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
