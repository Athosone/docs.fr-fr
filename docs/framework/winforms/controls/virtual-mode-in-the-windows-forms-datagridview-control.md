---
title: Mode virtuel dans le contrôle DataGridView Windows Forms
ms.date: 03/30/2017
helpviewer_keywords:
- DataGridView control [Windows Forms], virtual mode
ms.assetid: feae5d43-2848-4b1a-8ea7-77085dc415b5
ms.openlocfilehash: f284835578221ad1fe859f260e37bb829cd64b2d
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62009134"
---
# <a name="virtual-mode-in-the-windows-forms-datagridview-control"></a>Mode virtuel dans le contrôle DataGridView Windows Forms
Avec le mode virtuel, vous pouvez gérer l’interaction entre le <xref:System.Windows.Forms.DataGridView> contrôle et un cache de données personnalisé. Pour implémenter le mode virtuel, affectez la <xref:System.Windows.Forms.DataGridView.VirtualMode%2A> propriété `true` et gérez un ou plusieurs des événements décrits dans cette rubrique. Vous gérerez généralement au moins les `CellValueNeeded` événement, ce qui permet au contrôle de rechercher des valeurs dans le cache de données.  
  
## <a name="bound-mode-and-virtual-mode"></a>Mode dépendant et Mode virtuel  
 Mode virtuel est nécessaire uniquement lorsque vous avez besoin compléter ou remplacer le mode dépendant. En mode dépendant, vous définissez le <xref:System.Windows.Forms.DataGridView.DataSource%2A> propriété et le contrôle charge automatiquement les données à partir de la source spécifiée et soumet les modifications d’utilisateur de le. Vous pouvez contrôler les colonnes liées sont affichés, et la source de données elle-même gère en général, les opérations telles que le tri.  
  
## <a name="supplementing-bound-mode"></a>Complément du Mode dépendant  
 Vous pouvez compléter le mode dépendant en affichant des colonnes indépendantes, ainsi que les colonnes dépendantes. Cela est parfois appelé « mode mixte » et est utile pour afficher des éléments comme des valeurs calculées ou l’interface utilisateur (IU) de contrôle.  
  
 Étant donné que les colonnes indépendantes sont en dehors de la source de données, elles sont ignorées par les opérations de tri de la source de données. Par conséquent, lorsque vous activez le tri en mode mixte, vous devez gérer les données indépendantes dans un cache local et implémenter le mode virtuel pour permettre la <xref:System.Windows.Forms.DataGridView> contrôle interagir avec lui.  
  
 Pour plus d’informations sur l’utilisation du mode virtuel pour gérer les valeurs dans les colonnes indépendantes, consultez les exemples dans le <xref:System.Windows.Forms.DataGridViewCheckBoxColumn.ThreeState%2A?displayProperty=nameWithType> propriété et <xref:System.Windows.Forms.DataGridViewComboBoxColumn?displayProperty=nameWithType> rubriques de référence de classe.  
  
## <a name="replacing-bound-mode"></a>Remplacement du Mode dépendant  
 Si le mode dépendant ne répond pas à vos besoins en performances, vous pouvez gérer toutes vos données dans un cache personnalisé via des gestionnaires d’événements de mode virtuel. Par exemple, vous pouvez utiliser le mode virtuel pour implémenter une mécanisme qui récupère uniquement de chargement de données juste-à-temps autant de données à partir d’une base de données en réseau est nécessaire pour des performances optimales. Ce scénario est particulièrement utile lorsque vous travaillez avec grandes quantités de données sur une connexion réseau lente ou aux ordinateurs clients qui ont une quantité limitée de mémoire RAM d’espace de stockage.  
  
 Pour plus d’informations sur l’utilisation du mode virtuel dans un scénario juste-à-temps, consultez [implémentation du Mode virtuel avec le chargement de données juste à temps dans le contrôle de DataGridView Windows Forms](implementing-virtual-mode-jit-data-loading-in-the-datagrid.md).  
  
