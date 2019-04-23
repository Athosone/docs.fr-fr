---
title: Consommation d’un DataSet à partir d’un service web XML
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 9edd6b71-0fa5-4649-ae1d-ac1c12541019
ms.openlocfilehash: 7b284a8f085ab7e93651c829ac16e47fb63a8b51
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59297778"
---
# <a name="consuming-a-dataset-from-an-xml-web-service"></a><span data-ttu-id="1db5c-102">Consommation d’un DataSet à partir d’un service web XML</span><span class="sxs-lookup"><span data-stu-id="1db5c-102">Consuming a DataSet from an XML Web Service</span></span>
<span data-ttu-id="1db5c-103">L'objet <xref:System.Data.DataSet> a été conçu avec une architecture déconnectée, en partie afin de faciliter le transport des données sur Internet.</span><span class="sxs-lookup"><span data-stu-id="1db5c-103">The <xref:System.Data.DataSet> was architected with a disconnected design, in part to facilitate the convenient transport of data over the Internet.</span></span> <span data-ttu-id="1db5c-104">Le **DataSet** est « sérialisable » dans la mesure où il peut être spécifié en tant qu’entrée ou de sortie à partir des services Web XML sans aucun codage supplémentaire requis pour transmettre le contenu de la **DataSet** à partir d’un service Web XML pour un client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="1db5c-104">The **DataSet** is "serializable" in that it can be specified as an input to or output from XML Web services without any additional coding required to stream the contents of the **DataSet** from an XML Web service to a client and back.</span></span> <span data-ttu-id="1db5c-105">Le **DataSet** est implicitement converti en flux XML en utilisant le format DiffGram, envoyé sur le réseau, puis reconstruit à partir du flux XML en tant qu’un **DataSet** sur l’extrémité de réception.</span><span class="sxs-lookup"><span data-stu-id="1db5c-105">The **DataSet** is implicitly converted to an XML stream using the DiffGram format, sent over the network, and then reconstructed from the XML stream as a **DataSet** on the receiving end.</span></span> <span data-ttu-id="1db5c-106">Vous disposez ainsi d’une méthode alliant simplicité et souplesse pour la transmission et le retour de données relationnelles à l’aide des services web XML.</span><span class="sxs-lookup"><span data-stu-id="1db5c-106">This gives you a very simple and flexible method for transmitting and returning relational data using XML Web services.</span></span> <span data-ttu-id="1db5c-107">Pour plus d’informations sur le format DiffGram, consultez [DiffGrams](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/diffgrams.md).</span><span class="sxs-lookup"><span data-stu-id="1db5c-107">For more information about the DiffGram format, see [DiffGrams](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/diffgrams.md).</span></span>  
  
 <span data-ttu-id="1db5c-108">L’exemple suivant montre comment créer un service Web XML et un client qui utilisent le **DataSet** pour transporter des données relationnelles (notamment des données modifiées) et de résoudre les mises à jour dans la source de données d’origine.</span><span class="sxs-lookup"><span data-stu-id="1db5c-108">The following example shows how to create an XML Web service and client that use the **DataSet** to transport relational data (including modified data) and resolve any updates back to the original data source.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="1db5c-109">Nous recommandons de toujours tenir compte des impératifs de sécurité lorsque vous créez un service Web XML.</span><span class="sxs-lookup"><span data-stu-id="1db5c-109">We recommend that you always consider security implications when creating an XML Web service.</span></span> <span data-ttu-id="1db5c-110">Pour plus d’informations sur la sécurisation d’un service Web XML, consultez [sécurisation des Services Web XML créés à l’aide d’ASP.NET](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/w67h0dw7(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="1db5c-110">For information on securing an XML Web service, see [Securing XML Web Services Created Using ASP.NET](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/w67h0dw7(v=vs.100)).</span></span>  
  
### <a name="to-create-an-xml-web-service-that-returns-and-consumes-a-dataset"></a><span data-ttu-id="1db5c-111">Pour créer un service web XML qui retourne et utilise un DataSet</span><span class="sxs-lookup"><span data-stu-id="1db5c-111">To create an XML Web service that returns and consumes a DataSet</span></span>  
  
1. <span data-ttu-id="1db5c-112">Créez le service web XML.</span><span class="sxs-lookup"><span data-stu-id="1db5c-112">Create the XML Web service.</span></span>  
  
     <span data-ttu-id="1db5c-113">Dans l’exemple, un service Web XML est créé qui retourne une liste de clients à partir des données, dans ce cas le **Northwind** de base de données et reçoit un **DataSet** avec les mises à jour les données, qui le service Web XML résout la source de données d’origine.</span><span class="sxs-lookup"><span data-stu-id="1db5c-113">In the example, an XML Web service is created that returns data, in this case a list of customers from the **Northwind** database, and receives a **DataSet** with updates to the data, which the XML Web service resolves back to the original data source.</span></span>  
  
     <span data-ttu-id="1db5c-114">Le service Web XML expose deux méthodes : **GetCustomers**pour retourner la liste des clients, et **UpdateCustomers**, pour répercuter les mises à jour dans la source de données.</span><span class="sxs-lookup"><span data-stu-id="1db5c-114">The XML Web service exposes two methods: **GetCustomers**, to return the list of customers, and **UpdateCustomers**, to resolve updates back to the data source.</span></span> <span data-ttu-id="1db5c-115">Le service Web XML est stocké sur le serveur Web dans le fichier DataSetSample.asmx.</span><span class="sxs-lookup"><span data-stu-id="1db5c-115">The XML Web service is stored in a file on the Web server called DataSetSample.asmx.</span></span> <span data-ttu-id="1db5c-116">Le code suivant représente le contenu de ce fichier.</span><span class="sxs-lookup"><span data-stu-id="1db5c-116">The following code outlines the contents of DataSetSample.asmx.</span></span>  
  
    ```vb  
    <% @ WebService Language = "vb" Class = "Sample" %>  
    Imports System  
    Imports System.Data  
    Imports System.Data.SqlClient  
    Imports System.Web.Services  
  
    <WebService(Namespace:="http://microsoft.com/webservices/")> _  
    Public Class Sample  
  
    Public connection As SqlConnection = New SqlConnection("Data Source=(local);Integrated Security=SSPI;Initial Catalog=Northwind")  
  
      <WebMethod( Description := "Returns Northwind Customers", EnableSession := False )> _  
      Public Function GetCustomers() As DataSet  
        Dim adapter As SqlDataAdapter = New SqlDataAdapter( _  
          "SELECT CustomerID, CompanyName FROM Customers", connection)  
  
        Dim custDS As DataSet = New DataSet()  
        adapter.MissingSchemaAction = MissingSchemaAction.AddWithKey  
        adapter.Fill(custDS, "Customers")  
  
        Return custDS  
      End Function  
  
      <WebMethod( Description := "Updates Northwind Customers", EnableSession := False )> _  
      Public Function UpdateCustomers(custDS As DataSet) As DataSet  
        Dim adapter As SqlDataAdapter = New SqlDataAdapter()  
  
        adapter.InsertCommand = New SqlCommand( _  
          "INSERT INTO Customers (CustomerID, CompanyName) " & _  
          "Values(@CustomerID, @CompanyName)", connection)  
        adapter.InsertCommand.Parameters.Add( _  
          "@CustomerID", SqlDbType.NChar, 5, "CustomerID")  
        adapter.InsertCommand.Parameters.Add( _  
          "@CompanyName", SqlDbType.NChar, 15, "CompanyName")  
  
        adapter.UpdateCommand = New SqlCommand( _  
          "UPDATE Customers Set CustomerID = @CustomerID, " & _  
          "CompanyName = @CompanyName WHERE CustomerID = " & _  
          @OldCustomerID", connection)  
        adapter.UpdateCommand.Parameters.Add( _  
          "@CustomerID", SqlDbType.NChar, 5, "CustomerID")  
        adapter.UpdateCommand.Parameters.Add( _  
          "@CompanyName", SqlDbType.NChar, 15, "CompanyName")  
  
        Dim parameter As SqlParameter = _  
          adapter.UpdateCommand.Parameters.Add( _  
          "@OldCustomerID", SqlDbType.NChar, 5, "CustomerID")  
        parameter.SourceVersion = DataRowVersion.Original  
  
        adapter.DeleteCommand = New SqlCommand( _  
          "DELETE FROM Customers WHERE CustomerID = @CustomerID", _  
          connection)  
        parameter = adapter.DeleteCommand.Parameters.Add( _  
          "@CustomerID", SqlDbType.NChar, 5, "CustomerID")  
        parameter.SourceVersion = DataRowVersion.Original  
  
        adapter.Update(custDS, "Customers")  
  
        Return custDS  
      End Function  
    End Class  
    ```  
  
    ```csharp  
    <% @ WebService Language = "C#" Class = "Sample" %>  
    using System;  
    using System.Data;  
    using System.Data.SqlClient;  
    using System.Web.Services;  
  
    [WebService(Namespace="http://microsoft.com/webservices/")]  
    public class Sample  
    {  
      public SqlConnection connection = new SqlConnection("Data Source=(local);Integrated Security=SSPI;Initial Catalog=Northwind");  
  
      [WebMethod( Description = "Returns Northwind Customers", EnableSession = false )]  
      public DataSet GetCustomers()  
      {  
        SqlDataAdapter adapter = new SqlDataAdapter(  
          "SELECT CustomerID, CompanyName FROM Customers", connection);  
  
        DataSet custDS = new DataSet();  
        adapter.MissingSchemaAction = MissingSchemaAction.AddWithKey;  
        adapter.Fill(custDS, "Customers");  
  
        return custDS;  
      }  
  
      [WebMethod( Description = "Updates Northwind Customers",  
        EnableSession = false )]  
      public DataSet UpdateCustomers(DataSet custDS)  
      {  
        SqlDataAdapter adapter = new SqlDataAdapter();  
  
        adapter.InsertCommand = new SqlCommand(  
          "INSERT INTO Customers (CustomerID, CompanyName) " +  
          "Values(@CustomerID, @CompanyName)", connection);  
        adapter.InsertCommand.Parameters.Add(  
          "@CustomerID", SqlDbType.NChar, 5, "CustomerID");  
        adapter.InsertCommand.Parameters.Add(  
          "@CompanyName", SqlDbType.NChar, 15, "CompanyName");  
  
        adapter.UpdateCommand = new SqlCommand(  
          "UPDATE Customers Set CustomerID = @CustomerID, " +  
          "CompanyName = @CompanyName WHERE CustomerID = " +  
          "@OldCustomerID", connection);  
        adapter.UpdateCommand.Parameters.Add(  
          "@CustomerID", SqlDbType.NChar, 5, "CustomerID");  
        adapter.UpdateCommand.Parameters.Add(  
          "@CompanyName", SqlDbType.NChar, 15, "CompanyName");  
        SqlParameter parameter = adapter.UpdateCommand.Parameters.Add(  
          "@OldCustomerID", SqlDbType.NChar, 5, "CustomerID");  
        parameter.SourceVersion = DataRowVersion.Original;  
  
        adapter.DeleteCommand = new SqlCommand(  
        "DELETE FROM Customers WHERE CustomerID = @CustomerID",  
         connection);  
        parameter = adapter.DeleteCommand.Parameters.Add(  
          "@CustomerID", SqlDbType.NChar, 5, "CustomerID");  
        parameter.SourceVersion = DataRowVersion.Original;  
  
        adapter.Update(custDS, "Customers");  
  
        return custDS;  
      }  
    }  
    ```  
  
     <span data-ttu-id="1db5c-117">Dans un scénario classique, le **UpdateCustomers** méthode serait écrite pour intercepter les violations d’accès concurrentiel optimiste.</span><span class="sxs-lookup"><span data-stu-id="1db5c-117">In a typical scenario, the **UpdateCustomers** method would be written to catch optimistic concurrency violations.</span></span> <span data-ttu-id="1db5c-118">Par souci de simplicité, cet exemple ne le fait pas.</span><span class="sxs-lookup"><span data-stu-id="1db5c-118">For simplicity, the example does not include this.</span></span> <span data-ttu-id="1db5c-119">Pour plus d’informations sur l’accès concurrentiel optimiste, consultez [d’accès concurrentiel optimiste](../../../../../docs/framework/data/adonet/optimistic-concurrency.md).</span><span class="sxs-lookup"><span data-stu-id="1db5c-119">For more information about optimistic concurrency, see [Optimistic Concurrency](../../../../../docs/framework/data/adonet/optimistic-concurrency.md).</span></span>  
  
2. <span data-ttu-id="1db5c-120">Créez un proxy de service web XML.</span><span class="sxs-lookup"><span data-stu-id="1db5c-120">Create an XML Web service proxy.</span></span>  
  
     <span data-ttu-id="1db5c-121">Les clients du service web XML ont besoin d’un proxy SOAP pour pouvoir utiliser les méthodes exposées.</span><span class="sxs-lookup"><span data-stu-id="1db5c-121">Clients of the XML Web service require a SOAP proxy in order to consume the exposed methods.</span></span> <span data-ttu-id="1db5c-122">Vous pouvez faire en sorte que Visual Studio génère ce proxy pour vous.</span><span class="sxs-lookup"><span data-stu-id="1db5c-122">You can have Visual Studio generate this proxy for you.</span></span> <span data-ttu-id="1db5c-123">En définissant une référence Web à un service Web existant depuis Visual Studio, tout le comportement décrit dans cette étape se passe de façon transparente.</span><span class="sxs-lookup"><span data-stu-id="1db5c-123">By setting a Web reference to an existing Web service from within Visual Studio, all the behavior described in this step occurs transparently.</span></span> <span data-ttu-id="1db5c-124">Si vous souhaitez créer la classe proxy vous-même, passez à cette description.</span><span class="sxs-lookup"><span data-stu-id="1db5c-124">If you want to create the proxy class yourself, continue with this discussion.</span></span> <span data-ttu-id="1db5c-125">Le plus souvent, cependant, l'utilisation de Visual Studio pour créer la classe proxy pour l'application cliente suffit.</span><span class="sxs-lookup"><span data-stu-id="1db5c-125">In most circumstances, however, using Visual Studio to create the proxy class for the client application is sufficient.</span></span>  
  
     <span data-ttu-id="1db5c-126">Un proxy peut être créé à l'aide de l'outil Web Services Description Language Tool.</span><span class="sxs-lookup"><span data-stu-id="1db5c-126">A proxy can be created using the Web Services Description Language Tool.</span></span> <span data-ttu-id="1db5c-127">Par exemple, si le service Web XML est exposé à l’URL `http://myserver/data/DataSetSample.asmx`, émettre une commande semblable à celle-ci pour créer un proxy Visual Basic .NET avec un espace de noms **WebData.DSSample** et stockez-le dans le fichier sample.vb.</span><span class="sxs-lookup"><span data-stu-id="1db5c-127">For example, if the XML Web service is exposed at the URL `http://myserver/data/DataSetSample.asmx`, issue a command such as the following to create a Visual Basic .NET proxy with a namespace of **WebData.DSSample** and store it in the file sample.vb.</span></span>  
  
    ```console
    wsdl /l:VB -out:sample.vb http://myserver/data/DataSetSample.asmx /n:WebData.DSSample  
    ```  
  
     <span data-ttu-id="1db5c-128">Pour créer un proxy C# dans le fichier sample.cs, écrivez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="1db5c-128">To create a C# proxy in the file sample.cs, issue the following command.</span></span>  
  
    ```console
    wsdl -l:CS -out:sample.cs http://myserver/data/DataSetSample.asmx -n:WebData.DSSample  
    ```  
  
     <span data-ttu-id="1db5c-129">Le proxy peut ensuite être compilé en tant que bibliothèque et importé dans le client du service web XML.</span><span class="sxs-lookup"><span data-stu-id="1db5c-129">The proxy can then be compiled as a library and imported into the XML Web service client.</span></span> <span data-ttu-id="1db5c-130">Pour compiler le code Visual Basic .NET du proxy stocké dans sample.vb en tant que sample.dll, écrivez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="1db5c-130">To compile the Visual Basic .NET proxy code stored in sample.vb as sample.dll, issue the following command.</span></span>  
  
    ```console  
    vbc -t:library -out:sample.dll sample.vb -r:System.dll -r:System.Web.Services.dll -r:System.Data.dll -r:System.Xml.dll  
    ```  
  
     <span data-ttu-id="1db5c-131">Pour compiler le code C# du proxy stocké dans sample.cs en tant que sample.dll, écrivez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="1db5c-131">To compile the C# proxy code stored in sample.cs as sample.dll, issue the following command.</span></span>  
  
    ```console
    csc -t:library -out:sample.dll sample.cs -r:System.dll -r:System.Web.Services.dll -r:System.Data.dll -r:System.Xml.dll  
    ```  
  
3. <span data-ttu-id="1db5c-132">Créez un client de service web XML.</span><span class="sxs-lookup"><span data-stu-id="1db5c-132">Create an XML Web service client.</span></span>  
  
     <span data-ttu-id="1db5c-133">Si vous souhaitez que Visual Studio de générer la classe de proxy de service Web pour vous, tout simplement créer le projet client et, dans la fenêtre Explorateur de solutions, cliquez sur le projet, cliquez sur **ajouter une référence Web**, puis sélectionnez le service Web à partir de la liste des services Web disponibles (Cela peut nécessiter en fournissant l’adresse du point de terminaison de service Web, si le service Web n’est pas disponible dans la solution actuelle ou sur l’ordinateur actuel.) Si vous créez le proxy de service web XML vous-même (comme décrit à l’étape précédente), vous pouvez l’importer dans votre code client et utiliser les méthodes de service web XML.</span><span class="sxs-lookup"><span data-stu-id="1db5c-133">If you want to have Visual Studio generate the Web service proxy class for you, simply create the client project, and, in the Solution Explorer window, right-click the project, click **Add Web Reference**, and select the Web service from the list of available Web services (this may require supplying the address of the Web service endpoint, if the Web service isn't available within the current solution, or on the current computer.) If you create the XML Web service proxy yourself (as described in the previous step), you can import it into your client code and consume the XML Web service methods.</span></span> <span data-ttu-id="1db5c-134">L’exemple de code suivant importe la bibliothèque de proxy, appelle **GetCustomers** pour obtenir une liste de clients, ajoute un nouveau client, puis retourne un **DataSet** avec les mises à jour **UpdateCustomers** .</span><span class="sxs-lookup"><span data-stu-id="1db5c-134">The following sample code imports the proxy library, calls **GetCustomers** to get a list of customers, adds a new customer, and then returns a **DataSet** with the updates to **UpdateCustomers**.</span></span>  
  
     <span data-ttu-id="1db5c-135">Notez que l’exemple passe la **DataSet** retourné par **DataSet.GetChanges** à **UpdateCustomers** , car seules les lignes modifiées doivent être transmis au  **UpdateCustomers**.</span><span class="sxs-lookup"><span data-stu-id="1db5c-135">Notice that the example passes the **DataSet** returned by **DataSet.GetChanges** to **UpdateCustomers** because only modified rows need to be passed to **UpdateCustomers**.</span></span> <span data-ttu-id="1db5c-136">**UpdateCustomers** retourne résolu **DataSet**, que vous pouvez ensuite **fusion** dans existant **DataSet** pour intégrer les modifications résolues et toute informations d’erreur de ligne à partir de la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="1db5c-136">**UpdateCustomers** returns the resolved **DataSet**, which you can then **Merge** into the existing **DataSet** to incorporate the resolved changes and any row error information from the update.</span></span> <span data-ttu-id="1db5c-137">Le code suivant part du principe que vous avez utilisé Visual Studio pour créer la référence Web, et que vous avez renommé la référence Web en DsSample dans la **ajouter une référence Web** boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="1db5c-137">The following code assumes that you have used Visual Studio to create the Web reference, and that you have renamed the Web reference to DsSample in the **Add Web Reference** dialog box.</span></span>  
  
    ```vb  
    Imports System  
    Imports System.Data  
  
    Public Class Client  
  
      Public Shared Sub Main()  
        Dim proxySample As New DsSample.Sample ()  ' Proxy object.  
        Dim customersDataSet As DataSet = proxySample.GetCustomers()  
        Dim customersTable As DataTable = _  
          customersDataSet.Tables("Customers")  
  
        Dim rowAs DataRow = customersTable.NewRow()  
        row("CustomerID") = "ABCDE"  
        row("CompanyName") = "New Company Name"  
        customersTable.Rows.Add(row)  
  
        Dim updateDataSet As DataSet = _  
          proxySample.UpdateCustomers(customersDataSet.GetChanges())  
  
        customersDataSet.Merge(updateDataSet)  
        customersDataSet.AcceptChanges()  
      End Sub  
    End Class  
    ```  
  
    ```csharp  
    using System;  
    using System.Data;  
  
    public class Client  
    {  
      public static void Main()  
      {  
        Sample proxySample = new DsSample.Sample();  // Proxy object.  
        DataSet customersDataSet = proxySample.GetCustomers();  
        DataTable customersTable = customersDataSet.Tables["Customers"];  
  
        DataRow row = customersTable.NewRow();  
        row["CustomerID"] = "ABCDE";  
        row["CompanyName"] = "New Company Name";  
        customersTable.Rows.Add(row);  
  
        DataSet updateDataSet = new DataSet();  
  
        updateDataSet =   
          proxySample.UpdateCustomers(customersDataSet.GetChanges());  
  
        customersDataSet.Merge(updateDataSet);  
        customersDataSet.AcceptChanges();  
      }  
    }  
    ```  
  
     <span data-ttu-id="1db5c-138">Si vous décidez de créer la classe proxy vous-même, vous devez prendre les mesures supplémentaires suivantes.</span><span class="sxs-lookup"><span data-stu-id="1db5c-138">If you decide to create the proxy class yourself, you must take the following extra steps.</span></span> <span data-ttu-id="1db5c-139">Pour compiler l'exemple, fournissez la bibliothèque de proxy qui a été créée (sample.dll) ainsi que les bibliothèques .NET connexes.</span><span class="sxs-lookup"><span data-stu-id="1db5c-139">To compile the sample, supply the proxy library that was created (sample.dll) and the related .NET libraries.</span></span> <span data-ttu-id="1db5c-140">Pour compiler la version Visual Basic .NET de l'exemple, stockée dans le fichier client.vb, écrivez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="1db5c-140">To compile the Visual Basic .NET version of the sample, stored in the file client.vb, issue the following command.</span></span>  
  
    ```console
    vbc client.vb -r:sample.dll -r:System.dll -r:System.Data.dll -r:System.Xml.dll -r:System.Web.Services.dll  
    ```  
  
     <span data-ttu-id="1db5c-141">Pour compiler la version C# de l'exemple, stockée dans le fichier client.cs, écrivez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="1db5c-141">To compile the C# version of the sample, stored in the file client.cs, issue the following command.</span></span>  
  
    ```console
    csc client.cs -r:sample.dll -r:System.dll -r:System.Data.dll -r:System.Xml.dll -r:System.Web.Services.dll  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="1db5c-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1db5c-142">See also</span></span>

- [<span data-ttu-id="1db5c-143">ADO.NET</span><span class="sxs-lookup"><span data-stu-id="1db5c-143">ADO.NET</span></span>](../../../../../docs/framework/data/adonet/index.md)
- [<span data-ttu-id="1db5c-144">DataSets, DataTables et DataViews</span><span class="sxs-lookup"><span data-stu-id="1db5c-144">DataSets, DataTables, and DataViews</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/index.md)
- [<span data-ttu-id="1db5c-145">DataTables</span><span class="sxs-lookup"><span data-stu-id="1db5c-145">DataTables</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/datatables.md)
- [<span data-ttu-id="1db5c-146">Remplissage d’un DataSet à partir d’un DataAdapter</span><span class="sxs-lookup"><span data-stu-id="1db5c-146">Populating a DataSet from a DataAdapter</span></span>](../../../../../docs/framework/data/adonet/populating-a-dataset-from-a-dataadapter.md)
- [<span data-ttu-id="1db5c-147">Mise à jour de sources de données avec des DataAdapters</span><span class="sxs-lookup"><span data-stu-id="1db5c-147">Updating Data Sources with DataAdapters</span></span>](../../../../../docs/framework/data/adonet/updating-data-sources-with-dataadapters.md)
- [<span data-ttu-id="1db5c-148">Paramètres DataAdapter</span><span class="sxs-lookup"><span data-stu-id="1db5c-148">DataAdapter Parameters</span></span>](../../../../../docs/framework/data/adonet/dataadapter-parameters.md)
- <span data-ttu-id="1db5c-149">[Outil Web Services Description Language Tool (Wsdl.exe)](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/7h3ystb6(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="1db5c-149">[Web Services Description Language Tool (Wsdl.exe)](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/7h3ystb6(v=vs.100))</span></span>
- [<span data-ttu-id="1db5c-150">Fournisseurs managés ADO.NET et centre de développement DataSet</span><span class="sxs-lookup"><span data-stu-id="1db5c-150">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
