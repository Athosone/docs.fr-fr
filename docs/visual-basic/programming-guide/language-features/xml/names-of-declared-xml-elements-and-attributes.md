---
title: Nom des attributs et des éléments XML déclarés (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- declarations [XML in Visual Basic]
- element names [XML in Visual Basic]
- names in XML literals [Visual Basic]
- attribute names [XML in Visual Basic]
- XML literals [Visual Basic], element names
ms.assetid: cc110118-b6cf-4ff9-a4e4-6233c90c9fbf
ms.openlocfilehash: 2221f2677183cf360fa82a4d73a679a8b68927d1
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61761700"
---
# <a name="names-of-declared-xml-elements-and-attributes-visual-basic"></a><span data-ttu-id="6a0ff-102">Nom des attributs et des éléments XML déclarés (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="6a0ff-102">Names of Declared XML Elements and Attributes (Visual Basic)</span></span>
<span data-ttu-id="6a0ff-103">Cette rubrique fournit des instructions de Visual Basic pour nommer les éléments XML et les attributs dans les littéraux XML.</span><span class="sxs-lookup"><span data-stu-id="6a0ff-103">This topic provides Visual Basic guidelines for naming XML elements and attributes in XML literals.</span></span>  <span data-ttu-id="6a0ff-104">Dans un littéral XML, vous pouvez spécifier un nom local ou un nom qualifié.</span><span class="sxs-lookup"><span data-stu-id="6a0ff-104">In an XML literal, you can specify a local name or a qualified name.</span></span> <span data-ttu-id="6a0ff-105">Un nom qualifié se compose d’un préfixe d’espace de noms XML, un signe deux-points et un nom local.</span><span class="sxs-lookup"><span data-stu-id="6a0ff-105">A qualified name consists of an XML namespace prefix, a colon, and a local name.</span></span> <span data-ttu-id="6a0ff-106">Pour plus d’informations sur les préfixes d’espace de noms XML, consultez [XML élément littéral](../../../../visual-basic/language-reference/xml-literals/xml-element-literal.md).</span><span class="sxs-lookup"><span data-stu-id="6a0ff-106">For more information about XML namespace prefixes, see [XML Element Literal](../../../../visual-basic/language-reference/xml-literals/xml-element-literal.md).</span></span>  
  
## <a name="rules"></a><span data-ttu-id="6a0ff-107">Règles</span><span class="sxs-lookup"><span data-stu-id="6a0ff-107">Rules</span></span>  
 <span data-ttu-id="6a0ff-108">Un nom local d’un élément ou attribut en Visual Basic doit respecter les règles suivantes.</span><span class="sxs-lookup"><span data-stu-id="6a0ff-108">A local name of an element or attribute in Visual Basic must adhere to the following rules.</span></span>  
  
- <span data-ttu-id="6a0ff-109">Il peut commencer par un espace de noms.</span><span class="sxs-lookup"><span data-stu-id="6a0ff-109">It can begin with a namespace.</span></span> <span data-ttu-id="6a0ff-110">Il doit commencer par un caractère alphabétique ou un trait de soulignement (`_`).</span><span class="sxs-lookup"><span data-stu-id="6a0ff-110">It must begin with an alphabetical character or an underscore (`_`).</span></span>  
  
- <span data-ttu-id="6a0ff-111">Il doit contenir uniquement des caractères alphabétiques, des chiffres décimaux, des traits de soulignement, points (.) et des traits d’union (-).</span><span class="sxs-lookup"><span data-stu-id="6a0ff-111">It must contain only alphabetical characters, decimal digits, underscores, periods (.), and hyphens (-).</span></span>  
  
- <span data-ttu-id="6a0ff-112">Il ne doit pas être plus de 1 024 caractères.</span><span class="sxs-lookup"><span data-stu-id="6a0ff-112">It must not be more than 1,024 characters long.</span></span>  
  
- <span data-ttu-id="6a0ff-113">Signes deux-points qui apparaissent dans les noms indiquent la délimitation de l’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="6a0ff-113">Colons that appear in names indicate namespace demarcation.</span></span> <span data-ttu-id="6a0ff-114">Par conséquent, vous pouvez utiliser des signes deux-points uniquement pour spécifier un espace de noms XML pour un nom particulier.</span><span class="sxs-lookup"><span data-stu-id="6a0ff-114">Therefore, you can use colons only to specify an XML namespace for a particular name.</span></span>  
  
 <span data-ttu-id="6a0ff-115">En outre, vous devez respecter les recommandations ci-après.</span><span class="sxs-lookup"><span data-stu-id="6a0ff-115">In addition, you should adhere to the following guideline.</span></span>  
  
- <span data-ttu-id="6a0ff-116">La spécification XML 1.0 réserve tous les noms commençant par la chaîne « xml » de toute variation de la mise en majuscules.</span><span class="sxs-lookup"><span data-stu-id="6a0ff-116">The XML 1.0 specification reserves all names starting with the string "xml", of any capitalization variation.</span></span> <span data-ttu-id="6a0ff-117">Par conséquent, n’utilisez pas ces noms pour votre élément et les noms d’attributs.</span><span class="sxs-lookup"><span data-stu-id="6a0ff-117">Therefore, do not use those names for your element and attribute names.</span></span>  
  
### <a name="name-length-guidelines"></a><span data-ttu-id="6a0ff-118">Instructions de longueur de nom</span><span class="sxs-lookup"><span data-stu-id="6a0ff-118">Name Length Guidelines</span></span>  
 <span data-ttu-id="6a0ff-119">Dans la pratique, un nom doit être aussi court que possible tout en identifiant clairement la nature de l’élément.</span><span class="sxs-lookup"><span data-stu-id="6a0ff-119">As a practical matter, a name should be as short as possible while still clearly identifying the nature of the element.</span></span> <span data-ttu-id="6a0ff-120">Cela améliore la lisibilité de votre code et réduit la taille de ligne de longueur et le fichier source.</span><span class="sxs-lookup"><span data-stu-id="6a0ff-120">This improves the readability of your code and reduces line length and source-file size.</span></span>  
  
 <span data-ttu-id="6a0ff-121">Toutefois, votre nom ne doit pas être si court que ne pas correctement décrit l’élément ou la façon dont votre code utilise.</span><span class="sxs-lookup"><span data-stu-id="6a0ff-121">However, your name should not be so short that it does not adequately describe the element or how your code uses it.</span></span> <span data-ttu-id="6a0ff-122">Ceci est important pour la lisibilité de votre code.</span><span class="sxs-lookup"><span data-stu-id="6a0ff-122">This is important for the readability of your code.</span></span> <span data-ttu-id="6a0ff-123">Si quelqu'un d’autre tente de le comprendre, ou si vous avez vous-même l’observer beaucoup de temps après que l’avoir écrit, noms d’éléments appropriés peuvent gagner du temps.</span><span class="sxs-lookup"><span data-stu-id="6a0ff-123">If somebody else is trying to understand it, or if you yourself are looking at it a long time after you wrote it, appropriate element names can save time.</span></span>  
  
## <a name="case-sensitivity-in-names"></a><span data-ttu-id="6a0ff-124">Respecte la casse dans les noms</span><span class="sxs-lookup"><span data-stu-id="6a0ff-124">Case Sensitivity in Names</span></span>  
 <span data-ttu-id="6a0ff-125">Noms d’élément XML respectent la casse.</span><span class="sxs-lookup"><span data-stu-id="6a0ff-125">XML element names are case sensitive.</span></span> <span data-ttu-id="6a0ff-126">Cela signifie que lorsque le compilateur Visual Basic compare deux noms qui diffèrent uniquement par la casse des lettres, il les interprète comme des noms différents.</span><span class="sxs-lookup"><span data-stu-id="6a0ff-126">This means that when the Visual Basic compiler compares two names that differ in alphabetical case only, it interprets them as different names.</span></span> <span data-ttu-id="6a0ff-127">Par exemple, il interprète `ABC` et `abc` en tant que deux éléments distincts.</span><span class="sxs-lookup"><span data-stu-id="6a0ff-127">For example, it interprets `ABC` and `abc` as referring to separate elements.</span></span>  
  
## <a name="xml-namespaces"></a><span data-ttu-id="6a0ff-128">Espaces de noms XML</span><span class="sxs-lookup"><span data-stu-id="6a0ff-128">XML Namespaces</span></span>  
 <span data-ttu-id="6a0ff-129">Lorsque vous créez un élément XML littérale, vous pouvez spécifier le préfixe d’espace de noms XML pour le nom d’élément.</span><span class="sxs-lookup"><span data-stu-id="6a0ff-129">When creating an XML element literal, you can specify the XML namespace prefix for the element name.</span></span> <span data-ttu-id="6a0ff-130">Pour plus d’informations, consultez [XML élément littéral](../../../../visual-basic/language-reference/xml-literals/xml-element-literal.md).</span><span class="sxs-lookup"><span data-stu-id="6a0ff-130">For more information, see [XML Element Literal](../../../../visual-basic/language-reference/xml-literals/xml-element-literal.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6a0ff-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6a0ff-131">See also</span></span>

- [<span data-ttu-id="6a0ff-132">Création de code XML dans Visual Basic</span><span class="sxs-lookup"><span data-stu-id="6a0ff-132">Creating XML in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/xml/creating-xml.md)
- [<span data-ttu-id="6a0ff-133">Littéral d’élément XML</span><span class="sxs-lookup"><span data-stu-id="6a0ff-133">XML Element Literal</span></span>](../../../../visual-basic/language-reference/xml-literals/xml-element-literal.md)
