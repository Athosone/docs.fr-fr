---
title: Blessiwbemservices, fonction (référence des API non managées)
description: Blessiwbemservices, de la fonction indique si les informations d’identification utilisateur autorisent l’accès à une classe IWbemServices.
ms.date: 11/06/2017
api_name:
- BlessIWbemServices
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- BlessIWbemServices
helpviewer_keywords:
- BlessIWbemServices function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 23b72856015d028e50c1e3bfd4a12e0f220291c3
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62049321"
---
# <a name="blessiwbemservices-function"></a><span data-ttu-id="ec90d-103">BlessIWbemServices, fonction</span><span class="sxs-lookup"><span data-stu-id="ec90d-103">BlessIWbemServices function</span></span>
<span data-ttu-id="ec90d-104">Indique si les informations d’identification autorisent l’accès spécifié [IWbemServices](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) classe.</span><span class="sxs-lookup"><span data-stu-id="ec90d-104">Indicates whether the user credentials permit access to the specified [IWbemServices](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) class.</span></span>   
  
[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
  
## <a name="syntax"></a><span data-ttu-id="ec90d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ec90d-105">Syntax</span></span>  
  
```  
HRESULT BlessIWbemServices (
   [in] IWbemServices* pIWbemServices,
   [in] BSTR strUser, 
   [in] BSTR strPassword, 
   [in] BSTR strAuthority, 
   [in] DWORD impLevel, 
   [in] DWORD authnLevel
);
```  

## <a name="parameters"></a><span data-ttu-id="ec90d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ec90d-106">Parameters</span></span>

`pIWbemServices`\
<span data-ttu-id="ec90d-107">[in] Un pointeur vers le [IWbemServices](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) objet pour lequel les autorisations sont requises.</span><span class="sxs-lookup"><span data-stu-id="ec90d-107">[in] A pointer to the [IWbemServices](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) object for which permissions are required.</span></span>

`strUser`\
<span data-ttu-id="ec90d-108">[in] Le nom d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ec90d-108">[in] The user name.</span></span>

`strPassword`\
<span data-ttu-id="ec90d-109">[in] Le mot de passe associé `strUser`.</span><span class="sxs-lookup"><span data-stu-id="ec90d-109">[in] The password associated with `strUser`.</span></span>

`strAuthority`\
<span data-ttu-id="ec90d-110">[in] Le nom de domaine de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ec90d-110">[in] The domain name of the user.</span></span> <span data-ttu-id="ec90d-111">Consultez le [ConnectServerWmi](connectserverwmi.md) (fonction) pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="ec90d-111">See the [ConnectServerWmi](connectserverwmi.md) function for more information.</span></span>

`impLevel`\
<span data-ttu-id="ec90d-112">[in] Le niveau d’emprunt d’identité.</span><span class="sxs-lookup"><span data-stu-id="ec90d-112">[in] The impersonation level.</span></span>

`authnLevel`\
<span data-ttu-id="ec90d-113">[in] Le niveau d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="ec90d-113">[in] The authorization level.</span></span>

## <a name="return-value"></a><span data-ttu-id="ec90d-114">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="ec90d-114">Return value</span></span>

<span data-ttu-id="ec90d-115">Les valeurs suivantes est retournées par cette fonction sont définies dans le *WinError.h* fichier d’en-tête, ou vous pouvez les définir en tant que constantes dans votre code :</span><span class="sxs-lookup"><span data-stu-id="ec90d-115">The following values returned by this function are defined in the *WinError.h* header file, or you can define them as constants in your code:</span></span>

|<span data-ttu-id="ec90d-116">Constante</span><span class="sxs-lookup"><span data-stu-id="ec90d-116">Constant</span></span>  |<span data-ttu-id="ec90d-117">Value</span><span class="sxs-lookup"><span data-stu-id="ec90d-117">Value</span></span>  |<span data-ttu-id="ec90d-118">Description</span><span class="sxs-lookup"><span data-stu-id="ec90d-118">Description</span></span>  |
|---------|---------|---------|
| `E_INVALIDARG` | <span data-ttu-id="ec90d-119">0x80070057</span><span class="sxs-lookup"><span data-stu-id="ec90d-119">0x80070057</span></span> | <span data-ttu-id="ec90d-120">Un ou plusieurs arguments ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="ec90d-120">One or more arguments are invalid.</span></span> |
| `E_POINTER` | <span data-ttu-id="ec90d-121">0x80004003</span><span class="sxs-lookup"><span data-stu-id="ec90d-121">0x80004003</span></span> | <span data-ttu-id="ec90d-122">`pIWbemServices` a la valeur `null`.</span><span class="sxs-lookup"><span data-stu-id="ec90d-122">`pIWbemServices` is `null`.</span></span> | 
| `E_FAIL` | <span data-ttu-id="ec90d-123">0x80000008</span><span class="sxs-lookup"><span data-stu-id="ec90d-123">0x80000008</span></span> | <span data-ttu-id="ec90d-124">Une erreur non spécifiée s’est produite.</span><span class="sxs-lookup"><span data-stu-id="ec90d-124">An unspecified error has occurred.</span></span> |
| `E_OUTOFMEMORY` | <span data-ttu-id="ec90d-125">0x80000002</span><span class="sxs-lookup"><span data-stu-id="ec90d-125">0x80000002</span></span> | <span data-ttu-id="ec90d-126">Mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="ec90d-126">Insufficient memory is available to perform the operation.</span></span> | 
| `S_OK` | <span data-ttu-id="ec90d-127">0</span><span class="sxs-lookup"><span data-stu-id="ec90d-127">0</span></span> | <span data-ttu-id="ec90d-128">L’appel de fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="ec90d-128">The function call was successful.</span></span> | 

## <a name="requirements"></a><span data-ttu-id="ec90d-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ec90d-129">Requirements</span></span>  

 <span data-ttu-id="ec90d-130">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ec90d-130">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ec90d-131">**En-tête :** WMINet_Utils.idl</span><span class="sxs-lookup"><span data-stu-id="ec90d-131">**Header:** WMINet_Utils.idl</span></span>  
  
 <span data-ttu-id="ec90d-132">**Versions du .NET Framework :** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="ec90d-132">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ec90d-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ec90d-133">See also</span></span>

- [<span data-ttu-id="ec90d-134">WMI et compteurs de performances (référence des API non managées)</span><span class="sxs-lookup"><span data-stu-id="ec90d-134">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)