## <a name="virtual-mode-events"></a>Événements de Mode virtuel  
 Si vos données sont en lecture seule, le `CellValueNeeded` événement peut être le seul événement que vous devrez gérer. Les événements de mode virtuel supplémentaires vous permettent d’activer des fonctionnalités spécifiques telles que la modification de l’utilisateur, ajout de ligne et la suppression et les transactions au niveau des lignes.  
  
 Certains standard <xref:System.Windows.Forms.DataGridView> événements (tels que les événements qui se produisent lorsque les utilisateurs à ajouter ou suppriment des lignes ou lorsque des valeurs de cellules sont modifiées, analysés, validés ou mis en forme) sont utiles en mode virtuel. Vous pouvez également gérer les événements qui vous permettent de mettre à jour les valeurs généralement pas stockées dans une source de données, telles que le texte d’info-bulle de cellule, cellule texte d’erreur de ligne, cellule et données de menu contextuel de ligne et des données de hauteur de ligne.  
  
 Pour plus d’informations sur l’implémentation du mode virtuel pour gérer des données en lecture/écriture avec une portée de validation au niveau de la ligne, consultez [procédure pas à pas : Implémentation du Mode virtuel dans les Windows Forms DataGridView Control](implementing-virtual-mode-wf-datagridview-control.md).  
  
 Pour obtenir un exemple qui implémente le mode virtuel avec une portée de validation de niveau cellule, consultez la <xref:System.Windows.Forms.DataGridView.VirtualMode%2A> rubrique de référence de propriété.  
  
 Les événements suivants se produisent uniquement lors de la <xref:System.Windows.Forms.DataGridView.VirtualMode%2A> propriété est définie sur `true`.  
  
|Événement|Description|  
|-----------|-----------------|  
|<xref:System.Windows.Forms.DataGridView.CellValueNeeded>|Utilisé par le contrôle pour récupérer une valeur de cellule dans le cache de données pour l’affichage. Cet événement se produit uniquement pour les cellules dans les colonnes indépendantes.|  
|<xref:System.Windows.Forms.DataGridView.CellValuePushed>|Utilisé par le contrôle pour valider les entrées d’utilisateur pour une cellule dans le cache de données. Cet événement se produit uniquement pour les cellules dans les colonnes indépendantes.<br /><br /> Appelez le <xref:System.Windows.Forms.DataGridView.UpdateCellValue%2A> méthode lorsque vous modifiez une valeur mise en cache en dehors d’un <xref:System.Windows.Forms.DataGridView.CellValuePushed> Gestionnaire d’événements pour garantir que la valeur actuelle est affichée dans le contrôle et appliquer des modes de dimensionnement automatique actuellement en vigueur.|  
|<xref:System.Windows.Forms.DataGridView.NewRowNeeded>|Utilisé par le contrôle pour indiquer la nécessité d’une nouvelle ligne dans le cache de données.|  
|<xref:System.Windows.Forms.DataGridView.RowDirtyStateNeeded>|Utilisé par le contrôle pour déterminer si une ligne comporte des modifications non validées.|  
|<xref:System.Windows.Forms.DataGridView.CancelRowEdit>|Utilisé par le contrôle pour indiquer qu’une ligne doit rétablir ses valeurs mises en cache.|  
  
 Les événements suivants sont utiles en mode virtuel, mais peut être utilisées indépendamment de la <xref:System.Windows.Forms.DataGridView.VirtualMode%2A> paramètre de propriété.  
  
