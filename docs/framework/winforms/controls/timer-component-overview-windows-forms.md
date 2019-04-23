---
title: Vue d'ensemble du composant Timer (Windows Forms)
ms.date: 03/30/2017
f1_keywords:
- Timer
helpviewer_keywords:
- Timer component [Windows Forms], about Timer components
- timers [Windows Forms], about timers
ms.assetid: e672c05b-a8b6-4b26-9e4d-9223aa9e3873
ms.openlocfilehash: 5bef0ba87d6a496acf7575965128be2b20b437ab
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59074207"
---
# <a name="timer-component-overview-windows-forms"></a><span data-ttu-id="d6794-102">Vue d'ensemble du composant Timer (Windows Forms)</span><span class="sxs-lookup"><span data-stu-id="d6794-102">Timer Component Overview (Windows Forms)</span></span>
<span data-ttu-id="d6794-103"><xref:System.Windows.Forms.Timer> est un composant Windows Forms qui déclenche un événement à intervalles réguliers.</span><span class="sxs-lookup"><span data-stu-id="d6794-103">The Windows Forms <xref:System.Windows.Forms.Timer> is a component that raises an event at regular intervals.</span></span> <span data-ttu-id="d6794-104">Ce composant est conçu pour un environnement Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="d6794-104">This component is designed for a Windows Forms environment.</span></span> <span data-ttu-id="d6794-105">Si vous avez besoin d’un minuteur adapté à un environnement de serveur, consultez l’article [Introduction aux minuteurs serveur](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2008/tb9yt5e6(v=vs.90)).</span><span class="sxs-lookup"><span data-stu-id="d6794-105">If you need a timer that is suitable for a server environment, see [Introduction to Server-Based Timers](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2008/tb9yt5e6(v=vs.90)).</span></span>  
  
## <a name="key-properties-methods-and-events"></a><span data-ttu-id="d6794-106">Événements, méthodes et propriétés de clé</span><span class="sxs-lookup"><span data-stu-id="d6794-106">Key Properties, Methods, and Events</span></span>  
 <span data-ttu-id="d6794-107">La durée des intervalles est définie par le <xref:System.Windows.Forms.Timer.Interval%2A> propriété, dont la valeur est exprimée en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="d6794-107">The length of the intervals is defined by the <xref:System.Windows.Forms.Timer.Interval%2A> property, whose value is in milliseconds.</span></span> <span data-ttu-id="d6794-108">Lorsque le composant est activé, le <xref:System.Windows.Forms.Timer.Tick> événement est déclenché chaque intervalle.</span><span class="sxs-lookup"><span data-stu-id="d6794-108">When the component is enabled, the <xref:System.Windows.Forms.Timer.Tick> event is raised every interval.</span></span> <span data-ttu-id="d6794-109">Voici où vous devez ajouter le code qui doit être exécuté.</span><span class="sxs-lookup"><span data-stu-id="d6794-109">This is where you would add code to be executed.</span></span> <span data-ttu-id="d6794-110">Pour plus d'informations, voir [Procédure : Exécuter des procédures à intervalles définis avec le composant Timer Windows Forms](run-procedures-at-set-intervals-with-wf-timer-component.md).</span><span class="sxs-lookup"><span data-stu-id="d6794-110">For more information, see [How to: Run Procedures at Set Intervals with the Windows Forms Timer Component](run-procedures-at-set-intervals-with-wf-timer-component.md).</span></span> <span data-ttu-id="d6794-111">Les principales méthodes de la <xref:System.Windows.Forms.Timer> composant sont <xref:System.Windows.Forms.Timer.Start%2A> et <xref:System.Windows.Forms.Timer.Stop%2A>, lequel activer le minuteur et désactiver.</span><span class="sxs-lookup"><span data-stu-id="d6794-111">The key methods of the <xref:System.Windows.Forms.Timer> component are <xref:System.Windows.Forms.Timer.Start%2A> and <xref:System.Windows.Forms.Timer.Stop%2A>, which turn the timer on and off.</span></span> <span data-ttu-id="d6794-112">Lorsque la minuterie est désactivée, elle est réinitialisée ; Il n’existe aucun moyen pour suspendre un <xref:System.Windows.Forms.Timer> composant.</span><span class="sxs-lookup"><span data-stu-id="d6794-112">When the timer is switched off, it resets; there is no way to pause a <xref:System.Windows.Forms.Timer> component.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d6794-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d6794-113">See also</span></span>

- <xref:System.Windows.Forms.Timer>
- [<span data-ttu-id="d6794-114">Timer, composant</span><span class="sxs-lookup"><span data-stu-id="d6794-114">Timer Component</span></span>](timer-component-windows-forms.md)
- [<span data-ttu-id="d6794-115">Restrictions relatives à la propriété Interval du composant Timer Windows Forms</span><span class="sxs-lookup"><span data-stu-id="d6794-115">Limitations of the Windows Forms Timer Component's Interval Property</span></span>](limitations-of-the-timer-component-interval-property.md)
