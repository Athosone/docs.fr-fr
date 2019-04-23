---
title: Endmethodenumeration, fonction (référence des API non managées)
description: Endmethodenumeration, de la fonction termine une séquence d’énumération de méthode.
ms.date: 11/06/2017
api_name:
- EndMethodEnumeration
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- EndMethodEnumeration
helpviewer_keywords:
- EndMethodEnumeration function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: e7f29c365e9f6ba85f85ceb232f7af89446af2a1
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59213049"
---
# <a name="endmethodenumeration-function"></a><span data-ttu-id="b7277-103">EndMethodEnumeration, fonction</span><span class="sxs-lookup"><span data-stu-id="b7277-103">EndMethodEnumeration function</span></span>
<span data-ttu-id="b7277-104">Met fin à une séquence d’énumération démarrée avec un appel à la [beginmethodenumeration, fonction](beginmethodenumeration.md).</span><span class="sxs-lookup"><span data-stu-id="b7277-104">Terminates an enumeration sequence started with a call to the [BeginMethodEnumeration function](beginmethodenumeration.md).</span></span>  

[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
    
## <a name="syntax"></a><span data-ttu-id="b7277-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b7277-105">Syntax</span></span>  
  
```  
HRESULT EndMethodEnumeration (
   [in] int               vFunc, 
   [in] IWbemClassObject* ptr 
); 
```  

## <a name="parameters"></a><span data-ttu-id="b7277-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b7277-106">Parameters</span></span>

`vFunc`  
<span data-ttu-id="b7277-107">[in] Ce paramètre n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="b7277-107">[in] This parameter is unused.</span></span>

`ptr`  
<span data-ttu-id="b7277-108">[in] Un pointeur vers un [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) instance.</span><span class="sxs-lookup"><span data-stu-id="b7277-108">[in] A pointer to an [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) instance.</span></span>

## <a name="return-value"></a><span data-ttu-id="b7277-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="b7277-109">Return value</span></span>

<span data-ttu-id="b7277-110">Les valeurs suivantes est retournées par cette fonction sont définies dans le *WbemCli.h* fichier d’en-tête, ou vous pouvez les définir en tant que constantes dans votre code :</span><span class="sxs-lookup"><span data-stu-id="b7277-110">The following values returned by this function are defined in the *WbemCli.h* header file, or you can define them as constants in your code:</span></span>

|<span data-ttu-id="b7277-111">Constante</span><span class="sxs-lookup"><span data-stu-id="b7277-111">Constant</span></span>  |<span data-ttu-id="b7277-112">Value</span><span class="sxs-lookup"><span data-stu-id="b7277-112">Value</span></span>  |<span data-ttu-id="b7277-113">Description</span><span class="sxs-lookup"><span data-stu-id="b7277-113">Description</span></span>  |
|---------|---------|---------|
|`WBEM_E_UNEXPECTED` | <span data-ttu-id="b7277-114">0x8004101d</span><span class="sxs-lookup"><span data-stu-id="b7277-114">0x8004101d</span></span> | <span data-ttu-id="b7277-115">Une erreur interne s’est produite.</span><span class="sxs-lookup"><span data-stu-id="b7277-115">An internal error occurred.</span></span> |
|`WBEM_S_NO_ERROR` | <span data-ttu-id="b7277-116">0</span><span class="sxs-lookup"><span data-stu-id="b7277-116">0</span></span> | <span data-ttu-id="b7277-117">L’appel de fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="b7277-117">The function call was successful.</span></span>  |
  
## <a name="remarks"></a><span data-ttu-id="b7277-118">Notes</span><span class="sxs-lookup"><span data-stu-id="b7277-118">Remarks</span></span>

<span data-ttu-id="b7277-119">Cette fonction encapsule un appel à la [IWbemClassObject::EndMethodEnumeration](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-endmethodenumeration) (méthode).</span><span class="sxs-lookup"><span data-stu-id="b7277-119">This function wraps a call to the [IWbemClassObject::EndMethodEnumeration](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-endmethodenumeration) method.</span></span>

<span data-ttu-id="b7277-120">L’appelant commence la séquence d’énumération à l’aide [beginmethodenumeration, fonction](beginmethodenumeration.md), puis appelle la [NextMethod fonction](nextmethod.md )jusqu'à ce que la méthode retourne `WBEM_S_NO_MORE_DATA`.</span><span class="sxs-lookup"><span data-stu-id="b7277-120">The caller begins the enumeration sequence using [BeginMethodEnumeration function](beginmethodenumeration.md), and then calls the [NextMethod function](nextmethod.md )until the method  returns `WBEM_S_NO_MORE_DATA`.</span></span> <span data-ttu-id="b7277-121">L’appelant éventuellement termine la séquence en appelant `EndMethodEnumeration`.</span><span class="sxs-lookup"><span data-stu-id="b7277-121">The caller optionally finishes the sequence by calling `EndMethodEnumeration`.</span></span> <span data-ttu-id="b7277-122">L’appelant peut arrêter l’énumération au début en appelant `EndMethodEnumeration` à tout moment.</span><span class="sxs-lookup"><span data-stu-id="b7277-122">The caller may terminate the enumeration early by calling `EndMethodEnumeration` at any time.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7277-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b7277-123">Requirements</span></span>  
 <span data-ttu-id="b7277-124">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b7277-124">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b7277-125">**En-tête :** WMINet_Utils.idl</span><span class="sxs-lookup"><span data-stu-id="b7277-125">**Header:** WMINet_Utils.idl</span></span>  
  
 <span data-ttu-id="b7277-126">**Versions du .NET Framework :** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="b7277-126">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b7277-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b7277-127">See also</span></span>

- [<span data-ttu-id="b7277-128">WMI et compteurs de performances (référence des API non managées)</span><span class="sxs-lookup"><span data-stu-id="b7277-128">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)
