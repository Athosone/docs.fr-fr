---
title: RelativeSource, extension de balisage
ms.date: 03/30/2017
f1_keywords:
- RelativeSource
helpviewer_keywords:
- RelativeSource markup extensions [WPF]
- XAML [WPF], RelativeSource markup extension
ms.assetid: 26be4721-49b5-4717-a92e-7d54ad0d3a81
ms.openlocfilehash: a6a7d615a3a54fbc75bb86b295fdf80433a31dc5
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62053494"
---
# <a name="relativesource-markupextension"></a><span data-ttu-id="2c984-102">RelativeSource, extension de balisage</span><span class="sxs-lookup"><span data-stu-id="2c984-102">RelativeSource MarkupExtension</span></span>

<span data-ttu-id="2c984-103">Spécifie les propriétés d’un <xref:System.Windows.Data.RelativeSource> source de liaison, à l’intérieur un [Extension de balisage de liaison](binding-markup-extension.md), ou lors de la définition la <xref:System.Windows.Data.Binding.RelativeSource%2A> propriété d’un <xref:System.Windows.Data.Binding> élément établie dans XAML.</span><span class="sxs-lookup"><span data-stu-id="2c984-103">Specifies properties of a <xref:System.Windows.Data.RelativeSource> binding source, to be used within a [Binding Markup Extension](binding-markup-extension.md), or when setting the <xref:System.Windows.Data.Binding.RelativeSource%2A> property of a <xref:System.Windows.Data.Binding> element established in XAML.</span></span>

## <a name="xaml-attribute-usage"></a><span data-ttu-id="2c984-104">Utilisation d'attributs XAML</span><span class="sxs-lookup"><span data-stu-id="2c984-104">XAML Attribute Usage</span></span>

```xml
<Binding RelativeSource="{RelativeSource modeEnumValue}" .../>
```

## <a name="xaml-attribute-usage-nested-within-binding-extension"></a><span data-ttu-id="2c984-105">Utilisation des attributs XAML (imbriqués dans l'extension de liaison)</span><span class="sxs-lookup"><span data-stu-id="2c984-105">XAML Attribute Usage (nested within Binding extension)</span></span>

```xml
<object property="{Binding RelativeSource={RelativeSource modeEnumValue} ...}" .../>
```

## <a name="xaml-object-element-usage"></a><span data-ttu-id="2c984-106">Utilisation d'éléments objet XAML</span><span class="sxs-lookup"><span data-stu-id="2c984-106">XAML Object Element Usage</span></span>

```xml
<Binding>
  <Binding.RelativeSource>
    <RelativeSource Mode="modeEnumValue"/>
  </Binding.RelativeSource>
</Binding>
```

<span data-ttu-id="2c984-107">- ou -</span><span class="sxs-lookup"><span data-stu-id="2c984-107">-or-</span></span>

```xml
<Binding>
  <Binding.RelativeSource>
    <RelativeSource
      Mode="FindAncestor"
      AncestorType="{x:Type typeName}"
      AncestorLevel="intLevel"
    />
  </Binding.RelativeSource>
</Binding>
```

## <a name="xaml-values"></a><span data-ttu-id="2c984-108">Valeurs XAML</span><span class="sxs-lookup"><span data-stu-id="2c984-108">XAML Values</span></span>

