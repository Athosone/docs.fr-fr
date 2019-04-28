---
title: Vue d'ensemble de l'animation et du système de minutage
ms.date: 03/30/2017
helpviewer_keywords:
- timing system [WPF]
- animation [WPF]
ms.assetid: 172cd5a8-a333-4c81-9456-fafccc19f382
ms.openlocfilehash: f64431e7804ba6e068a3d05f512c6ead089d7712
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62020337"
---
# <a name="animation-and-timing-system-overview"></a>Vue d'ensemble de l'animation et du système de minutage
Cette rubrique décrit comment le système de minutage utilise l’animation, <xref:System.Windows.Media.Animation.Timeline>, et <xref:System.Windows.Media.Animation.Clock> classes pour animer des propriétés.  
  
<a name="prerequisites"></a>   
## <a name="prerequisites"></a>Prérequis  
 Pour comprendre cette rubrique, vous devez être en mesure d’utiliser des animations [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] pour animer des propriétés, comme décrit dans la [Vue d’ensemble de l’animation](animation-overview.md). Il est également conseillé de vous familiariser avec les propriétés de dépendance. Pour plus d’informations, consultez [Vue d’ensemble des propriétés de dépendance](../advanced/dependency-properties-overview.md).  
  
<a name="timelinesandclocks"></a>   
## <a name="timelines-and-clocks"></a>Chronologies et horloges  
 Le [vue d’ensemble de l’Animation](animation-overview.md) décrit comment un <xref:System.Windows.Media.Animation.Timeline> représente un segment de temps et d’une animation est un type de <xref:System.Windows.Media.Animation.Timeline> qui produit des valeurs de sortie. En soi, un <xref:System.Windows.Media.Animation.Timeline>, ne fait rien d’autre que décrire un segment de temps. Il s’agit de la chronologie <xref:System.Windows.Media.Animation.Clock> objet qui effectue le travail réel. De même, l’animation n’anime pas réellement propriétés : une classe d’animation décrit comment les valeurs de sortie doivent être calculées, mais il est le <xref:System.Windows.Media.Animation.Clock> qui a été créé pour l’animation qui achemine la sortie d’animation et l’applique aux propriétés.  
  
 Un <xref:System.Windows.Media.Animation.Clock> est un type spécial d’objet qui conserve l’état d’exécution de temporisation pour la <xref:System.Windows.Media.Animation.Timeline>. Il fournit trois éléments d’information qui sont essentielles à l’animation et le système de minutage : <xref:System.Windows.Media.Animation.Clock.CurrentTime%2A>, <xref:System.Windows.Media.Animation.Clock.CurrentProgress%2A>, et <xref:System.Windows.Media.Animation.Clock.CurrentState%2A>. Un <xref:System.Windows.Media.Animation.Clock> détermine l’heure actuelle, sa progression et l’état en utilisant les comportements de minutage décrits par sa <xref:System.Windows.Media.Animation.Timeline>: <xref:System.Windows.Media.Animation.Timeline.Duration%2A>, <xref:System.Windows.Media.Animation.Timeline.RepeatBehavior%2A>, <xref:System.Windows.Media.Animation.Timeline.AutoReverse%2A>, et ainsi de suite.  
  
 Dans la plupart des cas, un <xref:System.Windows.Media.Animation.Clock> est créé automatiquement pour votre chronologie. Lorsque vous animez en utilisant un <xref:System.Windows.Media.Animation.Storyboard> ou <xref:System.Windows.Media.Animation.Animatable.BeginAnimation%2A> (méthode), les horloges sont automatiquement créés pour vos chronologies et animations et appliquées à leurs propriétés ciblées. Vous pouvez également créer un <xref:System.Windows.Media.Animation.Clock> explicitement en utilisant la <xref:System.Windows.Media.Animation.Timeline.CreateClock%2A> méthode de votre <xref:System.Windows.Media.Animation.Timeline>. Le <xref:System.Windows.Media.MediaTimeline.CreateClock%2A?displayProperty=nameWithType> méthode crée une horloge du type approprié pour le <xref:System.Windows.Media.Animation.Timeline> sur laquelle elle est appelée. Si le <xref:System.Windows.Media.Animation.Timeline> contient des chronologies enfants, il crée <xref:System.Windows.Media.Animation.Clock> des objets pour eux. Résultant <xref:System.Windows.Media.Animation.Clock> objets sont organisés en arborescences qui correspondent à la structure de la <xref:System.Windows.Media.Animation.Timeline> arborescence des objets à partir de laquelle ils sont créés.  
  
 Il existe différents types d’horloges pour différents types de chronologies. Le tableau suivant présente le <xref:System.Windows.Media.Animation.Clock> types qui correspondent à certains des différents <xref:System.Windows.Media.Animation.Timeline> types.  
  
