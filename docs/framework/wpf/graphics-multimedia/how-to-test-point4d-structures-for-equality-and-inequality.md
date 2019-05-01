---
title: 'Procédure : Tester l’égalité et l’inégalité de structures Point4D'
ms.date: 03/30/2017
helpviewer_keywords:
- inequality [WPF], testing Point4D structures for
- equality [WPF], testing Point4D structures for
- testing [WPF], Point4D structures for equality
- Point4D structures [WPF], testing for inequality
- testing [WPF], Point4D structures for inequality
- Point4D structures [WPF], testing for equality
ms.assetid: e004a67e-db7f-4af8-a31f-e6b2a44ccf34
ms.openlocfilehash: ce1188e99ef2b0682427cc2e227aaccd27f7c4f4
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62050634"
---
# <a name="how-to-test-point4d-structures-for-equality-and-inequality"></a>Procédure : Tester l’égalité et l’inégalité de structures Point4D
Cet exemple montre comment tester <xref:System.Windows.Media.Media3D.Point4D> d’égalité et d’inégalité des structures.  
  
 Le code suivant illustre comment tester <xref:System.Windows.Media.Media3D.Point4D> d’égalité et inégalité à l’aide de structures le <xref:System.Windows.Media.Media3D.Point4D> méthodes d’égalité.  Le <xref:System.Windows.Media.Media3D.Point4D> structures sont testées pour l’égalité à l’aide de l’égalité surchargée (`==`) opérateur, puis d’inégalité à l’aide de l’inégalité surchargée (`!=`) (opérateur) et enfin un <xref:System.Windows.Media.Media3D.Point3D> structure et un <xref:System.Windows.Media.Media3D.Point4D> structure sont vérifiées pour l’égalité à l’aide de la méthode statique <xref:System.Windows.Media.Media3D.Point4D.Equals%2A> (méthode).  
  
## <a name="example"></a>Exemple  
 [!code-csharp[3DGallery_procedural_snip#Point4DEqualityExample_csharp](~/samples/snippets/csharp/VS_Snippets_Wpf/3DGallery_procedural_snip/CSharp/Misc3DOperationsExample.cs#point4dequalityexample_csharp)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Media.Media3D.Point4D.op_Equality%2A>
- <xref:System.Windows.Media.Media3D.Point4D.op_Inequality%2A>
- <xref:System.Windows.Media.Media3D.Point4D.Equals%2A>
