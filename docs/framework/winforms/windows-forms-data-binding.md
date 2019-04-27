---
title: Liaison de données Windows Forms
ms.date: 03/30/2017
helpviewer_keywords:
- data [Windows Forms]
- Windows Forms, data binding
- data [Windows Forms], architecture
- Windows Forms controls, data binding
ms.assetid: c3826d8e-ea25-4ad4-a669-45bfb19192aa
ms.openlocfilehash: ed456807137e8cf7594bc50eb0eebb67b88e6b40
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61800111"
---
# <a name="windows-forms-data-binding"></a><span data-ttu-id="acbc7-102">Liaison de données Windows Forms</span><span class="sxs-lookup"><span data-stu-id="acbc7-102">Windows Forms Data Binding</span></span>
<span data-ttu-id="acbc7-103">La liaison de données dans les Windows Forms vous permet d'afficher et de modifier les informations d'une source de données dans les contrôles du formulaire.</span><span class="sxs-lookup"><span data-stu-id="acbc7-103">Data binding in Windows Forms gives you the means to display and make changes to information from a data source in controls on the form.</span></span> <span data-ttu-id="acbc7-104">Vous pouvez établir une liaison à une source de données traditionnelle et à presque toute structure qui contient des données.</span><span class="sxs-lookup"><span data-stu-id="acbc7-104">You can bind to both traditional data sources as well as almost any structure that contains data.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="acbc7-105">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="acbc7-105">In This Section</span></span>  
 [<span data-ttu-id="acbc7-106">Liaison de données et Windows Forms</span><span class="sxs-lookup"><span data-stu-id="acbc7-106">Data Binding and Windows Forms</span></span>](data-binding-and-windows-forms.md)  
 <span data-ttu-id="acbc7-107">Fournit une vue d’ensemble de la liaison de données dans les Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="acbc7-107">Provides an overview of data binding in Windows Forms.</span></span>  
  
 [<span data-ttu-id="acbc7-108">Sources de données prises en charge par les Windows Forms</span><span class="sxs-lookup"><span data-stu-id="acbc7-108">Data Sources Supported by Windows Forms</span></span>](data-sources-supported-by-windows-forms.md)  
 <span data-ttu-id="acbc7-109">Décrit les sources de données qui peuvent être utilisées avec Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="acbc7-109">Describes the data sources that can be used with Windows Forms.</span></span>  
  
 [<span data-ttu-id="acbc7-110">Interfaces participant à la liaison de données</span><span class="sxs-lookup"><span data-stu-id="acbc7-110">Interfaces Related to Data Binding</span></span>](interfaces-related-to-data-binding.md)  
 <span data-ttu-id="acbc7-111">Décrit plusieurs interfaces utilisées avec la liaison de données Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="acbc7-111">Describes several of the interfaces used with Windows Forms data binding.</span></span>  
  
 [<span data-ttu-id="acbc7-112">Guide pratique pour Naviguer parmi les données dans les Windows Forms</span><span class="sxs-lookup"><span data-stu-id="acbc7-112">How to: Navigate Data in Windows Forms</span></span>](how-to-navigate-data-in-windows-forms.md)  
 <span data-ttu-id="acbc7-113">Montre comment parcourir les éléments dans une source de données.</span><span class="sxs-lookup"><span data-stu-id="acbc7-113">Shows how to navigate through items in a data source.</span></span>  
  
 [<span data-ttu-id="acbc7-114">Notification de modifications dans la liaison de données Windows Forms</span><span class="sxs-lookup"><span data-stu-id="acbc7-114">Change Notification in Windows Forms Data Binding</span></span>](change-notification-in-windows-forms-data-binding.md)  
 <span data-ttu-id="acbc7-115">Décrit les différents types de notifications de modifications pour la liaison de données Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="acbc7-115">Describes different types of change notification for Windows Forms data binding.</span></span>  
  
 [<span data-ttu-id="acbc7-116">Guide pratique pour Implémenter l’Interface INotifyPropertyChanged</span><span class="sxs-lookup"><span data-stu-id="acbc7-116">How to: Implement the INotifyPropertyChanged Interface</span></span>](how-to-implement-the-inotifypropertychanged-interface.md)  
 <span data-ttu-id="acbc7-117">Montre comment implémenter l'interface <xref:System.ComponentModel.INotifyPropertyChanged>.</span><span class="sxs-lookup"><span data-stu-id="acbc7-117">Shows how to implement the <xref:System.ComponentModel.INotifyPropertyChanged> interface.</span></span> <span data-ttu-id="acbc7-118">L'interface communique à un contrôle dépendant les modifications apportées aux propriétés d'un objet métier.</span><span class="sxs-lookup"><span data-stu-id="acbc7-118">The interface  communicates to a bound control the property changes on a business object</span></span>  
  
 [<span data-ttu-id="acbc7-119">Guide pratique pour Appliquer le modèle PropertyNameChanged</span><span class="sxs-lookup"><span data-stu-id="acbc7-119">How to: Apply the PropertyNameChanged Pattern</span></span>](how-to-apply-the-propertynamechanged-pattern.md)  
 <span data-ttu-id="acbc7-120">Montre comment appliquer le *PropertyName*modèle Changed aux propriétés d’un contrôle utilisateur Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="acbc7-120">Shows how to apply the *PropertyName*Changed pattern to properties of a Windows Forms user control.</span></span>  
  
 [<span data-ttu-id="acbc7-121">Guide pratique pour Implémenter l’Interface ITypedList</span><span class="sxs-lookup"><span data-stu-id="acbc7-121">How to: Implement the ITypedList Interface</span></span>](how-to-implement-the-itypedlist-interface.md)  
 <span data-ttu-id="acbc7-122">Montre comment activer la découverte du schéma pour une liste pouvant être liée en implémentant l'interface <xref:System.ComponentModel.ITypedList>.</span><span class="sxs-lookup"><span data-stu-id="acbc7-122">Shows how to enable discovery of the schema for a bindable list by implementing the <xref:System.ComponentModel.ITypedList> interface.</span></span>  
  
 [<span data-ttu-id="acbc7-123">Guide pratique pour Implémenter l’Interface IListSource</span><span class="sxs-lookup"><span data-stu-id="acbc7-123">How to: Implement the IListSource Interface</span></span>](how-to-implement-the-ilistsource-interface.md)  
 <span data-ttu-id="acbc7-124">Montre comment implémenter l'interface <xref:System.ComponentModel.IListSource> pour créer une classe pouvant être liée qui n'implémente pas <xref:System.Collections.IList> mais fournit une liste à partir d'un autre emplacement.</span><span class="sxs-lookup"><span data-stu-id="acbc7-124">Shows how to implement the <xref:System.ComponentModel.IListSource> interface to create a bindable class does not implement <xref:System.Collections.IList>, but provides a list from another location.</span></span>  
  
 [<span data-ttu-id="acbc7-125">Guide pratique pour S’assurer que plusieurs contrôles liés à la même Source de données restent synchronisés</span><span class="sxs-lookup"><span data-stu-id="acbc7-125">How to: Ensure Multiple Controls Bound to the Same Data Source Remain Synchronized</span></span>](multiple-controls-bound-to-data-source-synchronized.md)  
 <span data-ttu-id="acbc7-126">Montre comment gérer l’événement <xref:System.Windows.Forms.BindingSource.BindingComplete> pour garantir que tous les contrôles liés à une source de données restent synchronisés.</span><span class="sxs-lookup"><span data-stu-id="acbc7-126">Shows how to handle the <xref:System.Windows.Forms.BindingSource.BindingComplete> event to ensure all controls bound to a data source remain synchronized.</span></span>  
  
 [<span data-ttu-id="acbc7-127">Guide pratique pour S’assurer que la ligne sélectionnée dans une Table enfant reste au bon emplacement</span><span class="sxs-lookup"><span data-stu-id="acbc7-127">How to: Ensure the Selected Row in a Child Table Remains at the Correct Position</span></span>](ensure-the-selected-row-in-a-child-table-correct.md)  
 <span data-ttu-id="acbc7-128">Montre comment s'assurer que la ligne sélectionnée dans une table enfant ne change pas quand une modification est apportée à un champ de la table parente.</span><span class="sxs-lookup"><span data-stu-id="acbc7-128">Shows how to ensure the selected row of a child table does not change, when a change is made to a field of the parent table.</span></span>  
  
 <span data-ttu-id="acbc7-129">Consultez également [Interfaces associées à une liaison de données](interfaces-related-to-data-binding.md), [Comment : Naviguer parmi les données dans les Windows Forms](how-to-navigate-data-in-windows-forms.md), et [Comment : Créer un contrôle de liaison Simple dans un formulaire Windows](how-to-create-a-simple-bound-control-on-a-windows-form.md).</span><span class="sxs-lookup"><span data-stu-id="acbc7-129">Also see [Interfaces Related to Data Binding](interfaces-related-to-data-binding.md), [How to: Navigate Data in Windows Forms](how-to-navigate-data-in-windows-forms.md), and [How to: Create a Simple-Bound Control on a Windows Form](how-to-create-a-simple-bound-control-on-a-windows-form.md).</span></span>  
  
