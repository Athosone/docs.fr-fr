---
title: Conception de paramètres
ms.date: 10/22/2008
ms.technology: dotnet-standard
helpviewer_keywords:
- member design guidelines [.NET Framework], parameters
- members [.NET Framework], parameters
- names [.NET Framework], parameters
- parameters, design guidelines
- reserved parameters
ms.assetid: 3f33bf46-4a7b-43b3-bb78-1ffebe0dcfa6
author: KrzysztofCwalina
ms.openlocfilehash: 5a0f6e0fab5d0f2fe8574e348fc6b8ae726eeb99
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61757402"
---
# <a name="parameter-design"></a><span data-ttu-id="b7dd8-102">Conception de paramètres</span><span class="sxs-lookup"><span data-stu-id="b7dd8-102">Parameter Design</span></span>
<span data-ttu-id="b7dd8-103">Cette section fournit des indications générales sur la conception de paramètres, y compris les sections contenant des instructions pour la vérification des arguments.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-103">This section provides broad guidelines on parameter design, including sections with guidelines for checking arguments.</span></span> <span data-ttu-id="b7dd8-104">En outre, vous devez consulter les instructions décrites dans [d’affectation de noms de paramètres](../../../docs/standard/design-guidelines/naming-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="b7dd8-104">In addition, you should refer to the guidelines described in [Naming Parameters](../../../docs/standard/design-guidelines/naming-parameters.md).</span></span>  
  
 <span data-ttu-id="b7dd8-105">**✓ DO** utiliser le type de paramètre moins dérivé qui fournit les fonctionnalités requises par le membre.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-105">**✓ DO** use the least derived parameter type that provides the functionality required by the member.</span></span>  
  
 <span data-ttu-id="b7dd8-106">Par exemple, supposons que vous souhaitez concevoir une méthode qui énumère une collection et imprime chaque élément dans la console.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-106">For example, suppose you want to design a method that enumerates a collection and prints each item to the console.</span></span> <span data-ttu-id="b7dd8-107">Une telle méthode doit prendre <xref:System.Collections.IEnumerable> comme paramètre, pas <xref:System.Collections.ArrayList> ou <xref:System.Collections.IList>, par exemple.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-107">Such a method should take <xref:System.Collections.IEnumerable> as the parameter, not <xref:System.Collections.ArrayList> or <xref:System.Collections.IList>, for example.</span></span>  
  
 <span data-ttu-id="b7dd8-108">**X DO NOT** utiliser des paramètres réservés.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-108">**X DO NOT** use reserved parameters.</span></span>  
  
 <span data-ttu-id="b7dd8-109">Si plus d’entrée à un membre est nécessaire dans une version ultérieure, une nouvelle surcharge peut être ajoutée.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-109">If more input to a member is needed in some future version, a new overload can be added.</span></span>  
  
 <span data-ttu-id="b7dd8-110">**X DO NOT** ont exposés publiquement de méthodes qui prennent des pointeurs, des tableaux de pointeurs ou des tableaux multidimensionnels en tant que paramètres.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-110">**X DO NOT** have publicly exposed methods that take pointers, arrays of pointers, or multidimensional arrays as parameters.</span></span>  
  
 <span data-ttu-id="b7dd8-111">Pointeurs et les tableaux multidimensionnels sont relativement difficiles à utiliser correctement.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-111">Pointers and multidimensional arrays are relatively difficult to use properly.</span></span> <span data-ttu-id="b7dd8-112">Dans presque tous les cas, l’API peuvent être repensées pour éviter de prendre ces types en tant que paramètres.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-112">In almost all cases, APIs can be redesigned to avoid taking these types as parameters.</span></span>  
  
 <span data-ttu-id="b7dd8-113">**✓ DO** placer tous les `out` paramètres après toute la valeur et `ref` paramètres (à l’exclusion des tableaux de paramètres), même si cela aboutit à une incohérence dans le paramètre de classement entre les surcharges (consultez [membre La surcharge](../../../docs/standard/design-guidelines/member-overloading.md)).</span><span class="sxs-lookup"><span data-stu-id="b7dd8-113">**✓ DO** place all `out` parameters following all of the by-value and `ref` parameters (excluding parameter arrays), even if it results in an inconsistency in parameter ordering between overloads (see [Member Overloading](../../../docs/standard/design-guidelines/member-overloading.md)).</span></span>  
  
 <span data-ttu-id="b7dd8-114">Le `out` paramètres peuvent être considérés comme valeurs de retour supplémentaires et regroupant les rend plus facile à comprendre la signature de méthode.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-114">The `out` parameters can be seen as extra return values, and grouping them together makes the method signature easier to understand.</span></span>  
  
 <span data-ttu-id="b7dd8-115">**✓ DO** cohérente dans les paramètres d’affectation de noms lors de la substitution de membres ou de l’implémentation des membres d’interface.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-115">**✓ DO** be consistent in naming parameters when overriding members or implementing interface members.</span></span>  
  
 <span data-ttu-id="b7dd8-116">La relation entre les méthodes est mieux communique.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-116">This better communicates the relationship between the methods.</span></span>  
  
