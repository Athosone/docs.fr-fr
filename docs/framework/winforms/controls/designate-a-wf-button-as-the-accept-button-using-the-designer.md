---
title: 'Procédure : désigner un bouton Windows Forms comme bouton Accepter à l’aide du concepteur'
ms.date: 03/30/2017
helpviewer_keywords:
- buttons [Windows Forms], default on Windows Forms
- Accept button on Windows Forms
- Button control [Windows Forms], designating as default
- Windows Forms controls, default button on form
ms.assetid: a1da0590-755f-49f2-aca7-609fac6351bf
ms.openlocfilehash: e0eaa90c8450888ea325470db5d4adae555f8d82
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59304166"
---
# <a name="how-to-designate-a-windows-forms-button-as-the-accept-button-using-the-designer"></a>Procédure : désigner un bouton Windows Forms comme bouton Accepter à l’aide du concepteur
Sur n’importe quel formulaire Windows, vous pouvez désigner un <xref:System.Windows.Forms.Button> contrôle de bouton Accepter, également connu sous le bouton par défaut. Chaque fois que l’utilisateur appuie sur la touche entrée, le bouton par défaut un clic sur quel autre contrôle sur le formulaire a le focus. Les exceptions sont lorsque le contrôle ayant le focus est un autre bouton, dans ce cas, un clic sur le bouton qui a le focus, ou une zone de texte multiligne ou un contrôle personnalisé qui intercepte la touche ENTRÉE.  
  
> [!NOTE]
>  Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée. Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** . Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).  
  
### <a name="to-designate-the-accept-button"></a>Pour désigner le bouton Accepter  
  
1. Sélectionnez le formulaire sur lequel réside le bouton.  
  
2. Dans le **propriétés** fenêtre, définissez le formulaire <xref:System.Windows.Forms.Form.AcceptButton%2A> propriété le <xref:System.Windows.Forms.Button> nom du contrôle.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.Form.AcceptButton%2A>
- [Vue d'ensemble du contrôle Button](button-control-overview-windows-forms.md)
- [Méthodes de sélection du contrôle Button Windows Forms](ways-to-select-a-windows-forms-button-control.md)
- [Guide pratique pour Répondre aux clics de bouton Windows Forms](how-to-respond-to-windows-forms-button-clicks.md)
- [Guide pratique pour Désigner un contrôle Button Windows Forms comme bouton Annuler à l’aide du Concepteur](designate-a-wf-button-as-the-cancel-button-using-the-designer.md)
- [Button, contrôle](button-control-windows-forms.md)
