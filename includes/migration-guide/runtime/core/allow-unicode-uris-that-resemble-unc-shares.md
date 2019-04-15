---
ms.openlocfilehash: fbc39b6e1cc19f6c2846caaabb9a8a721494b4e6
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59236135"
---
### <a name="allow-unicode-in-uris-that-resemble-unc-shares"></a>Autoriser les caractères Unicode dans les URI qui ressemblent à des partages UNC

|   |   |
|---|---|
|Détails|Dans <xref:System.Uri?displayProperty=fullName>, la construction d’un URI de fichier contenant à la fois un nom de partage UNC et des caractères Unicode n’aboutit plus à un URI présentant un état interne non valide. Le comportement change uniquement quand toutes les conditions suivantes sont vraies :<ul><li>L’URI a le schéma <code>file:</code> et est suivi d’au moins quatre barres obliques.</li><li>Le nom d’hôte commence par un trait de soulignement ou un autre symbole non réservé.</li><li>L’URI contient des caractères Unicode.</li></ul>|
|Suggestion|Les applications qui utilisent des URI contenant systématiquement des caractères Unicode sont susceptibles de suivre ce comportement pour interdire les références à des partages UNC. Ces applications doivent utiliser <xref:System.Uri.IsUnc> à la place.|
|Portée|Microsoft Edge|
|Version|4.7.2|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Uri?displayProperty=nameWithType></li></ul>|
