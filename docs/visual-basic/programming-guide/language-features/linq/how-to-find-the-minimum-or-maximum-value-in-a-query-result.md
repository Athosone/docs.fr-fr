---
title: 'Procédure : Rechercher la valeur minimale ou maximale dans un résultat de requête à l’aide de LINQ (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- max operator [LINQ in Visual Basic]
- aggregate operator [LINQ in Visual Basic]
- aggregate queries
- minimum values [LINQ in Visual Basic]
- min operator [LINQ in Visual Basic]
- queries [LINQ in Visual Basic], minimum and maximum values
- Max property
- maximum values [LINQ in Visual Basic]
- Aggregate clause [Visual Basic]
- queries [LINQ in Visual Basic], aggregate queries
- queries [LINQ in Visual Basic], how-to topics
ms.assetid: 238b763b-7dcd-4b14-8050-b65500a4f71c
ms.openlocfilehash: af5f4bf829664057c40004a842df95d927cc5d71
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59337472"
---
# <a name="how-to-find-the-minimum-or-maximum-value-in-a-query-result-by-using-linq-visual-basic"></a>Procédure : Rechercher la valeur minimale ou maximale dans un résultat de requête à l’aide de LINQ (Visual Basic)
Language-Integrated Query (LINQ) facilite l’accès aux informations de base de données et exécuter des requêtes.  
  
 L’exemple suivant montre comment créer une application qui effectue des requêtes sur une base de données SQL Server. L’exemple détermine les valeurs minimales et maximales pour les résultats à l’aide de la `Aggregate` et `Group By` clauses. Pour plus d’informations, consultez [Aggregate, Clause](../../../../visual-basic/language-reference/queries/aggregate-clause.md) et [Group By Clause](../../../../visual-basic/language-reference/queries/group-by-clause.md).  
  
 Les exemples de cette rubrique utilisent la base de données Northwind. Si vous n’avez pas de cette base de données sur votre ordinateur de développement, vous pouvez le télécharger à partir du Microsoft Download Center. Pour obtenir des instructions, consultez [téléchargement d’exemples de bases de données](../../../../framework/data/adonet/sql/linq/downloading-sample-databases.md).  
  
[!INCLUDE[note_settings_general](~/includes/note-settings-general-md.md)]  
  
### <a name="to-create-a-connection-to-a-database"></a>Pour créer une connexion à une base de données  
  
1. Dans Visual Studio, ouvrez **Explorateur de serveurs**/**Database Explorer** en cliquant sur **Explorateur de serveurs**/**base de données Explorer** sur le **vue** menu.  
  
2. Avec le bouton droit **des connexions de données** dans **Explorateur de serveurs**/**Database Explorer** puis cliquez sur **ajouter une connexion**.  
  
3. Spécifiez une connexion valide à la base de données Northwind.  
  
### <a name="to-add-a-project-that-contains-a-linq-to-sql-file"></a>Pour ajouter un projet qui contient un fichier LINQ to SQL  
  
1. Dans Visual Studio, dans le menu **Fichier**,pointez sur **Nouveau**, puis cliquez sur **Projet**. Sélectionnez Visual Basic **Windows Forms Application** comme type de projet.  
  
2. Dans le menu **Projet** , cliquez sur **Ajouter un nouvel élément**. Sélectionnez le **Classes LINQ to SQL** modèle d’élément.  
  
3. Nommez le fichier `northwind.dbml`. Cliquez sur **Ajouter**. Le Concepteur Objet/Relationnel (Concepteur O/R) est ouvert pour le fichier northwind.dbml.  
  
### <a name="to-add-tables-to-query-to-the-or-designer"></a>Pour ajouter des tables à interroger au Concepteur O/R  
  
1. Dans **Explorateur de serveurs**/**Database Explorer**, développez la connexion à la base de données Northwind. Développez le **Tables** dossier.  
  
     Si vous avez fermé le Concepteur O/R, vous pouvez le rouvrir en double-cliquant sur le fichier northwind.dbml que vous avez ajouté précédemment.  
  
2. Cliquez sur la table Customers et faites-le glisser vers le volet gauche du concepteur. Cliquez sur la table Orders et faites-le glisser vers le volet gauche du concepteur.  
  
     Le concepteur crée de nouveaux `Customer` et `Order` objets pour votre projet. Notez que le concepteur détecte les relations entre les tables automatiquement et crée des propriétés pour les objets enfants. Par exemple, IntelliSense qui affichera le `Customer` objet possède un `Orders` propriété pour toutes les commandes associées à ce client.  
  
3. Enregistrez vos modifications et fermez le concepteur.  
  
4. Enregistrez votre projet.  
  
### <a name="to-add-code-to-query-the-database-and-display-the-results"></a>Pour ajouter du code pour interroger la base de données et afficher les résultats  
  
1. À partir de la **boîte à outils**, faites glisser un <xref:System.Windows.Forms.DataGridView> contrôle sur le formulaire de Windows par défaut pour votre projet, Form1.  
  
2. Double-cliquez sur Form1 pour ajouter du code pour le `Load` événement sous la forme.  
  
3. Lorsque vous avez ajouté des tables au Concepteur O/R, le concepteur a ajouté un <xref:System.Data.Linq.DataContext> objet pour votre projet. Cet objet contient le code dont vous devez disposer pour accéder à ces tables, en plus des collections et des objets individuels de chaque table. Le <xref:System.Data.Linq.DataContext> objet pour votre projet est nommé d’après le nom de votre fichier .dbml. Pour ce projet, le <xref:System.Data.Linq.DataContext> objet est nommé `northwindDataContext`.  
  
     Vous pouvez créer une instance de la <xref:System.Data.Linq.DataContext> dans votre code et interroger les tables spécifiées par le Concepteur O/R.  
  
     Ajoutez le code suivant à la `Load` événement. Ce code interroge les tables qui sont exposées comme propriétés de votre contexte de données et détermine les valeurs minimales et maximales pour les résultats. L’exemple utilise `Aggregate` clause pour interroger un résultat unique et le `Group By` clause pour afficher une moyenne pour les résultats groupés.  
  
     [!code-vb[VbLINQToSQLHowTos#14](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbLINQtoSQLHowTos/VB/Form7.vb#14)]  
  
4. Appuyez sur F5 pour exécuter votre projet et afficher les résultats.  
  
## <a name="see-also"></a>Voir aussi

- [LINQ](../../../../visual-basic/programming-guide/language-features/linq/index.md)
- [Requêtes](../../../../visual-basic/language-reference/queries/index.md)
- [LINQ to SQL](../../../../framework/data/adonet/sql/linq/index.md)
- [DataContext, méthodes (Concepteur O/R)](/visualstudio/data-tools/datacontext-methods-o-r-designer)
