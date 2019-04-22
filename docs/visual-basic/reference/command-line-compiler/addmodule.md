---
title: -addmodule
ms.date: 03/09/2018
helpviewer_keywords:
- /addmodule compiler option [Visual Basic]
- addmodule compiler option [Visual Basic]
- -addmodule compiler option [Visual Basic]
ms.assetid: fb4b89d4-4926-4f20-868d-427fa28497b2
ms.openlocfilehash: 2de5fe82f1969a2fdb305d45951d7d698252c0c8
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58816432"
---
# <a name="-addmodule"></a>-addmodule
Entraîne la mise à disposition par le compilateur de toutes les informations de type à partir du ou des fichiers spécifiés, pour le projet en cours de compilation.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
-addmodule:fileList  
```  
  
## <a name="arguments"></a>Arguments  
 `fileList`  
 Obligatoire. Liste délimitée par des virgules des fichiers qui contiennent des métadonnées, mais ne contiennent pas de manifestes d’assembly. Les noms de fichiers contenant des espaces doivent être entourés de guillemets ( » «).  
  
## <a name="remarks"></a>Notes  
 Les fichiers répertoriés par le `fileList` paramètre doit être créé avec le `-target:module` option, ou avec l’équivalent d’un autre compilateur `-target:module`.  
  
 Tous les modules ajoutés par `-addmodule` doit être dans le même répertoire que le fichier de sortie au moment de l’exécution. Autrement dit, vous pouvez spécifier un module dans n’importe quel répertoire au moment de la compilation, mais le module doit être dans le répertoire de l’application en cours d’exécution. Si elle n’est pas le cas, vous obtenez un <xref:System.TypeLoadException> erreur.  
  
 Si vous spécifiez (implicitement ou explicitement) n’importe quel[-cible (Visual Basic)](../../../visual-basic/reference/command-line-compiler/target.md) option autre que `-target:module` avec `-addmodule`, les fichiers que vous transmettez à `-addmodule` deviennent partie intégrante de l’assembly du projet. Un assembly est requis pour exécuter un fichier de sortie qui contient un ou plusieurs fichiers ajoutés avec `-addmodule`.  
  
 Utilisez [/reference (Visual Basic)](../../../visual-basic/reference/command-line-compiler/reference.md) pour importer les métadonnées à partir d’un fichier qui contient un assembly.  
  
> [!NOTE]
>  Le `-addmodule` option n’est pas disponible dans l’environnement de développement Visual Studio ; il est disponible uniquement lors de la compilation à partir de la ligne de commande.  
  
## <a name="example"></a>Exemple  
 Le code suivant crée un module.  
  
 [!code-vb[VbVbalrCompiler#47](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrCompiler/VB/OptionStrictOff.vb#47)]  
  
 Le code suivant importe les types du module.  
  
 [!code-vb[VbVbalrCompiler#48](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrCompiler/VB/OptionStrictOff.vb#48)]  
  
 Lorsque vous exécutez `t1`, elle génère `802`.  
  
## <a name="see-also"></a>Voir aussi

- [Compilateur de ligne de commande de Visual Basic](../../../visual-basic/reference/command-line-compiler/index.md)
- [-target (Visual Basic)](../../../visual-basic/reference/command-line-compiler/target.md)
- [-référence (Visual Basic)](../../../visual-basic/reference/command-line-compiler/reference.md)
- [Exemples de lignes de commande de compilation](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