|Événements|Description|  
|------------|-----------------|  
|<xref:System.Windows.Forms.DataGridView.UserDeletingRow><br /><br /> <xref:System.Windows.Forms.DataGridView.UserDeletedRow><br /><br /> <xref:System.Windows.Forms.DataGridView.RowsRemoved><br /><br /> <xref:System.Windows.Forms.DataGridView.RowsAdded>|Utilisé par le contrôle pour indiquer quand les lignes sont supprimées ou ajoutées, ce qui permet à jour le cache de données en conséquence.|  
|<xref:System.Windows.Forms.DataGridView.CellFormatting><br /><br /> <xref:System.Windows.Forms.DataGridView.CellParsing><br /><br /> <xref:System.Windows.Forms.DataGridView.CellValidating><br /><br /> <xref:System.Windows.Forms.DataGridView.CellValidated><br /><br /> <xref:System.Windows.Forms.DataGridView.RowValidating><br /><br /> <xref:System.Windows.Forms.DataGridView.RowValidated>|Utilisé par le contrôle aux valeurs des cellules de format pour l’affichage et à analyser et valider l’entrée utilisateur.|  
|<xref:System.Windows.Forms.DataGridView.CellToolTipTextNeeded>|Utilisé par le contrôle pour extraire le texte d’info-bulle de cellule lorsque le <xref:System.Windows.Forms.DataGridView.DataSource%2A> propriété est définie ou la <xref:System.Windows.Forms.DataGridView.VirtualMode%2A> propriété est `true`.<br /><br /> Info-bulles de cellule sont affichés uniquement lorsque le <xref:System.Windows.Forms.DataGridView.ShowCellToolTips%2A> valeur de propriété est `true`.|  
|<xref:System.Windows.Forms.DataGridView.CellErrorTextNeeded><br /><br /> <xref:System.Windows.Forms.DataGridView.RowErrorTextNeeded>|Permet de récupérer le texte d’erreur de cellule ou la ligne par le contrôle lorsque la <xref:System.Windows.Forms.DataGridView.DataSource%2A> propriété est définie ou la <xref:System.Windows.Forms.DataGridView.VirtualMode%2A> propriété est `true`.<br /><br /> Appelez le <xref:System.Windows.Forms.DataGridView.UpdateCellErrorText%2A> méthode ou le <xref:System.Windows.Forms.DataGridView.UpdateRowErrorText%2A> méthode lorsque vous modifiez le texte d’erreur de ligne ou cellule pour garantir que la valeur actuelle est affichée dans le contrôle.<br /><br /> Les glyphes d’erreur de cellule et de ligne sont affichés lorsque la <xref:System.Windows.Forms.DataGridView.ShowCellErrors%2A> et <xref:System.Windows.Forms.DataGridView.ShowRowErrors%2A> sont des valeurs de propriété `true`.|  
|<xref:System.Windows.Forms.DataGridView.CellContextMenuStripNeeded><br /><br /> <xref:System.Windows.Forms.DataGridView.RowContextMenuStripNeeded>|Utilisé par le contrôle pour récupérer une ligne ou cellule <xref:System.Windows.Forms.ContextMenuStrip> lorsque le contrôle <xref:System.Windows.Forms.DataGridView.DataSource%2A> propriété est définie ou la <xref:System.Windows.Forms.DataGridView.VirtualMode%2A> propriété est `true`.|  
|<xref:System.Windows.Forms.DataGridView.RowHeightInfoNeeded><br /><br /> <xref:System.Windows.Forms.DataGridView.RowHeightInfoPushed>|Utilisé par le contrôle à récupérer ou de stocker des informations de hauteur de ligne dans le cache de données. Appelez le <xref:System.Windows.Forms.DataGridView.UpdateRowHeightInfo%2A> méthode lorsque vous modifiez les informations de hauteur de ligne mise en cache en dehors d’un <xref:System.Windows.Forms.DataGridView.RowHeightInfoPushed> Gestionnaire d’événements pour vous assurer que la valeur actuelle est utilisée dans l’affichage du contrôle.|  
  
## <a name="best-practices-in-virtual-mode"></a>Meilleures pratiques en Mode virtuel  
 Si vous implémentez le mode virtuel afin de fonctionner efficacement de grandes quantités de données, vous devez également vous assurer que vous utilisez efficacement le <xref:System.Windows.Forms.DataGridView> contrôle lui-même. Pour plus d’informations sur l’utilisation efficace de styles de cellules, le dimensionnement automatique, des sélections et partage de lignes, consultez [meilleures pratiques pour la mise à l’échelle le contrôle de DataGridView Windows Forms](best-practices-for-scaling-the-windows-forms-datagridview-control.md).  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridView.VirtualMode%2A>
- [Réglage des performances dans le contrôle DataGridView Windows Forms](performance-tuning-in-the-windows-forms-datagridview-control.md)
- [Meilleures pratiques pour la mise à l'échelle du contrôle DataGridView Windows Forms](best-practices-for-scaling-the-windows-forms-datagridview-control.md)
- [Procédure pas à pas : Implémentation du Mode virtuel dans le contrôle de DataGridView Windows Forms](implementing-virtual-mode-wf-datagridview-control.md)
- [Implémentation du mode virtuel avec le chargement immédiat des données dans le contrôle DataGridView Windows Forms](implementing-virtual-mode-jit-data-loading-in-the-datagrid.md)
