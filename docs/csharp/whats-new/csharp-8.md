---
title: Nouveautés de C# 8.0 – Guide C#
description: Vue d’ensemble des nouvelles fonctionnalités disponibles dans C# 8.0. Cet article est à jour par rapport à la préversion 2.
ms.date: 02/12/2019
ms.openlocfilehash: eecc37433e4b026b7337418eac1a5e80ef48ea6e
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59427277"
---
# <a name="whats-new-in-c-80"></a><span data-ttu-id="6cc2d-104">Nouveautés de C# 8.0</span><span class="sxs-lookup"><span data-stu-id="6cc2d-104">What's new in C# 8.0</span></span>

<span data-ttu-id="6cc2d-105">Vous pouvez d’ores et déjà tester de nombreuses améliorations apportées au langage C# avec la préversion 2.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-105">There are many enhancements to the C# language that you can try out already with preview 2.</span></span> <span data-ttu-id="6cc2d-106">Voici les fonctionnalités ajoutées dans la préversion 2 :</span><span class="sxs-lookup"><span data-stu-id="6cc2d-106">The new features added in preview 2 are:</span></span>

- <span data-ttu-id="6cc2d-107">[Amélioration des critères spéciaux](#more-patterns-in-more-places) :</span><span class="sxs-lookup"><span data-stu-id="6cc2d-107">[Pattern matching enhancements](#more-patterns-in-more-places):</span></span>
  * [<span data-ttu-id="6cc2d-108">Expressions switch</span><span class="sxs-lookup"><span data-stu-id="6cc2d-108">Switch expressions</span></span>](#switch-expressions)
  * [<span data-ttu-id="6cc2d-109">Modèles de propriétés</span><span class="sxs-lookup"><span data-stu-id="6cc2d-109">Property patterns</span></span>](#property-patterns)
  * [<span data-ttu-id="6cc2d-110">Modèles de tuples</span><span class="sxs-lookup"><span data-stu-id="6cc2d-110">Tuple patterns</span></span>](#tuple-patterns)
  * [<span data-ttu-id="6cc2d-111">Modèles positionnels</span><span class="sxs-lookup"><span data-stu-id="6cc2d-111">Positional patterns</span></span>](#positional-patterns)
- [<span data-ttu-id="6cc2d-112">Déclarations using</span><span class="sxs-lookup"><span data-stu-id="6cc2d-112">Using declarations</span></span>](#using-declarations)
- [<span data-ttu-id="6cc2d-113">Fonctions locales statiques</span><span class="sxs-lookup"><span data-stu-id="6cc2d-113">Static local functions</span></span>](#static-local-functions)
- [<span data-ttu-id="6cc2d-114">Structs ref jetables</span><span class="sxs-lookup"><span data-stu-id="6cc2d-114">Disposable ref structs</span></span>](#disposable-ref-structs)

<span data-ttu-id="6cc2d-115">Les fonctionnalités suivantes du langage sont apparues initialement dans la préversion 1 de C# 8.0 :</span><span class="sxs-lookup"><span data-stu-id="6cc2d-115">The following language features first appeared in C# 8.0 preview 1:</span></span>

- [<span data-ttu-id="6cc2d-116">Types de référence Nullable</span><span class="sxs-lookup"><span data-stu-id="6cc2d-116">Nullable reference types</span></span>](#nullable-reference-types)
- [<span data-ttu-id="6cc2d-117">Flux asynchrones</span><span class="sxs-lookup"><span data-stu-id="6cc2d-117">Asynchronous streams</span></span>](#asynchronous-streams)
- [<span data-ttu-id="6cc2d-118">Index et plages</span><span class="sxs-lookup"><span data-stu-id="6cc2d-118">Indices and ranges</span></span>](#indices-and-ranges)

> [!NOTE]
> <span data-ttu-id="6cc2d-119">Cet article a été mis à jour pour la préversion 2 de C# 8.0.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-119">This article was last updated for C# 8.0 preview 2.</span></span>

<span data-ttu-id="6cc2d-120">La suite de cet article décrit brièvement ces fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-120">The remainder of this article briefly describes these features.</span></span> <span data-ttu-id="6cc2d-121">Lorsque des articles détaillés sont disponibles, des liens vers ces tutoriels et vues d’ensemble sont indiqués.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-121">Where in-depth articles are available, links to those tutorials and overviews are provided.</span></span>

## <a name="more-patterns-in-more-places"></a><span data-ttu-id="6cc2d-122">Ajout de modèles à différents endroits</span><span class="sxs-lookup"><span data-stu-id="6cc2d-122">More patterns in more places</span></span>

<span data-ttu-id="6cc2d-123">Les **critères spéciaux** offrent des outils permettant de produire des fonctionnalités dépendantes de la forme sur des types de données liés mais différents.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-123">**Pattern matching** gives tools to provide shape-dependent functionality across related but different kinds of data.</span></span> <span data-ttu-id="6cc2d-124">C# 7.0 a introduit la syntaxe des modèles de type et des modèles de constantes avec l’expression [`is`](../language-reference/keywords/is.md) et l’instruction [`switch`](../language-reference/keywords/switch.md).</span><span class="sxs-lookup"><span data-stu-id="6cc2d-124">C# 7.0 introduced syntax for type patterns and constant patterns by using the [`is`](../language-reference/keywords/is.md) expression and the [`switch`](../language-reference/keywords/switch.md) statement.</span></span> <span data-ttu-id="6cc2d-125">Ces fonctionnalités représentaient les premières étapes provisoires de prise en charge de paradigmes de programmation distinguant données et fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-125">These features represented the first tentative steps toward supporting programming paradigms where data and functionality live apart.</span></span> <span data-ttu-id="6cc2d-126">Face à la transition du secteur vers de nouveaux microservices et autres architectures cloud, d’autres outils sont nécessaires pour le langage.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-126">As the industry moves toward more microservices and other cloud-based architectures, other language tools are needed.</span></span>

<span data-ttu-id="6cc2d-127">C# 8.0 développe ce vocabulaire en offrant la possibilité d’utiliser d’autres expressions de modèle à davantage d’endroits dans le code.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-127">C# 8.0 expands this vocabulary so you can use more pattern expressions in more places in your code.</span></span> <span data-ttu-id="6cc2d-128">Étudiez ces fonctionnalités si vos données et vos fonctionnalités sont séparées.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-128">Consider these features when your data and functionality are separate.</span></span> <span data-ttu-id="6cc2d-129">Les critères spéciaux peuvent être intéressants si vos algorithmes dépendent d’un fait autre que le type de runtime d’un objet.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-129">Consider pattern matching when your algorithms depend on a fact other than the runtime type of an object.</span></span> <span data-ttu-id="6cc2d-130">Ces techniques représentent un autre moyen d’exprimer des conceptions.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-130">These techniques provide another way to express designs.</span></span>

<span data-ttu-id="6cc2d-131">En plus des nouveaux modèles en de nouveaux endroits, C# 8.0 ajoute des **modèles récursifs**.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-131">In addition to new patterns in new places, C# 8.0 adds **recursive patterns**.</span></span> <span data-ttu-id="6cc2d-132">Le résultat d’une expression de modèle est une expression.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-132">The result of any pattern expression is an expression.</span></span> <span data-ttu-id="6cc2d-133">Un modèle récursif constitue simplement une expression de modèle appliquée à la sortie d’une autre expression de modèle.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-133">A recursive pattern is simply a pattern expression applied to the output of another pattern expression.</span></span>

### <a name="switch-expressions"></a><span data-ttu-id="6cc2d-134">Expressions switch</span><span class="sxs-lookup"><span data-stu-id="6cc2d-134">switch expressions</span></span>

<span data-ttu-id="6cc2d-135">Souvent, une instruction [`switch`](../language-reference/keywords/switch.md) produit une valeur dans chacun de ses blocs `case`.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-135">Often, a [`switch`](../language-reference/keywords/switch.md) statement produces a value in each of its `case` blocks.</span></span> <span data-ttu-id="6cc2d-136">**Les expressions switch** permettent d’utiliser une syntaxe d’expression plus concise,</span><span class="sxs-lookup"><span data-stu-id="6cc2d-136">**Switch expressions** enable you to use more concise expression syntax.</span></span> <span data-ttu-id="6cc2d-137">comprenant moins de mots clés `case` et `break` répétitifs et moins d’accolades.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-137">There are fewer repetitive `case` and `break` keywords, and fewer curly braces.</span></span>  <span data-ttu-id="6cc2d-138">Prenons par exemple l’enum suivant, qui liste les couleurs de l’arc-en-ciel :</span><span class="sxs-lookup"><span data-stu-id="6cc2d-138">As an example, consider the following enum that lists the colors of the rainbow:</span></span>

```csharp
public enum Rainbow
{
    Red,
    Orange,
    Yellow,
    Green,
    Blue,
    Indigo,
    Violet
}
```

<span data-ttu-id="6cc2d-139">Si votre application a défini un type `RGBColor` construit à partir des composants `R`, `G` et `B`, vous pouvez convertir une valeur `Rainbow` en valeurs RVB avec la méthode suivante, qui contient une expression switch :</span><span class="sxs-lookup"><span data-stu-id="6cc2d-139">If your application defined an `RGBColor` type that is constructed from the `R`, `G` and `B` components, you could convert a `Rainbow` value to its RGB values using the following method containing a switch expression:</span></span>

```csharp
public static RGBColor FromRainbow(Rainbow colorBand) =>
    colorBand switch
    {
        Rainbow.Red    => new RGBColor(0xFF, 0x00, 0x00),
        Rainbow.Orange => new RGBColor(0xFF, 0x7F, 0x00),
        Rainbow.Yellow => new RGBColor(0xFF, 0xFF, 0x00),
        Rainbow.Green  => new RGBColor(0x00, 0xFF, 0x00),
        Rainbow.Blue   => new RGBColor(0x00, 0x00, 0xFF),
        Rainbow.Indigo => new RGBColor(0x4B, 0x00, 0x82),
        Rainbow.Violet => new RGBColor(0x94, 0x00, 0xD3),
        _              => throw new ArgumentException(message: "invalid enum value", paramName: nameof(colorBand)),
    };
```

<span data-ttu-id="6cc2d-140">Plusieurs améliorations ont ici été apportées à la syntaxe :</span><span class="sxs-lookup"><span data-stu-id="6cc2d-140">There are several syntax improvements here:</span></span>

- <span data-ttu-id="6cc2d-141">La variable se situe avant le mot clé `switch`.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-141">The variable comes before the `switch` keyword.</span></span> <span data-ttu-id="6cc2d-142">Ce nouvel ordre permet de distinguer visuellement l’expression switch de l’instruction switch.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-142">The different order makes it visually easy to distinguish the switch expression from the switch statement.</span></span>
- <span data-ttu-id="6cc2d-143">Les éléments `case` et `:` sont remplacés par `=>`,</span><span class="sxs-lookup"><span data-stu-id="6cc2d-143">The `case` and `:` elements are replaced with `=>`.</span></span> <span data-ttu-id="6cc2d-144">plus concis et plus intuitif.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-144">It's more concise and intuitive.</span></span>
- <span data-ttu-id="6cc2d-145">Le cas `default` est remplacé par un discard `_`.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-145">The `default` case is replaced with a `_` discard.</span></span>
- <span data-ttu-id="6cc2d-146">Les corps sont des expressions et non des instructions.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-146">The bodies are expressions, not statements.</span></span>

<span data-ttu-id="6cc2d-147">Comparez cela avec le code équivalent utilisant l’instruction `switch` classique :</span><span class="sxs-lookup"><span data-stu-id="6cc2d-147">Contrast that with the equivalent code using the classic `switch` statement:</span></span>

```csharp
public static RGBColor FromRainbowClassic(Rainbow colorBand)
{
    switch (colorBand)
    {
        case Rainbow.Red:
            return new RGBColor(0xFF, 0x00, 0x00);
        case Rainbow.Orange:
            return new RGBColor(0xFF, 0x7F, 0x00);
        case Rainbow.Yellow:
            return new RGBColor(0xFF, 0xFF, 0x00);
        case Rainbow.Green:
            return new RGBColor(0x00, 0xFF, 0x00);
        case Rainbow.Blue:
            return new RGBColor(0x00, 0x00, 0xFF);
        case Rainbow.Indigo:
            return new RGBColor(0x4B, 0x00, 0x82);
        case Rainbow.Violet:
            return new RGBColor(0x94, 0x00, 0xD3);
        default:
            throw new ArgumentException(message: "invalid enum value", paramName: nameof(colorBand));
    };
}
```

### <a name="property-patterns"></a><span data-ttu-id="6cc2d-148">Modèles de propriétés</span><span class="sxs-lookup"><span data-stu-id="6cc2d-148">Property patterns</span></span>

<span data-ttu-id="6cc2d-149">Le **modèle de propriété** permet de faire correspondre les propriétés de l’objet examiné.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-149">The **property pattern** enables you to match on properties of the object examined.</span></span> <span data-ttu-id="6cc2d-150">Prenons un site d’e-commerce qui doit calculer les taxes sur les ventes en fonction de l’adresse de l’acheteur.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-150">Consider an eCommerce site that must compute sales tax based on the buyer's address.</span></span> <span data-ttu-id="6cc2d-151">Ce calcul ne fait pas partie des attributions fondamentales d’une classe `Address`.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-151">That computation is not a core responsibility of an `Address` class.</span></span> <span data-ttu-id="6cc2d-152">Il changera au fil du temps, probablement plus souvent que n’évoluera le format de l’adresse.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-152">It will change over time, likely more often than address format changes.</span></span> <span data-ttu-id="6cc2d-153">Le montant des taxes sur les ventes varie selon la propriété `State` de l’adresse.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-153">The amount of sales tax depends on the `State` property of the address.</span></span> <span data-ttu-id="6cc2d-154">La méthode suivante utilise le modèle de propriété pour calculer les taxes sur les ventes à partir de l’adresse et du prix :</span><span class="sxs-lookup"><span data-stu-id="6cc2d-154">The following method uses the property pattern to compute the sales tax from the address and the price:</span></span>

```csharp
public static decimal ComputeSalesTax(Address location, decimal salePrice) =>
    location switch
    {
        { State: "WA" } => salePrice * 0.06M,
        { State: "MN" } => salePrice * 0.75M,
        { State: "MI" } => salePrice * 0.05M,
        // other cases removed for brevity...
        _ => 0M
    };
```

<span data-ttu-id="6cc2d-155">Les critères spéciaux offrent une syntaxe concise pour exprimer cet algorithme.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-155">Pattern matching creates a concise syntax for expressing this algorithm.</span></span>

### <a name="tuple-patterns"></a><span data-ttu-id="6cc2d-156">Modèles de tuples</span><span class="sxs-lookup"><span data-stu-id="6cc2d-156">Tuple patterns</span></span>

<span data-ttu-id="6cc2d-157">Certains algorithmes dépendent de plusieurs entrées.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-157">Some algorithms depend on multiple inputs.</span></span> <span data-ttu-id="6cc2d-158">Les **modèles de tuples** permettent de basculer des unes aux autres en fonction de plusieurs valeurs exprimées sous forme de [tuple](../tuples.md).</span><span class="sxs-lookup"><span data-stu-id="6cc2d-158">**Tuple patterns** allow you to switch based on multiple values expressed as a [tuple](../tuples.md).</span></span>  <span data-ttu-id="6cc2d-159">Le code suivant montre une expression switch pour le jeu *Pierre-papier-ciseaux* :</span><span class="sxs-lookup"><span data-stu-id="6cc2d-159">The following code shows a switch expression for the game *rock, paper, scissors*:</span></span>

```csharp
public static string RockPaperScissors(string first, string second)
    => (first, second) switch
    {
        ("rock", "paper") => "rock is covered by paper. Paper wins.",
        ("rock", "scissors") => "rock breaks scissors. Rock wins.",
        ("paper", "rock") => "paper covers rock. Paper wins.",
        ("paper", "scissors") => "paper is cut by scissors. Scissors wins.",
        ("scissors", "rock") => "scissors is broken by rock. Rock wins.",
        ("scissors", "paper") => "scissors cuts paper. Scissors wins.",
        (_, _) => "tie"
    };
```

<span data-ttu-id="6cc2d-160">Les messages indiquent le vainqueur.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-160">The messages indicate the winner.</span></span> <span data-ttu-id="6cc2d-161">Le cas discard représente les trois combinaisons pour les égalités, ou d’autres entrées de texte.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-161">The discard case represents the three combinations for ties, or other text inputs.</span></span>

### <a name="positional-patterns"></a><span data-ttu-id="6cc2d-162">Modèles positionnels</span><span class="sxs-lookup"><span data-stu-id="6cc2d-162">Positional patterns</span></span>

<span data-ttu-id="6cc2d-163">Certains types comportent une méthode `Deconstruct` qui décompose ses propriétés en variables discrètes.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-163">Some types include a `Deconstruct` method that deconstructs its properties into discrete variables.</span></span> <span data-ttu-id="6cc2d-164">Lorsqu’une méthode `Deconstruct` est accessible, il est possible d’utiliser des **modèles positionnels** pour inspecter les propriétés de l’objet et de se servir de ces dernières pour un modèle.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-164">When a `Deconstruct` method is accessible, you can use **positional patterns** to inspect properties of the object and use those properties for a pattern.</span></span>  <span data-ttu-id="6cc2d-165">Considérez la classe `Point` suivante, dont la méthode `Deconstruct` sert à créer des variables discrètes pour `X` et `Y` :</span><span class="sxs-lookup"><span data-stu-id="6cc2d-165">Consider the following `Point` class that includes a `Deconstruct` method to create discrete variables for `X` and `Y`:</span></span>

```csharp
public class Point
{
    public int X { get; }
    public int Y { get; }

    public Point(int x, int y) => (X, Y) = (x, y);

    public void Deconstruct(out int x, out int y) =>
        (x, y) = (X, Y);
}
```

<span data-ttu-id="6cc2d-166">De plus, envisagez l’énumération suivante qui représente diverses positions d’un quadrant :</span><span class="sxs-lookup"><span data-stu-id="6cc2d-166">Additionally, consider the following enum that represents various positions of a quadrant:</span></span>

```csharp
public enum Quadrant
{
    Unknown,
    Origin,
    One,
    Two,
    Three,
    Four,
    OnBorder
}
```

<span data-ttu-id="6cc2d-167">La méthode suivante utilise le **modèle positionnel** pour extraire les valeurs de `x` et de `y`.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-167">The following method uses the **positional pattern** to extract the values of `x` and `y`.</span></span> <span data-ttu-id="6cc2d-168">Ensuite, elle utilise une clause `when` pour déterminer le `Quadrant` du point :</span><span class="sxs-lookup"><span data-stu-id="6cc2d-168">Then, it uses a `when` clause to determine the `Quadrant` of the point:</span></span>

```csharp
static Quadrant GetQuadrant(Point point) => point switch
{
    (0, 0) => Quadrant.Origin,
    var (x, y) when x > 0 && y > 0 => Quadrant.One,
    var (x, y) when x < 0 && y > 0 => Quadrant.Two,
    var (x, y) when x < 0 && y < 0 => Quadrant.Three,
    var (x, y) when x > 0 && y < 0 => Quadrant.Four,
    var (_, _) => Quadrant.OnBorder,
    _ => Quadrant.Unknown
};
```

<span data-ttu-id="6cc2d-169">Le modèle discard dans le switch précédent indique une correspondance lorsque soit `x`, soit `y` est égal à 0, mais pas les deux.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-169">The discard pattern in the preceding switch matches when either `x` or `y` is 0, but not both.</span></span> <span data-ttu-id="6cc2d-170">Une expression switch doit produire une valeur ou,</span><span class="sxs-lookup"><span data-stu-id="6cc2d-170">A switch expression must either produce a value or throw an exception.</span></span> <span data-ttu-id="6cc2d-171">si aucun des cas ne correspond, lever une exception.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-171">If none of the cases match, the switch expression throws an exception.</span></span> <span data-ttu-id="6cc2d-172">Le compilateur génère un avertissement si tous les cas possibles ne sont pas couverts dans l’expression switch.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-172">The compiler generates a warning for you if you do not cover all possible cases in your switch expression.</span></span>

<span data-ttu-id="6cc2d-173">Vous pouvez explorer des techniques de critères spéciaux dans ce [tutoriel avancé sur les critères spéciaux](../tutorials/pattern-matching.md).</span><span class="sxs-lookup"><span data-stu-id="6cc2d-173">You can explore pattern matching techniques in this [advanced tutorial on pattern matching](../tutorials/pattern-matching.md).</span></span>

## <a name="using-declarations"></a><span data-ttu-id="6cc2d-174">Déclarations using</span><span class="sxs-lookup"><span data-stu-id="6cc2d-174">using declarations</span></span>

<span data-ttu-id="6cc2d-175">Une **déclaration using** est une déclaration de variable précédée par le mot clé `using`.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-175">A **using declaration** is a variable declaration preceded by the `using` keyword.</span></span> <span data-ttu-id="6cc2d-176">Elle indique au compilateur que la variable déclarée doit être supprimée à la fin de la portée englobante.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-176">It tells the compiler that the variable being declared should be disposed at the end of the enclosing scope.</span></span> <span data-ttu-id="6cc2d-177">Prenons par exemple le code suivant, qui écrit un fichier texte :</span><span class="sxs-lookup"><span data-stu-id="6cc2d-177">For example, consider the following code that writes a text file:</span></span>

```csharp
static void WriteLinesToFile(IEnumerable<string> lines)
{
    using var file = new System.IO.StreamWriter("WriteLines2.txt");
    foreach (string line in lines)
    {
        // If the line doesn't contain the word 'Second', write the line to the file.
        if (!line.Contains("Second"))
        {
            file.WriteLine(line);
        }
    }
// file is disposed here
}
```

<span data-ttu-id="6cc2d-178">Dans l’exemple précédent, le fichier est supprimé une fois l’accolade fermante de la méthode atteinte.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-178">In the preceding example, the file is disposed when the closing brace for the method is reached.</span></span> <span data-ttu-id="6cc2d-179">C’est la fin de la portée dans laquelle `file` est déclaré.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-179">That's the end of the scope in which `file` is declared.</span></span> <span data-ttu-id="6cc2d-180">Le code précédent équivaut au suivant, qui utilise des [instructions using](../language-reference/keywords/using-statement.md) classiques :</span><span class="sxs-lookup"><span data-stu-id="6cc2d-180">The preceding code is equivalent to the following code using the classic [using statements](../language-reference/keywords/using-statement.md) statement:</span></span>

```csharp
static void WriteLinesToFile(IEnumerable<string> lines)
{
    using (var file = new System.IO.StreamWriter("WriteLines2.txt"))
    {
        foreach (string line in lines)
        {
            // If the line doesn't contain the word 'Second', write the line to the file.
            if (!line.Contains("Second"))
            {
                file.WriteLine(line);
            }
        }
    } // file is disposed here
}
```

<span data-ttu-id="6cc2d-181">Dans l’exemple précédent, le fichier est supprimé une fois l’accolade fermante associée à l’instruction `using` atteinte.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-181">In the preceding example, the file is disposed when the closing brace associated with the `using` statement is reached.</span></span>

<span data-ttu-id="6cc2d-182">Dans les deux cas, le compilateur génère l’appel à `Dispose()`.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-182">In both cases, the compiler generates the call to `Dispose()`.</span></span> <span data-ttu-id="6cc2d-183">Il soulève une erreur si l’expression qui se trouve dans l’instruction using n’est pas jetable.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-183">The compiler generates an error if the expression in the using statement is not disposable.</span></span>

## <a name="static-local-functions"></a><span data-ttu-id="6cc2d-184">Fonctions locales statiques</span><span class="sxs-lookup"><span data-stu-id="6cc2d-184">Static local functions</span></span>

<span data-ttu-id="6cc2d-185">Il est maintenant possible d’ajouter le modificateur `static` à des fonctions locales pour éviter qu’elles ne capturent (fassent référence à) des variables au sein de la portée englobante.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-185">You can now add the `static` modifier to local functions to ensure that local function doesn't capture (reference) any variables from the enclosing scope.</span></span> <span data-ttu-id="6cc2d-186">Cela génère `CS8421`, « A static local function can’t contain a reference to \< variable> ».</span><span class="sxs-lookup"><span data-stu-id="6cc2d-186">Doing so generates `CS8421`, "A static local function can't contain a reference to \<variable>."</span></span> 

<span data-ttu-id="6cc2d-187">Prenons le code suivant.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-187">Consider the following code.</span></span> <span data-ttu-id="6cc2d-188">La fonction locale `LocalFunction` accède à la variable `y`, déclarée dans la portée englobante (la méthode `M`).</span><span class="sxs-lookup"><span data-stu-id="6cc2d-188">The local function `LocalFunction` accesses the variable `y`, declared in the enclosing scope (the method `M`).</span></span> <span data-ttu-id="6cc2d-189">Par conséquent, `LocalFunction` ne peut pas être déclarée avec le modificateur `static` :</span><span class="sxs-lookup"><span data-stu-id="6cc2d-189">Therefore, `LocalFunction` can't be declared with the `static` modifier:</span></span>

```csharp
int M()
{
    int y;
    LocalFunction();
    return y;

    void LocalFunction() => y = 0;
}
```

<span data-ttu-id="6cc2d-190">Le code suivant contient une fonction locale statique.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-190">The following code contains a static local function.</span></span> <span data-ttu-id="6cc2d-191">Elle peut être statique, car elle n’accède à aucune variable dans la portée englobante :</span><span class="sxs-lookup"><span data-stu-id="6cc2d-191">It can be static because it doesn't access any variables in the enclosing scope:</span></span>

```csharp
int M()
{
    int y = 5;
    int x = 7;
    return Add(x, y);

    static int Add(int left, int right) => left + right;
}
```

## <a name="disposable-ref-structs"></a><span data-ttu-id="6cc2d-192">Structs ref jetables</span><span class="sxs-lookup"><span data-stu-id="6cc2d-192">Disposable ref structs</span></span>

<span data-ttu-id="6cc2d-193">Comme un `struct` déclaré avec le modificateur `ref` ne peut pas implémenter d’interfaces, il ne peut pas implémenter <xref:System.IDisposable>.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-193">A `struct` declared with the `ref` modifier may not implement any interfaces and so cannot implement <xref:System.IDisposable>.</span></span> <span data-ttu-id="6cc2d-194">Par conséquent, pour qu’un `ref struct` soit supprimable, il doit avoir une méthode `void Dispose()` accessible.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-194">Therefore, to enable a `ref struct` to be disposed, it must have an accessible `void Dispose()` method.</span></span> <span data-ttu-id="6cc2d-195">Cela s’applique également aux déclarations `readonly ref struct`.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-195">This also applies to `readonly ref struct` declarations.</span></span>

## <a name="nullable-reference-types"></a><span data-ttu-id="6cc2d-196">Types références Nullables</span><span class="sxs-lookup"><span data-stu-id="6cc2d-196">Nullable reference types</span></span>

<span data-ttu-id="6cc2d-197">Dans un contexte d’annotation Nullable, toute variable d’un type référence est considérée comme un **type référence n'acceptant pas la valeur Null**.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-197">Inside a nullable annotation context, any variable of a reference type is considered to be a **nonnullable reference type**.</span></span> <span data-ttu-id="6cc2d-198">Si vous souhaitez indiquer qu’une variable peut être Null, ajoutez `?` au nom de type pour la déclarer comme **type référence Nullable**.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-198">If you want to indicate that a variable may be null, you must append the type name with the `?` to declare the variable as a **nullable reference type**.</span></span>

<span data-ttu-id="6cc2d-199">Avec les types références n'acceptant pas la valeur Null, le compilateur utilise l’analyse de flux pour que les variables locales soient initialisées à une valeur non Null une fois déclarées.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-199">For nonnullable reference types, the compiler uses flow analysis to ensure that local variables are initialized to a non-null value when declared.</span></span> <span data-ttu-id="6cc2d-200">Les champs doivent être initialisés à la construction.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-200">Fields must be initialized during construction.</span></span> <span data-ttu-id="6cc2d-201">Le compilateur génère un avertissement si la variable n’est pas définie par un appel à l’un des constructeurs disponibles ou par un initialiseur.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-201">The compiler generates a warning if the variable is not set by a call to any of the available constructors or by an initializer.</span></span> <span data-ttu-id="6cc2d-202">Par ailleurs, les types références n’acceptant pas la valeur Null ne peuvent pas avoir de valeur pouvant être Null.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-202">Furthermore, nonnullable reference types can't be assigned a value that could be null.</span></span>

<span data-ttu-id="6cc2d-203">Les types références Nullables font l’objet d’aucun contrôle visant à vérifier qu’ils ne sont pas affectés ou initialisées sur Null.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-203">Nullable reference types aren't checked to ensure they aren't assigned or initialized to null.</span></span> <span data-ttu-id="6cc2d-204">Toutefois, le compilateur utilise l’analyse de flux pour comparer à Null toutes les variables d’un type référence Nullable avant d’y accéder ou de lui affecter un type référence n’acceptant pas la valeur Null.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-204">However, the compiler uses flow analysis to ensure that any variable of a nullable reference type is checked against null before it's accessed or assigned to a nonnullable reference type.</span></span>

<span data-ttu-id="6cc2d-205">Plus d’informations sur la fonctionnalité, voir la vue d’ensemble des [types références Nullables](../nullable-references.md).</span><span class="sxs-lookup"><span data-stu-id="6cc2d-205">You can learn more about the feature in the overview of [nullable reference types](../nullable-references.md).</span></span> <span data-ttu-id="6cc2d-206">Essayez par vous-même dans une nouvelle application avec ce [tutoriel des types références Nullables](../tutorials/nullable-reference-types.md).</span><span class="sxs-lookup"><span data-stu-id="6cc2d-206">Try it yourself in a new application in this [nullable reference types tutorial](../tutorials/nullable-reference-types.md).</span></span> <span data-ttu-id="6cc2d-207">Pour plus d’informations sur le processus de migration d’un codebase dans l’objectif d’utiliser des types références Nullables, voir le [tutoriel Migrer une application pour utiliser des types références Nullables](../tutorials/upgrade-to-nullable-references.md).</span><span class="sxs-lookup"><span data-stu-id="6cc2d-207">Learn about the steps to migrate an existing codebase to make use of nullable reference types in the [migrating an application to use nullable reference types tutorial](../tutorials/upgrade-to-nullable-references.md).</span></span>

## <a name="asynchronous-streams"></a><span data-ttu-id="6cc2d-208">Flux asynchrones</span><span class="sxs-lookup"><span data-stu-id="6cc2d-208">Asynchronous streams</span></span>

<span data-ttu-id="6cc2d-209">À partir de C# 8.0, il est possible de créer et de consommer des flux de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-209">Starting with C# 8.0, you can create and consume streams asynchronously.</span></span> <span data-ttu-id="6cc2d-210">Une méthode qui retourne un flux asynchrone comporte trois propriétés :</span><span class="sxs-lookup"><span data-stu-id="6cc2d-210">A method that returns an asynchronous stream has three properties:</span></span>

1. <span data-ttu-id="6cc2d-211">Elle est déclarée avec le modificateur `async`.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-211">It's declared with the `async` modifier.</span></span>
1. <span data-ttu-id="6cc2d-212">Elle retourne un <xref:System.Collections.Generic.IAsyncEnumerable%601>.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-212">It returns an <xref:System.Collections.Generic.IAsyncEnumerable%601>.</span></span>
1. <span data-ttu-id="6cc2d-213">La méthode contient des instructions `yield return` pour retourner des éléments consécutifs dans le flux asynchrone.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-213">The method contains `yield return` statements to return successive elements in the asynchronous stream.</span></span>

<span data-ttu-id="6cc2d-214">Pour pouvoir consommer un flux asynchrone, il faut ajouter le mot clé `await` avant le mot clé `foreach` au moment d’énumérer les éléments du flux.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-214">Consuming an asynchronous stream requires you to add the `await` keyword before the `foreach` keyword when you enumerate the elements of the stream.</span></span> <span data-ttu-id="6cc2d-215">Le mot clé `await` exige que la méthode qui énumère le flux asynchrone soit déclarée avec le modificateur `async` et retourne un type autorisé pour une méthode `async`,</span><span class="sxs-lookup"><span data-stu-id="6cc2d-215">Adding the `await` keyword requires the method that enumerates the asynchronous stream to be declared with the `async` modifier and to return a type allowed for an `async` method.</span></span> <span data-ttu-id="6cc2d-216">soit en général <xref:System.Threading.Tasks.Task> ou <xref:System.Threading.Tasks.Task%601>.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-216">Typically that means returning a <xref:System.Threading.Tasks.Task> or <xref:System.Threading.Tasks.Task%601>.</span></span> <span data-ttu-id="6cc2d-217">Il peut également s’agir de <xref:System.Threading.Tasks.ValueTask> ou <xref:System.Threading.Tasks.ValueTask%601>.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-217">It can also be a <xref:System.Threading.Tasks.ValueTask> or <xref:System.Threading.Tasks.ValueTask%601>.</span></span> <span data-ttu-id="6cc2d-218">Une méthode peut consommer et produire un flux asynchrone ; elle retournerait alors un <xref:System.Collections.Generic.IAsyncEnumerable%601>.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-218">A method can both consume and produce an asynchronous stream, which means it would return an <xref:System.Collections.Generic.IAsyncEnumerable%601>.</span></span> <span data-ttu-id="6cc2d-219">Le code suivant génère une séquence de 0 à 19, en attendant 100 ms entre chaque nombre :</span><span class="sxs-lookup"><span data-stu-id="6cc2d-219">The following code generates a sequence from 0 to 19, waiting 100 ms between generating each number:</span></span>

```csharp
public static async System.Collections.Generic.IAsyncEnumerable<int> GenerateSequence()
{
    for (int i = 0; i < 20; i++)
    {
        await Task.Delay(100);
        yield return i;
    }
}
```

<span data-ttu-id="6cc2d-220">Pour énumérer la séquence, on utilise l’instruction `await foreach` :</span><span class="sxs-lookup"><span data-stu-id="6cc2d-220">You would enumerate the sequence using the `await foreach` statement:</span></span>

```csharp
await foreach (var number in GenerateSequence())
{
    Console.WriteLine(number);
}
```

<span data-ttu-id="6cc2d-221">Vous pouvez essayer par vous-même les flux asynchrones dans notre tutoriel [Créer et consommer des flux asynchrones](../tutorials/generate-consume-asynchronous-stream.md).</span><span class="sxs-lookup"><span data-stu-id="6cc2d-221">You can try asynchronous streams yourself in our tutorial on [creating and consuming async streams](../tutorials/generate-consume-asynchronous-stream.md).</span></span>

## <a name="indices-and-ranges"></a><span data-ttu-id="6cc2d-222">Index et plages</span><span class="sxs-lookup"><span data-stu-id="6cc2d-222">Indices and ranges</span></span>

<span data-ttu-id="6cc2d-223">Les plages et les index offrent une syntaxe concise pour spécifier des sous-plages dans un tableau, <xref:System.Span%601> ou <xref:System.ReadOnlySpan%601>.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-223">Ranges and indices provide a succinct syntax for specifying subranges in an array, <xref:System.Span%601>, or <xref:System.ReadOnlySpan%601>.</span></span>

<span data-ttu-id="6cc2d-224">Il est possible de spécifier un index **à partir de la fin**,</span><span class="sxs-lookup"><span data-stu-id="6cc2d-224">You can specify an index **from the end**.</span></span> <span data-ttu-id="6cc2d-225">Vous spécifiez **à partir de la fin** à l’aide de la `^` opérateur.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-225">You specify **from the end** using the `^` operator.</span></span> <span data-ttu-id="6cc2d-226">Vous connaissez déjà `array[2]`, qui signifie l’élément « 2 à partir du début ».</span><span class="sxs-lookup"><span data-stu-id="6cc2d-226">You are familiar with `array[2]` meaning the element "2 from the start".</span></span> <span data-ttu-id="6cc2d-227">Maintenant, `array[^2]` signifie que l’élément « 2 à partir de la fin ».</span><span class="sxs-lookup"><span data-stu-id="6cc2d-227">Now, `array[^2]` means the element "2 from the end".</span></span> <span data-ttu-id="6cc2d-228">L’index `^0` signifie « la fin », ou l’index qui suit le dernier élément.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-228">The index `^0` means "the end", or the index that follows the last element.</span></span>

<span data-ttu-id="6cc2d-229">Vous pouvez spécifier une **plage** avec **l’opérateur de plage** : `..`.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-229">You can specify a **range** with the **range operator**: `..`.</span></span> <span data-ttu-id="6cc2d-230">Par exemple, `0..^0` spécifie la totalité de la plage du tableau : 0 à partir du début jusqu'à 0 à partir de la fin non inclus.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-230">For example, `0..^0` specifies the entire range of the array: 0 from the start up to, but not including 0 from the end.</span></span> <span data-ttu-id="6cc2d-231">Les deux opérandes peuvent utiliser « à partir du début » ou « à partir de la fin ».</span><span class="sxs-lookup"><span data-stu-id="6cc2d-231">Either operand may use "from the start" or "from the end".</span></span> <span data-ttu-id="6cc2d-232">L’un comme l’autre peuvent être omis.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-232">Furthermore, either operand may be omitted.</span></span> <span data-ttu-id="6cc2d-233">Les valeurs par défaut sont `0` pour l’index de début et `^0` pour l’index de fin.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-233">The defaults are `0` for the start index, and `^0` for the end index.</span></span>

<span data-ttu-id="6cc2d-234">Prenons quelques exemples.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-234">Let's look at a few examples.</span></span> <span data-ttu-id="6cc2d-235">Examinez le tableau suivant, annoté avec son index à partir du début et de la fin :</span><span class="sxs-lookup"><span data-stu-id="6cc2d-235">Consider the following array, annotated with its index from the start and from the end:</span></span>

```csharp
var words = new string[]
{
                // index from start    index from end
    "The",      // 0                   ^9
    "quick",    // 1                   ^8
    "brown",    // 2                   ^7
    "fox",      // 3                   ^6
    "jumped",   // 4                   ^5
    "over",     // 5                   ^4
    "the",      // 6                   ^3
    "lazy",     // 7                   ^2
    "dog"       // 8                   ^1
};
```

<span data-ttu-id="6cc2d-236">L’index de chaque élément renforce le concept « à partir du début » et « à partir de la fin » ; ces plages excluent la fin de la plage.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-236">The index of each element reinforces the concept of "from the start", and "from the end", and that ranges are exclusive of the end of the range.</span></span> <span data-ttu-id="6cc2d-237">Le « début » de la totalité du tableau est le premier élément.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-237">The "start" of the entire array is the first element.</span></span> <span data-ttu-id="6cc2d-238">La « fin » de la totalité du tableau se trouve *après* le dernier élément.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-238">The "end" of the entire array is *past* the last element.</span></span>

<span data-ttu-id="6cc2d-239">Vous pouvez récupérer le dernier mot avec l’index `^1` :</span><span class="sxs-lookup"><span data-stu-id="6cc2d-239">You can retrieve the last word with the `^1` index:</span></span>

```csharp
Console.WriteLine($"The last word is {words[^1]}");
// writes "dog"
```

<span data-ttu-id="6cc2d-240">Le code suivant crée une sous-plage qui comporte les mots « quick », « brown » et « fox »</span><span class="sxs-lookup"><span data-stu-id="6cc2d-240">The following code creates a subrange with the words "quick", "brown", and "fox".</span></span> <span data-ttu-id="6cc2d-241">et va de `words[1]` à `words[3]`.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-241">It includes `words[1]` through `words[3]`.</span></span> <span data-ttu-id="6cc2d-242">L'élément `words[4]` ne se trouve pas dans la plage.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-242">The element `words[4]` is not in the range.</span></span>

```csharp
var quickBrownFox = words[1..4];
```

<span data-ttu-id="6cc2d-243">Le code suivant crée une sous-plage qui comporte « lazy » et « dog »</span><span class="sxs-lookup"><span data-stu-id="6cc2d-243">The following code creates a subrange with "lazy" and "dog".</span></span> <span data-ttu-id="6cc2d-244">et comprend `words[^2]` et `words[^1]`.</span><span class="sxs-lookup"><span data-stu-id="6cc2d-244">It includes `words[^2]` and `words[^1]`.</span></span> <span data-ttu-id="6cc2d-245">L’index de fin `words[^0]` n’est pas inclus :</span><span class="sxs-lookup"><span data-stu-id="6cc2d-245">The end index `words[^0]` is not included:</span></span>

```csharp
var lazyDog = words[^2..^0];
```

<span data-ttu-id="6cc2d-246">Les exemples suivants créent des plages ouvertes au début, à la fin ou les deux :</span><span class="sxs-lookup"><span data-stu-id="6cc2d-246">The following examples create ranges that are open ended for the start, end, or both:</span></span>

```csharp
var allWords = words[..]; // contains "The" through "dog".
var firstPhrase = words[..4]; // contains "The" through "fox"
var lastPhrase = words[6..]; // contains "the, "lazy" and "dog"
```

<span data-ttu-id="6cc2d-247">Vous pouvez également déclarer des plages comme variables :</span><span class="sxs-lookup"><span data-stu-id="6cc2d-247">You can also declare ranges as variables:</span></span>

```csharp
Range phrase = 1..4;
```

<span data-ttu-id="6cc2d-248">La plage peut ensuite être utilisée à l’intérieur des caractères `[` et `]` :</span><span class="sxs-lookup"><span data-stu-id="6cc2d-248">The range can then be used inside the `[` and `]` characters:</span></span>

```csharp
var text = words[phrase];
```
