---
title: <workflowIdle>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: b2ef703c-3e01-4213-9d2e-c14c7dba94d2
ms.openlocfilehash: 1dc186f5899935dab43c0d33894e659c4b19748c
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59201115"
---
# <a name="workflowidle"></a>\<workflowIdle>
Comportement de service qui contrôle à quel moment les instances de workflow inactives sont déchargées et rendues persistantes.  
  
\<system.ServiceModel>  
\<behaviors>  
\<serviceBehaviors>  
\<behavior>  
\<workflowIdle>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<behaviors>
  <serviceBehaviors>
    <behavior name="String">
      <workflowIdle timeToPersist="TimeSpan" 
                    timeToUnload="TimeSpan" />
    </behavior>
  </serviceBehaviors>
</behaviors>  
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|timeToPersist|Une valeur Timespan qui spécifie la durée entre le moment où le flux de travail devienne inactif et est rendu persistant. La valeur par défaut est TimeSpan.MaxValue.<br /><br /> La durée commence à s'écouler lorsque l'instance de flux de travail devient inactive. Cet attribut est utile si vous souhaitez conserver une instance de workflow de façon plus agressive tout en conservant l’instance en mémoire aussi longtemps que possible. Cet attribut est valide uniquement si sa valeur est inférieure à la **timeToUnload** attribut. Si elle est supérieure, elle est ignorée. Si cet attribut s’écoule avant la valeur spécifiée par le **timeToUnload** , attribut de persistance doit s’effectuer avant que le workflow est déchargé. Cela implique un éventuel retard de l'opération de déchargement tant que le flux de travail n'a pas été rendu persistant. La couche de persistance est responsable de la gestion de toutes les tentatives pour les erreurs temporaires et lève uniquement des exceptions sur les erreurs non récupérables. Par conséquent, toutes les exceptions levées pendant la persistance sont traitées comme fatales et l'instance de flux de travail est abandonnée.|  
|timeToUnload|Valeur Timespan qui spécifie la durée entre l'inactivation et le déchargement du flux de travail. La valeur par défaut est égale à 1 minute.<br /><br /> Le déchargement d'un flux de travail implique qu'il soit également rendu persistant. Si cet attribut est défini à zéro l’instance de workflow est rendue persistante et déchargée immédiatement après le workflow devient inactif. Cet attribut TimeSpan.MaxValue efficacement désactive l’opération de déchargement. Les instances de flux de travail inactives ne sont jamais déchargées.|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<comportement > de \<serviceBehaviors >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/behavior-of-servicebehaviors-of-workflow.md)|Spécifie un élément de comportement.|  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.ServiceModel.Activities.Description.WorkflowIdleBehavior>
- <xref:System.ServiceModel.Activities.Configuration.WorkflowIdleElement>
