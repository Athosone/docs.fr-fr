---
title: Vue d'ensemble du contrôle StatusStrip
ms.date: 03/30/2017
f1_keywords:
- StatusStrip
helpviewer_keywords:
- StatusStrip control [Windows Forms], about StatusStrip control
- status bars [Windows Forms], about status bars
ms.assetid: c0d9bcbb-f8b8-46ef-bae2-4146b8c8ce99
ms.openlocfilehash: f6f2d4b19b7ec91c964c72e3aca85e0253c7cc22
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62009641"
---
# <a name="statusstrip-control-overview"></a>Vue d'ensemble du contrôle StatusStrip
Un contrôle <xref:System.Windows.Forms.StatusStrip> affiche des informations sur un objet affiché sur un <xref:System.Windows.Forms.Form>, les composants de l'objet ou des informations contextuelles relatives au fonctionnement de cet objet dans votre application. En règle générale, un contrôle <xref:System.Windows.Forms.StatusStrip> est composé d'objets <xref:System.Windows.Forms.ToolStripStatusLabel>, chacun affichant du texte, une icône ou les deux. <xref:System.Windows.Forms.StatusStrip> peut également contenir des contrôles <xref:System.Windows.Forms.ToolStripDropDownButton>, <xref:System.Windows.Forms.ToolStripSplitButton> et <xref:System.Windows.Forms.ToolStripProgressBar>.  
  
 Le <xref:System.Windows.Forms.StatusStrip> par défaut n'a pas de panneau. Pour ajouter des panneaux à un <xref:System.Windows.Forms.StatusStrip>, utilisez la méthode <xref:System.Windows.Forms.ToolStripItemCollection.AddRange%2A?displayProperty=nameWithType>.  
  
 Visual Studio offre une prise en charge complète de la gestion des éléments et des commandes courantes de <xref:System.Windows.Forms.StatusStrip>.  
  
 Consultez également [éditeur de collections d’éléments StatusStrip](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/ms233631(v=vs.100)) et [Tâches StatusStrip, boîte de dialogue](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/ms233642(v=vs.100)).  
  
 Bien que <xref:System.Windows.Forms.StatusStrip> remplace et étende le contrôle <xref:System.Windows.Forms.StatusBar> des versions antérieures, <xref:System.Windows.Forms.StatusBar> est conservé à des fins de compatibilité descendante et pour une utilisation ultérieure si tel est votre choix.  
  
### <a name="important-statusstrip-members"></a>Membres importants de StatusStrip  
  
|Nom|Description|  
|----------|-----------------|  
|<xref:System.Windows.Forms.StatusStrip.CanOverflow%2A>|Obtient ou définit une valeur indiquant si le <xref:System.Windows.Forms.StatusStrip> prend en charge les fonctionnalités de dépassement de capacité.|  
|<xref:System.Windows.Forms.StatusStrip.Stretch%2A>|Obtient ou définit une valeur indiquant si le <xref:System.Windows.Forms.StatusStrip> s'étire d'un bout à l'autre dans son <xref:System.Windows.Forms.ToolStripContainer>.|  
  
### <a name="important-statusstrip-companion-classes"></a>Classes auxiliaires importantes de StatusStrip  
  
|Nom|Description|  
|----------|-----------------|  
|<xref:System.Windows.Forms.ToolStripStatusLabel>|Représente un panneau dans un contrôle <xref:System.Windows.Forms.StatusStrip>.|  
|<xref:System.Windows.Forms.ToolStripDropDownButton>|Affiche un <xref:System.Windows.Forms.ToolStripDropDown> associé à partir duquel l'utilisateur peut sélectionner un élément unique.|  
|<xref:System.Windows.Forms.ToolStripSplitButton>|Représente un contrôle en deux parties constitué d'un bouton standard et d'un menu déroulant.|  
|<xref:System.Windows.Forms.ToolStripProgressBar>|Affiche l'état d'achèvement d'un processus.|  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.StatusStrip>
- <xref:System.Windows.Forms.ToolStripStatusLabel>
- <xref:System.Windows.Forms.ToolStripStatusLabel.Spring%2A>
