---
title: GetQualifierSet (fonction) (référence des API non managées)
description: La fonction GetQualifierSet récupère le qualificateur définie pour une classe ou instance.
ms.date: 11/06/2017
api_name:
- GetQualifierSet
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- GetQualifierSet
helpviewer_keywords:
- GetQualifierSet function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 75bf52fbf9552dc464d9c646f0a2b1bc01cf89c0
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61723327"
---
# <a name="getqualifierset-function"></a><span data-ttu-id="b3ae1-103">GetQualifierSet (fonction)</span><span class="sxs-lookup"><span data-stu-id="b3ae1-103">GetQualifierSet function</span></span>
<span data-ttu-id="b3ae1-104">Récupère le jeu de qualificateurs pour une instance de classe ou une définition de classe.</span><span class="sxs-lookup"><span data-stu-id="b3ae1-104">Retrieves the qualifier set for a class instance or a class definition.</span></span>

[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
    
## <a name="syntax"></a><span data-ttu-id="b3ae1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b3ae1-105">Syntax</span></span>  
  
```  
HRESULT GetQualifierSet (
   [in] int                 vFunc, 
   [in] IWbemClassObject*   ptr, 
   [out] IWbemQualifierSet  **ppQualSet
); 
```  

## <a name="parameters"></a><span data-ttu-id="b3ae1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b3ae1-106">Parameters</span></span>

`vFunc`  
<span data-ttu-id="b3ae1-107">[in] Ce paramètre n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="b3ae1-107">[in] This parameter is unused.</span></span>

`ptr`  
<span data-ttu-id="b3ae1-108">[in] Un pointeur vers un [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) instance.</span><span class="sxs-lookup"><span data-stu-id="b3ae1-108">[in] A pointer to an [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) instance.</span></span>

`ppQualSet`  
<span data-ttu-id="b3ae1-109">[out] Reçoit le pointeur d’interface qui autorise l’accès pour les qualificateurs de l’objet de classe.</span><span class="sxs-lookup"><span data-stu-id="b3ae1-109">[out] Receives the interface pointer that allows access to the qualifiers of the class object.</span></span> <span data-ttu-id="b3ae1-110">`ppQualSet` ne peut pas avoir la valeur `null`.</span><span class="sxs-lookup"><span data-stu-id="b3ae1-110">`ppQualSet` cannot be `null`.</span></span> <span data-ttu-id="b3ae1-111">Si une erreur se produit, un nouvel objet n’est pas retourné, et le pointeur reste non modifié.</span><span class="sxs-lookup"><span data-stu-id="b3ae1-111">If an error occurs, a new object is not returned, and the pointer is left unmodified.</span></span> 

## <a name="return-value"></a><span data-ttu-id="b3ae1-112">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="b3ae1-112">Return value</span></span>

<span data-ttu-id="b3ae1-113">Les valeurs suivantes est retournées par cette fonction sont définies dans le *WbemCli.h* fichier d’en-tête, ou vous pouvez les définir en tant que constantes dans votre code :</span><span class="sxs-lookup"><span data-stu-id="b3ae1-113">The following values returned by this function are defined in the *WbemCli.h* header file, or you can define them as constants in your code:</span></span>

|<span data-ttu-id="b3ae1-114">Constante</span><span class="sxs-lookup"><span data-stu-id="b3ae1-114">Constant</span></span>  |<span data-ttu-id="b3ae1-115">Value</span><span class="sxs-lookup"><span data-stu-id="b3ae1-115">Value</span></span>  |<span data-ttu-id="b3ae1-116">Description</span><span class="sxs-lookup"><span data-stu-id="b3ae1-116">Description</span></span>  |
|---------|---------|---------|
|`WBEM_E_FAILED` | <span data-ttu-id="b3ae1-117">0x80041001</span><span class="sxs-lookup"><span data-stu-id="b3ae1-117">0x80041001</span></span> | <span data-ttu-id="b3ae1-118">Il y a eu une défaillance générale.</span><span class="sxs-lookup"><span data-stu-id="b3ae1-118">There has been a general failure.</span></span> |
|`WBEM_E_NOT_FOUND` | <span data-ttu-id="b3ae1-119">0x80041002</span><span class="sxs-lookup"><span data-stu-id="b3ae1-119">0x80041002</span></span> | <span data-ttu-id="b3ae1-120">La méthode spécifiée n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="b3ae1-120">The specified method does not exist.</span></span> |
|`WBEM_E_OUT_OF_MEMORY` | <span data-ttu-id="b3ae1-121">0x80041006</span><span class="sxs-lookup"><span data-stu-id="b3ae1-121">0x80041006</span></span> | <span data-ttu-id="b3ae1-122">Mémoire est insuffisante pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="b3ae1-122">Not enough memory is available to complete the operation.</span></span> |
|`WBEM_E_INVALID_PARAMETER` | <span data-ttu-id="b3ae1-123">0x80041008</span><span class="sxs-lookup"><span data-stu-id="b3ae1-123">0x80041008</span></span> | <span data-ttu-id="b3ae1-124">Un paramètre est `null`.</span><span class="sxs-lookup"><span data-stu-id="b3ae1-124">A parameter is `null`.</span></span> |
|`WBEM_S_NO_ERROR` | <span data-ttu-id="b3ae1-125">0</span><span class="sxs-lookup"><span data-stu-id="b3ae1-125">0</span></span> | <span data-ttu-id="b3ae1-126">L’appel de fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="b3ae1-126">The function call was successful.</span></span>  |
  
## <a name="remarks"></a><span data-ttu-id="b3ae1-127">Notes</span><span class="sxs-lookup"><span data-stu-id="b3ae1-127">Remarks</span></span>

<span data-ttu-id="b3ae1-128">Cette fonction encapsule un appel à la [IWbemClassObject::GetQualifierSet](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-getqualifierset) (méthode).</span><span class="sxs-lookup"><span data-stu-id="b3ae1-128">This function wraps a call to the [IWbemClassObject::GetQualifierSet](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-getqualifierset) method.</span></span> 

<span data-ttu-id="b3ae1-129">Le [IWbemQualifierSet pointeur](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemqualifierset) permet à l’appelant ajouter, modifier ou supprimer ces qualificateurs.</span><span class="sxs-lookup"><span data-stu-id="b3ae1-129">The [IWbemQualifierSet pointer](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemqualifierset) lets the caller add, edit, or delete these qualifiers.</span></span> <span data-ttu-id="b3ae1-130">Ces qualificateurs ajoutés, modifiés ou supprimés s’appliquent à la définition de classe ou instance entière.</span><span class="sxs-lookup"><span data-stu-id="b3ae1-130">Such added, edited, or deleted qualifiers apply to the entire instance or class definition.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3ae1-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b3ae1-131">Requirements</span></span>  
<span data-ttu-id="b3ae1-132">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b3ae1-132">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b3ae1-133">**En-tête :** WMINet_Utils.idl</span><span class="sxs-lookup"><span data-stu-id="b3ae1-133">**Header:** WMINet_Utils.idl</span></span>  
  
 <span data-ttu-id="b3ae1-134">**Versions du .NET Framework :** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="b3ae1-134">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b3ae1-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b3ae1-135">See also</span></span>

- [<span data-ttu-id="b3ae1-136">WMI et compteurs de performances (référence des API non managées)</span><span class="sxs-lookup"><span data-stu-id="b3ae1-136">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)
