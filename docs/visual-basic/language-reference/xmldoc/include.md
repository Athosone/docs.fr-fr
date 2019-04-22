---
title: <include> (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- include XML tag
- <include> XML tag
ms.assetid: ba8e9173-82cd-460b-8938-a075a2dfb36d
ms.openlocfilehash: d9c1c1a50f0e3530c842a6058e288b8d2be15f95
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58832539"
---
# <a name="include-visual-basic"></a><span data-ttu-id="a9cf1-102">\<Inclure > (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="a9cf1-102">\<include> (Visual Basic)</span></span>
<span data-ttu-id="a9cf1-103">Fait référence à un autre fichier qui décrit les types et membres dans votre code source.</span><span class="sxs-lookup"><span data-stu-id="a9cf1-103">Refers to another file that describes the types and members in your source code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a9cf1-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a9cf1-104">Syntax</span></span>  
  
```xml  
<include file="filename" path="tagpath[@name='id']" />  
```  
  
## <a name="parameters"></a><span data-ttu-id="a9cf1-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a9cf1-105">Parameters</span></span>  
 `filename`  
 <span data-ttu-id="a9cf1-106">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="a9cf1-106">Required.</span></span> <span data-ttu-id="a9cf1-107">Nom du fichier contenant la documentation.</span><span class="sxs-lookup"><span data-stu-id="a9cf1-107">The name of the file containing the documentation.</span></span> <span data-ttu-id="a9cf1-108">Le nom de fichier peut être qualifié avec un chemin.</span><span class="sxs-lookup"><span data-stu-id="a9cf1-108">The file name can be qualified with a path.</span></span> <span data-ttu-id="a9cf1-109">Placez `filename` dans des guillemets doubles ( » «).</span><span class="sxs-lookup"><span data-stu-id="a9cf1-109">Enclose `filename` in double quotation marks (" ").</span></span>  
  
 `tagpath`  
 <span data-ttu-id="a9cf1-110">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="a9cf1-110">Required.</span></span> <span data-ttu-id="a9cf1-111">Chemin des balises contenues dans `filename` qui mène à la balise `name`.</span><span class="sxs-lookup"><span data-stu-id="a9cf1-111">The path of the tags in `filename` that leads to the tag `name`.</span></span> <span data-ttu-id="a9cf1-112">Placez le chemin d’accès entre guillemets doubles ( » «).</span><span class="sxs-lookup"><span data-stu-id="a9cf1-112">Enclose the path in double quotation marks (" ").</span></span>  
  
 `name`  
 <span data-ttu-id="a9cf1-113">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="a9cf1-113">Required.</span></span> <span data-ttu-id="a9cf1-114">Le spécificateur de nom dans la balise qui précède les commentaires.</span><span class="sxs-lookup"><span data-stu-id="a9cf1-114">The name specifier in the tag that precedes the comments.</span></span> <span data-ttu-id="a9cf1-115">`Name` aura un `id`.</span><span class="sxs-lookup"><span data-stu-id="a9cf1-115">`Name` will have an `id`.</span></span>  
  
 `id`  
 <span data-ttu-id="a9cf1-116">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="a9cf1-116">Required.</span></span> <span data-ttu-id="a9cf1-117">ID de la balise qui précède les commentaires.</span><span class="sxs-lookup"><span data-stu-id="a9cf1-117">The ID for the tag that precedes the comments.</span></span> <span data-ttu-id="a9cf1-118">Mettez l’ID entre guillemets simples (' ').</span><span class="sxs-lookup"><span data-stu-id="a9cf1-118">Enclose the ID in single quotation marks (' ').</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="a9cf1-119">Notes</span><span class="sxs-lookup"><span data-stu-id="a9cf1-119">Remarks</span></span>  
 <span data-ttu-id="a9cf1-120">Utilisez le `<include>` balise pour faire référence à des commentaires dans un autre fichier qui décrivent les types et membres dans votre code source.</span><span class="sxs-lookup"><span data-stu-id="a9cf1-120">Use the `<include>` tag to refer to comments in another file that describe the types and members in your source code.</span></span> <span data-ttu-id="a9cf1-121">Il s’agit d’une solution alternative au placement direct des commentaires de la documentation dans votre fichier de code source.</span><span class="sxs-lookup"><span data-stu-id="a9cf1-121">This is an alternative to placing documentation comments directly in your source code file.</span></span>  
  
 <span data-ttu-id="a9cf1-122">Le `<include>` balise utilise la recommandation de la Version 1.0 W3C XML Path Language (XPath).</span><span class="sxs-lookup"><span data-stu-id="a9cf1-122">The `<include>` tag uses the W3C XML Path Language (XPath) Version 1.0 Recommendation.</span></span> <span data-ttu-id="a9cf1-123">Pour plus d’informations sur les façons de personnaliser votre `<include>` utiliser, consultez <https://www.w3.org/TR/xpath>.</span><span class="sxs-lookup"><span data-stu-id="a9cf1-123">For more information about ways to customize your `<include>` use, see <https://www.w3.org/TR/xpath>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="a9cf1-124">Exemple</span><span class="sxs-lookup"><span data-stu-id="a9cf1-124">Example</span></span>  
 <span data-ttu-id="a9cf1-125">Cet exemple utilise le `<include>` balise pour importer des commentaires de documentation de membre à partir d’un fichier appelé `commentFile.xml`.</span><span class="sxs-lookup"><span data-stu-id="a9cf1-125">This example uses the `<include>` tag to import member documentation comments from a file called `commentFile.xml`.</span></span>  
  
 [!code-vb[VbVbcnXmlDocComments#4](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnXmlDocComments/VB/Class1.vb#4)]  
  
 <span data-ttu-id="a9cf1-126">Le format de la `commentFile.xml` se présente comme suit.</span><span class="sxs-lookup"><span data-stu-id="a9cf1-126">The format of the `commentFile.xml` is as follows.</span></span>  
  
```xml  
<Docs>  
<Members name="Open">  
<summary>Opens a file.</summary>  
<param name="filename">File name to open.</param>  
</Members>  
<Members name="Close">  
<summary>Closes a file.</summary>  
<param name="filename">File name to close.</param>  
</Members>  
</Docs>  
```  
  
## <a name="see-also"></a><span data-ttu-id="a9cf1-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a9cf1-127">See also</span></span>

- [<span data-ttu-id="a9cf1-128">Étiquettes XML pour les commentaires</span><span class="sxs-lookup"><span data-stu-id="a9cf1-128">XML Comment Tags</span></span>](../../../visual-basic/language-reference/xmldoc/index.md)
