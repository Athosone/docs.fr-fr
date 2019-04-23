---
title: ISymUnmanagedBinder2::GetReaderForFile2, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedBinder2.GetReaderForFile2
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedBinder2::GetReaderForFile2
helpviewer_keywords:
- ISymUnmanagedBinder2::GetReaderForFile2 method [.NET Framework debugging]
- GetReaderForFile2 method [.NET Framework debugging]
ms.assetid: dd92dcaf-403c-464d-a254-21594985dddd
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: fed289b2776e8ac4a12969060cd16c6163ebed2f
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59091965"
---
# <a name="isymunmanagedbinder2getreaderforfile2-method"></a><span data-ttu-id="59717-102">ISymUnmanagedBinder2::GetReaderForFile2, méthode</span><span class="sxs-lookup"><span data-stu-id="59717-102">ISymUnmanagedBinder2::GetReaderForFile2 Method</span></span>
<span data-ttu-id="59717-103">Une interface de métadonnées et un nom de fichier, retourne le correct [ISymUnmanagedReader](isymunmanagedreader-interface.md) interface qui lit les symboles de débogage associés au module.</span><span class="sxs-lookup"><span data-stu-id="59717-103">Given a metadata interface and a file name, returns the correct [ISymUnmanagedReader](isymunmanagedreader-interface.md) interface that will read the debugging symbols associated with the module.</span></span>  
  
 <span data-ttu-id="59717-104">Cette méthode fournit une recherche plus étendue pour le fichier du programme (PDB) de la base de données que le [ISymUnmanagedBinder::GetReaderForFile](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder-getreaderforfile-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="59717-104">This method provides a more extensive search for the program database (PDB) file than the [ISymUnmanagedBinder::GetReaderForFile](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder-getreaderforfile-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="59717-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="59717-105">Syntax</span></span>  
  
```  
HRESULT GetReaderForFile2(  
    [in]  IUnknown     *importer,  
    [in]  const WCHAR  *fileName,  
    [in]  const WCHAR  *searchPath,  
    [in]  ULONG32      searchPolicy,  
    [out,retval] ISymUnmanagedReader  **pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="59717-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="59717-106">Parameters</span></span>  
 `importer`  
 <span data-ttu-id="59717-107">[in] Pointeur vers l’interface d’importation de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="59717-107">[in] A pointer to the metadata import interface.</span></span>  
  
 `fileName`  
 <span data-ttu-id="59717-108">[in] Pointeur vers le nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="59717-108">[in] A pointer to the file name.</span></span>  
  
 `searchPath`  
 <span data-ttu-id="59717-109">[in] Pointeur vers le chemin de recherche.</span><span class="sxs-lookup"><span data-stu-id="59717-109">[in] A pointer to the search path.</span></span>  
  
 `searchPolicy`  
 <span data-ttu-id="59717-110">[in] Une valeur de la [CorSymSearchPolicyAttributes](../../../../docs/framework/unmanaged-api/diagnostics/corsymsearchpolicyattributes-enumeration.md) énumération qui spécifie la stratégie à utiliser lors d’une recherche pour un lecteur de symboles.</span><span class="sxs-lookup"><span data-stu-id="59717-110">[in] A value of the [CorSymSearchPolicyAttributes](../../../../docs/framework/unmanaged-api/diagnostics/corsymsearchpolicyattributes-enumeration.md) enumeration that specifies the policy to be used when doing a search for a symbol reader.</span></span>  
  
 `pRetVal`  
 <span data-ttu-id="59717-111">[out] Un pointeur qui est défini à retourné [ISymUnmanagedReader](isymunmanagedreader-interface.md) interface.</span><span class="sxs-lookup"><span data-stu-id="59717-111">[out] A pointer that is set to the returned [ISymUnmanagedReader](isymunmanagedreader-interface.md) interface.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="59717-112">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="59717-112">Return Value</span></span>  
 <span data-ttu-id="59717-113">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="59717-113">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="59717-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="59717-114">Requirements</span></span>  
 <span data-ttu-id="59717-115">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="59717-115">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="59717-116">Notes</span><span class="sxs-lookup"><span data-stu-id="59717-116">Remarks</span></span>  
 <span data-ttu-id="59717-117">Cette version de la méthode peut rechercher le fichier PDB dans des domaines autres que juste à côté du module.</span><span class="sxs-lookup"><span data-stu-id="59717-117">This version of the method can search for the PDB file in areas other than right next to the module.</span></span> <span data-ttu-id="59717-118">La stratégie de recherche peut être contrôlée en combinant [CorSymSearchPolicyAttributes](../../../../docs/framework/unmanaged-api/diagnostics/corsymsearchpolicyattributes-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="59717-118">The search policy can be controlled by combining [CorSymSearchPolicyAttributes](../../../../docs/framework/unmanaged-api/diagnostics/corsymsearchpolicyattributes-enumeration.md).</span></span> <span data-ttu-id="59717-119">Par exemple, `AllowReferencePathAccess | AllowSymbolServerAccess` recherche le fichier PDB en regard du fichier exécutable et sur un serveur de symboles, mais ne pas interroger le Registre ou le chemin d’accès dans le fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="59717-119">For example, `AllowReferencePathAccess | AllowSymbolServerAccess` looks for the PDB next to the executable file and on a symbol server, but does not query the registry or use the path in the executable file.</span></span> <span data-ttu-id="59717-120">Si le `searchPath` paramètre est fourni, ces répertoires seront toujours recherchées.</span><span class="sxs-lookup"><span data-stu-id="59717-120">If the `searchPath` parameter is provided, those directories will always be searched.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="59717-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59717-121">See also</span></span>

- [<span data-ttu-id="59717-122">ISymUnmanagedBinder2, interface</span><span class="sxs-lookup"><span data-stu-id="59717-122">ISymUnmanagedBinder2 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder2-interface.md)
- [<span data-ttu-id="59717-123">GetReaderForFile, méthode</span><span class="sxs-lookup"><span data-stu-id="59717-123">GetReaderForFile Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder-getreaderforfile-method.md)
