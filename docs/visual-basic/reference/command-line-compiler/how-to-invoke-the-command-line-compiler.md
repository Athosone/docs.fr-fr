---
title: 'Procédure : Appeler le compilateur de ligne de commande (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- command-line arguments
- vbc.exe
- Visual Basic compiler, starting
- command line [Visual Basic], arguments
ms.assetid: 0fd9a8f6-f34e-4c35-a49d-9b9bbd8da4a9
ms.openlocfilehash: 67cad0df3f10ff1fa1f6a58546fe150232fe1283
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62032069"
---
# <a name="how-to-invoke-the-command-line-compiler-visual-basic"></a>Procédure : Appeler le compilateur de ligne de commande (Visual Basic)
Vous pouvez appeler le compilateur de ligne de commande en tapant le nom de son fichier exécutable dans la ligne de commande, également appelée invite de commande MS-DOS. Si vous compilez à partir de l’invite de commandes de Windows par défaut, vous devez taper le chemin d’accès complet au fichier exécutable. Pour remplacer ce comportement par défaut, vous pouvez utiliser l’invite de commandes développeur pour Visual Studio, ou modifier la variable d’environnement PATH. Les deux permettent de compiler à partir de n’importe quel répertoire il suffit de taper le nom du compilateur.  
  
[!INCLUDE[note_settings_general](~/includes/note-settings-general-md.md)]  
  
### <a name="to-invoke-the-compiler-using-the-developer-command-prompt-for-visual-studio"></a>Pour appeler le compilateur à l’aide de l’invite de commandes développeur pour Visual Studio  
  
1. Ouvrez le dossier de programme Visual Studio Tools dans le groupe de programmes de Microsoft Visual Studio.  
  
2. Vous pouvez utiliser l’invite de commandes développeur pour Visual Studio pour accéder au compilateur à partir de n’importe quel répertoire sur votre ordinateur, si Visual Studio est installé.  
  
3. Appeler l’invite de commandes développeur pour Visual Studio.  
  
4. À la ligne de commande, tapez `vbc.exe` *sourceFileName* puis appuyez sur ENTRÉE.  
  
     Par exemple, si vous avez stocké votre code source dans un répertoire appelé `SourceFiles`, vous ouvririez l’invite de commandes et le type `cd SourceFiles` pour accéder à ce répertoire. Si le répertoire contenait un fichier source nommé `Source.vb`, vous pouvez le compiler en tapant `vbc.exe Source.vb`.  
  
### <a name="to-set-the-path-environment-variable-to-the-compiler-for-the-windows-command-prompt"></a>Pour définir la variable d’environnement de chemin d’accès au compilateur pour l’invite de commandes Windows.  
  
1. Utilisez la fonctionnalité de Windows Search pour rechercher Vbc.exe sur votre disque local.  
  
     Le nom exact du répertoire où se trouve le compilateur dépend de l’emplacement du répertoire Windows et la version de « Installé le .NET Framework ». Si vous avez plusieurs versions de « .NET Framework » installé, vous devez déterminer quelle version utiliser (généralement la dernière version).  
  
2. À partir de votre **Démarrer** Menu, avec le bouton droit **poste de travail**, puis cliquez sur **propriétés** dans le menu contextuel.  
  
3. Cliquez sur le **avancé** onglet, puis cliquez sur **Variables d’environnement**.  
  
4. Dans le **système** volet variables, sélectionnez **chemin d’accès** à partir de la liste et cliquez **modifier**.  
  
5. Dans le **système modifier** boîte de dialogue Variable déplacer le point d’insertion à la fin de la chaîne dans le **valeur de la Variable** champ et tapez un point-virgule ( ;) suivi du nom complet du répertoire trouvé à l’étape 1.  
  
6. Cliquez sur **OK** pour confirmer vos modifications et fermer les boîtes de dialogue.  
  
     Après avoir modifié la variable d’environnement PATH, vous pouvez exécuter le compilateur Visual Basic à l’invite de commandes Windows à partir de n’importe quel répertoire sur l’ordinateur.  
  
### <a name="to-invoke-the-compiler-using-the-windows-command-prompt"></a>Pour appeler le compilateur à l’aide de l’invite de commandes Windows  
  
1. À partir de la **Démarrer** menu, cliquez sur le **Accessoires** , puis ouvrez le **invite de commandes Windows**.  
  
2. À la ligne de commande, tapez `vbc.exe` *sourceFileName* puis appuyez sur ENTRÉE.  
  
     Par exemple, si vous avez stocké votre code source dans un répertoire appelé `SourceFiles`, vous ouvririez l’invite de commandes et le type `cd SourceFiles` pour accéder à ce répertoire. Si le répertoire contenait un fichier source nommé `Source.vb`, vous pouvez le compiler en tapant `vbc.exe Source.vb`.  
  
## <a name="see-also"></a>Voir aussi

- [Compilateur de ligne de commande de Visual Basic](../../../visual-basic/reference/command-line-compiler/index.md)
- [Compilation conditionnelle](../../../visual-basic/programming-guide/program-structure/conditional-compilation.md)
