---
title: 'Procédure : Effectuer une liaison avec XDocument, XElement ou LINQ pour des résultats de requête XML'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- data binding [WPF], binding to XDocument
- data binding [WPF], binding to XElement
ms.assetid: 6a629a49-fe1c-465d-b76a-3dcbf4307b64
ms.openlocfilehash: afecb87dcfce1a8c48f1b2108edeae3cfd2aa16f
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59209656"
---
# <a name="how-to-bind-to-xdocument-xelement-or-linq-for-xml-query-results"></a>Procédure : Effectuer une liaison avec XDocument, XElement ou LINQ pour des résultats de requête XML
Cet exemple montre comment lier des données XML à un <xref:System.Windows.Controls.ItemsControl> à l’aide de <xref:System.Xml.Linq.XDocument>.  
  
## <a name="example"></a>Exemple  
 Le code XAML suivant définit un <xref:System.Windows.Controls.ItemsControl> et inclut un modèle de données pour les données de type `Planet` dans le `http://planetsNS` espace de noms XML. Un type de données XML qui occupe un espace de noms doit inclure l’espace de noms entre accolades, et s’il s’affiche là où une extension de balisage XAML pourrait apparaître, il doit précéder l’espace de noms avec une séquence d’échappement d’accolades. Ce code lie aux propriétés dynamiques qui correspondent à la <xref:System.Xml.Linq.XContainer.Element%2A> et <xref:System.Xml.Linq.XElement.Attribute%2A> méthodes de la <xref:System.Xml.Linq.XElement> classe. Les propriétés dynamiques permettent à XAML de se lier aux propriétés dynamiques qui partagent les noms des méthodes. Pour en savoir plus, consultez [Propriétés dynamiques LINQ to XML](/visualstudio/designers/linq-to-xml-dynamic-properties). Notez comment la déclaration d’espace de noms par défaut pour XML ne s’applique pas aux noms d’attribut.  
  
 [!code-xaml[XLinqExample#StackPanelResources](~/samples/snippets/csharp/VS_Snippets_Wpf/XLinqExample/CSharp/Window1.xaml#stackpanelresources)]  
[!code-xaml[XLinqExample#ItemsControl](~/samples/snippets/csharp/VS_Snippets_Wpf/XLinqExample/CSharp/Window1.xaml#itemscontrol)]  
  
 Le code c# suivant appelle <xref:System.Xml.Linq.XDocument.Load%2A> et définit le contexte de données de panneau de configuration de pile sur tous les sous-éléments de l’élément nommé `SolarSystemPlanets` dans le `http://planetsNS` espace de noms XML.  
  
 [!code-csharp[XLinqExample#LoadDCFromFile](~/samples/snippets/csharp/VS_Snippets_Wpf/XLinqExample/CSharp/Window1.xaml.cs#loaddcfromfile)]
 [!code-vb[XLinqExample#LoadDCFromFile](~/samples/snippets/visualbasic/VS_Snippets_Wpf/XLinqExample/visualbasic/window1.xaml.vb#loaddcfromfile)]  
  
 Données XML peuvent être stockées comme une ressource XAML à l’aide <xref:System.Windows.Data.ObjectDataProvider>. Pour obtenir un exemple complet, consultez [code source L2DBForm.xaml](/visualstudio/designers/l2dbform-xaml-source-code). L’exemple suivant montre comment le code peut définir le contexte de données sur une ressource d’objet.  
  
 [!code-csharp[XLinqExample#LoadDCFromXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/XLinqExample/CSharp/Window1.xaml.cs#loaddcfromxaml)]
 [!code-vb[XLinqExample#LoadDCFromXAML](~/samples/snippets/visualbasic/VS_Snippets_Wpf/XLinqExample/visualbasic/window1.xaml.vb#loaddcfromxaml)]  
  
 Les propriétés dynamiques qui mappent aux <xref:System.Xml.Linq.XContainer.Element%2A> et <xref:System.Xml.Linq.XElement.Attribute%2A> fournissent une grande souplesse au XAML. Votre code peut également être lié aux résultats d’une requête LINQ to XML. Cet exemple se lie aux résultats de la requête triés par une valeur d’élément.  
  
 [!code-csharp[XLinqExample#BindToResults](~/samples/snippets/csharp/VS_Snippets_Wpf/XLinqExample/CSharp/Window1.xaml.cs#bindtoresults)]
 [!code-vb[XLinqExample#BindToResults](~/samples/snippets/visualbasic/VS_Snippets_Wpf/XLinqExample/visualbasic/window1.xaml.vb#bindtoresults)]  
  
## <a name="see-also"></a>Voir aussi

- [Vue d'ensemble des sources de liaison](binding-sources-overview.md)
- [Vue d’ensemble de la liaison de données WPF avec LINQ to XML](/visualstudio/designers/wpf-data-binding-with-linq-to-xml-overview)
- [Exemple de liaison de données WPF à l’aide de LINQ to XML](/visualstudio/designers/wpf-data-binding-using-linq-to-xml-example)
- [Propriétés dynamiques LINQ to XML](/visualstudio/designers/linq-to-xml-dynamic-properties)
