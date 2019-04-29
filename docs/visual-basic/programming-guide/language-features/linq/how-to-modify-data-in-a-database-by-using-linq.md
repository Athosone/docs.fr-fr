---
title: 'Procédure : Modifier des données dans une base de données à l’aide de LINQ (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- inserting rows [LINQ to SQL]
- deleting rows [LINQ to SQL]
- updating rows [LINQ to SQL]
- inserting data [Visual Basic]
- deleting data
- data [Visual Basic], updating
- updating data [LINQ]
- queries [LINQ in Visual Basic], data changes in database
- queries [LINQ in Visual Basic], how-to topics
ms.assetid: cf52635f-0c1b-46c3-aff1-bdf181cf19b1
ms.openlocfilehash: 8770a8761af4b55394d9280b21d2a6a5b71b6ed5
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61594216"
---
# <a name="how-to-modify-data-in-a-database-by-using-linq-visual-basic"></a>Procédure : Modifier des données dans une base de données à l’aide de LINQ (Visual Basic)
Language-Integrated des requêtes de requête (LINQ) facilitent l’accès aux informations de base de données et modifier les valeurs dans la base de données.  
  
 L’exemple suivant montre comment créer une application qui Récupère et informations mises à jour dans une base de données SQL Server.  
  
 Les exemples de cette rubrique utilisent la base de données Northwind. Si vous n’avez pas de cette base de données sur votre ordinateur de développement, vous pouvez le télécharger à partir du Microsoft Download Center. Pour obtenir des instructions, consultez [téléchargement d’exemples de bases de données](../../../../framework/data/adonet/sql/linq/downloading-sample-databases.md).  
  
### <a name="to-create-a-connection-to-a-database"></a>Pour créer une connexion à une base de données  
  
1. Dans Visual Studio, ouvrez **Explorateur de serveurs**/**Database Explorer** en cliquant sur le **vue** menu, puis sélectionnez **Explorateur de serveurs** / **Explorateur de base de données**.  
  
2. Avec le bouton droit **des connexions de données** dans **Explorateur de serveurs**/**Database Explorer**, puis cliquez sur **ajouter une connexion**.  
  
3. Spécifiez une connexion valide à la base de données Northwind.  
  
### <a name="to-add-a-project-with-a-linq-to-sql-file"></a>Pour ajouter un projet avec un LINQ vers le fichier SQL  
  
1. Dans Visual Studio, dans le menu **Fichier**,pointez sur **Nouveau**, puis cliquez sur **Projet**. Sélectionnez Visual Basic **Windows Forms Application** comme type de projet.  
  
2. Dans le menu **Projet** , cliquez sur **Ajouter un nouvel élément**. Sélectionnez le **Classes LINQ to SQL** modèle d’élément.  
  
3. Nommez le fichier `northwind.dbml`. Cliquez sur **Ajouter**. Le Concepteur Objet/Relationnel (Concepteur O/R) est ouvert pour la `northwind.dbml` fichier.  
  
### <a name="to-add-tables-to-query-and-modify-to-the-designer"></a>Pour ajouter des tables pour interroger et modifier dans le Concepteur  
  
