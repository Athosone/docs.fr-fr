---
title: Informations d'accessibilité sur les contrôles d'un Windows Form
ms.date: 03/30/2017
helpviewer_keywords:
- Windows Forms controls, accessibility
- controls [Windows Forms], accessibility
- accessibility [Windows Forms], Windows Forms controls
ms.assetid: 887dee6f-5059-4d57-957d-7c6fcd4acb10
ms.openlocfilehash: 0f589f37d79c9ec8d55153aac4c846726a379055
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61948017"
---
# <a name="providing-accessibility-information-for-controls-on-a-windows-form"></a>Informations d'accessibilité sur les contrôles d'un Windows Form
Les aides à l’accessibilité sont des programmes et des dispositifs spécialisés qui aident les personnes handicapées à utiliser plus efficacement les ordinateurs. Tel est le cas notamment des lecteurs d’écran pour les non-voyants et des systèmes d’entrée vocale pour les personnes qui prononcent des commandes verbales au lieu d’utiliser la souris ou le clavier. Ces aides à l’accessibilité interagissent avec les propriétés d’accessibilité exposées par les contrôles Windows Forms. Ces propriétés sont :  
  
- **AccessibilityObject**  
  
- **AccessibleDefaultActionDescription**  
  
- **AccessibleDescription**  
  
- **AccessibleName**  
  
- **AccessibleRole**  
  
## <a name="accessibilityobject-property"></a>Propriété AccessibilityObject  
 Cette propriété en lecture seule contient une instance de la <xref:System.Windows.Forms.AccessibleObject> . La classe **AccessibleObject** implémente l’interface <xref:Accessibility.IAccessible> , qui fournit des informations concernant la description, l’emplacement à l’écran, les capacités de navigation et la valeur du contrôle. Le concepteur définit cette valeur au moment d’ajouter le contrôle au formulaire.  
  
## <a name="accessibledefaultactiondescription-property"></a>Propriété AccessibleDefaultActionDescription  
 Cette chaîne décrit l’action du contrôle. Elle n’apparaît pas dans la fenêtre Propriétés et peut uniquement être définie dans du code. Dans l’exemple de code suivant, cette propriété est définie pour un contrôle bouton :  
  
```  
' Visual Basic  
Button1.AccessibleDefaultActionDescription = _  
   "Closes the application."  
  
// C#  
Button1.AccessibleDefaultActionDescription =   
   "Closes the application.";  
  
// C++  
button1->AccessibleDefaultActionDescription =  
   "Closes the application.";  
```  
  
## <a name="accessibledescription-property"></a>Propriété AccessibleDescription  
 Cette chaîne décrit le contrôle. Elle peut être définie dans la fenêtre Propriétés ou dans du code comme suit :  
  
```  
' Visual Basic  
Button1.AccessibleDescription = "A button with text 'Exit'."  
  
// C#  
Button1.AccessibleDescription = "A button with text 'Exit'";  
  
// C++  
button1->AccessibleDescription = "A button with text 'Exit'";  
```  
  
## <a name="accessiblename-property"></a>Propriété AccessibleName  
 Il s’agit du nom d’un contrôle indiqué aux aides à l’accessibilité. Elle peut être définie dans la fenêtre Propriétés ou dans du code comme suit :  
  
```  
' Visual Basic  
Button1.AccessibleName = "Order"  
  
// C#  
Button1.AccessibleName = "Order";  
  
// C++  
button1->AccessibleName = "Order";  
```  
  
## <a name="accessiblerole-property"></a>Propriété AccessibleRole  
 Cette propriété, qui contient une <xref:System.Windows.Forms.AccessibleRole> , décrit le rôle du contrôle dans l’interface utilisateur. Un nouveau contrôle a la valeur `Default`. Cela signifie que, par défaut, un contrôle **Button** (bouton) agit en tant que **Button**. Vous pouvez éventuellement réinitialiser cette propriété si un contrôle a un autre rôle. Par exemple, si vous utilisez un contrôle **PictureBox** (zone d’image) en tant que **Chart**(graphique), vous pouvez faire en sorte que les aides à l’accessibilité indique le rôle **Chart**, et non **PictureBox**. Vous pouvez aussi spécifier cette propriété pour des contrôles personnalisés que vous avez développés. Cette propriété être définie dans la fenêtre Propriétés ou dans du code comme suit :  
  
```  
' Visual Basic  
PictureBox1.AccessibleRole = AccessibleRole.Chart  
  
// C#  
PictureBox1.AccessibleRole = AccessibleRole.Chart;  
  
// C++  
pictureBox1->AccessibleRole = AccessibleRole::Chart;  
```  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.AccessibleObject>
- <xref:System.Windows.Forms.Control.AccessibilityObject%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.Control.AccessibleDefaultActionDescription%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.Control.AccessibleDescription%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.Control.AccessibleName%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.Control.AccessibleRole%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.AccessibleRole>
