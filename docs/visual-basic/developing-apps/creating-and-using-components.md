---
title: Création et utilisation de composants dans Visual Basic
ms.date: 07/20/2015
helpviewer_keywords:
- components [Visual Basic]
ms.assetid: ee6a4156-73f7-4e9b-8e01-c74c4798b65c
ms.openlocfilehash: ca336e2ffa3831167088d92bfca017ce2226d8a9
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62014321"
---
# <a name="creating-and-using-components-in-visual-basic"></a>Création et utilisation de composants dans Visual Basic
Un *composant* est une classe qui implémente l’interface <xref:System.ComponentModel.IComponent?displayProperty=nameWithType> ou qui dérive directement ou indirectement d’une classe implémentant <xref:System.ComponentModel.IComponent>. Un composant [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] est un objet réutilisable qui peut interagir avec d’autres objets, qui permet de contrôler les ressources externes et qui offre une prise en charge au moment du design.  
  
 Une caractéristique importante des composants est qu’ils peuvent servir au design, ce qui signifie qu’une classe qui est un composant peut être utilisée dans l’environnement de développement intégré (IDE) de Visual Studio. Un composant peut être ajouté à la boîte à outils, faire l’objet d’un glisser-déplacer sur un formulaire et être manipulé sur une aire de conception. Notez que la prise en charge de base au moment du design pour les composants est intégrée au [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)]. Un développeur de composant n’a pas besoin d’effectuer du travail supplémentaire pour tirer parti de la fonctionnalité de base au moment du design.  
  
 Un *contrôle* est similaire à un composant dans la mesure où tous les deux peuvent servir au design. Toutefois, un contrôle fournit une interface utilisateur, ce qui n’est pas le cas d’un composant. Un contrôle doit dériver de l’une des classes de contrôle de base : <xref:System.Windows.Forms.Control> ou <xref:System.Web.UI.Control>.  
  
## <a name="when-to-create-a-component"></a>Quand créer un composant  
 Si votre classe doit être utilisée sur une aire de conception (telle que le concepteur Windows Forms ou Web Forms), mais qu’elle n’a pas d’interface utilisateur, elle doit être un composant et implémenter <xref:System.ComponentModel.IComponent>, ou dériver d’une classe qui implémente directement ou indirectement <xref:System.ComponentModel.IComponent>.  
  
 Les classes <xref:System.ComponentModel.Component> et <xref:System.ComponentModel.MarshalByValueComponent> constituent des implémentations de base de l’interface <xref:System.ComponentModel.IComponent>. La principale différence entre ces classes est que la classe <xref:System.ComponentModel.Component> est marshalée par référence, tandis que la classe <xref:System.ComponentModel.IComponent> est marshalée par valeur. La liste suivante fournit des indications générales relatives aux implémenteurs.  
  
- Si votre composant doit être marshalé par référence, dérivez de <xref:System.ComponentModel.Component>.  
  
- Si votre composant doit être marshalé par valeur, dérivez de <xref:System.ComponentModel.MarshalByValueComponent>.  
  
- Si votre composant ne peut pas dériver de l’une des implémentations de base en raison d’un héritage unique, implémentez <xref:System.ComponentModel.IComponent>.  
  
## <a name="component-classes"></a>Classes de composant  
 L’espace de noms <xref:System.ComponentModel> fournit des classes utilisées pour implémenter le comportement des composants et des contrôles au moment de l’exécution et au moment du design. Cet espace de noms inclut les classes et les interfaces de base servant à l’implémentation des attributs et des convertisseurs de type, à la liaison à des sources de données et à la gestion des licences des composants.  
  
 Les classes de composant principales sont les suivantes :  
  
- <xref:System.ComponentModel.Component>. Implémentation de base pour l’interface <xref:System.ComponentModel.IComponent>. Cette classe permet le partage d’objets entre applications.  
  
- <xref:System.ComponentModel.MarshalByValueComponent>. Implémentation de base pour l’interface <xref:System.ComponentModel.IComponent>.  
  
- <xref:System.ComponentModel.Container>. Implémentation de base pour l’interface <xref:System.ComponentModel.IContainer>. Cette classe encapsule zéro, un ou plusieurs composants.  
  
 Les classes utilisées pour la gestion des licences des composants sont, entre autres, les suivantes :  
  
- <xref:System.ComponentModel.License>. Classe de base abstraite pour toutes les licences. Une licence est accordée à une instance spécifique d’un composant.  
  
- <xref:System.ComponentModel.LicenseManager>. Fournit des propriétés et des méthodes permettant d’ajouter une licence à un composant et de gérer un <xref:System.ComponentModel.LicenseProvider>.  
  
- <xref:System.ComponentModel.LicenseProvider>. Classe de base abstraite pour l’implémentation d’un fournisseur de licences.  
  
- <xref:System.ComponentModel.LicenseProviderAttribute>. Spécifie la classe <xref:System.ComponentModel.LicenseProvider> à utiliser avec une classe.  
  
 Classes couramment utilisées pour la description et la persistance des composants.  
  
- <xref:System.ComponentModel.TypeDescriptor>. Fournit des informations relatives aux caractéristiques d’un composant, telles que ses attributs, ses propriétés et ses événements.  
  
- <xref:System.ComponentModel.EventDescriptor>. Fournit des informations sur un événement.  
  
- <xref:System.ComponentModel.PropertyDescriptor>. Fournit des informations sur une propriété.  
  
## <a name="related-sections"></a>Rubriques connexes  
 [Dépannage de la création de contrôles et de composants](../../framework/winforms/controls/troubleshooting-control-and-component-authoring.md)  
 Explique comment résoudre certains problèmes courants.  
  
## <a name="see-also"></a>Voir aussi

- [Guide pratique pour Prise en charge d’accès au moment du Design dans les Windows Forms](../../framework/winforms/controls/developing-windows-forms-controls-at-design-time.md)
