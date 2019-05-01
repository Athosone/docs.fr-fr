---
title: Multithreading dans les contrôles Windows Forms
ms.date: 03/30/2017
helpviewer_keywords:
- BackgroundWorker component
- threading [Windows Forms], controls
ms.assetid: c311d652-0f26-45fa-bdcc-b1615d73ce4e
ms.openlocfilehash: cc7f358a62c8057abb77e1f5a28544bb6c858d98
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62012722"
---
# <a name="multithreading-in-windows-forms-controls"></a><span data-ttu-id="ef0af-102">Multithreading dans les contrôles Windows Forms</span><span class="sxs-lookup"><span data-stu-id="ef0af-102">Multithreading in Windows Forms Controls</span></span>
<span data-ttu-id="ef0af-103">Dans de nombreuses applications, vous pouvez rendre votre interface utilisateur (IU) plus réactive en effectuant les opérations de longue durée sur un autre thread.</span><span class="sxs-lookup"><span data-stu-id="ef0af-103">In many applications, you can make your user interface (UI) more responsive by performing time-consuming operations on another thread.</span></span> <span data-ttu-id="ef0af-104">Un certain nombre d’outils est disponible pour le multithreading vos contrôles Windows Forms, y compris le <xref:System.Threading> espace de noms, le <xref:System.Windows.Forms.Control.BeginInvoke%2A?displayProperty=nameWithType> (méthode) et le `BackgroundWorker` composant.</span><span class="sxs-lookup"><span data-stu-id="ef0af-104">A number of tools are available for multithreading your Windows Forms controls, including the <xref:System.Threading> namespace, the <xref:System.Windows.Forms.Control.BeginInvoke%2A?displayProperty=nameWithType> method, and the `BackgroundWorker` component.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="ef0af-105">Le `BackgroundWorker` composant remplace et ajoute des fonctionnalités à la <xref:System.Threading> espace de noms et le <xref:System.Windows.Forms.Control.BeginInvoke%2A?displayProperty=nameWithType> méthode ; Toutefois, ceux-ci sont conservés pour la compatibilité descendante et une utilisation ultérieure, si vous choisissez.</span><span class="sxs-lookup"><span data-stu-id="ef0af-105">The `BackgroundWorker` component replaces and adds functionality to the <xref:System.Threading> namespace and the <xref:System.Windows.Forms.Control.BeginInvoke%2A?displayProperty=nameWithType> method; however, these are retained for both backward compatibility and future use, if you choose.</span></span> <span data-ttu-id="ef0af-106">Pour plus d’informations, consultez [vue d’ensemble du composant BackgroundWorker](backgroundworker-component-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ef0af-106">For more information, see [BackgroundWorker Component Overview](backgroundworker-component-overview.md).</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="ef0af-107">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="ef0af-107">In This Section</span></span>  
 [<span data-ttu-id="ef0af-108">Guide pratique pour Effectuer des appels Thread-Safe aux contrôles de Windows Forms</span><span class="sxs-lookup"><span data-stu-id="ef0af-108">How to: Make Thread-Safe Calls to Windows Forms Controls</span></span>](how-to-make-thread-safe-calls-to-windows-forms-controls.md)  
 <span data-ttu-id="ef0af-109">Montre comment effectuer des appels thread-safe aux contrôles Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="ef0af-109">Shows how to make thread-safe calls to Windows Forms controls.</span></span>  
  
 [<span data-ttu-id="ef0af-110">Guide pratique pour Utiliser un Thread d’arrière-plan pour rechercher des fichiers</span><span class="sxs-lookup"><span data-stu-id="ef0af-110">How to: Use a Background Thread to Search for Files</span></span>](how-to-use-a-background-thread-to-search-for-files.md)  
 <span data-ttu-id="ef0af-111">Montre comment utiliser le <xref:System.Threading> espace de noms et le <xref:System.Windows.Forms.Control.BeginInvoke%2A> méthode pour rechercher les fichiers de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="ef0af-111">Shows how to use the <xref:System.Threading> namespace and the <xref:System.Windows.Forms.Control.BeginInvoke%2A> method to search for files asynchronously.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="ef0af-112">Référence</span><span class="sxs-lookup"><span data-stu-id="ef0af-112">Reference</span></span>  
 <xref:System.ComponentModel.BackgroundWorker>  
 <span data-ttu-id="ef0af-113">Documente un composant qui encapsule un thread de travail pour les opérations asynchrones.</span><span class="sxs-lookup"><span data-stu-id="ef0af-113">Documents a component that encapsulates a worker thread for asynchronous operations.</span></span>  
  
 <xref:System.Media.SoundPlayer.LoadAsync%2A>  
 <span data-ttu-id="ef0af-114">Décrit comment charger un son de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="ef0af-114">Documents how to load a sound asynchronously.</span></span>  
  
 <xref:System.Windows.Forms.PictureBox.LoadAsync%2A>  
 <span data-ttu-id="ef0af-115">Décrit comment charger une image de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="ef0af-115">Documents how to load an image asynchronously.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="ef0af-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ef0af-116">Related Sections</span></span>  
 [<span data-ttu-id="ef0af-117">Guide pratique pour exécuter une opération en arrière-plan</span><span class="sxs-lookup"><span data-stu-id="ef0af-117">How to: Run an Operation in the Background</span></span>](how-to-run-an-operation-in-the-background.md)  
 <span data-ttu-id="ef0af-118">Montre comment effectuer une opération longue avec le <xref:System.ComponentModel.BackgroundWorker> composant.</span><span class="sxs-lookup"><span data-stu-id="ef0af-118">Shows how to perform a time-consuming operation with the <xref:System.ComponentModel.BackgroundWorker> component.</span></span>  
  
 [<span data-ttu-id="ef0af-119">Vue d'ensemble du composant BackgroundWorker</span><span class="sxs-lookup"><span data-stu-id="ef0af-119">BackgroundWorker Component Overview</span></span>](backgroundworker-component-overview.md)  
 <span data-ttu-id="ef0af-120">Fournit des rubriques qui décrivent comment utiliser le <xref:System.ComponentModel.BackgroundWorker> composant pour les opérations asynchrones.</span><span class="sxs-lookup"><span data-stu-id="ef0af-120">Provides topics that describe how to use the <xref:System.ComponentModel.BackgroundWorker> component for asynchronous operations.</span></span>
