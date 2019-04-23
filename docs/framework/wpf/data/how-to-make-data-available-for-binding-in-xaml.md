---
title: 'Procédure : Rendre des données disponibles pour la liaison en XAML'
ms.date: 01/29/2018
dev_langs:
- csharp
- vb
helpviewer_keywords:
- data binding [WPF], making data available for binding
- binding data [WPF], making data available for
ms.assetid: 7103c2e8-0e31-4a13-bf12-ca382221a8d5
ms.openlocfilehash: 2d51f06da31482c46b04d1eb86172c3eda246c20
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59145364"
---
# <a name="how-to-make-data-available-for-binding-in-xaml"></a>Procédure : Rendre des données disponibles pour la liaison en XAML
Cette rubrique présente les différentes manières vous rendre les données disponibles pour la liaison dans [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)], selon les besoins de votre application.  
  
## <a name="example"></a>Exemple  
 Si vous avez un [!INCLUDE[TLA#tla_clr](../../../../includes/tlasharptla-clr-md.md)] vous souhaitez lier à partir de l’objet [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)], une façon vous pouvez rendre l’objet disponible pour liaison consiste à définir en tant que ressource et lui donner un `x:Key`. Dans l’exemple suivant, vous avez un `Person` objet avec une propriété de chaîne nommée `PersonName`. Le `Person` objet (sur la ligne indiquée en surbrillance qui contient le `<src>` élément) est défini dans l’espace de noms appelé `SDKSample`.  
  
 [!code-xaml[SimpleBinding#Instantiation](~/samples/snippets/csharp/VS_Snippets_Wpf/SimpleBinding/CSharp/Page1.xaml?highlight=9,37)]  
  
 Vous pouvez ensuite lier le <xref:System.Windows.Controls.TextBlock> contrôle à l’objet dans [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)], comme la mise en surbrillance la ligne qui contient le `<TextBlock>` montre de l’élément. 
  
 Vous pouvez également utiliser le <xref:System.Windows.Data.ObjectDataProvider> classe, comme dans l’exemple suivant :  
  
 [!code-xaml[ObjectDataProvider}](~/samples/snippets/visualbasic/VS_Snippets_Wpf/SimpleBinding/VisualBasic/Page1.xaml?highlight=10-14,42)]  
  
 Vous définissez la liaison de la même façon, que la ligne en surbrillance qui contient le `<TextBlock>` montre de l’élément.  
  
 Dans cet exemple particulier, le résultat est le même : vous avez un <xref:System.Windows.Controls.TextBlock> avec le contenu de texte `Joe`. Toutefois, la <xref:System.Windows.Data.ObjectDataProvider> classe fournit des fonctionnalités telles que la capacité à lier au résultat d’une méthode. Vous pouvez choisir d’utiliser la <xref:System.Windows.Data.ObjectDataProvider> classe si vous avez besoin de la fonctionnalité qu’elle fournit.  
  
 Toutefois, si vous liez à un objet qui a déjà été créé, vous devez définir le `DataContext` dans le code, comme dans l’exemple suivant.  
  
 [!code-csharp[ADODataSet#1](~/samples/snippets/csharp/VS_Snippets_Wpf/ADODataSet/CSharp/Window1.xaml.cs#1)]
 [!code-vb[ADODataSet#1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ADODataSet/VisualBasic/Window1.xaml.vb#1)]  
  
 Pour accéder à [!INCLUDE[TLA2#tla_xml](../../../../includes/tla2sharptla-xml-md.md)] les données de liaison à l’aide du <xref:System.Windows.Data.XmlDataProvider> de classe, consultez [lier aux données XML à l’aide un XMLDataProvider et requêtes XPath](how-to-bind-to-xml-data-using-an-xmldataprovider-and-xpath-queries.md). Pour accéder à [!INCLUDE[TLA2#tla_xml](../../../../includes/tla2sharptla-xml-md.md)] les données de liaison à l’aide du <xref:System.Windows.Data.ObjectDataProvider> de classe, consultez [effectuer une liaison avec XDocument, XElement ou LINQ pour des résultats de requête XML](how-to-bind-to-xdocument-xelement-or-linq-for-xml-query-results.md).  
  
 Pour plus d’informations sur les nombreuses façons vous pouvez spécifier les données que vous liez à, consultez [spécifier la Source de liaison](how-to-specify-the-binding-source.md). Pour plus d’informations sur les types de données que vous pouvez lier à ou d’implémenter votre propre [!INCLUDE[TLA#tla_clr](../../../../includes/tlasharptla-clr-md.md)] objets pour la liaison, consultez [vue d’ensemble des Sources de liaison](binding-sources-overview.md).  
  
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble de la liaison de données](data-binding-overview.md)
- [Rubriques de guide pratique](data-binding-how-to-topics.md)
