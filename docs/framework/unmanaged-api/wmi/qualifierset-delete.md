---
title: QualifierSet_Delete (fonction) (référence des API non managées)
description: La fonction QualifierSet_Delete supprime un qualificateur par nom.
ms.date: 11/06/2017
api_name:
- QualifierSet_Delete
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- QualifierSet_Delete
helpviewer_keywords:
- QualifierSet_Delete function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 543cc63b3e2188c11a6a8bf1eaa846461375be99
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61597269"
---
# <a name="qualifiersetdelete-function"></a><span data-ttu-id="b9de4-103">QualifierSet_Delete (fonction)</span><span class="sxs-lookup"><span data-stu-id="b9de4-103">QualifierSet_Delete function</span></span>
<span data-ttu-id="b9de4-104">Supprime un qualificateur spécifié par nom.</span><span class="sxs-lookup"><span data-stu-id="b9de4-104">Deletes a specified qualifier by name.</span></span>  

[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
  
## <a name="syntax"></a><span data-ttu-id="b9de4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b9de4-105">Syntax</span></span>  
  
```  
HRESULT QualifierSet_Delete (
   [in] int                  vFunc, 
   [in] IWbemQualifierSet*   ptr, 
   [in] LPCWSTR              wszName
); 
```  

## <a name="parameters"></a><span data-ttu-id="b9de4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b9de4-106">Parameters</span></span>

`vFunc`  
<span data-ttu-id="b9de4-107">[in] Ce paramètre n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="b9de4-107">[in] This parameter is unused.</span></span>

`ptr`   
<span data-ttu-id="b9de4-108">[in] Un pointeur vers un [IWbemQualifierSet](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemqualifierset) instance.</span><span class="sxs-lookup"><span data-stu-id="b9de4-108">[in] A pointer to an [IWbemQualifierSet](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemqualifierset) instance.</span></span>

`wszName`   
<span data-ttu-id="b9de4-109">[in] Le nom du qualificateur à supprimer.</span><span class="sxs-lookup"><span data-stu-id="b9de4-109">[in] The name of the qualifier to delete.</span></span>

## <a name="return-value"></a><span data-ttu-id="b9de4-110">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="b9de4-110">Return value</span></span>

<span data-ttu-id="b9de4-111">Les valeurs suivantes est retournées par cette fonction sont définies dans le *WbemCli.h* fichier d’en-tête, ou vous pouvez les définir en tant que constantes dans votre code :</span><span class="sxs-lookup"><span data-stu-id="b9de4-111">The following values returned by this function are defined in the *WbemCli.h* header file, or you can define them as constants in your code:</span></span>

|<span data-ttu-id="b9de4-112">Constante</span><span class="sxs-lookup"><span data-stu-id="b9de4-112">Constant</span></span>  |<span data-ttu-id="b9de4-113">Value</span><span class="sxs-lookup"><span data-stu-id="b9de4-113">Value</span></span>  |<span data-ttu-id="b9de4-114">Description</span><span class="sxs-lookup"><span data-stu-id="b9de4-114">Description</span></span>  |
|---------|---------|---------|
|`WBEM_E_INVALID_PARAMETER` | <span data-ttu-id="b9de4-115">0x80041008</span><span class="sxs-lookup"><span data-stu-id="b9de4-115">0x80041008</span></span> | <span data-ttu-id="b9de4-116">Le paramètre `wszName` n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="b9de4-116">The `wszName` parameter is not valid.</span></span> |
|`WBEM_E_INVALID_OPERATION` | <span data-ttu-id="b9de4-117">0x80041016</span><span class="sxs-lookup"><span data-stu-id="b9de4-117">0x80041016</span></span> | <span data-ttu-id="b9de4-118">La suppression de ce qualificateur est non conforme.</span><span class="sxs-lookup"><span data-stu-id="b9de4-118">Deleting this qualifier is illegal.</span></span> |
|`WBEM_E_NOT_FOUND` | <span data-ttu-id="b9de4-119">0x80041002</span><span class="sxs-lookup"><span data-stu-id="b9de4-119">0x80041002</span></span> | <span data-ttu-id="b9de4-120">Le qualificateur spécifié est introuvable.</span><span class="sxs-lookup"><span data-stu-id="b9de4-120">The specified qualifier was not found.</span></span> |
|`WBEM_S_NO_ERROR` | <span data-ttu-id="b9de4-121">0</span><span class="sxs-lookup"><span data-stu-id="b9de4-121">0</span></span> | <span data-ttu-id="b9de4-122">L’appel de fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="b9de4-122">The function call was successful.</span></span>  |
| `WBEM_S_RESET_TO_DEFAULT` | <span data-ttu-id="b9de4-123">0x40002</span><span class="sxs-lookup"><span data-stu-id="b9de4-123">0x40002</span></span> | <span data-ttu-id="b9de4-124">La valeur de remplacement locale a été supprimé et le qualificateur d’origine à partir de l’objet parent a repris l’étendue.</span><span class="sxs-lookup"><span data-stu-id="b9de4-124">The local override was deleted and the original qualifier from the parent object has resumed scope.</span></span> |

## <a name="remarks"></a><span data-ttu-id="b9de4-125">Notes</span><span class="sxs-lookup"><span data-stu-id="b9de4-125">Remarks</span></span>

<span data-ttu-id="b9de4-126">Cette fonction encapsule un appel à la [IWbemQualifierSet::Delete](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemqualifierset-delete) (méthode).</span><span class="sxs-lookup"><span data-stu-id="b9de4-126">This function wraps a call to the [IWbemQualifierSet::Delete](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemqualifierset-delete) method.</span></span>

<span data-ttu-id="b9de4-127">En raison des règles de propagation d’un qualificateur de nom, un qualificateur particulier peut ont été hérité d’un autre objet et simplement de substitution dans la classe en cours ou l’instance.</span><span class="sxs-lookup"><span data-stu-id="b9de4-127">Due to qualifier propagation rules, a particular qualifier may have been inherited from another object and merely overridden in the current class or instance.</span></span> <span data-ttu-id="b9de4-128">Dans ce cas, le `QualifierSet_Delete` méthode réinitialise le qualificateur à sa valeur d’origine hérité.</span><span class="sxs-lookup"><span data-stu-id="b9de4-128">In this case, the `QualifierSet_Delete` method resets the qualifier to its original inherited value.</span></span> <span data-ttu-id="b9de4-129">Dans ce cas, la fonction retourne le code d’état `WBEM_S_RESET_TO_DEFAULT`.</span><span class="sxs-lookup"><span data-stu-id="b9de4-129">The function in this case returns the status code `WBEM_S_RESET_TO_DEFAULT`.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9de4-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b9de4-130">Requirements</span></span>  
 <span data-ttu-id="b9de4-131">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b9de4-131">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b9de4-132">**En-tête :** WMINet_Utils.idl</span><span class="sxs-lookup"><span data-stu-id="b9de4-132">**Header:** WMINet_Utils.idl</span></span>  
  
 <span data-ttu-id="b9de4-133">**Versions du .NET Framework :** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="b9de4-133">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b9de4-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b9de4-134">See also</span></span>

- [<span data-ttu-id="b9de4-135">WMI et compteurs de performances (référence des API non managées)</span><span class="sxs-lookup"><span data-stu-id="b9de4-135">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)
