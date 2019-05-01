---
title: 'Communications principales : Prise en charge de Webhost'
ms.date: 03/30/2017
ms.assetid: 034c501f-96f9-4ef7-9602-3ac21788fd3e
ms.openlocfilehash: 8ee107ffcb9fab629541ce004d1c587fcad652c8
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61998710"
---
# <a name="core-communications-webhost-support"></a>Communications principales : Prise en charge de Webhost

Cette rubrique répertorie toutes les exceptions générées par la prise en charge Webhost.

## <a name="exception-list"></a>Liste des exceptions

|Code de la ressource|Chaîne de la ressource|
|-------------------|---------------------|
|Hosting_CompatibilityServiceNotHosted|Ce service requiert la compatibilité ASP.NET. Il doit également être hébergé dans IIS. Hébergez le service dans IIS en activant la compatibilité ASP.NET dans Web.config ou affectez à la propriété AspNetCompatibilityRequirementsAttribute.AspNetCompatibilityRequirementsMode une valeur autre que Required.|
|Hosting_ListenerNotFoundForActivationInRecycling|Aucun canal n'écoute activement au niveau de l'adresse spécifiée. En cas de recyclage d'une application, le service est fermé.|
|Hosting_NonHTTPInCompatibilityMode|Les seuls protocoles pris en charge sous compatibilité ASP.NET sont HTTP et HTTPS. Supprimez le point de terminaison spécifié ou désactivez la compatibilité ASP.NET pour l'application concernée.|
|Hosting_ProcessNotExecutingUnderHostedContext|Le processus d’hébergement spécifié ne peut pas être appelé au sein de l’environnement d’hébergement actuel. Cette API nécessite que l'application effectuant l'appel soit hébergée dans les Services Internet (IIS) ou dans les services d'activation Windows (Windows Process Activation Service, WAS).|
|Hosting_ServiceCompatibilityRequire|Le service ne peut pas être activé car il requiert la compatibilité ASP.NET. La compatibilité ASP.NET n'est pas activée pour cette application. Activez la compatibilité ASP.NET dans le fichier Web.config ou définissez la compatibilité AspNetCompatibilityRequirementsAttribute.AspNetCompatibility.|
