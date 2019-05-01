---
title: Valeurs des variables objets (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- object variables [Visual Basic], values
- values [Visual Basic], of object variables
- data types [Visual Basic], object variable
- variables [Visual Basic], object
ms.assetid: 31555704-58a3-49f1-9a0a-6421f605664f
ms.openlocfilehash: c17c5f85952596f0a080ca473e8f792740e66b8f
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62054183"
---
# <a name="object-variable-values-visual-basic"></a><span data-ttu-id="b4cff-102">Valeurs des variables objets (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="b4cff-102">Object Variable Values (Visual Basic)</span></span>
<span data-ttu-id="b4cff-103">Une variable de la [Object Data Type](../../../../visual-basic/language-reference/data-types/object-data-type.md) peuvent faire référence à des données de n’importe quel type.</span><span class="sxs-lookup"><span data-stu-id="b4cff-103">A variable of the [Object Data Type](../../../../visual-basic/language-reference/data-types/object-data-type.md) can refer to data of any type.</span></span> <span data-ttu-id="b4cff-104">La valeur que vous stockez dans un `Object` variable est conservée ailleurs en mémoire, tandis que la variable contient un pointeur vers les données.</span><span class="sxs-lookup"><span data-stu-id="b4cff-104">The value you store in an `Object` variable is kept elsewhere in memory, while the variable itself holds a pointer to the data.</span></span>  
  
## <a name="object-classifier-functions"></a><span data-ttu-id="b4cff-105">Fonctions classifieur d’objets</span><span class="sxs-lookup"><span data-stu-id="b4cff-105">Object Classifier Functions</span></span>  
 <span data-ttu-id="b4cff-106">Visual Basic fournit des fonctions qui retournent des informations sur ce qu’un `Object` variable fait référence, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="b4cff-106">Visual Basic supplies functions that return information about what an `Object` variable refers to, as shown in the following table.</span></span>  
  
|<span data-ttu-id="b4cff-107">Fonction</span><span class="sxs-lookup"><span data-stu-id="b4cff-107">Function</span></span>|<span data-ttu-id="b4cff-108">Retourne la valeur True si la variable objet fait référence à</span><span class="sxs-lookup"><span data-stu-id="b4cff-108">Returns True if the Object variable refers to</span></span>|  
|--------------|---------------------------------------------------|  
|<xref:Microsoft.VisualBasic.Information.IsArray%2A>|<span data-ttu-id="b4cff-109">Un tableau de valeurs, plutôt qu’une seule valeur</span><span class="sxs-lookup"><span data-stu-id="b4cff-109">An array of values, rather than a single value</span></span>|  
|<xref:Microsoft.VisualBasic.Information.IsDate%2A>|<span data-ttu-id="b4cff-110">Un [Type de données Date](../../../../visual-basic/language-reference/data-types/date-data-type.md) valeur, ou une chaîne qui peut être interprétée comme une valeur de date et d’heure</span><span class="sxs-lookup"><span data-stu-id="b4cff-110">A [Date Data Type](../../../../visual-basic/language-reference/data-types/date-data-type.md) value, or a string that can be interpreted as a date and time value</span></span>|  
|<xref:Microsoft.VisualBasic.Information.IsDBNull%2A>|<span data-ttu-id="b4cff-111">Un objet de type <xref:System.DBNull>, qui représente les données manquantes ou inexistantes</span><span class="sxs-lookup"><span data-stu-id="b4cff-111">An object of type <xref:System.DBNull>, which represents missing or nonexistent data</span></span>|  
|<xref:Microsoft.VisualBasic.Information.IsError%2A>|<span data-ttu-id="b4cff-112">Un objet d’exception qui dérive de <xref:System.Exception></span><span class="sxs-lookup"><span data-stu-id="b4cff-112">An exception object, which derives from <xref:System.Exception></span></span>|  
|<xref:Microsoft.VisualBasic.Information.IsNothing%2A>|<span data-ttu-id="b4cff-113">[Nothing](../../../../visual-basic/language-reference/nothing.md), autrement dit, aucun objet n’est actuellement assigné à la variable</span><span class="sxs-lookup"><span data-stu-id="b4cff-113">[Nothing](../../../../visual-basic/language-reference/nothing.md), that is, no object is currently assigned to the variable</span></span>|  
|<xref:Microsoft.VisualBasic.Information.IsNumeric%2A>|<span data-ttu-id="b4cff-114">Un nombre ou une chaîne qui peut être interprétée comme un nombre</span><span class="sxs-lookup"><span data-stu-id="b4cff-114">A number, or a string that can be interpreted as a number</span></span>|  
|<xref:Microsoft.VisualBasic.Information.IsReference%2A>|<span data-ttu-id="b4cff-115">Un type référence (par exemple, une chaîne, un tableau, un délégué ou un type de classe)</span><span class="sxs-lookup"><span data-stu-id="b4cff-115">A reference type (such as a string, array, delegate, or class type)</span></span>|  
  
 <span data-ttu-id="b4cff-116">Vous pouvez utiliser ces fonctions pour éviter de soumettre une valeur non valide à une opération ou une procédure.</span><span class="sxs-lookup"><span data-stu-id="b4cff-116">You can use these functions to avoid submitting an invalid value to an operation or a procedure.</span></span>  
  
## <a name="typeof-operator"></a><span data-ttu-id="b4cff-117">TypeOf, opérateur</span><span class="sxs-lookup"><span data-stu-id="b4cff-117">TypeOf Operator</span></span>  
 <span data-ttu-id="b4cff-118">Vous pouvez également utiliser le [TypeOf, opérateur](../../../../visual-basic/language-reference/operators/typeof-operator.md) pour déterminer si une variable objet fait actuellement référence à un type de données spécifique.</span><span class="sxs-lookup"><span data-stu-id="b4cff-118">You can also use the [TypeOf Operator](../../../../visual-basic/language-reference/operators/typeof-operator.md) to determine whether an object variable currently refers to a specific data type.</span></span> <span data-ttu-id="b4cff-119">Le `TypeOf`... `Is` expression prend la valeur `True` si le type au moment de l’exécution de l’opérande est dérivé ou implémente le type spécifié.</span><span class="sxs-lookup"><span data-stu-id="b4cff-119">The `TypeOf`...`Is` expression evaluates to `True` if the run-time type of the operand is derived from or implements the specified type.</span></span>  
  
 <span data-ttu-id="b4cff-120">L’exemple suivant utilise `TypeOf` variables objets faisant référence à des types valeur et référence.</span><span class="sxs-lookup"><span data-stu-id="b4cff-120">The following example uses `TypeOf` on object variables referring to value and reference types.</span></span>  
  
```  
' The following statement puts a value type (Integer) in an Object variable.  
Dim num As Object = 10  
' The following statement puts a reference type (Form) in an Object variable.  
Dim frm As Object = New Form()  
If TypeOf num Is Long Then Debug.WriteLine("num is Long")  
If TypeOf num Is Integer Then Debug.WriteLine("num is Integer")  
If TypeOf num Is Short Then Debug.WriteLine("num is Short")  
If TypeOf num Is Object Then Debug.WriteLine("num is Object")  
If TypeOf frm Is Form Then Debug.WriteLine("frm is Form")  
If TypeOf frm Is Label Then Debug.WriteLine("frm is Label")  
If TypeOf frm Is Object Then Debug.WriteLine("frm is Object")  
```  
  
 <span data-ttu-id="b4cff-121">L’exemple précédent écrit les lignes suivantes à la **déboguer** fenêtre :</span><span class="sxs-lookup"><span data-stu-id="b4cff-121">The preceding example writes the following lines to the **Debug** window:</span></span>  
  
 `num is Integer`  
  
 `num is Object`  
  
 `frm is Form`  
  
 `frm is Object`  
  
 <span data-ttu-id="b4cff-122">La variable objet `num` fait référence aux données de type `Integer`, et `frm` fait référence à un objet de classe <xref:System.Windows.Forms.Form>.</span><span class="sxs-lookup"><span data-stu-id="b4cff-122">The object variable `num` refers to data of type `Integer`, and `frm` refers to an object of class <xref:System.Windows.Forms.Form>.</span></span>  
  
## <a name="object-arrays"></a><span data-ttu-id="b4cff-123">Tableaux d’objets</span><span class="sxs-lookup"><span data-stu-id="b4cff-123">Object Arrays</span></span>  
 <span data-ttu-id="b4cff-124">Vous pouvez déclarer et utiliser un tableau de `Object` variables.</span><span class="sxs-lookup"><span data-stu-id="b4cff-124">You can declare and use an array of `Object` variables.</span></span> <span data-ttu-id="b4cff-125">Cela est utile lorsque vous avez besoin gérer une variété de types de données et des classes d’objets.</span><span class="sxs-lookup"><span data-stu-id="b4cff-125">This is useful when you need to handle a variety of data types and object classes.</span></span> <span data-ttu-id="b4cff-126">Tous les éléments dans un tableau doivent avoir les mêmes données déclarées de type.</span><span class="sxs-lookup"><span data-stu-id="b4cff-126">All the elements in an array must have the same declared data type.</span></span> <span data-ttu-id="b4cff-127">Déclaration de ce type de données en tant que `Object` vous permet de stocker des objets et instances en même temps que d’autres types de données dans le tableau de la classe.</span><span class="sxs-lookup"><span data-stu-id="b4cff-127">Declaring this data type as `Object` allows you to store objects and class instances alongside other data types in the array.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b4cff-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b4cff-128">See also</span></span>

- [<span data-ttu-id="b4cff-129">Variables objets</span><span class="sxs-lookup"><span data-stu-id="b4cff-129">Object Variables</span></span>](../../../../visual-basic/programming-guide/language-features/variables/object-variables.md)
- [<span data-ttu-id="b4cff-130">Déclaration des variables objets</span><span class="sxs-lookup"><span data-stu-id="b4cff-130">Object Variable Declaration</span></span>](../../../../visual-basic/programming-guide/language-features/variables/object-variable-declaration.md)
- [<span data-ttu-id="b4cff-131">Assignation des variables objets</span><span class="sxs-lookup"><span data-stu-id="b4cff-131">Object Variable Assignment</span></span>](../../../../visual-basic/programming-guide/language-features/variables/object-variable-assignment.md)
- [<span data-ttu-id="b4cff-132">Guide pratique pour Reportez-vous à l’Instance actuelle d’un objet</span><span class="sxs-lookup"><span data-stu-id="b4cff-132">How to: Refer to the Current Instance of an Object</span></span>](../../../../visual-basic/programming-guide/language-features/variables/how-to-refer-to-the-current-instance-of-an-object.md)
- [<span data-ttu-id="b4cff-133">Guide pratique pour Déterminer le Type désigné par une Variable objet</span><span class="sxs-lookup"><span data-stu-id="b4cff-133">How to: Determine What Type an Object Variable Refers To</span></span>](../../../../visual-basic/programming-guide/language-features/variables/how-to-determine-what-type-an-object-variable-refers-to.md)
- [<span data-ttu-id="b4cff-134">Guide pratique pour Déterminer si deux objets sont liés</span><span class="sxs-lookup"><span data-stu-id="b4cff-134">How to: Determine Whether Two Objects Are Related</span></span>](../../../../visual-basic/programming-guide/language-features/variables/how-to-determine-whether-two-objects-are-related.md)
- [<span data-ttu-id="b4cff-135">Guide pratique pour Déterminer si deux objets sont identiques</span><span class="sxs-lookup"><span data-stu-id="b4cff-135">How to: Determine Whether Two Objects Are Identical</span></span>](../../../../visual-basic/programming-guide/language-features/variables/how-to-determine-whether-two-objects-are-identical.md)
- [<span data-ttu-id="b4cff-136">Types de données</span><span class="sxs-lookup"><span data-stu-id="b4cff-136">Data Types</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/index.md)
