---
title: Mappage de modèle de contrôle pour les clients UI Automation
ms.date: 03/30/2017
helpviewer_keywords:
- control patterns, for UI Automation clients
- UI Automation, clients, control patterns for
ms.assetid: 8b81645b-8be3-4e26-9c98-4fb0fceca06b
ms.openlocfilehash: 829df66f49d5df5f5c8cf8d2b6cfa74f0a2172dd
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59101131"
---
# <a name="control-pattern-mapping-for-ui-automation-clients"></a>Mappage de modèle de contrôle pour les clients UI Automation
> [!NOTE]
>  Cette documentation s'adresse aux développeurs .NET Framework qui souhaitent utiliser les classes [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] managées définies dans l'espace de noms <xref:System.Windows.Automation>. Pour plus d’informations sur [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)], consultez [Windows Automation API : UI Automation](https://go.microsoft.com/fwlink/?LinkID=156746).  
  
 Cette rubrique répertorie les types de contrôle et leurs modèles de contrôle associés.  
  
 Le tableau suivant organise les modèles de contrôle dans les catégories suivantes :  
  
-   Prise en charge. Le contrôle doit prendre en charge ce modèle de contrôle.  
  
-   Prise en charge conditionnelle. Le contrôle peut prendre en charge ce modèle de contrôle en fonction de l’état du contrôle.  
  
-   Non pris en charge. Le contrôle ne prend pas en charge ce modèle de contrôle. Les contrôles personnalisés peuvent prendre en charge ce modèle de contrôle.  
  
> [!NOTE]
>  Certains contrôles disposent d’une prise en charge conditionnelle pour plusieurs modèles de contrôle selon les fonctionnalités du contrôle. Par exemple, le contrôle d’élément de menu dispose d’une prise en charge conditionnelle pour le modèle de contrôle <xref:System.Windows.Automation.InvokePattern>, <xref:System.Windows.Automation.ExpandCollapsePattern>, <xref:System.Windows.Automation.TogglePattern>ou <xref:System.Windows.Automation.SelectionItemPattern> , selon sa fonction dans le contrôle de menu.  
  
<a name="control_mapping_clients"></a>   
## <a name="ui-automation-control-patterns-for-clients"></a>Modèles de contrôle UI Automation pour les clients  
  
|Type de contrôle|Prise en charge|Prise en charge conditionnelle|Non prise en charge|  
|------------------|---------------|-------------------------|-------------------|  
|Bouton|Aucun.|Invoke, Toggle, Expand Collapse|Aucun.|  
|Calendrier|Grid, Table|Selection, Scroll|Value|  
|Case à cocher|Basculer|Aucun.|Aucun.|  
|Combo Box|Développer/Réduire|Selection, Value|Scroll|  
|DataGrid|Grille|Scroll, Selection, Table|Aucun.|  
|DataItem|Selection Item|Expand Collapse, Grid Item, Scroll Item, Table, Toggle, Value|Aucun.|  
|Document|Texte|Scroll, Value|Aucun.|  
|Modifier|Aucun.|Text, Range Value, Value|Aucun.|  
|Regrouper|Aucun.|Développer/Réduire|Aucun.|  
|En-tête|Aucun.|Transformer|Aucun.|  
|HeaderItem|Aucun.|Transform, Invoke|Aucun.|  
|Lien hypertexte|Appeler|Value|Aucun.|  
|Image|Aucun.|Grid Item, Table Item|Invoke, Selection Item|  
|Liste|Aucun.|Grid, Multiple View, Scroll, Selection|Table|  
|List Item|Selection Item|Expand Collapse, Grid Item, Invoke, Scroll Item, Toggle, Value|Aucun.|  
|Menu|Aucun.|Aucun.|Aucun.|  
|Barre de menus|Aucun.|Expand Collapse, Dock, Transform|Aucun.|  
|Élément de menu|Aucun.|Expand Collapse, Invoke, Selection Item, Toggle|Aucun.|  
|Volet|Aucun.|Dock. Scroll, Transform|Fenêtre|  
|ProgressBar|Aucun.|Range Value, Value|Aucun.|  
|RadioButton|Selection Item|Aucun.|Basculer|  
|Scroll Bar|Aucun.|Range Value|Scroll|  
|Séparateur|Aucun.|Aucun.|Aucun.|  
|Curseur|None|Range Value, Selection, Value|Aucun.|  
|Spinner|Aucun.|Range Value, Selection, Value|Aucun.|  
|Bouton partagé|Invoke, Expand Collapse|Aucun.|Aucun.|  
|Barre d'état|Aucun.|Grille|Aucun.|  
|Onglet|Sélection|Scroll|Aucun.|  
|TabItem|Selection Item|Aucun.|Appeler|  
|Table|Grid, Grid Item, Table, Table Item|Aucun.|Aucun.|  
|Texte|Aucun.|Grid Item, Table Item, Text|Value|  
|Thumb|Transformer|Aucun.|Aucun.|  
|Barre de titre|Aucun.|Aucun.|Aucun.|  
|Tool Bar|Aucun.|Dock, Expand Collapse, Transform|Aucun.|  
|Tool Tip|Aucun.|Text, Window|Aucun.|  
|Arborescence|Aucun.|Scroll, Selection|Aucun.|  
|TreeItem|Développer/Réduire|Invoke, Scroll Item, Selection Item, Toggle|Aucun.|  
|Fenêtre|Transform, Window|Station d' accueil|Aucun.|  
  
> [!NOTE]
>  Si un type de contrôle ne possède aucun modèle de contrôle pris en charge répertorié, mais possède un ou plusieurs modèles de contrôle pris en charge de manière conditionnelle, l’un de ces modèles de contrôle conditionnels est constamment pris en charge.  
  
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble d’UI Automation](../../../docs/framework/ui-automation/ui-automation-overview.md)
