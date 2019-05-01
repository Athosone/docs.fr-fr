---
title: StrongNameKeyGen, fonction
ms.date: 03/30/2017
api_name:
- StrongNameKeyGen
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- StrongNameKeyGen
helpviewer_keywords:
- StrongNameKeyGen function [.NET Framework strong naming]
ms.assetid: 883e413a-ad2f-4f7f-b1b9-aeb8fe5b65f8
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a8ebecce4078ba6c2b59e6bfba2d54300ba0c4ee
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62000257"
---
# <a name="strongnamekeygen-function"></a><span data-ttu-id="25a34-102">StrongNameKeyGen, fonction</span><span class="sxs-lookup"><span data-stu-id="25a34-102">StrongNameKeyGen Function</span></span>
<span data-ttu-id="25a34-103">Crée une nouvelle paire de clés publique/privée pour une utilisation de nom fort.</span><span class="sxs-lookup"><span data-stu-id="25a34-103">Creates a new public/private key pair for strong name use.</span></span>  
  
 <span data-ttu-id="25a34-104">Cette fonction a été déconseillée.</span><span class="sxs-lookup"><span data-stu-id="25a34-104">This function has been deprecated.</span></span> <span data-ttu-id="25a34-105">Utilisez le [ICLRStrongName::StrongNameKeyGen](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamekeygen-method.md) méthode à la place.</span><span class="sxs-lookup"><span data-stu-id="25a34-105">Use the [ICLRStrongName::StrongNameKeyGen](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamekeygen-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="25a34-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="25a34-106">Syntax</span></span>  
  
```  
BOOLEAN StrongNameKeyGen (  
    [in]  LPCWSTR   wszKeyContainer,  
    [in]  DWORD     dwFlags,  
    [out] BYTE      **ppbKeyBlob,  
    [out] ULONG     *pcbKeyBlob  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="25a34-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="25a34-107">Parameters</span></span>  
 `wszKeyContainer`  
 <span data-ttu-id="25a34-108">[in] Le nom du conteneur de clé demandé.</span><span class="sxs-lookup"><span data-stu-id="25a34-108">[in] The requested key container name.</span></span> <span data-ttu-id="25a34-109">`wszKeyContainer` doit être une chaîne non vide, ou null pour générer un nom temporaire.</span><span class="sxs-lookup"><span data-stu-id="25a34-109">`wszKeyContainer` must be a non-empty string, or null to generate a temporary name.</span></span>  
  
 `dwFlags`  
 <span data-ttu-id="25a34-110">[in] Spécifie s’il faut laisser la clé enregistrée.</span><span class="sxs-lookup"><span data-stu-id="25a34-110">[in] Specifies whether to leave the key registered.</span></span> <span data-ttu-id="25a34-111">Les valeurs suivantes sont prises en charge :</span><span class="sxs-lookup"><span data-stu-id="25a34-111">The following values are supported:</span></span>  
  
- <span data-ttu-id="25a34-112">0 x 00000000 - utilisée lorsque `wszKeyContainer` a la valeur null pour générer un nom de conteneur de clé temporaire.</span><span class="sxs-lookup"><span data-stu-id="25a34-112">0x00000000 - Used when `wszKeyContainer` is null to generate a temporary key container name.</span></span>  
  
- <span data-ttu-id="25a34-113">0 x 00000001 (`SN_LEAVE_KEY`)-Spécifie que la clé doit être inscrit à gauche.</span><span class="sxs-lookup"><span data-stu-id="25a34-113">0x00000001 (`SN_LEAVE_KEY`) - Specifies that the key should be left registered.</span></span>  
  
 `ppbKeyBlob`  
 <span data-ttu-id="25a34-114">[out] La paire de clés publique/privée retournée.</span><span class="sxs-lookup"><span data-stu-id="25a34-114">[out] The returned public/private key pair.</span></span>  
  
 `pcbKeyBlob`  
 <span data-ttu-id="25a34-115">[out] La taille, en octets, de `ppbKeyBlob`.</span><span class="sxs-lookup"><span data-stu-id="25a34-115">[out] The size, in bytes, of `ppbKeyBlob`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="25a34-116">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="25a34-116">Return Value</span></span>  
 <span data-ttu-id="25a34-117">`true` de réussite ; Sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="25a34-117">`true` on successful completion; otherwise, `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="25a34-118">Notes</span><span class="sxs-lookup"><span data-stu-id="25a34-118">Remarks</span></span>  
 <span data-ttu-id="25a34-119">Le `StrongNameKeyGen` fonction crée une clé 1024 bits.</span><span class="sxs-lookup"><span data-stu-id="25a34-119">The `StrongNameKeyGen` function creates a 1024-bit key.</span></span> <span data-ttu-id="25a34-120">Une fois que la clé est récupérée, vous devez appeler la [StrongNameFreeBuffer](../../../../docs/framework/unmanaged-api/strong-naming/strongnamefreebuffer-function.md) (fonction) pour libérer la mémoire allouée.</span><span class="sxs-lookup"><span data-stu-id="25a34-120">After the key is retrieved, you should call the [StrongNameFreeBuffer](../../../../docs/framework/unmanaged-api/strong-naming/strongnamefreebuffer-function.md) function to release the allocated memory.</span></span>  
  
 <span data-ttu-id="25a34-121">Si le `StrongNameKeyGen` (fonction) ne pas aboutir, appelez le [StrongNameErrorInfo](../../../../docs/framework/unmanaged-api/strong-naming/strongnameerrorinfo-function.md) fonction pour récupérer la dernière erreur générée.</span><span class="sxs-lookup"><span data-stu-id="25a34-121">If the `StrongNameKeyGen` function does not complete successfully, call the [StrongNameErrorInfo](../../../../docs/framework/unmanaged-api/strong-naming/strongnameerrorinfo-function.md) function to retrieve the last generated error.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="25a34-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="25a34-122">Requirements</span></span>  
 <span data-ttu-id="25a34-123">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="25a34-123">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="25a34-124">**En-tête :** StrongName.h</span><span class="sxs-lookup"><span data-stu-id="25a34-124">**Header:** StrongName.h</span></span>  
  
 <span data-ttu-id="25a34-125">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="25a34-125">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="25a34-126">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="25a34-126">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="25a34-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="25a34-127">See also</span></span>

- [<span data-ttu-id="25a34-128">StrongNameKeyGen, méthode</span><span class="sxs-lookup"><span data-stu-id="25a34-128">StrongNameKeyGen Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamekeygen-method.md)
- [<span data-ttu-id="25a34-129">StrongNameKeyGenEx, méthode</span><span class="sxs-lookup"><span data-stu-id="25a34-129">StrongNameKeyGenEx Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamekeygenex-method.md)
- [<span data-ttu-id="25a34-130">ICLRStrongName, interface</span><span class="sxs-lookup"><span data-stu-id="25a34-130">ICLRStrongName Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)
