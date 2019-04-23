---
title: 'Procédure : Définir la durée d’une animation'
ms.date: 03/30/2017
helpviewer_keywords:
- animation [WPF], duration
- Timelines [WPF], description
- duration of animations [WPF]
ms.assetid: 155034ef-7d00-4416-a73c-b1713992d2eb
ms.openlocfilehash: bdae1689ffeb8c54d756b9debbd26d57a052892d
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59198788"
---
# <a name="how-to-set-a-duration-for-an-animation"></a><span data-ttu-id="f7208-102">Procédure : Définir la durée d’une animation</span><span class="sxs-lookup"><span data-stu-id="f7208-102">How to: Set a Duration for an Animation</span></span>
<span data-ttu-id="f7208-103">Un <xref:System.Windows.Media.Animation.Timeline> représente un segment de temps et la longueur de ce segment sont déterminées par la chronologie <xref:System.Windows.Duration>.</span><span class="sxs-lookup"><span data-stu-id="f7208-103">A <xref:System.Windows.Media.Animation.Timeline> represents a segment of time and the length of that segment is determined by the timeline's <xref:System.Windows.Duration>.</span></span> <span data-ttu-id="f7208-104">Quand un <xref:System.Windows.Media.Animation.Timeline> atteint la fin de sa durée, elle s’arrête.</span><span class="sxs-lookup"><span data-stu-id="f7208-104">When a <xref:System.Windows.Media.Animation.Timeline> reaches the end of its duration, it stops playing.</span></span> <span data-ttu-id="f7208-105">Si le <xref:System.Windows.Media.Animation.Timeline> a des chronologies enfants, celles-ci s’arrêtent également.</span><span class="sxs-lookup"><span data-stu-id="f7208-105">If the <xref:System.Windows.Media.Animation.Timeline> has child timelines, they stop playing as well.</span></span> <span data-ttu-id="f7208-106">Dans le cas d’une animation, la <xref:System.Windows.Duration> spécifie la durée pendant laquelle l’animation nécessaire pour passer de sa valeur initiale à sa valeur finale.</span><span class="sxs-lookup"><span data-stu-id="f7208-106">In the case of an animation, the <xref:System.Windows.Duration> specifies how long the animation takes to transition from its starting value to its ending value.</span></span>  
  
 <span data-ttu-id="f7208-107">Vous pouvez spécifier un <xref:System.Windows.Duration> avec une durée finie spécifique ou des valeurs spéciales <xref:System.Windows.Duration.Automatic%2A> ou <xref:System.Windows.Duration.Forever%2A>.</span><span class="sxs-lookup"><span data-stu-id="f7208-107">You can specify a <xref:System.Windows.Duration> with a specific, finite time or the special values <xref:System.Windows.Duration.Automatic%2A> or <xref:System.Windows.Duration.Forever%2A>.</span></span> <span data-ttu-id="f7208-108">Durée d’une animation doit toujours être une valeur de temps, car une animation doit toujours avoir une longueur finie spécifique, dans le cas contraire, l’animation ne serait pas capable d’effectuer la transition entre ses valeurs cibles.</span><span class="sxs-lookup"><span data-stu-id="f7208-108">An animation's duration must always be a time value, because an animation must always have a defined, finite length—otherwise, the animation would not know how to transition between its target values.</span></span> <span data-ttu-id="f7208-109">Les chronologies de conteneur (<xref:System.Windows.Media.Animation.TimelineGroup> objets), tel que <xref:System.Windows.Media.Animation.Storyboard> et <xref:System.Windows.Media.Animation.ParallelTimeline>, ont une durée par défaut de <xref:System.Windows.Duration.Automatic%2A>, ce qui signifie qu’elles se terminent automatiquement lorsque leur dernier enfant s’arrête.</span><span class="sxs-lookup"><span data-stu-id="f7208-109">Container timelines (<xref:System.Windows.Media.Animation.TimelineGroup> objects), such as <xref:System.Windows.Media.Animation.Storyboard> and <xref:System.Windows.Media.Animation.ParallelTimeline>, have a default duration of <xref:System.Windows.Duration.Automatic%2A>, which means they automatically end when their last child stops playing.</span></span>  
  
 <span data-ttu-id="f7208-110">Dans la couleur d’exemple, de la largeur, hauteur et remplissage suivante d’un <xref:System.Windows.Shapes.Rectangle> est animée.</span><span class="sxs-lookup"><span data-stu-id="f7208-110">In the following example, the width, height and fill color of a <xref:System.Windows.Shapes.Rectangle> is animated.</span></span> <span data-ttu-id="f7208-111">Les durées sont définies sur les chronologies d’animation et de conteneur entraînant des effets d’animation, y compris le contrôle de la vitesse perçue d’une animation et la substitution de la durée des chronologies enfants avec la durée d’une chronologie de conteneur.</span><span class="sxs-lookup"><span data-stu-id="f7208-111">Durations are set on animation and container timelines resulting in animation effects including controlling the perceived speed of an animation and overriding the duration of child timelines with the duration of a container timeline.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f7208-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="f7208-112">Example</span></span>  
 [!code-xaml[timingbehaviors_snip#DurationExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_snip/CSharp/DurationExample.xaml#durationexamplewholepage)]  
  
## <a name="see-also"></a><span data-ttu-id="f7208-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f7208-113">See also</span></span>

- <xref:System.Windows.Duration>
- [<span data-ttu-id="f7208-114">Vue d’ensemble de l’animation</span><span class="sxs-lookup"><span data-stu-id="f7208-114">Animation Overview</span></span>](animation-overview.md)
