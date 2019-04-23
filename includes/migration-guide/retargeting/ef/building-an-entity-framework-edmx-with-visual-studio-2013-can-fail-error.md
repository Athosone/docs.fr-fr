---
ms.openlocfilehash: ffafb0c9e3982dd168f907d32a8f59f96e6040d0
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59234754"
---
### <a name="building-an-entity-framework-edmx-with-visual-studio-2013-can-fail-with-error-msb4062-if-using-the-entitydeploysplit-or-entityclean-tasks"></a>La génération d’un fichier edmx Entity Framework avec Visual Studio 2013 peut échouer avec l’erreur MSB4062 si vous utilisez les tâches EntityDeploySplit ou EntityClean

|   |   |
|---|---|
|Détails|L’emplacement des fichiers des outils MSBuild 12.0 (inclus dans Visual Studio 2013) a changé, ce qui rend les anciens fichiers de cibles Entity Framework non valides. Les tâches <code>EntityDeploySplit</code> et <code>EntityClean</code> échouent, car elles ne parviennent pas à trouver <code>Microsoft.Data.Entity.Build.Tasks.dll</code>. Notez que ce problème est dû à un changement d’ensemble d’outils (MSBuild/VS), et non à un changement du .NET Framework. Il est dû à la mise à niveau des outils de développement, et non à celle du .NET Framework.|
|Suggestion|Les fichiers de cibles Entity Framework ont été corrigés pour fonctionner avec la nouvelle disposition MSBuild de .NET Framework 4.6. Vous pouvez résoudre ce problème en mettant à niveau votre .NET Framework vers la version 4.6. Vous pouvez également appliquer [cette solution de contournement](https://stackoverflow.com/a/24249247/131944) pour corriger directement les fichiers de cibles.|
|Portée|Majeur|
|Version|4.5.1|
|Type|Reciblage|