|Type de chronologie|Type d’horloge|Objectif de l’horloge|  
|-------------------|----------------|-------------------|  
|Animation (hérite de <xref:System.Windows.Media.Animation.AnimationTimeline>)|<xref:System.Windows.Media.Animation.AnimationClock>|Génère les valeurs de sortie d’une propriété de dépendance.|  
|<xref:System.Windows.Media.MediaTimeline>|<xref:System.Windows.Media.MediaClock>|Traite un fichier multimédia.|  
|<xref:System.Windows.Media.Animation.ParallelTimeline>|<xref:System.Windows.Media.Animation.ClockGroup>|Regroupe et contrôle son enfant <xref:System.Windows.Media.Animation.Clock> objets|  
|<xref:System.Windows.Media.Animation.Storyboard>|<xref:System.Windows.Media.Animation.ClockGroup>|Regroupe et contrôle son enfant <xref:System.Windows.Media.Animation.Clock> objets|  
  
 Vous pouvez appliquer les <xref:System.Windows.Media.Animation.AnimationClock> objets vous créez aux propriétés de dépendance compatibles en utilisant la <xref:System.Windows.Media.Animation.IAnimatable.ApplyAnimationClock%2A> (méthode).  
  
 Dans les scénarios exigeants en performances, tels que l’animation grand nombre d’objets semblables, la gestion de vos propres <xref:System.Windows.Media.Animation.Clock> utilisation peut améliorer les performances.  
  
<a name="timemanager"></a>   
## <a name="clocks-and-the-time-manager"></a>Horloges et gestionnaire de temps  
 Lorsque vous animez des objets dans [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)], il est le Gestionnaire de temps qui gère la <xref:System.Windows.Media.MediaPlayer.Clock%2A> objets créés pour vos chronologies. Le gestionnaire de temps est la racine d’une arborescence d’objets <xref:System.Windows.Media.MediaPlayer.Clock%2A> et contrôle le flux de temps dans cette arborescence.  Un gestionnaire de temps est créé automatiquement pour chaque application [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] et reste invisible au développeur d'applications. Le gestionnaire de temps a de nombreuses graduations par seconde. Le nombre réel de cycles qui se produisent à chaque seconde varie selon les ressources système disponibles. Pendant chacun de ces battements, le Gestionnaire de temps calcule l’état de tous les <xref:System.Windows.Media.Animation.ClockState.Active> <xref:System.Windows.Media.Animation.Clock> objets dans l’arborescence de minutage.  
  
 L’illustration suivante montre la relation entre le Gestionnaire de temps, et <xref:System.Windows.Media.Animation.AnimationClock>et une propriété de dépendance animée.  
  
 ![Composants du système de minutage](./media/graphicsmm-clocks-1clock1prop.png "graphicsmm_clocks_1clock1prop")  
Animation d’une propriété  
  
 Lorsque le Gestionnaire de temps effectue un battement, il met à jour l’heure de chaque <xref:System.Windows.Media.Animation.ClockState.Active> <xref:System.Windows.Media.Animation.Clock> dans l’application. Si le <xref:System.Windows.Media.Animation.Clock> est un <xref:System.Windows.Media.Animation.AnimationClock>, il utilise le <xref:System.Windows.Media.Animation.AnimationTimeline.GetCurrentValue%2A> méthode de la <xref:System.Windows.Media.Animation.AnimationTimeline> à partir duquel il a été créé pour calculer actuelle à la valeur de sortie. Le <xref:System.Windows.Media.Animation.AnimationClock> fournit le <xref:System.Windows.Media.Animation.AnimationTimeline> avec l’heure locale actuelle, une valeur d’entrée, qui est généralement la valeur de la propriété de base et une valeur de destination par défaut. Lorsque vous récupérez la valeur animée par propriété à l’aide du <xref:System.Windows.DependencyObject.GetValue%2A> méthode ou son accesseur CLR, vous obtenez la sortie de son <xref:System.Windows.Media.Animation.AnimationClock>.  
  
#### <a name="clock-groups"></a>Groupes d’horloges  
 La section précédente a décrit les différents types de <xref:System.Windows.Media.Animation.Clock> objets pour différents types de chronologies. L’illustration suivante montre la relation entre le Gestionnaire de temps, un <xref:System.Windows.Media.Animation.ClockGroup>, un <xref:System.Windows.Media.Animation.AnimationClock>et une propriété de dépendance animée. Un <xref:System.Windows.Media.Animation.ClockGroup> est créé pour les chronologies qui groupent d’autres chronologies, telles que le <xref:System.Windows.Media.Animation.Storyboard> (classe), qui regroupe des animations et autres chronologies.  
  
 ![Composants du système de minutage](./media/graphicsmm-clocks-2clock1clockgroup2prop.png "graphicsmm_clocks_2clock1clockgroup2prop")  
Un groupe d’horloges  
  
