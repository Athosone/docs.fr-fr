---
title: Ordre de sérialisation personnalisé avec XmlSerializer
ms.date: 03/30/2017
ms.assetid: 975abd20-2a1d-42db-aed3-e898025ccce7
ms.openlocfilehash: f63d460163c33c4253cf565a5755babc1030164f
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61776075"
---
# <a name="custom-serialization-order-with-xmlserializer"></a><span data-ttu-id="71604-102">Ordre de sérialisation personnalisé avec XmlSerializer</span><span class="sxs-lookup"><span data-stu-id="71604-102">Custom Serialization Order With XmlSerializer</span></span>
[<span data-ttu-id="71604-103">Télécharger l’exemple</span><span class="sxs-lookup"><span data-stu-id="71604-103">Download Sample</span></span>](https://download.microsoft.com/download/4/7/B/47B2164C-E780-4B10-8DE4-2CB5B886E0A6/Technologies/Serialization/Xml%20Serialization/CustomOrder.zip.exe)  
  
 <span data-ttu-id="71604-104">Cet exemple montre comment contrôler l'ordre des éléments sérialisés et désérialisés pour la sérialisation XML.</span><span class="sxs-lookup"><span data-stu-id="71604-104">This sample shows how to control the order of serialized and deserialized elements for XML serialization.</span></span>  
  
 <span data-ttu-id="71604-105">Pour plus d'informations sur la sérialisation, consultez les commentaires inclus dans les fichiers de code source et dans les fichiers build-proj.</span><span class="sxs-lookup"><span data-stu-id="71604-105">Review comments in the source code and build.proj files for more information on serialization.</span></span>  
  
### <a name="to-build-the-sample-using-the-command-prompt"></a><span data-ttu-id="71604-106">Pour générer l'exemple à partir de l'invite de commandes</span><span class="sxs-lookup"><span data-stu-id="71604-106">To build the sample using the Command Prompt</span></span>  
  
1. <span data-ttu-id="71604-107">Ouvrez la fenêtre d'invite de commandes et accédez à l'un des sous-répertoires spécifiques aux différents langages pour l'exemple.</span><span class="sxs-lookup"><span data-stu-id="71604-107">Open the Command Prompt window and navigate to one of the language-specific subdirectories for the sample.</span></span>  
  
2. <span data-ttu-id="71604-108">Tapez **msbuild CustomOrder.sln** sur la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="71604-108">Type **msbuild CustomOrder.sln** at the command line.</span></span>  
  
### <a name="to-build-the-sample-using-visual-studio"></a><span data-ttu-id="71604-109">Pour générer l'exemple à l'aide de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="71604-109">To build the sample using Visual Studio</span></span>  
  
1. <span data-ttu-id="71604-110">Ouvrez l'[!INCLUDE[fileExplorer](../../../includes/fileexplorer-md.md)] et accédez à l'un des sous-répertoires spécifiques aux différents langages de l'exemple.</span><span class="sxs-lookup"><span data-stu-id="71604-110">Open [!INCLUDE[fileExplorer](../../../includes/fileexplorer-md.md)] and navigate to one of the language-specific subdirectories for the sample.</span></span>  
  
2. <span data-ttu-id="71604-111">Double-cliquez sur l'icône de CustomOrder.sln pour ouvrir le fichier dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="71604-111">Double-click the icon for the CustomOrder.sln to open the file in Visual Studio.</span></span>  
  
3. <span data-ttu-id="71604-112">Dans le menu **Générer**, sélectionnez **Générer la solution**.</span><span class="sxs-lookup"><span data-stu-id="71604-112">In the **Build** menu, select **Build Solution**.</span></span>  
  
4. <span data-ttu-id="71604-113">L'exemple d'application est généré dans le sous-répertoire \bin ou \bin\Debug par défaut.</span><span class="sxs-lookup"><span data-stu-id="71604-113">The sample application is built in the default \bin or \bin\Debug subdirectory.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="71604-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="71604-114">See also</span></span>

- [<span data-ttu-id="71604-115">Sérialisation de base</span><span class="sxs-lookup"><span data-stu-id="71604-115">Basic Serialization</span></span>](../../../docs/standard/serialization/basic-serialization.md)
- [<span data-ttu-id="71604-116">Sérialisation binaire</span><span class="sxs-lookup"><span data-stu-id="71604-116">Binary Serialization</span></span>](../../../docs/standard/serialization/binary-serialization.md)
- [<span data-ttu-id="71604-117">Contrôle de la sérialisation XML à l’aide d’attributs</span><span class="sxs-lookup"><span data-stu-id="71604-117">Controlling XML Serialization Using Attributes</span></span>](../../../docs/standard/serialization/controlling-xml-serialization-using-attributes.md)
- [<span data-ttu-id="71604-118">Introduction à la sérialisation XML</span><span class="sxs-lookup"><span data-stu-id="71604-118">Introducing XML Serialization</span></span>](../../../docs/standard/serialization/introducing-xml-serialization.md)
- [<span data-ttu-id="71604-119">Sérialisation</span><span class="sxs-lookup"><span data-stu-id="71604-119">Serialization</span></span>](../../../docs/standard/serialization/index.md)
- [<span data-ttu-id="71604-120">Sérialisation XML et SOAP</span><span class="sxs-lookup"><span data-stu-id="71604-120">XML and SOAP Serialization</span></span>](../../../docs/standard/serialization/xml-and-soap-serialization.md)
