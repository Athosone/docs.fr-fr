---
title: Microsoft.VisualStudio.Activities.Asr.ClientActivityBuilder..ctor
ms.date: 03/30/2017
ms.topic: reference
api_name:
- Microsoft.VisualStudio.Activities.Asr.ClientActivityBuilder..ctor
api_location:
- Microsoft.VisualStudio.Activities.dll
api_type:
- Assembly
ms.assetid: 6b44b13c-7a23-4df2-8f9f-45e2b1430002
ms.openlocfilehash: 0ce9be30182f9181bcb6449529d9b9796aadbc2b
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59133534"
---
# <a name="microsoftvisualstudioactivitiesasrclientactivitybuilderctor"></a><span data-ttu-id="2a3dd-102">Microsoft.VisualStudio.Activities.Asr.ClientActivityBuilder..ctor</span><span class="sxs-lookup"><span data-stu-id="2a3dd-102">Microsoft.VisualStudio.Activities.Asr.ClientActivityBuilder..ctor</span></span>
<span data-ttu-id="2a3dd-103">Crée une instance de la [Microsoft.VisualStudio.Activities.Asr.ClientActivityBuilder](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/microsoft-visualstudio-activities-asr-clientactivitybuilder.md) classe.</span><span class="sxs-lookup"><span data-stu-id="2a3dd-103">Creates an instance of the [Microsoft.VisualStudio.Activities.Asr.ClientActivityBuilder](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/microsoft-visualstudio-activities-asr-clientactivitybuilder.md) class.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2a3dd-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2a3dd-104">Syntax</span></span>  
  
```csharp  
public ClientActivityBuilder(OperationDescription operationDescription, string configurationName, string proxyNamespace);  
```  
  
## <a name="parameters"></a><span data-ttu-id="2a3dd-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2a3dd-105">Parameters</span></span>  
  
## <a name="parameter-values"></a><span data-ttu-id="2a3dd-106">Valeurs du paramètre</span><span class="sxs-lookup"><span data-stu-id="2a3dd-106">Parameter Values</span></span>  
 <span data-ttu-id="2a3dd-107">*operationDescription*</span><span class="sxs-lookup"><span data-stu-id="2a3dd-107">*operationDescription*</span></span>  
  
 <span data-ttu-id="2a3dd-108">Décrit l'opération à effectuer dans l'activité de workflow qui doit être générée, notamment le nom de l'opération, le type de retour et les informations de paramètre.</span><span class="sxs-lookup"><span data-stu-id="2a3dd-108">Describes the operation to be performed in the workflow activity that is to be generated, including the operation name, return type, and parameter information.</span></span> <span data-ttu-id="2a3dd-109">La valeur de ce paramètre ne doit pas être **null**.</span><span class="sxs-lookup"><span data-stu-id="2a3dd-109">The value of this parameter must not be **null**.</span></span> <span data-ttu-id="2a3dd-110">Elle doit décrire une opération synchrone qui utilise un contrat de message et prend un argument avec un message.</span><span class="sxs-lookup"><span data-stu-id="2a3dd-110">It should describe a synchronous operation which uses a message contract and takes an argument with one message.</span></span> <span data-ttu-id="2a3dd-111">Si ces conditions ne sont pas satisfaites, le résultat d'exécution du constructeur et des autres méthodes de cette classe est indéfini.</span><span class="sxs-lookup"><span data-stu-id="2a3dd-111">If these conditions are not satisfied, the runtime result of using the constructor and the other methods of this class are undefined.</span></span>  
  
 <span data-ttu-id="2a3dd-112">*configurationName*</span><span class="sxs-lookup"><span data-stu-id="2a3dd-112">*configurationName*</span></span>  
  
 <span data-ttu-id="2a3dd-113">Spécifie le nom de configuration du point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="2a3dd-113">Specifies the endpoint configuration name.</span></span> <span data-ttu-id="2a3dd-114">La valeur de ce paramètre ne doit pas être soit **null** ou vide.</span><span class="sxs-lookup"><span data-stu-id="2a3dd-114">The value of this parameter must not be either **null** or empty.</span></span> <span data-ttu-id="2a3dd-115">Si ces conditions ne sont pas satisfaites, le résultat d'exécution du constructeur et des autres méthodes de cette classe est indéfini.</span><span class="sxs-lookup"><span data-stu-id="2a3dd-115">If these conditions are not satisfied, the runtime result of using the constructor and the other methods of this class are undefined.</span></span>  
  
 <span data-ttu-id="2a3dd-116">*proxyNamespace*</span><span class="sxs-lookup"><span data-stu-id="2a3dd-116">*proxyNamespace*</span></span>  
  
 <span data-ttu-id="2a3dd-117">Spécifie l'espace de noms du service pour l'opération.</span><span class="sxs-lookup"><span data-stu-id="2a3dd-117">Specifies the service namespace for the operation.</span></span> <span data-ttu-id="2a3dd-118">La valeur de ce paramètre ne doit pas être soit **null** ou vide.</span><span class="sxs-lookup"><span data-stu-id="2a3dd-118">The value of this parameter must not be either **null** or empty.</span></span> <span data-ttu-id="2a3dd-119">Si ces conditions ne sont pas satisfaites, le résultat d'exécution du constructeur et des autres méthodes de cette classe est indéfini.</span><span class="sxs-lookup"><span data-stu-id="2a3dd-119">If these conditions are not satisfied, the runtime result of using the constructor and the other methods of this class are undefined.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2a3dd-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2a3dd-120">See also</span></span>

- [<span data-ttu-id="2a3dd-121">Microsoft.VisualStudio.Activities.Asr.ClientActivityBuilder</span><span class="sxs-lookup"><span data-stu-id="2a3dd-121">Microsoft.VisualStudio.Activities.Asr.ClientActivityBuilder</span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/microsoft-visualstudio-activities-asr-clientactivitybuilder.md)
