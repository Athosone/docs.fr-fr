---
title: Assistant Débogage managé disconnectedContext
ms.date: 03/30/2017
helpviewer_keywords:
- DisconnectedContext MDA
- MDAs (managed debugging assistants), disconnected context
- dead context
- transitioning disconnected apartment or context
- context disconnections
- managed debugging assistants (MDAs), disconnected context
ms.assetid: 1887d31d-7006-4491-93b3-68fd5b05f71d
author: mairaw
ms.author: mairaw
ms.openlocfilehash: cb42c04df6e02ff43421b7af6bf2d51b53aa3e69
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61755127"
---
# <a name="disconnectedcontext-mda"></a>Assistant Débogage managé disconnectedContext
L'Assistant Débogage managé `disconnectedContext` est activé quand le CLR essaie d'effectuer une transition vers un contexte ou un cloisonnement déconnecté pendant le traitement d'une demande concernant un objet COM.  
  
## <a name="symptoms"></a>Symptômes  
 Les appels effectués sur un [wrapper RCW](../../../docs/framework/interop/runtime-callable-wrapper.md) (Runtime Callable Wrapper) sont fournis au composant COM sous-jacent dans le contexte ou cloisonnement actuel plutôt que celui où ils se trouvent. Cela peut entraîner une altération et/ou une perte de données si le composant COM n'est pas multithread, comme dans le cas de composants de thread cloisonné. Par ailleurs, si le wrapper RCW est lui-même un proxy, l'appel peut se traduire par la levée d'une <xref:System.Runtime.InteropServices.COMException> avec un HRESULT de valeur RPC_E_WRONG_THREAD.  
  
## <a name="cause"></a>Cause  
 Le contexte ou cloisonnement OLE a été arrêté au moment où le CLR a essayé d'effectuer une transition vers ce contexte ou cloisonnement. En règle générale, cela se produit quand les threads cloisonnés sont arrêtés avant que tous les composants COM détenus par le cloisonnement ne soient complètement libérés. Cela peut être dû à un appel explicite à partir du code utilisateur sur un wrapper RCW ou à la manipulation du composant COM par le CLR lui-même, par exemple quand le CLR libère le composant COM alors que le wrapper RCW associé a été récupéré par le Garbage Collector.  
  
## <a name="resolution"></a>Résolution  
 Pour éviter ce problème, assurez-vous que le thread qui détient le thread cloisonné ne prend pas fin tant que l'application n'a pas terminé de traiter tous les objets qui se trouvent dans le cloisonnement. Il en va de même pour les contextes ; assurez-vous qu'un contexte n'est pas arrêté tant que l'application n'a pas complètement terminé de traiter tous les composants COM qui appartiennent à ce contexte.  
  
## <a name="effect-on-the-runtime"></a>Effet sur le runtime  
 Cet Assistant Débogage managé n'a aucun effet sur le CLR. Il fournit uniquement des informations sur le contexte déconnecté.  
  
## <a name="output"></a>Sortie  
 Indique le cookie de contexte du contexte ou du cloisonnement déconnecté.  
  
## <a name="configuration"></a>Configuration  
  
```xml  
<mdaConfig>  
  <assistants>  
    <disconnectedContext />  
  </assistants>  
</mdaConfig>  
```  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Runtime.InteropServices.MarshalAsAttribute>
- [Diagnostic d’erreurs avec les Assistants Débogage managé](../../../docs/framework/debug-trace-profile/diagnosing-errors-with-managed-debugging-assistants.md)
- [Marshaling d'interopérabilité](../../../docs/framework/interop/interop-marshaling.md)
