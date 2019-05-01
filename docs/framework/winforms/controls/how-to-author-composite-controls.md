---
title: 'Procédure : créer des contrôles composites'
ms.date: 03/30/2017
helpviewer_keywords:
- UserControl class [Windows Forms], creating composite controls
- user controls [Windows Forms], creating
- user controls [Windows Forms], inheriting from
- composite controls [Windows Forms], creating
ms.assetid: 79c9cf05-5ab6-4a18-886d-88a64748b098
ms.openlocfilehash: 8bb630d3fb7e064935440439f2f07816e87c77dc
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62010954"
---
# <a name="how-to-author-composite-controls"></a>Procédure : créer des contrôles composites
Les contrôles composites peuvent être utilisés de plusieurs façons. Vous pouvez les créer dans le cadre d’un projet d’application de bureau Windows et les utiliser uniquement sur les formulaires du projet. Ou vous pouvez les créer dans un projet de bibliothèque de contrôles Windows, compiler le projet dans un assembly et utiliser les contrôles dans d’autres projets. Vous pouvez même hériter d’eux et utiliser l’héritage visuel pour les personnaliser rapidement à des fins spécifiques.  
  
> [!NOTE]
>  Si vous souhaitez créer un contrôle à utiliser sur des Web Forms, consultez [Développement de contrôles serveur ASP.NET personnalisés](https://docs.microsoft.com/previous-versions/aspnet/zt27tfhy(v=vs.100)).  
>   
>  Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée. Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** . Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).  
  
### <a name="to-author-a-composite-control"></a>Pour créer un contrôle composite  
  
1. Ouvrez un nouveau projet d’**application Windows** nommé `DemoControlHost`.  
  
2. Dans le menu **Projet** , cliquez sur **Ajouter un contrôle utilisateur**.  
  
3. Dans la boîte de dialogue **Ajouter un nouvel élément**, donnez au fichier de classe (fichier .vb ou .cs) le nom que vous souhaitez pour le contrôle composite.  
  
4. Sélectionnez le **ajouter** bouton pour créer le fichier de classe pour le contrôle composite.  
  
5. Utilisez la **boîte à outils** pour ajouter des contrôles à la surface du contrôle composite.  
  
6. Placez le code dans des procédures événementielles afin de gérer les événements déclenchés par le contrôle composite ou par ses contrôles constitutifs.  
  
7. Fermez le concepteur du contrôle composite et enregistrez le fichier lorsque vous y êtes invité.  
  
8. Dans le menu **Générer** , cliquez sur **Générer la solution**.  
  
     Le projet doit être généré de sorte que les contrôles personnalisés apparaissent dans la **boîte à outils**.  
  
9. Utilisez l’onglet **DemoControlHost** de la **boîte à outils** pour ajouter des instances de votre contrôle sur `Form1`.  
  
### <a name="to-author-a-control-class-library"></a>Pour créer une bibliothèque de classes de contrôle  
  
1. Ouvrez un nouveau projet de **bibliothèque de contrôles Windows**.  
  
     Par défaut, le projet contient un contrôle composite.  
  
2. Ajoutez des contrôles et du code, comme décrit dans la procédure ci-dessus.  
  
3. Sélectionnez un contrôle dont vous ne souhaitez pas modifier les classes qui héritent, puis définissez la propriété **Modifiers** de ce contrôle sur **Private**.  
  
4. Créez la DLL.  
  
### <a name="to-inherit-from-a-composite-control-in-a-control-class-library"></a>Pour hériter d’un contrôle composite dans une bibliothèque de classes de contrôle  
  
1. Dans le menu **Fichier**, pointez sur **Ajouter** et sélectionnez **Nouveau projet** pour ajouter un nouveau projet d’**application Windows** à la solution.  
  
2. Dans l’**Explorateur de solutions**, cliquez avec le bouton droit sur le dossier **References** du nouveau projet, puis sélectionnez **Ajouter une référence** pour ouvrir la boîte de dialogue **Ajouter une référence**.  
  
3. Sélectionnez l’onglet **Projets** et double-cliquez sur votre projet de bibliothèque de contrôles.  
  
4. Dans le menu **Générer** , cliquez sur **Générer la solution**.  
  
5. Dans l’**Explorateur de solutions**, cliquez avec le bouton droit sur votre projet de bibliothèque de contrôles, puis sélectionnez **Ajouter un nouvel élément** dans le menu contextuel.  
  
6. Sélectionnez le modèle **Contrôle utilisateur hérité** dans la boîte de dialogue **Ajouter un nouvel élément**.  
  
7. Dans la boîte de dialogue **Sélecteur d’héritage**, double-cliquez sur le contrôle dont vous voulez hériter.  
  
     Un nouveau contrôle est ajouté à votre projet.  
  
8. Ouvrez le concepteur visuel du nouveau contrôle et ajoutez d’autres contrôles constitutifs.  
  
     Vous pouvez voir les contrôles constitutifs hérités du contrôle composite dans votre DLL, et vous pouvez modifier les propriétés des contrôles dont la propriété **Modifiers** est définie sur **Public**. Vous ne pouvez pas modifier les propriétés du contrôle dont la propriété **Modifiers** est définie sur **Private**.  
  
## <a name="see-also"></a>Voir aussi

- [Procédure pas à pas : Création d’un contrôle Composite avec Visual Basic](walkthrough-authoring-a-composite-control-with-visual-basic.md)
- [Procédure pas à pas : Création d’un contrôle Composite avec VisualC#](walkthrough-authoring-a-composite-control-with-visual-csharp.md)
- [Procédure pas à pas : Héritage d’un contrôle de formulaire Windows avec Visual Basic](walkthrough-inheriting-from-a-windows-forms-control-with-visual-basic.md)
- [Procédure pas à pas : Héritage d’un contrôle de formulaire Windows avec VisualC#](walkthrough-inheriting-from-a-windows-forms-control-with-visual-csharp.md)
- [Recommandations relatives au type de contrôle](control-type-recommendations.md)
- [Guide pratique pour Créer des contrôles pour les Windows Forms](how-to-author-controls-for-windows-forms.md)
- [Variétés de contrôles personnalisés](varieties-of-custom-controls.md)
