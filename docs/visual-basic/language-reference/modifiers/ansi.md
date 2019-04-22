---
title: Ansi (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.Ansi
helpviewer_keywords:
- Declare statement [Visual Basic], marshaling strings [Visual Basic]
- ANSI, Visual Basic
- ANSI
ms.assetid: 4f1fa6ff-5557-41ab-b6da-90baf4c15917
ms.openlocfilehash: 98dafab3e524ea371bba228eb231e28d46cc3b4e
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58819449"
---
# <a name="ansi-visual-basic"></a><span data-ttu-id="dc4f5-102">Ansi (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="dc4f5-102">Ansi (Visual Basic)</span></span>
<span data-ttu-id="dc4f5-103">Spécifie que Visual Basic doit marshaler toutes les chaînes en valeurs American National Standards Institute (ANSI), quel que soit le nom de la procédure externe déclarée.</span><span class="sxs-lookup"><span data-stu-id="dc4f5-103">Specifies that Visual Basic should marshal all strings to American National Standards Institute (ANSI) values regardless of the name of the external procedure being declared.</span></span>  
  
 <span data-ttu-id="dc4f5-104">Lorsque vous appelez une procédure définie en dehors de votre projet, le compilateur Visual Basic n’a pas accès aux informations requises pour appeler la procédure correctement.</span><span class="sxs-lookup"><span data-stu-id="dc4f5-104">When you call a procedure defined outside your project, the Visual Basic compiler does not have access to the information it needs to call the procedure correctly.</span></span> <span data-ttu-id="dc4f5-105">Ces informations incluent où se trouve la procédure, comment il est identifié, sa séquence d’appel et de type de retour, et chaîne de jeu de caractères qu’il utilise.</span><span class="sxs-lookup"><span data-stu-id="dc4f5-105">This information includes where the procedure is located, how it is identified, its calling sequence and return type, and the string character set it uses.</span></span> <span data-ttu-id="dc4f5-106">Le [instruction Declare](../../../visual-basic/language-reference/statements/declare-statement.md) crée une référence à une procédure externe et fournit ces informations nécessaires.</span><span class="sxs-lookup"><span data-stu-id="dc4f5-106">The [Declare Statement](../../../visual-basic/language-reference/statements/declare-statement.md) creates a reference to an external procedure and supplies this necessary information.</span></span>  
  
 <span data-ttu-id="dc4f5-107">Le `charsetmodifier` dans le `Declare` instruction fournit les informations de jeu de caractères pour marshaler des chaînes lors d’un appel à la procédure externe.</span><span class="sxs-lookup"><span data-stu-id="dc4f5-107">The `charsetmodifier` part in the `Declare` statement supplies the character set information for marshaling strings during a call to the external procedure.</span></span> <span data-ttu-id="dc4f5-108">Elle affecte également la façon dont Visual Basic recherche le fichier externe pour le nom de la procédure externe.</span><span class="sxs-lookup"><span data-stu-id="dc4f5-108">It also affects how Visual Basic searches the external file for the external procedure name.</span></span> <span data-ttu-id="dc4f5-109">Le `Ansi` modificateur Spécifie que Visual Basic doit marshaler toutes les chaînes en valeurs ANSI et doit rechercher la procédure sans modifier son nom durant la recherche.</span><span class="sxs-lookup"><span data-stu-id="dc4f5-109">The `Ansi` modifier specifies that Visual Basic should marshal all strings to ANSI values and should look up the procedure without modifying its name during the search.</span></span>  
  
 <span data-ttu-id="dc4f5-110">Si aucun modificateur de jeu de caractères est spécifié, `Ansi` est la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="dc4f5-110">If no character set modifier is specified, `Ansi` is the default.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="dc4f5-111">Notes</span><span class="sxs-lookup"><span data-stu-id="dc4f5-111">Remarks</span></span>  
 <span data-ttu-id="dc4f5-112">Le `Ansi` modificateur peut être utilisé dans ce contexte :</span><span class="sxs-lookup"><span data-stu-id="dc4f5-112">The `Ansi` modifier can be used in this context:</span></span>  
  
 [<span data-ttu-id="dc4f5-113">Declare (instruction)</span><span class="sxs-lookup"><span data-stu-id="dc4f5-113">Declare Statement</span></span>](../../../visual-basic/language-reference/statements/declare-statement.md)  
  
## <a name="smart-device-developer-notes"></a><span data-ttu-id="dc4f5-114">Remarques sur le développement Smart Device</span><span class="sxs-lookup"><span data-stu-id="dc4f5-114">Smart Device Developer Notes</span></span>  
 <span data-ttu-id="dc4f5-115">Ce mot clé n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="dc4f5-115">This keyword is not supported.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dc4f5-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dc4f5-116">See also</span></span>

- [<span data-ttu-id="dc4f5-117">Auto</span><span class="sxs-lookup"><span data-stu-id="dc4f5-117">Auto</span></span>](../../../visual-basic/language-reference/modifiers/auto.md)
- [<span data-ttu-id="dc4f5-118">Unicode</span><span class="sxs-lookup"><span data-stu-id="dc4f5-118">Unicode</span></span>](../../../visual-basic/language-reference/modifiers/unicode.md)
- [<span data-ttu-id="dc4f5-119">Mots clés</span><span class="sxs-lookup"><span data-stu-id="dc4f5-119">Keywords</span></span>](../../../visual-basic/language-reference/keywords/index.md)