|||
|-|-|
|`modeEnumValue`|<span data-ttu-id="2c984-109">Une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="2c984-109">One of the following:</span></span><br /><br /> <span data-ttu-id="2c984-110">-Le jeton de chaîne `Self`; correspond à un <xref:System.Windows.Data.RelativeSource> comme créé avec sa <xref:System.Windows.Data.RelativeSource.Mode%2A> propriété définie sur <xref:System.Windows.Data.RelativeSourceMode.Self>.</span><span class="sxs-lookup"><span data-stu-id="2c984-110">-   The string token `Self`; corresponds to a <xref:System.Windows.Data.RelativeSource> as created with its <xref:System.Windows.Data.RelativeSource.Mode%2A> property set to <xref:System.Windows.Data.RelativeSourceMode.Self>.</span></span><br /><span data-ttu-id="2c984-111">-Le jeton de chaîne `TemplatedParent`; correspond à un <xref:System.Windows.Data.RelativeSource> comme créé avec sa <xref:System.Windows.Data.RelativeSource.Mode%2A> propriété définie sur <xref:System.Windows.Data.RelativeSourceMode.TemplatedParent>.</span><span class="sxs-lookup"><span data-stu-id="2c984-111">-   The string token `TemplatedParent`; corresponds to a <xref:System.Windows.Data.RelativeSource> as created with its <xref:System.Windows.Data.RelativeSource.Mode%2A> property set to <xref:System.Windows.Data.RelativeSourceMode.TemplatedParent>.</span></span><br /><span data-ttu-id="2c984-112">-Le jeton de chaîne `PreviousData`; correspond à un <xref:System.Windows.Data.RelativeSource> comme créé avec sa <xref:System.Windows.Data.RelativeSource.Mode%2A> propriété définie sur <xref:System.Windows.Data.RelativeSourceMode.PreviousData>.</span><span class="sxs-lookup"><span data-stu-id="2c984-112">-   The string token `PreviousData`; corresponds to a <xref:System.Windows.Data.RelativeSource> as created with its <xref:System.Windows.Data.RelativeSource.Mode%2A> property set to <xref:System.Windows.Data.RelativeSourceMode.PreviousData>.</span></span><br /><span data-ttu-id="2c984-113">-Voir ci-dessous pour plus d’informations sur `FindAncestor` mode.</span><span class="sxs-lookup"><span data-stu-id="2c984-113">-   See below for information on `FindAncestor` mode.</span></span>|
|`FindAncestor`|<span data-ttu-id="2c984-114">Le jeton de chaîne `FindAncestor`.</span><span class="sxs-lookup"><span data-stu-id="2c984-114">The string token `FindAncestor`.</span></span> <span data-ttu-id="2c984-115">L'utilisation de ce jeton accède à un mode dans lequel un `RelativeSource` spécifie un type d'ancêtre et, en option, un niveau d'ancêtre.</span><span class="sxs-lookup"><span data-stu-id="2c984-115">Using this token enters a mode whereby a `RelativeSource` specifies an ancestor type and optionally an ancestor level.</span></span> <span data-ttu-id="2c984-116">Ce correspond à un <xref:System.Windows.Data.RelativeSource> comme créé avec sa propriété <xref:System.Windows.Data.RelativeSource.Mode%2A> définie à <xref:System.Windows.Data.RelativeSourceMode.FindAncestor>.</span><span class="sxs-lookup"><span data-stu-id="2c984-116">This corresponds to a <xref:System.Windows.Data.RelativeSource> as created with its <xref:System.Windows.Data.RelativeSource.Mode%2A> property set to <xref:System.Windows.Data.RelativeSourceMode.FindAncestor>.</span></span>|
|`typeName`|<span data-ttu-id="2c984-117">Nécessaire pour le mode `FindAncestor`.</span><span class="sxs-lookup"><span data-stu-id="2c984-117">Required for `FindAncestor` mode.</span></span> <span data-ttu-id="2c984-118">Le nom d'un type, qui remplit la propriété <xref:System.Windows.Data.RelativeSource.AncestorType%2A>.</span><span class="sxs-lookup"><span data-stu-id="2c984-118">The name of a type, which fills the <xref:System.Windows.Data.RelativeSource.AncestorType%2A> property.</span></span>|
|`intLevel`|<span data-ttu-id="2c984-119">Facultatif pour le mode `FindAncestor`.</span><span class="sxs-lookup"><span data-stu-id="2c984-119">Optional for `FindAncestor` mode.</span></span> <span data-ttu-id="2c984-120">Un niveau d'ancêtre (évalué vers la direction du parent dans l'arborescence logique).</span><span class="sxs-lookup"><span data-stu-id="2c984-120">An ancestor level (evaluated towards the parent direction in the logical tree).</span></span>|

