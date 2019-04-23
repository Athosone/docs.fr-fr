---
title: Une référence à l'assembly '<assemblyidentity>' contenant le type '<typename>' est requise, mais une référence adéquate n'a pas été trouvée en raison de l'ambiguïté entre les projets '<projectname1>' et '<projectname2>'
ms.date: 07/20/2015
f1_keywords:
- bc30969
- vbc30969
helpviewer_keywords:
- BC30969
ms.assetid: 1b29dbc5-8268-45fe-bfc2-b2070a5c845c
ms.openlocfilehash: 9868598b32ae17ef5bfb5dd738f8a7541515f5ec
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59310669"
---
# <a name="reference-required-to-assembly-assemblyidentity-containing-type-typename-but-a-suitable-reference-could-not-be-found-due-to-ambiguity-between-projects-projectname1-and-projectname2"></a><span data-ttu-id="afcc4-102">Référence à l’assembly requise '\<assemblyidentity >' contenant le type '\<nom_type >', mais une référence appropriée est introuvable en raison de l’ambiguïté entre les projets\<nom_projet1 >' et '\< nom_projet2 >'</span><span class="sxs-lookup"><span data-stu-id="afcc4-102">Reference required to assembly '\<assemblyidentity>' containing type '\<typename>', but a suitable reference could not be found due to ambiguity between projects '\<projectname1>' and '\<projectname2>'</span></span>
<span data-ttu-id="afcc4-103">Une expression utilise un type, comme une classe, une structure, une interface, une énumération ou un délégué, qui est défini en dehors de votre projet.</span><span class="sxs-lookup"><span data-stu-id="afcc4-103">An expression uses a type, such as a class, structure, interface, enumeration, or delegate, that is defined outside your project.</span></span> <span data-ttu-id="afcc4-104">Cependant, des références de projet désignent plusieurs assemblys définissant ce type.</span><span class="sxs-lookup"><span data-stu-id="afcc4-104">However, you have project references to more than one assembly defining that type.</span></span>  
  
 <span data-ttu-id="afcc4-105">Les projets cités produisent des assemblys de même nom.</span><span class="sxs-lookup"><span data-stu-id="afcc4-105">The cited projects produce assemblies with the same name.</span></span> <span data-ttu-id="afcc4-106">Par conséquent, le compilateur ne peut pas déterminer quel assembly utiliser pour le type auquel vous accédez.</span><span class="sxs-lookup"><span data-stu-id="afcc4-106">Therefore, the compiler cannot determine which assembly to use for the type you are accessing.</span></span>  
  
 <span data-ttu-id="afcc4-107">Pour accéder à un type défini dans un autre assembly, le compilateur Visual Basic doit avoir une référence à cet assembly.</span><span class="sxs-lookup"><span data-stu-id="afcc4-107">To access a type defined in another assembly, the Visual Basic compiler must have a reference to that assembly.</span></span> <span data-ttu-id="afcc4-108">Il doit s’agir d’une référence unique et non équivoque qui ne provoque pas de références circulaires parmi des projets.</span><span class="sxs-lookup"><span data-stu-id="afcc4-108">This must be a single, unambiguous reference that does not cause circular references among projects.</span></span>  
  
 <span data-ttu-id="afcc4-109">**ID d’erreur :** BC30969</span><span class="sxs-lookup"><span data-stu-id="afcc4-109">**Error ID:** BC30969</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="afcc4-110">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="afcc4-110">To correct this error</span></span>  
  
1. <span data-ttu-id="afcc4-111">Identifiez le projet qui produit le meilleur assembly pour votre projet à référencer.</span><span class="sxs-lookup"><span data-stu-id="afcc4-111">Determine which project produces the best assembly for your project to reference.</span></span> <span data-ttu-id="afcc4-112">Pour prendre cette décision, vous pouvez utiliser des critères, tels que la facilité d’accès au fichier et la fréquence des mises à jour.</span><span class="sxs-lookup"><span data-stu-id="afcc4-112">For this decision, you might use criteria such as ease of file access and frequency of updates.</span></span>  
  
2. <span data-ttu-id="afcc4-113">Dans vos propriétés de projet, ajoutez une référence au fichier contenant l’assembly qui définit le type que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="afcc4-113">In your project properties, add a reference to the file that contains the assembly that defines the type you are using.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="afcc4-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="afcc4-114">See also</span></span>

- [<span data-ttu-id="afcc4-115">Gestion des références dans un projet</span><span class="sxs-lookup"><span data-stu-id="afcc4-115">Managing references in a project</span></span>](/visualstudio/ide/managing-references-in-a-project)
- [<span data-ttu-id="afcc4-116">Références aux éléments déclarés</span><span class="sxs-lookup"><span data-stu-id="afcc4-116">References to Declared Elements</span></span>](../../../visual-basic/programming-guide/language-features/declared-elements/references-to-declared-elements.md)

- [<span data-ttu-id="afcc4-117">Gestion des propriétés des projets et des solutions</span><span class="sxs-lookup"><span data-stu-id="afcc4-117">Managing Project and Solution Properties</span></span>](/visualstudio/ide/managing-project-and-solution-properties)
- [<span data-ttu-id="afcc4-118">Dépannage de références rompues</span><span class="sxs-lookup"><span data-stu-id="afcc4-118">Troubleshooting Broken References</span></span>](/visualstudio/ide/troubleshooting-broken-references)
