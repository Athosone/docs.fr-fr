---
title: Génération de classes de type de données à partir de XML
ms.date: 03/30/2017
ms.assetid: e4e5e4e8-527f-44d1-92fa-8904a08784ea
ms.openlocfilehash: c1b5dfda8aa5370dbc202ab90c75ab5677970467
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59309340"
---
# <a name="generating-data-type-classes-from-xml"></a><span data-ttu-id="eeb8b-102">Génération de classes de type de données à partir de XML</span><span class="sxs-lookup"><span data-stu-id="eeb8b-102">Generating Data Type Classes from XML</span></span>
[!INCLUDE[net_v45](../../../includes/net-v45-md.md)] <span data-ttu-id="eeb8b-103">inclut une nouvelle fonctionnalité pour générer les classes de type de données XML.</span><span class="sxs-lookup"><span data-stu-id="eeb8b-103">includes a new feature to generate data type classes from XML.</span></span> <span data-ttu-id="eeb8b-104">Cette rubrique décrit comment générer automatiquement des types de données pour les flux RSS du Blog .NET.</span><span class="sxs-lookup"><span data-stu-id="eeb8b-104">This topic describes how to automatically generate data types for the .NET Blog RSS feed.</span></span>  
  
### <a name="obtaining-the-xml-from-the-net-blog-rss-feed"></a><span data-ttu-id="eeb8b-105">Obtention du code XML à partir du RSS du Blog .NET de flux</span><span class="sxs-lookup"><span data-stu-id="eeb8b-105">Obtaining the XML from the .NET Blog RSS feed</span></span>  
  
1. <span data-ttu-id="eeb8b-106">Dans Internet Explorer, accédez à la [RSS du Blog .NET flux](https://devblogs.microsoft.com/dotnet/feed/).</span><span class="sxs-lookup"><span data-stu-id="eeb8b-106">In Internet Explorer, navigate to the [.NET Blog RSS feed](https://devblogs.microsoft.com/dotnet/feed/).</span></span>  
  
2. <span data-ttu-id="eeb8b-107">Cliquez sur la page et sélectionnez **afficher la Source**.</span><span class="sxs-lookup"><span data-stu-id="eeb8b-107">Right-click the page and select **View Source**.</span></span>  
  
3. <span data-ttu-id="eeb8b-108">Copiez le texte du flux en appuyant sur **Ctrl + A** pour sélectionner tout le texte, et **Ctrl + C** à copier.</span><span class="sxs-lookup"><span data-stu-id="eeb8b-108">Copy the text of the feed by pressing **Ctrl+A** to select all text, and **Ctrl+C** to copy.</span></span>  
  
### <a name="creating-the-data-types"></a><span data-ttu-id="eeb8b-109">Création des types de données</span><span class="sxs-lookup"><span data-stu-id="eeb8b-109">Creating the data types</span></span>  
  
1. <span data-ttu-id="eeb8b-110">Ouvrez un fichier de code où le proxy doit être utilisé.</span><span class="sxs-lookup"><span data-stu-id="eeb8b-110">Open a code file where the proxy is to be used.</span></span> <span data-ttu-id="eeb8b-111">Ce fichier doit faire partie d'un projet [!INCLUDE[net_v45](../../../includes/net-v45-md.md)].</span><span class="sxs-lookup"><span data-stu-id="eeb8b-111">This file should be part of a [!INCLUDE[net_v45](../../../includes/net-v45-md.md)] project.</span></span>  
  
2. <span data-ttu-id="eeb8b-112">Placez le curseur dans un emplacement du fichier à l'extérieur des classes existantes.</span><span class="sxs-lookup"><span data-stu-id="eeb8b-112">Place the cursor in a location in the file outside any existing classes.</span></span>  
  
3. <span data-ttu-id="eeb8b-113">Sélectionnez **modifier**, **Collage spécial**, **coller XML en tant que Classes**.</span><span class="sxs-lookup"><span data-stu-id="eeb8b-113">Select **Edit**, **Paste Special**, **Paste XML as Classes**.</span></span>  
  
4. <span data-ttu-id="eeb8b-114">Classes appelées `link`, `rss`, `rssChannel`, `rssChannelImage`, `rssChannelItem` et `rssChannelItemGuid` sont créés avec les membres nécessaires pour accéder aux éléments dans le flux RSS.</span><span class="sxs-lookup"><span data-stu-id="eeb8b-114">Classes called `link`, `rss`, `rssChannel`, `rssChannelImage`, `rssChannelItem` and `rssChannelItemGuid` are created with the necessary members for accessing the elements in the RSS feed.</span></span>  
  
### <a name="using-the-generated-classes"></a><span data-ttu-id="eeb8b-115">Utilisation des classes générées</span><span class="sxs-lookup"><span data-stu-id="eeb8b-115">Using the generated classes</span></span>  
  
1. <span data-ttu-id="eeb8b-116">Une fois les classes générées, elles peuvent être utilisées dans le code comme toute autre classe.</span><span class="sxs-lookup"><span data-stu-id="eeb8b-116">Once the classes are generated, they can be used in code like any other classes.</span></span> <span data-ttu-id="eeb8b-117">L'exemple suivant retourne une nouvelle instance de la classe `rssChannelImage`.</span><span class="sxs-lookup"><span data-stu-id="eeb8b-117">The following code example returns a new instance of the `rssChannelImage` class.</span></span>  
  
    ```  
    var channelImage = new rssChannelImage()   
    {   
        title = "MyImage",   
        link = "http://www.contoso.com/images/channelImage.jpg",   
        url = "http://www.contoso.com/entries/myEntry.html"   
    };  
    ```