## <a name="remarks"></a><span data-ttu-id="2c984-121">Notes</span><span class="sxs-lookup"><span data-stu-id="2c984-121">Remarks</span></span>

<span data-ttu-id="2c984-122">`{RelativeSource TemplatedParent}` utilisations de liaison sont une technique principale qui traite un concept plus vaste de séparation de l’interface utilisateur d’un contrôle et une logique de contrôle.</span><span class="sxs-lookup"><span data-stu-id="2c984-122">`{RelativeSource TemplatedParent}` binding usages are a key technique that addresses a larger concept of the separation of a control's UI and a control's logic.</span></span> <span data-ttu-id="2c984-123">Cela permet la liaison à partir de la définition de modèle au parent basé sur des modèles (instance de l'objet à l'exécution où le modèle est appliqué).</span><span class="sxs-lookup"><span data-stu-id="2c984-123">This enables binding from within the template definition to the templated parent (the run time object instance where the template is applied).</span></span> <span data-ttu-id="2c984-124">Dans ce cas, le [Extension de balisage TemplateBinding](templatebinding-markup-extension.md) est en fait un raccourci pour l’expression de liaison suivante : `{Binding RelativeSource={RelativeSource TemplatedParent}}`.</span><span class="sxs-lookup"><span data-stu-id="2c984-124">For this case, the [TemplateBinding Markup Extension](templatebinding-markup-extension.md) is in fact a shorthand for the following binding expression: `{Binding RelativeSource={RelativeSource TemplatedParent}}`.</span></span> <span data-ttu-id="2c984-125">`TemplateBinding` ou `{RelativeSource TemplatedParent}` utilisations sont tous deux uniquement pertinents dans le XAML qui définit un modèle.</span><span class="sxs-lookup"><span data-stu-id="2c984-125">`TemplateBinding` or `{RelativeSource TemplatedParent}` usages are both only relevant within the XAML that defines a template.</span></span> <span data-ttu-id="2c984-126">Pour plus d’informations, consultez [Extension de balisage TemplateBinding](templatebinding-markup-extension.md)</span><span class="sxs-lookup"><span data-stu-id="2c984-126">For more information, see [TemplateBinding Markup Extension](templatebinding-markup-extension.md)</span></span>

<span data-ttu-id="2c984-127">`{RelativeSource FindAncestor}` est principalement utilisée dans les modèles de contrôle ou compositions de l’interface utilisateur autonomes prévisibles, pour les cas où un contrôle est toujours censé être dans une arborescence d’éléments visuels d’un certain type ancêtre.</span><span class="sxs-lookup"><span data-stu-id="2c984-127">`{RelativeSource FindAncestor}` is mainly used in control templates or predictable self-contained UI compositions, for cases where a control is always expected to be in a visual tree of a certain ancestor type.</span></span> <span data-ttu-id="2c984-128">Par exemple, les éléments d'un contrôle d'éléments peuvent utiliser des utilisations de `FindAncestor` pour les lier aux propriétés de leur ancêtre parent du contrôle d'éléments.</span><span class="sxs-lookup"><span data-stu-id="2c984-128">For example, items of an items control might use `FindAncestor` usages to bind to properties of their items control parent ancestor.</span></span> <span data-ttu-id="2c984-129">Ou les éléments qui font partie de la composition de contrôle dans un modèle peuvent utiliser des liaisons de `FindAncestor` aux éléments parents dans cette même structure de composition.</span><span class="sxs-lookup"><span data-stu-id="2c984-129">Or, elements that are part of control composition in a template can use `FindAncestor` bindings to the parent elements in that same composition structure.</span></span>

