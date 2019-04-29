---
title: SpawnInstance (fonction) (référence des API non managées)
description: La fonction SpawnInstance crée une nouvelle instance d’une classe.
ms.date: 11/06/2017
api_name:
- SpawnInstance
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- SpawnInstance
helpviewer_keywords:
- SpawnInstance function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 8056ef18089f56f1f9b6717d505fa3d058957541
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61782524"
---
# <a name="spawninstance-function"></a><span data-ttu-id="a50f1-103">SpawnInstance (fonction)</span><span class="sxs-lookup"><span data-stu-id="a50f1-103">SpawnInstance function</span></span>
<span data-ttu-id="a50f1-104">Crée une instance d’une classe.</span><span class="sxs-lookup"><span data-stu-id="a50f1-104">Creates a new instance of a class.</span></span>    
  
[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
  
## <a name="syntax"></a><span data-ttu-id="a50f1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a50f1-105">Syntax</span></span>  
  
```  
HRESULT SpawnInstance (
   [in] int                  vFunc, 
   [in] IWbemClassObject*    ptr, 
   [in] LONG                 lFlags,
   [out] IWbemClassObject**  ppNewInstance); 
```  

## <a name="parameters"></a><span data-ttu-id="a50f1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a50f1-106">Parameters</span></span>

`vFunc`  
<span data-ttu-id="a50f1-107">[in] Ce paramètre n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="a50f1-107">[in] This parameter is unused.</span></span>

`ptr`  
<span data-ttu-id="a50f1-108">[in] Un pointeur vers un [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) instance.</span><span class="sxs-lookup"><span data-stu-id="a50f1-108">[in] A pointer to an [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) instance.</span></span>

`lFlags`  
<span data-ttu-id="a50f1-109">[in] Réservée.</span><span class="sxs-lookup"><span data-stu-id="a50f1-109">[in] Reserved.</span></span> <span data-ttu-id="a50f1-110">Ce paramètre doit être 0.</span><span class="sxs-lookup"><span data-stu-id="a50f1-110">This parameter must be 0.</span></span>

`ppNewInstance`  
<span data-ttu-id="a50f1-111">[out] Reçoit le pointeur vers la nouvelle instance de la classe.</span><span class="sxs-lookup"><span data-stu-id="a50f1-111">[out] Receives the pointer to the new instance of the class.</span></span> <span data-ttu-id="a50f1-112">Si une erreur se produit, un nouvel objet n’est pas retournée, et `ppNewInstance` est gauche tels quels.</span><span class="sxs-lookup"><span data-stu-id="a50f1-112">If an error occurs, a new object is not returned, and `ppNewInstance` is left unmodified.</span></span>

## <a name="return-value"></a><span data-ttu-id="a50f1-113">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="a50f1-113">Return value</span></span>

<span data-ttu-id="a50f1-114">Les valeurs suivantes est retournées par cette fonction sont définies dans le *WbemCli.h* fichier d’en-tête, ou vous pouvez les définir en tant que constantes dans votre code :</span><span class="sxs-lookup"><span data-stu-id="a50f1-114">The following values returned by this function are defined in the *WbemCli.h* header file, or you can define them as constants in your code:</span></span>

|<span data-ttu-id="a50f1-115">Constante</span><span class="sxs-lookup"><span data-stu-id="a50f1-115">Constant</span></span>  |<span data-ttu-id="a50f1-116">Value</span><span class="sxs-lookup"><span data-stu-id="a50f1-116">Value</span></span>  |<span data-ttu-id="a50f1-117">Description</span><span class="sxs-lookup"><span data-stu-id="a50f1-117">Description</span></span>  |
|---------|---------|---------|
| `WBEM_E_INCOMPLETE_CLASS` | <span data-ttu-id="a50f1-118">0x80041020</span><span class="sxs-lookup"><span data-stu-id="a50f1-118">0x80041020</span></span> | <span data-ttu-id="a50f1-119">`ptr` n’est pas une définition de classe valide et ne peut pas générer de nouvelles instances.</span><span class="sxs-lookup"><span data-stu-id="a50f1-119">`ptr` is not a valid class definition and cannot spawn new instances.</span></span> <span data-ttu-id="a50f1-120">Soit il est incomplet, soit il n’a pas été inscrit avec la gestion de Windows en appelant [PutClassWmi](putclasswmi.md).</span><span class="sxs-lookup"><span data-stu-id="a50f1-120">Either it is incomplete or it has not been registered with Windows Management by calling [PutClassWmi](putclasswmi.md).</span></span> |
| `WBEM_E_OUT_OF_MEMORY` | <span data-ttu-id="a50f1-121">0x80041006</span><span class="sxs-lookup"><span data-stu-id="a50f1-121">0x80041006</span></span> | <span data-ttu-id="a50f1-122">Mémoire est insuffisante pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="a50f1-122">Not enough memory is available to complete the operation.</span></span> |
| `WBEM_E_INVALID_PARAMETER` | <span data-ttu-id="a50f1-123">0x80041008</span><span class="sxs-lookup"><span data-stu-id="a50f1-123">0x80041008</span></span> | <span data-ttu-id="a50f1-124">`ppNewClass` a la valeur `null`.</span><span class="sxs-lookup"><span data-stu-id="a50f1-124">`ppNewClass` is `null`.</span></span> |
| `WBEM_S_NO_ERROR` | <span data-ttu-id="a50f1-125">0</span><span class="sxs-lookup"><span data-stu-id="a50f1-125">0</span></span> | <span data-ttu-id="a50f1-126">L’appel de fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="a50f1-126">The function call was successful.</span></span>  |
  
## <a name="remarks"></a><span data-ttu-id="a50f1-127">Notes</span><span class="sxs-lookup"><span data-stu-id="a50f1-127">Remarks</span></span>

<span data-ttu-id="a50f1-128">Cette fonction encapsule un appel à la [IWbemClassObject::SpawnInstance](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-spawninstance) (méthode).</span><span class="sxs-lookup"><span data-stu-id="a50f1-128">This function wraps a call to the [IWbemClassObject::SpawnInstance](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-spawninstance) method.</span></span>

<span data-ttu-id="a50f1-129">`ptr` doit être une définition de classe obtenue à partir de la gestion de Windows.</span><span class="sxs-lookup"><span data-stu-id="a50f1-129">`ptr` must be a class definition obtained from Windows Management.</span></span> <span data-ttu-id="a50f1-130">(Notez que lors de la génération une instance d’une instance est prise en charge, mais l’instance retournée est vide.) Vous utilisez ensuite cette définition de classe pour créer des instances.</span><span class="sxs-lookup"><span data-stu-id="a50f1-130">(Note that spawning an instance from an instance is supported but the returned instance is empty.) You then use this class definition to create new instances.</span></span> <span data-ttu-id="a50f1-131">Un appel à la [PutInstanceWmi](putinstancewmi.md) fonction est nécessaire si vous avez l’intention d’écrire l’instance à la gestion de Windows.</span><span class="sxs-lookup"><span data-stu-id="a50f1-131">A call to the [PutInstanceWmi](putinstancewmi.md) function is required if you intend to write the instance to Windows Management.</span></span>

<span data-ttu-id="a50f1-132">Le nouvel objet retourné dans `ppNewClass` devient automatiquement une sous-classe de l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="a50f1-132">The new object returned in `ppNewClass` automatically becomes a subclass of the current object.</span></span> <span data-ttu-id="a50f1-133">Ce comportement ne peut pas être remplacé.</span><span class="sxs-lookup"><span data-stu-id="a50f1-133">This behavior cannot be overridden.</span></span> <span data-ttu-id="a50f1-134">Il n’existe aucune autre méthode par laquelle les sous-classes (classes dérivées) peuvent être créés.</span><span class="sxs-lookup"><span data-stu-id="a50f1-134">There is no other method by which subclasses (derived classes) can be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="a50f1-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a50f1-135">Requirements</span></span>  
 <span data-ttu-id="a50f1-136">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a50f1-136">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a50f1-137">**En-tête :** WMINet_Utils.idl</span><span class="sxs-lookup"><span data-stu-id="a50f1-137">**Header:** WMINet_Utils.idl</span></span>  
  
 <span data-ttu-id="a50f1-138">**Versions du .NET Framework :** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="a50f1-138">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a50f1-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a50f1-139">See also</span></span>

- [<span data-ttu-id="a50f1-140">WMI et compteurs de performances (référence des API non managées)</span><span class="sxs-lookup"><span data-stu-id="a50f1-140">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)
