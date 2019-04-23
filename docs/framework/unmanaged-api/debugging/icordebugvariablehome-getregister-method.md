---
title: ICorDebugVariableHome::GetRegister (méthode)
ms.date: 03/30/2017
api_name:
- ICorDebugVariableHome.GetRegister
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugVariableHome::GetRegister
helpviewer_keywords:
- ICorDebugVariableHome::GetRegister method [.NET Framework debugging]
- GetRegister method, ICorDebugVariableHome interface [.NET Framework debugging]
ms.assetid: a5eecd7b-b04c-4266-bff2-7c8771d519a8
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 290647f0e0dcaeae53362762ed7f8e0c2f05a82c
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59189948"
---
# <a name="icordebugvariablehomegetregister-method"></a><span data-ttu-id="1366e-102">ICorDebugVariableHome::GetRegister (méthode)</span><span class="sxs-lookup"><span data-stu-id="1366e-102">ICorDebugVariableHome::GetRegister Method</span></span>
<span data-ttu-id="1366e-103">Obtient le Registre qui contient une variable avec un type d’emplacement de `VLT_REGISTER`, le Registre de base et d’une variable avec un type d’emplacement de `VLT_REGISTER_RELATIVE`.</span><span class="sxs-lookup"><span data-stu-id="1366e-103">Gets the register that contains a variable with a location type of `VLT_REGISTER`, and the base register for a variable with a location type of `VLT_REGISTER_RELATIVE`.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1366e-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1366e-104">Syntax</span></span>  
  
```  
HRESULT GetRegister(  
    [out] CorDebugRegister *pRegister  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="1366e-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1366e-105">Parameters</span></span>  
 `pRegister`  
 <span data-ttu-id="1366e-106">[out] Une valeur d’énumération CorDebugRegister qui indique le Registre pour une variable avec un type d’emplacement de `VLT_REGISTER`, le Registre de base et d’une variable avec un type d’emplacement de `VLT_REGISTER_RELATIVE`.</span><span class="sxs-lookup"><span data-stu-id="1366e-106">[out] A CorDebugRegister enumeration value  that indicates the register for a variable with a location type of `VLT_REGISTER`, and the base register for a variable with a location type of `VLT_REGISTER_RELATIVE`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="1366e-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="1366e-107">Return Value</span></span>  
 <span data-ttu-id="1366e-108">La méthode retourne les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="1366e-108">The method returns the following values:</span></span>  
  
|<span data-ttu-id="1366e-109">Value</span><span class="sxs-lookup"><span data-stu-id="1366e-109">Value</span></span>|<span data-ttu-id="1366e-110">Description</span><span class="sxs-lookup"><span data-stu-id="1366e-110">Description</span></span>|  
|-----------|-----------------|  
|`S_OK`|<span data-ttu-id="1366e-111">La variable est dans le Registre indiqué par le `pRegister` argument.</span><span class="sxs-lookup"><span data-stu-id="1366e-111">The variable is in the register indicated by the `pRegister` argument.</span></span>|  
|`E_FAIL`|<span data-ttu-id="1366e-112">La variable n’est pas dans un Registre ou un emplacement relative au Registre.</span><span class="sxs-lookup"><span data-stu-id="1366e-112">The variable is not in a register or a register-relative location.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="1366e-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1366e-113">Requirements</span></span>  
 <span data-ttu-id="1366e-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="1366e-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1366e-115">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="1366e-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="1366e-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="1366e-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="1366e-117">**Versions du .NET Framework :** [!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1366e-117">**.NET Framework Versions:** [!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1366e-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1366e-118">See also</span></span>

- [<span data-ttu-id="1366e-119">VariableLocationType, énumération</span><span class="sxs-lookup"><span data-stu-id="1366e-119">VariableLocationType Enumeration</span></span>](../../../../docs/framework/unmanaged-api/debugging/variablelocationtype-enumeration.md)
- [<span data-ttu-id="1366e-120">ICorDebugVariableHome, interface</span><span class="sxs-lookup"><span data-stu-id="1366e-120">ICorDebugVariableHome Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-interface.md)