## <a name="reference"></a><span data-ttu-id="acbc7-130">Référence</span><span class="sxs-lookup"><span data-stu-id="acbc7-130">Reference</span></span>  
 <xref:System.Windows.Forms.Binding?displayProperty=nameWithType>  
 <span data-ttu-id="acbc7-131">Décrit la classe qui représente la liaison entre un composant pouvant être lié et une source de données.</span><span class="sxs-lookup"><span data-stu-id="acbc7-131">Describes the class that represents the binding between a bindable component and a data source.</span></span>  
  
 <xref:System.Windows.Forms.BindingSource?displayProperty=nameWithType>  
 <span data-ttu-id="acbc7-132">Décrit la classe qui encapsule une source de données pour la liaison à des contrôles.</span><span class="sxs-lookup"><span data-stu-id="acbc7-132">Describes the class that encapsulates a data source for binding to controls.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="acbc7-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="acbc7-133">Related Sections</span></span>  
 [<span data-ttu-id="acbc7-134">BindingSource, composant</span><span class="sxs-lookup"><span data-stu-id="acbc7-134">BindingSource Component</span></span>](./controls/bindingsource-component.md)  
 <span data-ttu-id="acbc7-135">Contient une liste de rubriques qui expliquent comment utiliser le composant <xref:System.Windows.Forms.BindingSource>.</span><span class="sxs-lookup"><span data-stu-id="acbc7-135">Contains a list of topics that demonstrate how to use the <xref:System.Windows.Forms.BindingSource> component.</span></span>  
  
 [<span data-ttu-id="acbc7-136">DataGridView, contrôle</span><span class="sxs-lookup"><span data-stu-id="acbc7-136">DataGridView Control</span></span>](./controls/datagridview-control-windows-forms.md)  
 <span data-ttu-id="acbc7-137">Fournit une liste de rubriques qui expliquent comment utiliser un contrôle datagrid pouvant être lié.</span><span class="sxs-lookup"><span data-stu-id="acbc7-137">Provides a list of topics that demonstrate how to use a bindable datagrid control.</span></span>  
  
 <span data-ttu-id="acbc7-138">Consultez également [l’accès à des données dans Visual Studio](/visualstudio/data-tools/accessing-data-in-visual-studio).</span><span class="sxs-lookup"><span data-stu-id="acbc7-138">Also see [Accessing Data in Visual Studio](/visualstudio/data-tools/accessing-data-in-visual-studio).</span></span>
