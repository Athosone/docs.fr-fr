---
title: Numéro d'enregistrement incorrect
ms.date: 07/20/2015
f1_keywords:
- vbrID63
ms.assetid: 1fcc33f8-822a-4de9-a6e3-228ddb5824a6
ms.openlocfilehash: abd0a1467c0991a40b93e74a1d7a7889367fb8ca
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61977021"
---
# <a name="bad-record-number"></a><span data-ttu-id="9f5f9-102">Numéro d'enregistrement incorrect</span><span class="sxs-lookup"><span data-stu-id="9f5f9-102">Bad record number</span></span>
<span data-ttu-id="9f5f9-103">Le numéro d’enregistrement dans une instruction `a FileGet`, `FilePut`, `FileGetObject`ou `FilePutObject` est inférieur ou égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="9f5f9-103">The record number in `a FileGet`, `FilePut`, `FileGetObject`, or `FilePutObject` statement is less than or equal to zero.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="9f5f9-104">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="9f5f9-104">To correct this error</span></span>  
  
1. <span data-ttu-id="9f5f9-105">Vérifiez les calculs utilisés pour générer le numéro d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="9f5f9-105">Check the calculations used in generating the record number.</span></span> <span data-ttu-id="9f5f9-106">Vérifiez l’orthographe des variables contenant le numéro d’enregistrement ou utilisées dans le calcul des numéros d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="9f5f9-106">Verify spelling of the variables containing the record number or used in calculating record numbers.</span></span> <span data-ttu-id="9f5f9-107">Un nom de variable mal orthographié est déclaré implicitement et possède une valeur égale à zéro, sauf si vous avez utilisé `Option Explicit On` dans le module.</span><span class="sxs-lookup"><span data-stu-id="9f5f9-107">A misspelled variable name is implicitly declared and initialized to zero, unless you used `Option Explicit On` in the module.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9f5f9-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9f5f9-108">See also</span></span>

- [<span data-ttu-id="9f5f9-109">Option Explicit (instruction)</span><span class="sxs-lookup"><span data-stu-id="9f5f9-109">Option Explicit Statement</span></span>](../../visual-basic/language-reference/statements/option-explicit-statement.md)
