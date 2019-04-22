---
title: La variable '<variablename>' est utilisée avant qu'une valeur ne lui ait été assignée
ms.date: 07/20/2015
f1_keywords:
- vbc42104
- BC42104
helpviewer_keywords:
- BC42104
ms.assetid: 6909aa0b-b4a1-46f5-a18c-ba3e565c1dd8
ms.openlocfilehash: 46551a917aeb794c8d35985076b67a315386f628
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58819357"
---
# <a name="variable-variablename-is-used-before-it-has-been-assigned-a-value"></a><span data-ttu-id="438e4-102">Variable '\<nom_variable >' est utilisée avant qu’il a reçu une valeur</span><span class="sxs-lookup"><span data-stu-id="438e4-102">Variable '\<variablename>' is used before it has been assigned a value</span></span>
<span data-ttu-id="438e4-103">Variable '\<nom_variable >' est utilisée avant une valeur lui ait été assignée.</span><span class="sxs-lookup"><span data-stu-id="438e4-103">Variable '\<variablename>' is used before it has been assigned a value.</span></span> <span data-ttu-id="438e4-104">Cela peut provoquer une exception de référence null au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="438e4-104">A null reference exception could result at run time.</span></span>  
  
 <span data-ttu-id="438e4-105">Une application a au moins un chemin d’accès possible via son code qui lit une variable avant toute valeur est attribuée à ce dernier.</span><span class="sxs-lookup"><span data-stu-id="438e4-105">An application has at least one possible path through its code that reads a variable before any value is assigned to it.</span></span>  
  
 <span data-ttu-id="438e4-106">Si aucune valeur n’a jamais été assignée à une variable, elle contient la valeur par défaut de son type de données.</span><span class="sxs-lookup"><span data-stu-id="438e4-106">If a variable has never been assigned a value, it holds the default value for its data type.</span></span> <span data-ttu-id="438e4-107">Pour un type de données de référence, cette valeur par défaut est [Nothing](../../../visual-basic/language-reference/nothing.md).</span><span class="sxs-lookup"><span data-stu-id="438e4-107">For a reference data type, that default value is [Nothing](../../../visual-basic/language-reference/nothing.md).</span></span> <span data-ttu-id="438e4-108">La lecture d’une variable de référence qui a la valeur `Nothing` peut provoquer une <xref:System.NullReferenceException> dans certaines circonstances.</span><span class="sxs-lookup"><span data-stu-id="438e4-108">Reading a reference variable that has a value of `Nothing` can cause a <xref:System.NullReferenceException> in some circumstances.</span></span>  
  
 <span data-ttu-id="438e4-109">Par défaut, ce message est un avertissement.</span><span class="sxs-lookup"><span data-stu-id="438e4-109">By default, this message is a warning.</span></span> <span data-ttu-id="438e4-110">Pour plus d’informations sur le masquage des avertissements ou le traitement des avertissements en tant qu’erreurs, consultez [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).</span><span class="sxs-lookup"><span data-stu-id="438e4-110">For more information on hiding warnings or treating warnings as errors, see [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).</span></span>  
  
 <span data-ttu-id="438e4-111">**ID d’erreur :** BC42104</span><span class="sxs-lookup"><span data-stu-id="438e4-111">**Error ID:** BC42104</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="438e4-112">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="438e4-112">To correct this error</span></span>  
  
-   <span data-ttu-id="438e4-113">Vérifiez votre logique de flux de contrôle et assurez-vous que la variable a une valeur valide avant que le contrôle est passé à n’importe quelle instruction qui le lit.</span><span class="sxs-lookup"><span data-stu-id="438e4-113">Check your control flow logic and make sure the variable has a valid value before control passes to any statement that reads it.</span></span>  
  
-   <span data-ttu-id="438e4-114">Pour garantir que la variable a toujours une valeur valide consiste à initialiser dans le cadre de sa déclaration.</span><span class="sxs-lookup"><span data-stu-id="438e4-114">One way to guarantee that the variable always has a valid value is to initialize it as part of its declaration.</span></span> <span data-ttu-id="438e4-115">Consultez « Initialisation » dans [Dim, instruction](../../../visual-basic/language-reference/statements/dim-statement.md).</span><span class="sxs-lookup"><span data-stu-id="438e4-115">See "Initialization" in [Dim Statement](../../../visual-basic/language-reference/statements/dim-statement.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="438e4-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="438e4-116">See also</span></span>

- [<span data-ttu-id="438e4-117">Dim (instruction)</span><span class="sxs-lookup"><span data-stu-id="438e4-117">Dim Statement</span></span>](../../../visual-basic/language-reference/statements/dim-statement.md)
- [<span data-ttu-id="438e4-118">Déclaration de variable</span><span class="sxs-lookup"><span data-stu-id="438e4-118">Variable Declaration</span></span>](../../../visual-basic/programming-guide/language-features/variables/variable-declaration.md)
- [<span data-ttu-id="438e4-119">Dépannage des variables</span><span class="sxs-lookup"><span data-stu-id="438e4-119">Troubleshooting Variables</span></span>](../../../visual-basic/programming-guide/language-features/variables/troubleshooting-variables.md)
