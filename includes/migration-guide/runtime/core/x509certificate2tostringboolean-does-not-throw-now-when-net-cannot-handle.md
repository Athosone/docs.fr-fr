---
ms.openlocfilehash: 0dfc87201b9b31cd9d936f2c965c7d0ca0140cab
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59234254"
---
### <a name="x509certificate2tostringboolean-does-not-throw-now-when-net-cannot-handle-the-certificate"></a>X509Certificate2.ToString(Boolean) ne lève plus d’exception quand .NET ne peut pas gérer le certificat

|   |   |
|---|---|
|Détails|Dans .NET Framework 4.5.2 et antérieur, cette méthode levait une exception quand la valeur <code>true</code> était passée au paramètre verbose alors que des certificats non pris en charge par le .NET Framework étaient installés. À présent, la méthode n’échoue plus et retourne une chaîne valide qui omet les parties inaccessibles du certificat.|
|Suggestion|Le code qui dépend de <xref:System.Security.Cryptography.X509Certificates.X509Certificate2.ToString(System.Boolean)?displayProperty=nameWithType> doit être mis à jour pour s’attendre à ce que la chaîne retournée omette certaines données du certificat (telles que la clé publique, la clé privée et les extensions), ce qui aurait auparavant entraîné la levée d’une exception par l’API.|
|Portée|Microsoft Edge|
|Version|4.6|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Security.Cryptography.X509Certificates.X509Certificate2.ToString(System.Boolean)?displayProperty=nameWithType></li></ul>|
