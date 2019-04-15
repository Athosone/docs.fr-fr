---
ms.openlocfilehash: cda5df4b673412a7c8c59f80f89c19c13dc81dc1
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59235277"
---
### <a name="accessing-a-wpf-datagrids-selected-items-from-a-handler-of-the-datagrids-unloadingrow-event-can-cause-a-nullreferenceexception"></a><span data-ttu-id="53670-101">L’accès aux éléments sélectionnés d’un DataGrid WPF à partir d’un gestionnaire de l’événement UnloadingRow du DataGrid peut provoquer une exception NullReferenceException</span><span class="sxs-lookup"><span data-stu-id="53670-101">Accessing a WPF DataGrid's selected items from a handler of the DataGrid's UnloadingRow event can cause a NullReferenceException</span></span>

|   |   |
|---|---|
|<span data-ttu-id="53670-102">Détails</span><span class="sxs-lookup"><span data-stu-id="53670-102">Details</span></span>|<span data-ttu-id="53670-103">En raison d’un bogue dans .NET Framework 4.5, les gestionnaires d’événements pour les événements <xref:System.Windows.Controls.DataGrid> impliquant la suppression d’une ligne peuvent entraîner la levée d’une <xref:System.NullReferenceException?displayProperty=name> s’ils accèdent aux propriétés <xref:System.Windows.Controls.Primitives.Selector.SelectedItem?displayProperty=name> ou <xref:System.Windows.Controls.Primitives.MultiSelector.SelectedItems?displayProperty=name> de <xref:System.Windows.Controls.DataGrid>.</span><span class="sxs-lookup"><span data-stu-id="53670-103">Due to a bug in the .NET Framework 4.5, event handlers for <xref:System.Windows.Controls.DataGrid> events involving the removal of a row can cause a <xref:System.NullReferenceException?displayProperty=name> to be thrown if they access the <xref:System.Windows.Controls.DataGrid>'s <xref:System.Windows.Controls.Primitives.Selector.SelectedItem?displayProperty=name> or <xref:System.Windows.Controls.Primitives.MultiSelector.SelectedItems?displayProperty=name> properties.</span></span>|
|<span data-ttu-id="53670-104">Suggestion</span><span class="sxs-lookup"><span data-stu-id="53670-104">Suggestion</span></span>|<span data-ttu-id="53670-105">Ce problème a été corrigé dans .NET Framework 4.6 et vous pouvez le résoudre en effectuant une mise à niveau vers cette version du .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="53670-105">This issue has been fixed in the .NET Framework 4.6 and may be addressed by upgrading to that version of the .NET Framework.</span></span>|
|<span data-ttu-id="53670-106">Portée</span><span class="sxs-lookup"><span data-stu-id="53670-106">Scope</span></span>|<span data-ttu-id="53670-107">Mineur</span><span class="sxs-lookup"><span data-stu-id="53670-107">Minor</span></span>|
|<span data-ttu-id="53670-108">Version</span><span class="sxs-lookup"><span data-stu-id="53670-108">Version</span></span>|<span data-ttu-id="53670-109">4.5</span><span class="sxs-lookup"><span data-stu-id="53670-109">4.5</span></span>|
|<span data-ttu-id="53670-110">Type</span><span class="sxs-lookup"><span data-stu-id="53670-110">Type</span></span>|<span data-ttu-id="53670-111">Runtime</span><span class="sxs-lookup"><span data-stu-id="53670-111">Runtime</span></span>|
|<span data-ttu-id="53670-112">API affectées</span><span class="sxs-lookup"><span data-stu-id="53670-112">Affected APIs</span></span>|<ul><li><xref:System.Windows.Controls.DataGrid.UnloadingRow?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.DataGrid.UnloadingRowDetails?displayProperty=nameWithType></li></ul>|