#### <a name="composition"></a>Composition  
 Il est possible d’associer plusieurs horloges à une seule propriété, auquel cas chaque l’horloge utilise la valeur de sortie de l’exemple d’horloge précédent comme valeur de base. L’illustration suivante montre trois <xref:System.Windows.Media.Animation.AnimationClock> objets appliqués à la même propriété. Clock1 utilise la valeur de base de la propriété animée comme entrée et l’utilise pour générer la sortie. Clock2 prend la sortie de Clock1 comme entrée et l’utilise pour générer la sortie. Clock3 prend la sortie de Clock2 comme entrée et l’utilise pour générer la sortie. Lorsque plusieurs horloges affectent la même propriété simultanément, on dit qu’elles font partie d’une chaîne de composition.  
  
 ![Composants du système de minutage](./media/graphicsmm-clocks-2clock1prop.png "graphicsmm_clocks_2clock1prop")  
Une chaîne de composition  
  
 Notez que même si une relation est créée entre l’entrée et la sortie de la <xref:System.Windows.Media.Animation.AnimationClock> des objets dans la chaîne de composition, leurs comportements de minutage ne sont pas affectées ; <xref:System.Windows.Media.Animation.Clock> objets (y compris <xref:System.Windows.Media.Animation.AnimationClock> objets) ont une dépendance hiérarchique sur leur parent <xref:System.Windows.Media.Animation.Clock> objets.  
  
 Pour appliquer plusieurs horloges à la même propriété, utilisez le <xref:System.Windows.Media.Animation.HandoffBehavior.Compose> <xref:System.Windows.Media.Animation.HandoffBehavior> lors de l’application un <xref:System.Windows.Media.Animation.Storyboard>, animation, ou <xref:System.Windows.Media.Animation.AnimationClock>.  
  
#### <a name="ticks-and-event-consolidation"></a>Graduations et consolidation des événements  
 En plus du calcul des valeurs de sortie, le gestionnaire de temps effectue un autre travail à chaque graduation : il détermine l’état de chaque horloge et déclenche des événements comme il convient.  
  
 Étant donné que ces cycles sont fréquents, beaucoup de choses peuvent se passer entre chaque cycle. Par exemple, un <xref:System.Windows.Media.Animation.Clock> peut être arrêté, démarré et arrêté à nouveau, auquel cas sa <xref:System.Windows.Media.Animation.Clock.CurrentState%2A> valeur aura changé trois fois. En théorie, le <xref:System.Windows.Media.Animation.Clock.CurrentStateInvalidated> événement peut être déclenché plusieurs fois dans un seul battement ; Toutefois, le moteur de minutage consolide les événements, afin que le <xref:System.Windows.Media.Animation.Clock.CurrentStateInvalidated> peut être déclenché au maximum une fois par battement. Cela est vrai pour tous les événements d’horloge : un événement de chaque type au plus est déclenché pour une donnée <xref:System.Windows.Media.Animation.Clock> objet.  
  
 Quand un <xref:System.Windows.Media.Animation.Clock> change d’état et revient à son état d’origine entre les battements (telles que la modification de <xref:System.Windows.Media.Animation.ClockState.Active> à <xref:System.Windows.Media.Animation.ClockState.Stopped> , puis vers <xref:System.Windows.Media.Animation.ClockState.Active>), l’événement associé se produit toujours.  
  
 Pour plus d'informations sur les événements de minuterie, consultez [Vue d'ensemble des événements de minuterie](timing-events-overview.md).  
  
<a name="currentvaluesbasevaluesofproperties"></a>   
## <a name="current-values-and-base-values-of-properties"></a>Valeurs actuelles et les valeurs de base des propriétés  
 Une propriété pouvant être animée peut avoir deux valeurs : une valeur de base et une valeur actuelle. Lorsque vous définissez la propriété à l’aide de son accesseur CLR ou la <xref:System.Windows.DependencyObject.SetValue%2A> (méthode), vous définissez sa valeur de base. Lorsqu’une propriété n’est pas animée, ses valeurs de base et actuelles sont identiques.  
  
 Lorsque vous animez une propriété, le <xref:System.Windows.Media.Animation.AnimationClock> définit la propriété *actuel* valeur. Récupération de la valeur de propriété via son accesseur CLR ou la <xref:System.Windows.DependencyObject.GetValue%2A> méthode retourne la sortie de la <xref:System.Windows.Media.Animation.AnimationClock> lorsque le <xref:System.Windows.Media.Animation.AnimationClock> est <xref:System.Windows.Media.Animation.ClockState.Active> ou <xref:System.Windows.Media.Animation.ClockState.Filling>. Vous pouvez récupérer la valeur de base de la propriété à l’aide de la <xref:System.Windows.Media.Animation.IAnimatable.GetAnimationBaseValue%2A> (méthode).  
  
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble de l’animation](animation-overview.md)
- [Vue d'ensemble des événements de minuterie](timing-events-overview.md)
- [Vue d’ensemble des comportements de minutage](timing-behaviors-overview.md)