<span data-ttu-id="2c984-130">Dans la syntaxe d'élément objet du mode `FindAncestor` indiqué dans les sections de syntaxe XAML, la deuxième syntaxe d'élément objet est utilisée spécifiquement pour le mode `FindAncestor`.</span><span class="sxs-lookup"><span data-stu-id="2c984-130">In the object element syntax for `FindAncestor` mode shown in the XAML Syntax sections, the second object element syntax is used specifically for `FindAncestor` mode.</span></span> <span data-ttu-id="2c984-131">Le mode `FindAncestor` requiert une valeur <xref:System.Windows.Data.RelativeSource.AncestorType%2A>.</span><span class="sxs-lookup"><span data-stu-id="2c984-131">`FindAncestor` mode requires an <xref:System.Windows.Data.RelativeSource.AncestorType%2A> value.</span></span> <span data-ttu-id="2c984-132">Vous devez définir <xref:System.Windows.Data.RelativeSource.AncestorType%2A> comme un attribut utilisant un [x : Type Markup Extension](../../xaml-services/x-type-markup-extension.md) référence au type d’ancêtre à rechercher.</span><span class="sxs-lookup"><span data-stu-id="2c984-132">You must set <xref:System.Windows.Data.RelativeSource.AncestorType%2A> as an attribute using an [x:Type Markup Extension](../../xaml-services/x-type-markup-extension.md) reference to the type of ancestor to look for.</span></span> <span data-ttu-id="2c984-133">La valeur <xref:System.Windows.Data.RelativeSource.AncestorType%2A> est utilisée lorsque la demande de liaison est traitée lors de l'exécution.</span><span class="sxs-lookup"><span data-stu-id="2c984-133">The <xref:System.Windows.Data.RelativeSource.AncestorType%2A> value is used when the binding request is processed at run-time.</span></span>

<span data-ttu-id="2c984-134">Pour le mode `FindAncestor`, la propriété <xref:System.Windows.Data.RelativeSource.AncestorLevel%2A> facultative peut contribuer à désambiguïser la recherche d'ancêtre dans les cas où il existe peut-être plusieurs ancêtres de ce type présents dans l'arborescence d'éléments.</span><span class="sxs-lookup"><span data-stu-id="2c984-134">For `FindAncestor` mode, the optional property <xref:System.Windows.Data.RelativeSource.AncestorLevel%2A> can help disambiguate the ancestor lookup in cases where there is possibly more than one ancestor of that type existing in the element tree.</span></span>

<span data-ttu-id="2c984-135">Pour plus d'informations sur l'utilisation du mode `FindAncestor`, consultez <xref:System.Windows.Data.RelativeSource>.</span><span class="sxs-lookup"><span data-stu-id="2c984-135">For more information on how to use the `FindAncestor` mode, see <xref:System.Windows.Data.RelativeSource>.</span></span>

<span data-ttu-id="2c984-136">`{RelativeSource Self}` est utile pour les scénarios où une propriété d’une instance doit s’appuyer sur la valeur d’une autre propriété de la même instance et aucune relation de propriété de dépendance général (telle que la contrainte) déjà existe entre ces deux propriétés.</span><span class="sxs-lookup"><span data-stu-id="2c984-136">`{RelativeSource Self}` is useful for scenarios where one property of an instance should depend on the value of another property of the same instance, and no general dependency property relationship (such as coercion) already exists between those two properties.</span></span> <span data-ttu-id="2c984-137">Bien qu’il soit rare que deux propriétés existent sur un objet, telles que les valeurs sont littéralement identiques (et sont identiquement typées), vous pouvez également appliquer un `Converter` paramètre à une liaison qui a `{RelativeSource Self}`et utiliser le convertisseur pour convertir entre source et types de cibles.</span><span class="sxs-lookup"><span data-stu-id="2c984-137">Although it is rare that two properties exist on an object such that the values are literally identical (and are identically typed), you can also apply a `Converter` parameter to a binding that has `{RelativeSource Self}`, and use the converter to convert between source and target types.</span></span> <span data-ttu-id="2c984-138">Un autre scénario pour `{RelativeSource Self}` en tant qu’un <xref:System.Windows.MultiDataTrigger>.</span><span class="sxs-lookup"><span data-stu-id="2c984-138">Another scenario for `{RelativeSource Self}` is as part of a <xref:System.Windows.MultiDataTrigger>.</span></span>