### <a name="choosing-between-enum-and-boolean-parameters"></a><span data-ttu-id="b7dd8-117">Choix entre Enum et des paramètres booléens</span><span class="sxs-lookup"><span data-stu-id="b7dd8-117">Choosing Between Enum and Boolean Parameters</span></span>  
 <span data-ttu-id="b7dd8-118">**✓ DO** utiliser les énumérations si un membre possède deux ou plusieurs paramètres booléens.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-118">**✓ DO** use enums if a member would otherwise have two or more Boolean parameters.</span></span>  
  
 <span data-ttu-id="b7dd8-119">**X DO NOT** utiliser des valeurs booléennes, sauf si vous êtes absolument sûr, il y aura jamais besoin de plus de deux valeurs.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-119">**X DO NOT** use Booleans unless you are absolutely sure there will never be a need for more than two values.</span></span>  
  
 <span data-ttu-id="b7dd8-120">Enums donner à la place pour l’ajout ultérieur de valeurs, mais vous devez être conscient de toutes les implications de l’ajout de valeurs aux énumérations, qui sont décrites dans [conception d’énumérations](../../../docs/standard/design-guidelines/enum.md).</span><span class="sxs-lookup"><span data-stu-id="b7dd8-120">Enums give you some room for future addition of values, but you should be aware of all the implications of adding values to enums, which are described in [Enum Design](../../../docs/standard/design-guidelines/enum.md).</span></span>  
  
 <span data-ttu-id="b7dd8-121">**✓ CONSIDER** à l’aide de valeurs booléennes pour les paramètres du constructeur qui sont des valeurs de deux États réellement et sont uniquement utilisées pour initialiser les propriétés booléennes.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-121">**✓ CONSIDER** using Booleans for constructor parameters that are truly two-state values and are simply used to initialize Boolean properties.</span></span>  
  
### <a name="validating-arguments"></a><span data-ttu-id="b7dd8-122">Validation d’Arguments</span><span class="sxs-lookup"><span data-stu-id="b7dd8-122">Validating Arguments</span></span>  
 <span data-ttu-id="b7dd8-123">**✓ DO** valider les arguments passés aux membres publics, protégés ou implémentées explicitement.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-123">**✓ DO** validate arguments passed to public, protected, or explicitly implemented members.</span></span> <span data-ttu-id="b7dd8-124">Lever <xref:System.ArgumentException?displayProperty=nameWithType>, ou une de ses sous-classes, si la validation échoue.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-124">Throw <xref:System.ArgumentException?displayProperty=nameWithType>, or one of its subclasses, if the validation fails.</span></span>  
  
 <span data-ttu-id="b7dd8-125">Notez que la validation réelle ne doit pas nécessairement se produire dans le membre public ou protégé lui-même.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-125">Note that the actual validation does not necessarily have to happen in the public or protected member itself.</span></span> <span data-ttu-id="b7dd8-126">Il peut se produire à un niveau inférieur dans une routine privé ou interne.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-126">It could happen at a lower level in some private or internal routine.</span></span> <span data-ttu-id="b7dd8-127">Le point à retenir est que toute la surface exposée aux utilisateurs finaux vérifie les arguments.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-127">The main point is that the entire surface area that is exposed to the end users checks the arguments.</span></span>  
  
 <span data-ttu-id="b7dd8-128">**✓ DO** lever <xref:System.ArgumentNullException> si un argument null est passé et le membre ne prend pas en charge les arguments null.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-128">**✓ DO** throw <xref:System.ArgumentNullException> if a null argument is passed and the member does not support null arguments.</span></span>  
  
 <span data-ttu-id="b7dd8-129">**✓ DO** valider les paramètres d’énumération.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-129">**✓ DO** validate enum parameters.</span></span>  
  
 <span data-ttu-id="b7dd8-130">Ne supposez pas arguments enum seront dans la plage définie par l’énumération.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-130">Do not assume enum arguments will be in the range defined by the enum.</span></span> <span data-ttu-id="b7dd8-131">Le CLR permet la conversion de toute valeur entière en une valeur enum même si la valeur n’est pas définie dans l’énumération.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-131">The CLR allows casting any integer value into an enum value even if the value is not defined in the enum.</span></span>  
  
 <span data-ttu-id="b7dd8-132">**X DO NOT** utiliser <xref:System.Enum.IsDefined%2A?displayProperty=nameWithType> pour la plage enum vérifie.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-132">**X DO NOT** use <xref:System.Enum.IsDefined%2A?displayProperty=nameWithType> for enum range checks.</span></span>  
  
 <span data-ttu-id="b7dd8-133">**✓ DO** Sachez que les arguments mutables peuvent ont été modifiés après leur validation.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-133">**✓ DO** be aware that mutable arguments might have changed after they were validated.</span></span>  
  
 <span data-ttu-id="b7dd8-134">Si le membre est sensible à la sécurité, vous êtes invités à effectuer une copie puis valider et traiter l’argument.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-134">If the member is security sensitive, you are encouraged to make a copy and then validate and process the argument.</span></span>  
  
