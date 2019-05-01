---
title: SchemaImporterExtension, exemple de technologie
ms.date: 03/30/2017
ms.assetid: 3f5eb78f-0ef6-433a-b095-3a63b1ce0bc9
ms.openlocfilehash: 5027897bcf62e52dae5aab6090c01518a92636dc
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62028302"
---
# <a name="schemaimporterextension-technology-sample"></a><span data-ttu-id="7db77-102">SchemaImporterExtension, exemple de technologie</span><span class="sxs-lookup"><span data-stu-id="7db77-102">SchemaImporterExtension Technology Sample</span></span>
[<span data-ttu-id="7db77-103">Télécharger l’exemple</span><span class="sxs-lookup"><span data-stu-id="7db77-103">Download Sample</span></span>](https://download.microsoft.com/download/4/7/B/47B2164C-E780-4B10-8DE4-2CB5B886E0A6/Technologies/Serialization/Xml%20Serialization/SchemaImporterExtension.zip.exe)  
  
 <span data-ttu-id="7db77-104">Cet exemple illustre un <xref:System.Xml.Serialization.Advanced.SchemaImporterExtension> personnalisé qui permet de mieux contrôler la génération du code lors de l'importation d'un schéma XML.</span><span class="sxs-lookup"><span data-stu-id="7db77-104">This sample demonstrates a custom <xref:System.Xml.Serialization.Advanced.SchemaImporterExtension> that allows fine control over code generation when an XML schema is imported.</span></span> <span data-ttu-id="7db77-105">L'application illustre la procédure de génération, d'inscription et d'appel de cette extension.</span><span class="sxs-lookup"><span data-stu-id="7db77-105">The application shows how to build, register and invoke this extension.</span></span>  
  
### <a name="to-build-the-sample-using-the-command-prompt"></a><span data-ttu-id="7db77-106">Pour générer l'exemple à partir de l'invite de commandes :</span><span class="sxs-lookup"><span data-stu-id="7db77-106">To build the sample using the command prompt</span></span>  
  
1. <span data-ttu-id="7db77-107">Ouvrez une fenêtre d'invite de commandes et accédez à l'un des sous-répertoires spécifiques aux différents langages pour l'exemple.</span><span class="sxs-lookup"><span data-stu-id="7db77-107">Open a Command Prompt window and navigate to one of the language-specific subdirectories for the sample.</span></span>  
  
2. <span data-ttu-id="7db77-108">Tapez **msbuild.exe OrderSchemaImporterExtension.sln** à la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="7db77-108">Type **msbuild.exe OrderSchemaImporterExtension.sln** at the command line.</span></span>  
  
### <a name="to-build-the-sample-using-visual-studio"></a><span data-ttu-id="7db77-109">Pour générer l'exemple à l'aide de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="7db77-109">To build the sample using Visual Studio</span></span>  
  
1. <span data-ttu-id="7db77-110">Ouvrez l'[!INCLUDE[fileExplorer](../../../includes/fileexplorer-md.md)] et accédez à l'un des sous-répertoires spécifiques aux différents langages de l'exemple.</span><span class="sxs-lookup"><span data-stu-id="7db77-110">Open [!INCLUDE[fileExplorer](../../../includes/fileexplorer-md.md)] and navigate to one of the language-specific subdirectories for the sample.</span></span>  
  
2. <span data-ttu-id="7db77-111">Double-cliquez sur l'icône d'OrderSchemaImporterExtension.sln pour ouvrir le fichier dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="7db77-111">Double-click the icon for OrderSchemaImporterExtension.sln to open the file in Visual Studio.</span></span>  
  
3. <span data-ttu-id="7db77-112">Dans le menu **Générer** , cliquez sur **Générer la solution**.</span><span class="sxs-lookup"><span data-stu-id="7db77-112">On the **Build** menu, click **Build Solution**.</span></span>  
  
 <span data-ttu-id="7db77-113">L'application sera générée dans le répertoire \bin ou \bin\Debug par défaut.</span><span class="sxs-lookup"><span data-stu-id="7db77-113">The application will be built in the default \bin or \bin\Debug directory.</span></span>  
  
### <a name="to-run-the-sample"></a><span data-ttu-id="7db77-114">Pour exécuter l'exemple</span><span class="sxs-lookup"><span data-stu-id="7db77-114">To run the sample</span></span>  
  
1. <span data-ttu-id="7db77-115">Accédez au répertoire qui contient le nouveau fichier exécutable, à l'aide de l'invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="7db77-115">Navigate to the directory containing the new executable, using the command prompt.</span></span>  
  
2. <span data-ttu-id="7db77-116">Tapez **[nom exe]** à la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="7db77-116">Type **[exe name]** at the command line.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="7db77-117">Notes</span><span class="sxs-lookup"><span data-stu-id="7db77-117">Remarks</span></span>  
 <span data-ttu-id="7db77-118">Pour plus d'informations sur les étapes de création et d'inscription d'exemples de fichiers binaires, consultez les commentaires figurant dans le code source et dans les fichiers build.proj.</span><span class="sxs-lookup"><span data-stu-id="7db77-118">For more information about sample binary creation and registration steps, see the comments in the source code and build.proj files.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7db77-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7db77-119">See also</span></span>

- <xref:System.CodeDom.CodeCompileUnit>
- <xref:System.CodeDom.CodeNamespace>
- <xref:System.CodeDom.CodeNamespaceImport>
- <xref:Microsoft.CSharp.CSharpCodeProvider>
- <xref:System.Xml.Serialization.IXmlSerializable>
- <xref:System.Xml.Serialization.Advanced.SchemaImporterExtension>
- <xref:System.CodeDom>
- <xref:System.CodeDom.Compiler>
- <xref:System.Web.Services.Description>
- <xref:System.Web.Services.Discovery>
- <xref:System.Xml.Serialization>
- <xref:System.Uri>
- <xref:Microsoft.VisualBasic.VBCodeProvider>
- <xref:System.Web.Services.Description.WebReference>
- <xref:System.Xml.Serialization.XmlSchemaImporter>