<span data-ttu-id="2c984-139">Par exemple, le code XAML suivant définit un élément <xref:System.Windows.Shapes.Rectangle> tels que tout ce que la valeur est entrée pour <xref:System.Windows.FrameworkElement.Width%2A>, <xref:System.Windows.Shapes.Rectangle> est toujours angle droit : `<Rectangle Width="200" Height="{Binding RelativeSource={RelativeSource Self}, Path=Width}" .../>`</span><span class="sxs-lookup"><span data-stu-id="2c984-139">For example, the following XAML defines a <xref:System.Windows.Shapes.Rectangle> element such that no matter what value is entered for <xref:System.Windows.FrameworkElement.Width%2A>, the <xref:System.Windows.Shapes.Rectangle> is always a square: `<Rectangle Width="200" Height="{Binding RelativeSource={RelativeSource Self}, Path=Width}" .../>`</span></span>

<span data-ttu-id="2c984-140">`{RelativeSource PreviousData}` est utile dans les modèles de données ou dans les cas où les liaisons utilisent une collection comme source de données.</span><span class="sxs-lookup"><span data-stu-id="2c984-140">`{RelativeSource PreviousData}` is useful either in data templates, or in cases where bindings are using a collection as the data source.</span></span> <span data-ttu-id="2c984-141">Vous pouvez utiliser `{RelativeSource PreviousData}` pour mettre en évidence les relations entre les éléments de données adjacents dans la collection.</span><span class="sxs-lookup"><span data-stu-id="2c984-141">You can use `{RelativeSource PreviousData}` to highlight relationships between adjacent data items in the collection.</span></span> <span data-ttu-id="2c984-142">Une technique connexe est de générer <xref:System.Windows.Data.MultiBinding> entre des éléments actuels et précédents dans la source de données, et d'utiliser un convertisseur sur cette liaison pour déterminer la différence entre les deux éléments et leurs propriétés.</span><span class="sxs-lookup"><span data-stu-id="2c984-142">A related technique is to establish a <xref:System.Windows.Data.MultiBinding> between the current and previous items in the data source, and use a converter on that binding to determine the difference between the two items and their properties.</span></span>

<span data-ttu-id="2c984-143">Dans l'exemple suivant, le premier <xref:System.Windows.Controls.TextBlock> dans le modèle d'éléments affiche le numéro actuel.</span><span class="sxs-lookup"><span data-stu-id="2c984-143">In the following example, the first <xref:System.Windows.Controls.TextBlock> in the items template displays the current number.</span></span> <span data-ttu-id="2c984-144">La seconde <xref:System.Windows.Controls.TextBlock> liaison est un <xref:System.Windows.Data.MultiBinding> qui a nominalement deux <xref:System.Windows.Data.Binding> constituants : l’enregistrement en cours et une liaison qui utilise délibérément l’enregistrement de données précédent à l’aide de `{RelativeSource PreviousData}`.</span><span class="sxs-lookup"><span data-stu-id="2c984-144">The second <xref:System.Windows.Controls.TextBlock> binding is a <xref:System.Windows.Data.MultiBinding> that nominally has two <xref:System.Windows.Data.Binding> constituents: the current record, and a binding that deliberately uses the previous data record by using `{RelativeSource PreviousData}`.</span></span> <span data-ttu-id="2c984-145">Ensuite, un convertisseur sur <xref:System.Windows.Data.MultiBinding> calcule la différence et la retourne à la liaison.</span><span class="sxs-lookup"><span data-stu-id="2c984-145">Then, a converter on the <xref:System.Windows.Data.MultiBinding> calculates the difference and returns it to the binding.</span></span>

```xml
<ListBox Name="fibolist">
    <ListBox.ItemTemplate>
        <DataTemplate>
            <StackPanel Orientation="Horizontal">
            <TextBlock Text="{Binding}"/>
            <TextBlock>, difference = </TextBlock>
                <TextBlock>
                    <TextBlock.Text>
                        <MultiBinding Converter="{StaticResource DiffConverter}">
                            <Binding/>
                            <Binding RelativeSource="{RelativeSource PreviousData}"/>
                        </MultiBinding>
                    </TextBlock.Text>
                </TextBlock>
            </StackPanel>
        </DataTemplate>
    </ListBox.ItemTemplate>
```