1. Dans **Explorateur de serveurs**/**Database Explorer**, développez la connexion à la base de données Northwind. Développez le **Tables** dossier.  
  
     Si vous avez fermé le Concepteur O/R, vous pouvez le rouvrir en double-cliquant sur le `northwind.dbml` fichier que vous avez ajouté précédemment.  
  
2. Cliquez sur la table Customers et faites-le glisser vers le volet gauche du concepteur.  
  
     Le concepteur crée un nouvel objet Customer pour votre projet.  
  
3. Enregistrez vos modifications et fermez le concepteur.  
  
4. Enregistrez votre projet.  
  
### <a name="to-add-code-to-modify-the-database-and-display-the-results"></a>Pour ajouter du code pour modifier la base de données et afficher les résultats  
  
1. À partir de la **boîte à outils**, faites glisser un <xref:System.Windows.Forms.DataGridView> contrôle sur le formulaire de Windows par défaut pour votre projet, Form1.  
  
2. Lorsque vous avez ajouté des tables au Concepteur O/R, le concepteur a ajouté un <xref:System.Data.Linq.DataContext> objet à votre projet. Cet objet contient le code que vous pouvez utiliser pour accéder à la table Customers. Il contient également le code qui définit un objet de client local et une collection de clients pour la table. Le <xref:System.Data.Linq.DataContext> objet pour votre projet est nommé d’après le nom de votre fichier .dbml. Pour ce projet, le <xref:System.Data.Linq.DataContext> objet est nommé `northwindDataContext`.  
  
     Vous pouvez créer une instance de la <xref:System.Data.Linq.DataContext> de l’objet dans votre code et les interroger et modifier la collection de clients spécifiée par le Concepteur O/R. Les modifications que vous apportez à la collection des clients ne sont pas répercutées dans la base de données jusqu'à ce que vous les envoyez en appelant le <xref:System.Data.Linq.DataContext.SubmitChanges%2A> méthode de la <xref:System.Data.Linq.DataContext> objet.  
  
     Double-cliquez sur le formulaire Windows, Form1, pour ajouter du code pour le <xref:System.Windows.Forms.Form.Load> événement à interroger la table Customers qui est exposé en tant que propriété de votre <xref:System.Data.Linq.DataContext>. Ajoutez le code suivant :  
  
    ```vb  
    Private db As northwindDataContext  
  
    Private Sub Form1_Load(ByVal sender As System.Object,   
                           ByVal e As System.EventArgs  
                          ) Handles MyBase.Load  
      db = New northwindDataContext()  
  
      RefreshData()  
    End Sub  
  
    Private Sub RefreshData()  
      Dim customers = From cust In db.Customers   
                      Where cust.City(0) = "W"   
                      Select cust  
  
      DataGridView1.DataSource = customers  
    End Sub  
    ```  
  
3. À partir de la **boîte à outils**, faites glisser trois <xref:System.Windows.Forms.Button> contrôles vers le formulaire. Sélectionnez le premier `Button` contrôle. Dans le **propriétés** fenêtre, définissez la `Name` de la `Button` le contrôle à `AddButton` et `Text` à `Add`. Sélectionnez le deuxième bouton et définissez le `Name` propriété `UpdateButton` et `Text` propriété `Update`. Sélectionnez le troisième bouton et définissez le `Name` propriété `DeleteButton` et `Text` propriété `Delete`.  
  
4. Double-cliquez sur le **ajouter** pour ajouter du code à son `Click` événement. Ajoutez le code suivant :  
  
    ```vb  
    Private Sub AddButton_Click(ByVal sender As System.Object,   
                                ByVal e As System.EventArgs  
                               ) Handles AddButton.Click  
      Dim cust As New Customer With {   
        .City = "Wellington",   
        .CompanyName = "Blue Yonder Airlines",   
        .ContactName = "Jill Frank",   
        .Country = "New Zealand",   
        .CustomerID = "JILLF"}  
  
      db.Customers.InsertOnSubmit(cust)  
  
      Try  
        db.SubmitChanges()  
      Catch  
        ' Handle exception.  
      End Try  
  
      RefreshData()  
    End Sub  
    ```  
  
5. Double-cliquez sur le **mise à jour** pour ajouter du code à son `Click` événement. Ajoutez le code suivant :  
  
    ```vb  
    Private Sub UpdateButton_Click(ByVal sender As System.Object, _  
                                   ByVal e As System.EventArgs  
                                  ) Handles UpdateButton.Click  
      Dim updateCust = (From cust In db.Customers   
                        Where cust.CustomerID = "JILLF").ToList()(0)  
  
      updateCust.ContactName = "Jill Shrader"
      updateCust.Country = "Wales"
      updateCust.CompanyName = "Red Yonder Airlines"
      updateCust.City = "Cardiff"
  
      Try  
        db.SubmitChanges()  
      Catch  
        ' Handle exception.  
      End Try  
  
      RefreshData()  
    End Sub  
    ```  
  
6. Double-cliquez sur le **supprimer** pour ajouter du code à son `Click` événement. Ajoutez le code suivant :  
  
    ```vb  
    Private Sub DeleteButton_Click(ByVal sender As System.Object, _  
                                   ByVal e As System.EventArgs  
                                  ) Handles DeleteButton.Click  
      Dim deleteCust = (From cust In db.Customers   
                        Where cust.CustomerID = "JILLF").ToList()(0)  
  
      db.Customers.DeleteOnSubmit(deleteCust)  
  
      Try  
        db.SubmitChanges()  
      Catch  
        ' Handle exception.  
      End Try  
  
      RefreshData()  
    End Sub  
    ```  
  
7. Appuyez sur F5 pour exécuter votre projet. Cliquez sur **ajouter** pour ajouter un nouvel enregistrement. Cliquez sur **mise à jour** pour modifier le nouvel enregistrement. Cliquez sur **supprimer** pour supprimer le nouvel enregistrement.  
  
## <a name="see-also"></a>Voir aussi

- [LINQ](../../../../visual-basic/programming-guide/language-features/linq/index.md)
- [Requêtes](../../../../visual-basic/language-reference/queries/index.md)
- [LINQ to SQL](../../../../framework/data/adonet/sql/linq/index.md)
- [DataContext, méthodes (Concepteur O/R)](/visualstudio/data-tools/datacontext-methods-o-r-designer)
- [Guide pratique pour affecter des procédures stockées pour effectuer des mises à jour, des insertions et des suppressions (Concepteur O/R)](/visualstudio/data-tools/how-to-assign-stored-procedures-to-perform-updates-inserts-and-deletes-o-r-designer)