### <a name="parameter-passing"></a><span data-ttu-id="b7dd8-135">Passage de paramètres</span><span class="sxs-lookup"><span data-stu-id="b7dd8-135">Parameter Passing</span></span>  
 <span data-ttu-id="b7dd8-136">Du point de vue d’un concepteur de framework, il existe trois principaux groupes de paramètres : paramètres, par valeur `ref` paramètres, et `out` paramètres.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-136">From the perspective of a framework designer, there are three main groups of parameters: by-value parameters, `ref` parameters, and `out` parameters.</span></span>  
  
 <span data-ttu-id="b7dd8-137">Lorsqu’un argument est passé à un paramètre par valeur, le membre reçoit une copie de l’argument réel passé.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-137">When an argument is passed through a by-value parameter, the member receives a copy of the actual argument passed in.</span></span> <span data-ttu-id="b7dd8-138">Si l’argument est un type valeur, une copie de l’argument est placée sur la pile.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-138">If the argument is a value type, a copy of the argument is put on the stack.</span></span> <span data-ttu-id="b7dd8-139">Si l’argument est un type référence, une copie de la référence est placée sur la pile.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-139">If the argument is a reference type, a copy of the reference is put on the stack.</span></span> <span data-ttu-id="b7dd8-140">Langages CLR plus populaires, tels que c#, VB.NET et C++, default pour le passage de paramètres par valeur.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-140">Most popular CLR languages, such as C#, VB.NET, and C++, default to passing parameters by value.</span></span>  
  
 <span data-ttu-id="b7dd8-141">Quand un argument est passé via un `ref` paramètre, le membre reçoit une référence à l’argument réel passé.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-141">When an argument is passed through a `ref` parameter, the member receives a reference to the actual argument passed in.</span></span> <span data-ttu-id="b7dd8-142">Si l’argument est un type valeur, une référence à l’argument est placée sur la pile.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-142">If the argument is a value type, a reference to the argument is put on the stack.</span></span> <span data-ttu-id="b7dd8-143">Si l’argument est un type référence, une référence à la référence est placée sur la pile.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-143">If the argument is a reference type, a reference to the reference is put on the stack.</span></span> <span data-ttu-id="b7dd8-144">`Ref` paramètres peuvent être utilisés pour que le membre de modifier les arguments passés par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-144">`Ref` parameters can be used to allow the member to modify arguments passed by the caller.</span></span>  
  
 <span data-ttu-id="b7dd8-145">`Out` les paramètres sont similaires à `ref` paramètres, avec quelques petites différences.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-145">`Out` parameters are similar to `ref` parameters, with some small differences.</span></span> <span data-ttu-id="b7dd8-146">Le paramètre est considéré comme initialement non attribués et ne peut pas être lu dans le corps du membre avant lui est attribuée une valeur.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-146">The parameter is initially considered unassigned and cannot be read in the member body before it is assigned some value.</span></span> <span data-ttu-id="b7dd8-147">En outre, le paramètre a à assigner une valeur avant le retour du membre.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-147">Also, the parameter has to be assigned some value before the member returns.</span></span>  
  
 <span data-ttu-id="b7dd8-148">**X AVOID** à l’aide de `out` ou `ref` paramètres.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-148">**X AVOID** using `out` or `ref` parameters.</span></span>  
  
 <span data-ttu-id="b7dd8-149">À l’aide de `out` ou `ref` paramètres nécessite une certaine expérience des pointeurs, de comprendre la différence entre les types valeur et types référence et gestion de méthodes impliquant plusieurs valeurs de retour.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-149">Using `out` or `ref` parameters requires experience with pointers, understanding how value types and reference types differ, and handling methods with multiple return values.</span></span> <span data-ttu-id="b7dd8-150">En outre, la différence entre `out` et `ref` paramètres n’est pas généralement peu comprise.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-150">Also, the difference between `out` and `ref` parameters is not widely understood.</span></span> <span data-ttu-id="b7dd8-151">Les architectes de Framework conception destiné à une audience générale ne doivent pas s’attendre aux utilisateurs de maîtrisent l’utilisation des `out` ou `ref` paramètres.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-151">Framework architects designing for a general audience should not expect users to master working with `out` or `ref` parameters.</span></span>  
  
 <span data-ttu-id="b7dd8-152">**X DO NOT** passage de types référence par référence.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-152">**X DO NOT** pass reference types by reference.</span></span>  
  
 <span data-ttu-id="b7dd8-153">Il existe quelques rares exceptions à la règle, comme une méthode qui peut être utilisée pour échanger des références.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-153">There are some limited exceptions to the rule, such as a method that can be used to swap references.</span></span>  
  