<span data-ttu-id="2c984-146">Description de la liaison de données comme un concept n’est pas couverte ici, consultez [vue d’ensemble de la liaison de données](../data/data-binding-overview.md).</span><span class="sxs-lookup"><span data-stu-id="2c984-146">Describing data binding as a concept is not covered here, see [Data Binding Overview](../data/data-binding-overview.md).</span></span>

<span data-ttu-id="2c984-147">Dans le [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] implémentation du processeur XAML, la gestion de cette extension de balisage est définie par le <xref:System.Windows.Data.RelativeSource> classe.</span><span class="sxs-lookup"><span data-stu-id="2c984-147">In the [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] XAML processor implementation, the handling for this markup extension is defined by the <xref:System.Windows.Data.RelativeSource> class.</span></span>

<span data-ttu-id="2c984-148">`RelativeSource` est une extension de balisage.</span><span class="sxs-lookup"><span data-stu-id="2c984-148">`RelativeSource` is a markup extension.</span></span> <span data-ttu-id="2c984-149">Les extensions de balisage sont généralement implémentées pour éviter que les valeurs d’attribut ne soient autre chose que des valeurs littérales ou des noms de gestionnaire et lorsque l’exigence dépasse le cadre de la définition de convertisseurs de type sur certains types ou propriétés.</span><span class="sxs-lookup"><span data-stu-id="2c984-149">Markup extensions are typically implemented when there is a requirement to escape attribute values to be other than literal values or handler names, and the requirement is more global than just putting type converters on certain types or properties.</span></span> <span data-ttu-id="2c984-150">Toutes les extensions de balisage en cours d’utilisation XAML le `{` et `}` caractères dans leur syntaxe d’attribut, qui est la convention selon laquelle un processeur XAML reconnaît qu’une extension de balisage doit traiter l’attribut.</span><span class="sxs-lookup"><span data-stu-id="2c984-150">All markup extensions in XAML use the `{` and `}` characters in their attribute syntax, which is the convention by which a XAML processor recognizes that a markup extension must process the attribute.</span></span> <span data-ttu-id="2c984-151">Pour plus d’informations, consultez [Extensions de balisage et XAML WPF](markup-extensions-and-wpf-xaml.md).</span><span class="sxs-lookup"><span data-stu-id="2c984-151">For more information, see [Markup Extensions and WPF XAML](markup-extensions-and-wpf-xaml.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="2c984-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2c984-152">See also</span></span>

- <xref:System.Windows.Data.Binding>
- [<span data-ttu-id="2c984-153">Application d’un style et création de modèles</span><span class="sxs-lookup"><span data-stu-id="2c984-153">Styling and Templating</span></span>](../controls/styling-and-templating.md)
- [<span data-ttu-id="2c984-154">Vue d’ensemble du langage XAML (WPF)</span><span class="sxs-lookup"><span data-stu-id="2c984-154">XAML Overview (WPF)</span></span>](xaml-overview-wpf.md)
- [<span data-ttu-id="2c984-155">Extensions de balisage et XAML WPF</span><span class="sxs-lookup"><span data-stu-id="2c984-155">Markup Extensions and WPF XAML</span></span>](markup-extensions-and-wpf-xaml.md)
- [<span data-ttu-id="2c984-156">Vue d’ensemble de la liaison de données</span><span class="sxs-lookup"><span data-stu-id="2c984-156">Data Binding Overview</span></span>](../data/data-binding-overview.md)
- [<span data-ttu-id="2c984-157">Vue d'ensemble des déclarations de liaison</span><span class="sxs-lookup"><span data-stu-id="2c984-157">Binding Declarations Overview</span></span>](../data/binding-declarations-overview.md)
- [<span data-ttu-id="2c984-158">x:Type, extension de balisage</span><span class="sxs-lookup"><span data-stu-id="2c984-158">x:Type Markup Extension</span></span>](../../xaml-services/x-type-markup-extension.md)
