---
title: 'Procédure : Contrôler un MediaElement à l’aide d’une table de montage séquentiel'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- multimedia [WPF], controlling playback of media with Storyboards
- controlling playback of media [WPF], with Storyboards
- Storyboards [WPF], controlling playback of media with
- media [WPF], controlling playback with Storyboards
- playback of media [WPF], controlling with Storyboards
ms.assetid: 6128ca77-b826-4e36-b968-6f237157c543
ms.openlocfilehash: ae785e11b1da0f2c408b24021ad46ab071419378
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59100312"
---
# <a name="how-to-control-a-mediaelement-by-using-a-storyboard"></a><span data-ttu-id="e6a5a-102">Procédure : Contrôler un MediaElement à l’aide d’une table de montage séquentiel</span><span class="sxs-lookup"><span data-stu-id="e6a5a-102">How to: Control a MediaElement by Using a Storyboard</span></span>
<span data-ttu-id="e6a5a-103">Cet exemple montre comment contrôler un <xref:System.Windows.Controls.MediaElement> en utilisant un <xref:System.Windows.Media.MediaTimeline> dans un <xref:System.Windows.Media.Animation.Storyboard>.</span><span class="sxs-lookup"><span data-stu-id="e6a5a-103">This example shows how to control a <xref:System.Windows.Controls.MediaElement> by using a <xref:System.Windows.Media.MediaTimeline> in a <xref:System.Windows.Media.Animation.Storyboard>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="e6a5a-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="e6a5a-104">Example</span></span>  
 <span data-ttu-id="e6a5a-105">Lorsque vous utilisez un <xref:System.Windows.Media.MediaTimeline> dans un <xref:System.Windows.Media.Animation.Storyboard> pour contrôler le minutage d’une <xref:System.Windows.Controls.MediaElement>, les fonctionnalités sont identiques à celles des autres <xref:System.Windows.Media.Animation.Timeline> objets, tels que les animations.</span><span class="sxs-lookup"><span data-stu-id="e6a5a-105">When you use a <xref:System.Windows.Media.MediaTimeline> in a <xref:System.Windows.Media.Animation.Storyboard> to control the timing of a <xref:System.Windows.Controls.MediaElement>, the functionality is identical to the functionality of other <xref:System.Windows.Media.Animation.Timeline> objects, such as animations.</span></span> <span data-ttu-id="e6a5a-106">Par exemple, un <xref:System.Windows.Media.MediaTimeline> utilise <xref:System.Windows.Media.Animation.Timeline> propriétés telles que la <xref:System.Windows.Media.Animation.Timeline.BeginTime%2A> propriété pour indiquer quand commencer un <xref:System.Windows.Controls.MediaElement> (Démarrer la lecture du média).</span><span class="sxs-lookup"><span data-stu-id="e6a5a-106">For example, a <xref:System.Windows.Media.MediaTimeline> uses <xref:System.Windows.Media.Animation.Timeline> properties like the <xref:System.Windows.Media.Animation.Timeline.BeginTime%2A> property to specify when to start a <xref:System.Windows.Controls.MediaElement> (start media playback).</span></span> <span data-ttu-id="e6a5a-107">Il utilise également le <xref:System.Windows.Media.Animation.Timeline.Duration%2A> propriété pour spécifier la durée pendant laquelle le <xref:System.Windows.Controls.MediaElement> est actif (durée de lecture du média).</span><span class="sxs-lookup"><span data-stu-id="e6a5a-107">It also uses the <xref:System.Windows.Media.Animation.Timeline.Duration%2A> property to specify how long the <xref:System.Windows.Controls.MediaElement> is active (duration of media playback).</span></span> <span data-ttu-id="e6a5a-108">Pour plus d’informations sur l’utilisation de <xref:System.Windows.Media.Animation.Timeline> objets avec un <xref:System.Windows.Media.Animation.Storyboard>, consultez [vue d’ensemble des Storyboards](storyboards-overview.md).</span><span class="sxs-lookup"><span data-stu-id="e6a5a-108">For more information about using <xref:System.Windows.Media.Animation.Timeline> objects with a <xref:System.Windows.Media.Animation.Storyboard>, see [Storyboards Overview](storyboards-overview.md).</span></span>  
  
 <span data-ttu-id="e6a5a-109">Cet exemple montre comment créer un lecteur multimédia simple qui utilise un <xref:System.Windows.Media.MediaTimeline> pour contrôler la lecture.</span><span class="sxs-lookup"><span data-stu-id="e6a5a-109">This example shows how to create a simple media player that uses a <xref:System.Windows.Media.MediaTimeline> to control playback.</span></span> <span data-ttu-id="e6a5a-110">Le lecteur multimédia comprend play, suspendre, reprendre et arrêter des boutons.</span><span class="sxs-lookup"><span data-stu-id="e6a5a-110">The media player includes play, pause, resume, and stop buttons.</span></span> <span data-ttu-id="e6a5a-111">Le joueur a également un <xref:System.Windows.Controls.Slider> contrôle qui agit comme une barre de progression.</span><span class="sxs-lookup"><span data-stu-id="e6a5a-111">The player also has a <xref:System.Windows.Controls.Slider> control that acts as a progress bar.</span></span>  
  
 <span data-ttu-id="e6a5a-112">L’exemple suivant crée le [!INCLUDE[TLA#tla_ui](../../../../includes/tlasharptla-ui-md.md)] du lecteur multimédia.</span><span class="sxs-lookup"><span data-stu-id="e6a5a-112">The following example creates the [!INCLUDE[TLA#tla_ui](../../../../includes/tlasharptla-ui-md.md)] for the media player.</span></span>  
  
 [!code-xaml[MediaGallery_snip#MediaTimelineExampleWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/MediaGallery_snip/VB/MediaTimelineExample.xaml#mediatimelineexamplewholepage)]  
  
 <span data-ttu-id="e6a5a-113">L’exemple suivant crée les fonctionnalités de la barre de progression.</span><span class="sxs-lookup"><span data-stu-id="e6a5a-113">The following example creates the functionality for the progress bar.</span></span>  
  
 [!code-csharp[MediaGallery_snip#CodeBehindMediaTimelineExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/MediaGallery_snip/CSharp/MediaTimelineExample.xaml.cs#codebehindmediatimelineexamplewholepage)]
 [!code-vb[MediaGallery_snip#CodeBehindMediaTimelineExampleWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/MediaGallery_snip/VB/MediaTimelineExample.xaml.vb#codebehindmediatimelineexamplewholepage)]  
  
## <a name="see-also"></a><span data-ttu-id="e6a5a-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e6a5a-114">See also</span></span>

- <xref:System.Windows.Controls.MediaElement>
- <xref:System.Windows.Media.MediaTimeline>
- <xref:System.Windows.Media.Animation.Storyboard>
- [<span data-ttu-id="e6a5a-115">Contrôler un MediaElement (lecture, pause, arrêt, volume et vitesse)</span><span class="sxs-lookup"><span data-stu-id="e6a5a-115">Control a MediaElement (Play, Pause, Stop, Volume, and Speed)</span></span>](how-to-control-a-mediaelement-play-pause-stop-volume-and-speed.md)
- [<span data-ttu-id="e6a5a-116">Vue d'ensemble des plans conceptuels</span><span class="sxs-lookup"><span data-stu-id="e6a5a-116">Storyboards Overview</span></span>](storyboards-overview.md)
- [<span data-ttu-id="e6a5a-117">Vue d'ensemble des animations d'image clé</span><span class="sxs-lookup"><span data-stu-id="e6a5a-117">Key-Frame Animations Overview</span></span>](key-frame-animations-overview.md)
- [<span data-ttu-id="e6a5a-118">Vue d’ensemble de l’animation</span><span class="sxs-lookup"><span data-stu-id="e6a5a-118">Animation Overview</span></span>](animation-overview.md)
- [<span data-ttu-id="e6a5a-119">Rubriques de guide pratique</span><span class="sxs-lookup"><span data-stu-id="e6a5a-119">How-to Topics</span></span>](audio-and-video-how-to-topics.md)
- [<span data-ttu-id="e6a5a-120">Graphiques et multimédia</span><span class="sxs-lookup"><span data-stu-id="e6a5a-120">Graphics and Multimedia</span></span>](index.md)