### <a name="members-with-variable-number-of-parameters"></a><span data-ttu-id="b7dd8-154">Membres avec un nombre Variable de paramètres</span><span class="sxs-lookup"><span data-stu-id="b7dd8-154">Members with Variable Number of Parameters</span></span>  
 <span data-ttu-id="b7dd8-155">Les membres qui peuvent prendre un nombre variable d’arguments sont exprimées en fournissant un paramètre de tableau.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-155">Members that can take a variable number of arguments are expressed by providing an array parameter.</span></span> <span data-ttu-id="b7dd8-156">Par exemple, <xref:System.String> fournit la méthode suivante :</span><span class="sxs-lookup"><span data-stu-id="b7dd8-156">For example, <xref:System.String> provides the following method:</span></span>  
  
```  
public class String {  
    public static string Format(string format, object[] parameters);  
}  
```  
  
 <span data-ttu-id="b7dd8-157">Un utilisateur peut ensuite appeler la <xref:System.String.Format%2A?displayProperty=nameWithType> méthode, comme suit :</span><span class="sxs-lookup"><span data-stu-id="b7dd8-157">A user can then call the <xref:System.String.Format%2A?displayProperty=nameWithType> method, as follows:</span></span>  
  
 `String.Format("File {0} not found in {1}",new object[]{filename,directory});`  
  
 <span data-ttu-id="b7dd8-158">Ajout du mot clé c# params à un paramètre de tableau modifie le paramètre à un paramètre de tableau params ce que l'on appelle et fournit un raccourci à la création d’un tableau temporaire.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-158">Adding the C# params keyword to an array parameter changes the parameter to a so-called params array parameter and provides a shortcut to creating a temporary array.</span></span>  
  
