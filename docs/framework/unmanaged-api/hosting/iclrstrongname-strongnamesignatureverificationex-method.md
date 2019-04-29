---
title: Méthode ICLRStrongName::StrongNameSignatureVerificationEx
ms.date: 03/30/2017
api_name:
- ICLRStrongName.StrongNameSignatureVerificationEx
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRStrongName::StrongNameSignatureVerificationEx
helpviewer_keywords:
- StrongNameSignatureVerificationEx method, ICLRStrongName interface [.NET Framework hosting]
- ICLRStrongName::StrongNameSignatureVerificationEx method [.NET Framework hosting]
ms.assetid: dbd2f662-208b-4174-b301-5c99af91040f
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: b36e1d34b874f47f1edb0e1ffe3dc2fe2d87ddcc
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61787931"
---
# <a name="iclrstrongnamestrongnamesignatureverificationex-method"></a><span data-ttu-id="7729e-102">Méthode ICLRStrongName::StrongNameSignatureVerificationEx</span><span class="sxs-lookup"><span data-stu-id="7729e-102">ICLRStrongName::StrongNameSignatureVerificationEx Method</span></span>
<span data-ttu-id="7729e-103">Obtient une valeur qui indique si le manifeste d’assembly dans le chemin d’accès fourni contient une signature de nom fort.</span><span class="sxs-lookup"><span data-stu-id="7729e-103">Gets a value that indicates whether the assembly manifest at the supplied path contains a strong name signature.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7729e-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7729e-104">Syntax</span></span>  
  
```  
HRESULT StrongNameSignatureVerificationEx (  
    [in]  LPCWSTR   wszFilePath,  
    [in]  BOOLEAN   fForceVerification,  
    [out] BOOLEAN   *pfWasVerified  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="7729e-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7729e-105">Parameters</span></span>  
 `wszFilePath`  
 <span data-ttu-id="7729e-106">[in] Le chemin d’accès pour le fichier exécutable portable (.exe ou .dll) pour l’assembly à vérifier.</span><span class="sxs-lookup"><span data-stu-id="7729e-106">[in] The path to the portable executable (.exe or .dll) file for the assembly to be verified.</span></span>  
  
 `fForceVerification`  
 <span data-ttu-id="7729e-107">[in] `true` pour effectuer la vérification, même s’il est nécessaire de remplacer les paramètres de Registre ; sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="7729e-107">[in] `true` to perform verification, even if it is necessary to override registry settings; otherwise, `false`.</span></span>  
  
 `pfWasVerified`  
 <span data-ttu-id="7729e-108">[out] `true` si la signature de nom fort a été vérifiée ; sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="7729e-108">[out] `true` if the strong name signature was verified; otherwise, `false`.</span></span> <span data-ttu-id="7729e-109">`pfWasVerified` est également défini sur `false` si la vérification a réussi en raison des paramètres de Registre.</span><span class="sxs-lookup"><span data-stu-id="7729e-109">`pfWasVerified` is also set to `false` if the verification was successful due to registry settings.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="7729e-110">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="7729e-110">Return Value</span></span>  
 <span data-ttu-id="7729e-111">`S_OK` Si la vérification a réussi ; Sinon, une valeur HRESULT qui indique un échec (consultez [valeurs HRESULT courantes](https://go.microsoft.com/fwlink/?LinkId=213878) pour obtenir la liste).</span><span class="sxs-lookup"><span data-stu-id="7729e-111">`S_OK` if the verification was successful; otherwise, an HRESULT value that indicates failure (see [Common HRESULT Values](https://go.microsoft.com/fwlink/?LinkId=213878) for a list).</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="7729e-112">Notes</span><span class="sxs-lookup"><span data-stu-id="7729e-112">Remarks</span></span>  
 <span data-ttu-id="7729e-113">Le [ICLRStrongName::StrongNameSignatureVerificationEx](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamesignatureverificationex-method.md) méthode fournit une fonctionnalité semblable à la [ICLRStrongName::StrongNameSignatureVerification](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamesignatureverification-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="7729e-113">The [ICLRStrongName::StrongNameSignatureVerificationEx](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamesignatureverificationex-method.md) method provides a capability similar to the [ICLRStrongName::StrongNameSignatureVerification](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamesignatureverification-method.md) method.</span></span> <span data-ttu-id="7729e-114">Toutefois, le deuxième paramètre d’entrée et le paramètre de sortie pour [ICLRStrongName::StrongNameSignatureVerificationEx](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamesignatureverificationex-method.md) sont de type `BOOLEAN` au lieu de `DWORD`.</span><span class="sxs-lookup"><span data-stu-id="7729e-114">However, the second input parameter and the output parameter for [ICLRStrongName::StrongNameSignatureVerificationEx](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamesignatureverificationex-method.md) are of type `BOOLEAN` instead of `DWORD`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7729e-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7729e-115">Requirements</span></span>  
 <span data-ttu-id="7729e-116">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="7729e-116">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7729e-117">**En-tête :** MetaHost.h</span><span class="sxs-lookup"><span data-stu-id="7729e-117">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="7729e-118">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="7729e-118">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="7729e-119">**Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7729e-119">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7729e-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7729e-120">See also</span></span>

- [<span data-ttu-id="7729e-121">StrongNameSignatureVerification, méthode</span><span class="sxs-lookup"><span data-stu-id="7729e-121">StrongNameSignatureVerification Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamesignatureverification-method.md)
- [<span data-ttu-id="7729e-122">ICLRStrongName, interface</span><span class="sxs-lookup"><span data-stu-id="7729e-122">ICLRStrongName Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)
