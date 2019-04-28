---
title: 'Procédure : Lier un ornement à un élément'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- UIElements [WPF], binding adorners to
- adorners [WPF], binding to specified UIElements
ms.assetid: b2101611-a0ee-4137-bdb8-9b3673d2e6b9
ms.openlocfilehash: b6909fec466c2b31a7f4156c43b21a0c724f0217
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62018968"
---
# <a name="how-to-bind-an-adorner-to-an-element"></a>Procédure : Lier un ornement à un élément
Cet exemple montre comment lier par programmation un ornement à une certaine <xref:System.Windows.UIElement>.  
  
## <a name="example"></a>Exemple  
 Pour lier un ornement à un particulier <xref:System.Windows.UIElement>, procédez comme suit :  
  
1. Appeler le `static` méthode <xref:System.Windows.Documents.AdornerLayer.GetAdornerLayer%2A> pour obtenir un <xref:System.Windows.Documents.AdornerLayer> de l’objet pour le <xref:System.Windows.UIElement> à orner. <xref:System.Windows.Documents.AdornerLayer.GetAdornerLayer%2A> Remonte l’arborescence visuelle, en commençant à l’emplacement spécifié **UIElement**et retourne la première couche d’ornement qu’il trouve. (Si aucune couche d’ornement n’est trouvée, la méthode retourne Null.)  
  
2. Appelez le <xref:System.Windows.Documents.AdornerLayer.Add%2A> méthode à laquelle lier l’ornement à la cible **UIElement**.  
  
 L’exemple suivant lie un SimpleCircleAdorner (illustré ci-dessus) à un <xref:System.Windows.Controls.TextBox> nommé *myTextBox*.  
  
 [!code-csharp[Adorners_SimpleCircleAdorner#_AdornSingleElement](~/samples/snippets/csharp/VS_Snippets_Wpf/Adorners_SimpleCircleAdorner/CSharp/Window1.xaml.cs#_adornsingleelement)]
 [!code-vb[Adorners_SimpleCircleAdorner#_AdornSingleElement](~/samples/snippets/visualbasic/VS_Snippets_Wpf/Adorners_SimpleCircleAdorner/VisualBasic/Window1.xaml.vb#_adornsingleelement)]  
  
> [!NOTE]
>  L’utilisation du [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] pour lier un ornement à un autre élément n’est pas prise en charge pour l’instant.  
  
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble des ornements](adorners-overview.md)