```  
public class String {  
    public static string Format(string format, params object[] parameters);  
}  
```  
  
 <span data-ttu-id="b7dd8-159">Cela permet à l’utilisateur d’appeler la méthode en passant les éléments du tableau directement dans la liste d’arguments.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-159">Doing this allows the user to call the method by passing the array elements directly in the argument list.</span></span>  
  
 `String.Format("File {0} not found in {1}",filename,directory);`  
  
 <span data-ttu-id="b7dd8-160">Notez que le mot clé params peut être ajouté uniquement au dernier paramètre dans la liste de paramètres.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-160">Note that the params keyword can be added only to the last parameter in the parameter list.</span></span>  
  
 <span data-ttu-id="b7dd8-161">**✓ CONSIDER** Ajout du mot clé params aux paramètres de tableau, si vous pensez que les utilisateurs finaux pour passer des tableaux avec un petit nombre d’éléments.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-161">**✓ CONSIDER** adding the params keyword to array parameters if you expect the end users to pass arrays with a small number of elements.</span></span> <span data-ttu-id="b7dd8-162">S’il est prévu qu’un grand nombre d’éléments sera transmis en commun des scénarios, les utilisateurs sans doute ne passera pas ces éléments comme étant inline quand même, et par conséquent, le mot clé params n’est pas nécessaire.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-162">If it’s expected that lots of elements will be passed in common scenarios, users will probably not pass these elements inline anyway, and so the params keyword is not necessary.</span></span>  
  
 <span data-ttu-id="b7dd8-163">**X AVOID** à l’aide de tableaux params si l’appelant est presque toujours avoir l’entrée dans un tableau.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-163">**X AVOID** using params arrays if the caller would almost always have the input already in an array.</span></span>  
  
 <span data-ttu-id="b7dd8-164">Par exemple, les membres avec des paramètres de tableau d’octets seraient presque jamais être appelées en passant des octets individuels.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-164">For example, members with byte array parameters would almost never be called by passing individual bytes.</span></span> <span data-ttu-id="b7dd8-165">Pour cette raison, les paramètres de tableau d’octets dans le .NET Framework n’utilisent pas le mot clé params.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-165">For this reason, byte array parameters in the .NET Framework do not use the params keyword.</span></span>  
  
 <span data-ttu-id="b7dd8-166">**X DO NOT** utiliser des tableaux params si le tableau est modifié par le membre prenant le paramètre de tableau params.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-166">**X DO NOT** use params arrays if the array is modified by the member taking the params array parameter.</span></span>  
  
 <span data-ttu-id="b7dd8-167">En raison du fait que de nombreux compilateurs transforment les arguments pour le membre en un tableau temporaire sur le site d’appel, le tableau peut être un objet temporaire, et par conséquent, toute modification apportée à la baie seront perdues.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-167">Because of the fact that many compilers turn the arguments to the member into a temporary array at the call site, the array might be a temporary object, and therefore any modifications to the array will be lost.</span></span>  
  
 <span data-ttu-id="b7dd8-168">**✓ CONSIDER** à l’aide du mot clé params dans une surcharge simple, même si une surcharge plus complexe ne peut pas l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-168">**✓ CONSIDER** using the params keyword in a simple overload, even if a more complex overload could not use it.</span></span>  
  
 <span data-ttu-id="b7dd8-169">Demandez-vous si les utilisateurs importants ayant du tableau de paramètres dans une surcharge même si ce n’était pas dans toutes les surcharges.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-169">Ask yourself if users would value having the params array in one overload even if it wasn’t in all overloads.</span></span>  
  
 <span data-ttu-id="b7dd8-170">**✓ DO** essayez des paramètres de commande pour le rendre possible d’utiliser le mot clé params.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-170">**✓ DO** try to order parameters to make it possible to use the params keyword.</span></span>  
  
 <span data-ttu-id="b7dd8-171">**✓ CONSIDER** fournissant des surcharges spéciaux et les chemins de code pour les appels avec un petit nombre d’arguments dans les API très sensibles aux performances.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-171">**✓ CONSIDER** providing special overloads and code paths for calls with a small number of arguments in extremely performance-sensitive APIs.</span></span>  
  
 <span data-ttu-id="b7dd8-172">Cela rend possible pour éviter de créer des objets de tableau lors de l’API est appelée avec un petit nombre d’arguments.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-172">This makes it possible to avoid creating array objects when the API is called with a small number of arguments.</span></span> <span data-ttu-id="b7dd8-173">Les noms des paramètres du formulaire en prenant une forme au singulier du paramètre de tableau et en ajoutant un suffixe numérique.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-173">Form the names of the parameters by taking a singular form of the array parameter and adding a numeric suffix.</span></span>  
  
 <span data-ttu-id="b7dd8-174">Vous devez uniquement le faire si vous vous apprêtez à particulariser le chemin d’accès de l’ensemble du code, pas seulement créer un tableau et appelez la méthode plus générale.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-174">You should only do this if you are going to special-case the entire code path, not just create an array and call the more general method.</span></span>  
  
 <span data-ttu-id="b7dd8-175">**✓ DO** Sachez que la valeur null peut être passée comme un argument de tableau params.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-175">**✓ DO** be aware that null could be passed as a params array argument.</span></span>  
  
 <span data-ttu-id="b7dd8-176">Vous devez valider que le tableau n’est pas null avant le traitement.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-176">You should validate that the array is not null before processing.</span></span>  
  
 <span data-ttu-id="b7dd8-177">**X DO NOT** utiliser le `varargs` méthodes en tant que les points de suspension.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-177">**X DO NOT** use the `varargs` methods, otherwise known as the ellipsis.</span></span>  
  
 <span data-ttu-id="b7dd8-178">Certains langages CLR, tels que C++, prennent en charge une autre convention pour passer des listes de paramètres de variable appelées `varargs` méthodes.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-178">Some CLR languages, such as C++, support an alternative convention for passing variable parameter lists called `varargs` methods.</span></span> <span data-ttu-id="b7dd8-179">La convention de ne doit pas servir dans les infrastructures, car il n'est pas conforme CLS.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-179">The convention should not be used in frameworks, because it is not CLS compliant.</span></span>  
  
