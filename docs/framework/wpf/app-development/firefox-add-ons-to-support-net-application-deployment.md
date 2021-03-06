---
title: Modules complémentaires de Firefox pour la prise en charge du déploiement d'applications .NET
ms.date: 03/30/2017
helpviewer_keywords:
- Firefox add-ons for .NET application deployment
- WPF plug-in for Firefox
- .NET application deployment [WPF], deploying with Firefox add-ons
- .NET Framework Assistant for Firefox
ms.assetid: 2403403b-9b14-48e9-b70d-fa288a3c9081
ms.openlocfilehash: 4b0552ab9f565d9118415bc2da2823762f34fe2c
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62007407"
---
# <a name="firefox-add-ons-to-support-net-application-deployment"></a>Modules complémentaires de Firefox pour la prise en charge du déploiement d'applications .NET
Activer Windows Presentation Foundation (WPF) plug-in pour Firefox et l’Assistant .NET Framework pour Firefox [!INCLUDE[TLA#tla_winfxwebapp#plural](../../../../includes/tlasharptla-winfxwebappsharpplural-md.md)], libre [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)]et les applications ClickOnce pour travailler avec le navigateur Mozilla Firefox.  
  
## <a name="wpf-plug-in-for-firefox"></a>Plug-in de Firefox WPF  
 Le plug-in de Firefox WPF permet [!INCLUDE[TLA2#tla_xbap#plural](../../../../includes/tla2sharptla-xbapsharpplural-md.md)] et libre [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] fichiers cible de la navigation et l’exécution au niveau supérieur ou dans un IFRAME HTML dans le navigateur Firefox. Un [!INCLUDE[TLA2#tla_xbap](../../../../includes/tla2sharptla-xbap-md.md)] est un [!INCLUDE[TLA2#tla_wpf](../../../../includes/tla2sharptla-wpf-md.md)] application qui peut être publiée sur un serveur Web et lancée dans les navigateurs pris en charge. Libre [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] est un fichier XAML uniquement qui peut être accédé et navigateurs pris en charge, comme un fichier XML.  
  
 Le [!INCLUDE[TLA2#tla_wpf](../../../../includes/tla2sharptla-wpf-md.md)] plug-in de Firefox est installé avec le [!INCLUDE[net_v35_short](../../../../includes/net-v35-short-md.md)]. Windows 7 inclut la [!INCLUDE[net_v35_short](../../../../includes/net-v35-short-md.md)], mais n’inclut ne pas le [!INCLUDE[TLA2#tla_wpf](../../../../includes/tla2sharptla-wpf-md.md)] plug-in de Firefox. Vous ne pouvez pas installer le [!INCLUDE[TLA2#tla_wpf](../../../../includes/tla2sharptla-wpf-md.md)] plug-in de Firefox sur Windows 7.  
  
 Le [!INCLUDE[net_v40_short](../../../../includes/net-v40-short-md.md)] n’inclut pas le [!INCLUDE[TLA2#tla_wpf](../../../../includes/tla2sharptla-wpf-md.md)] plug-in de Firefox. Toutefois, si les deux le [!INCLUDE[net_v35_short](../../../../includes/net-v35-short-md.md)] et [!INCLUDE[net_v40_short](../../../../includes/net-v40-short-md.md)] sont, WPF plug-in de Firefox est installé avec le [!INCLUDE[net_v35_short](../../../../includes/net-v35-short-md.md)]. Par conséquent [!INCLUDE[net_v40_short](../../../../includes/net-v40-short-md.md)] applications s’exécutent toujours, car l’hôte WPF chargera la version correcte du framework. Pour plus d’informations, consultez [hôte WPF (PresentationHost.exe)](wpf-host-presentationhost-exe.md).  
  
## <a name="net-framework-assistant-for-firefox"></a>assistant .NET Framework pour Firefox  
 L’Assistant .NET Framework pour Firefox permet à des applications ClickOnce autonomes à exécuter à partir du navigateur Firefox. L’Assistant .NET Framework pour Firefox fonctionne de manière identique lorsqu’il est installé avant et après le navigateur Firefox. Lorsque le navigateur Firefox est lancé et le [!INCLUDE[net_v35SP1_short](../../../../includes/net-v35sp1-short-md.md)] est installé, Firefox recherche et installe l’Assistant .NET Framework pour Firefox. Les utilisateurs peuvent configurer l’Assistant .NET Framework pour Firefox pour effectuer les opérations suivantes :  
  
- Demander avant d’exécuter l’application ClickOnce.  
  
- Signaler toutes les versions installées du .NET Framework ou simplement la version la plus récente.  
  
 L’Assistant .NET Framework pour Firefox est inclus avec le [!INCLUDE[net_v35SP1_short](../../../../includes/net-v35sp1-short-md.md)]. Pour plus d’informations sur la suppression de l’Assistant .NET Framework pour Firefox, consultez [comment supprimer l’Assistant .NET Framework pour Firefox](https://go.microsoft.com/fwlink/?LinkId=177944).  
  
## <a name="see-also"></a>Voir aussi

- [Déploiement d’une application WPF](deploying-a-wpf-application-wpf.md)
- [Vue d’ensemble des applications du navigateur XAML WPF](wpf-xaml-browser-applications-overview.md)
- [Détecter si le plug-in WPF de Firefox est installé](how-to-detect-whether-the-wpf-plug-in-for-firefox-is-installed.md)