### <a name="pointer-parameters"></a><span data-ttu-id="b7dd8-180">Paramètres de pointeur</span><span class="sxs-lookup"><span data-stu-id="b7dd8-180">Pointer Parameters</span></span>  
 <span data-ttu-id="b7dd8-181">En règle générale, les pointeurs ne doivent pas apparaître dans la surface d’exposition publique d’une infrastructure bien conçue du code managé.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-181">In general, pointers should not appear in the public surface area of a well-designed managed code framework.</span></span> <span data-ttu-id="b7dd8-182">La plupart du temps, les pointeurs doivent être encapsulées.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-182">Most of the time, pointers should be encapsulated.</span></span> <span data-ttu-id="b7dd8-183">Toutefois, dans certains cas les pointeurs sont nécessaires pour des raisons de l’interopérabilité et l’utilisation des pointeurs dans ce cas est appropriée.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-183">However, in some cases pointers are required for interoperability reasons, and using pointers in such cases is appropriate.</span></span>  
  
 <span data-ttu-id="b7dd8-184">**✓ DO** offrent une alternative pour les membres qui prennent un argument de pointeur, étant donné que les pointeurs ne sont pas conformes CLS.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-184">**✓ DO** provide an alternative for any member that takes a pointer argument, because pointers are not CLS-compliant.</span></span>  
  
 <span data-ttu-id="b7dd8-185">**X AVOID** effectuant l’argument coûteux, la vérification des arguments de pointeur.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-185">**X AVOID** doing expensive argument checking of pointer arguments.</span></span>  
  
 <span data-ttu-id="b7dd8-186">**✓ DO** suivent les conventions de pointeur associé courantes lors de la conception de membres avec des pointeurs.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-186">**✓ DO** follow common pointer-related conventions when designing members with pointers.</span></span>  
  
 <span data-ttu-id="b7dd8-187">Par exemple, il n’est pas nécessaire de transmettre l’index de début, car l’opération arithmétique de pointeur simple peut être utilisé pour obtenir le même résultat.</span><span class="sxs-lookup"><span data-stu-id="b7dd8-187">For example, there is no need to pass the start index, because simple pointer arithmetic can be used to accomplish the same result.</span></span>  
  
 <span data-ttu-id="b7dd8-188">*Portions © 2005, 2009 Microsoft Corporation. Tous droits réservés.*</span><span class="sxs-lookup"><span data-stu-id="b7dd8-188">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>  
  
 <span data-ttu-id="b7dd8-189">*Réimprimé avec l’autorisation de Pearson éducation, Inc. à partir de [instructions de conception Framework : Conventions, les idiomes et les modèles pour les bibliothèques .NET réutilisable, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) Krzysztof Cwalina et Brad Abrams, publié le 22 octobre 2008 par Addison-Wesley Professional dans le cadre de la série de développement de Microsoft Windows.*</span><span class="sxs-lookup"><span data-stu-id="b7dd8-189">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b7dd8-190">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b7dd8-190">See also</span></span>

- [<span data-ttu-id="b7dd8-191">Instructions de conception des membres</span><span class="sxs-lookup"><span data-stu-id="b7dd8-191">Member Design Guidelines</span></span>](../../../docs/standard/design-guidelines/member.md)
- [<span data-ttu-id="b7dd8-192">Règles de conception de .NET Framework</span><span class="sxs-lookup"><span data-stu-id="b7dd8-192">Framework Design Guidelines</span></span>](../../../docs/standard/design-guidelines/index.md)
