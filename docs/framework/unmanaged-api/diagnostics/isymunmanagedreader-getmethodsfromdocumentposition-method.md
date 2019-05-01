---
title: ISymUnmanagedReader::GetMethodsFromDocumentPosition, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedReader.GetMethodsFromDocumentPosition
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedReader::GetMethodsFromDocumentPosition
helpviewer_keywords:
- GetMethodsFromDocumentPosition method [.NET Framework debugging]
- ISymUnmanagedReader::GetMethodsFromDocumentPosition method [.NET Framework debugging]
ms.assetid: 83605f1e-e4f3-49e6-859b-f13cad68bb54
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 64d7f138094e03ca76ec78a50a6f37aa3d9ca2f0
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61968764"
---
# <a name="isymunmanagedreadergetmethodsfromdocumentposition-method"></a><span data-ttu-id="8698d-102">ISymUnmanagedReader::GetMethodsFromDocumentPosition, méthode</span><span class="sxs-lookup"><span data-stu-id="8698d-102">ISymUnmanagedReader::GetMethodsFromDocumentPosition Method</span></span>
<span data-ttu-id="8698d-103">Retourne un tableau des méthodes, chacune contenant le point d’arrêt à la position donnée dans un document.</span><span class="sxs-lookup"><span data-stu-id="8698d-103">Returns an array of methods, each of which contains the breakpoint at the given position in a document.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8698d-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8698d-104">Syntax</span></span>  
  
```  
HRESULT GetMethodsFromDocumentPosition (  
    [in]  ISymUnmanagedDocument* document,  
    [in]  ULONG32 line,  
    [in]  ULONG32 column,  
    [in]  ULONG32 cMethod,  
    [out] ULONG32* pcMethod,  
    [out, size_is (cMethod),  
        length_is (*pcMethod)] ISymUnmanagedMethod* pRetVal[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="8698d-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8698d-105">Parameters</span></span>  
 `document`  
 <span data-ttu-id="8698d-106">[in] Le document spécifié.</span><span class="sxs-lookup"><span data-stu-id="8698d-106">[in] The specified document.</span></span>  
  
 `line`  
 <span data-ttu-id="8698d-107">[in] La ligne du document spécifié.</span><span class="sxs-lookup"><span data-stu-id="8698d-107">[in] The line of the specified document.</span></span>  
  
 `column`  
 <span data-ttu-id="8698d-108">[in] La colonne du document spécifié.</span><span class="sxs-lookup"><span data-stu-id="8698d-108">[in] The column of the specified document.</span></span>  
  
 `cMethod`  
 <span data-ttu-id="8698d-109">[in] Taille du tableau `pRetVal`.</span><span class="sxs-lookup"><span data-stu-id="8698d-109">[in] The size of the `pRetVal` array.</span></span>  
  
 `pcMethod`  
 <span data-ttu-id="8698d-110">[out] Un pointeur vers une variable qui reçoit le nombre d’éléments retournés dans le `pRetVal` tableau.</span><span class="sxs-lookup"><span data-stu-id="8698d-110">[out] A pointer to a variable that receives the number of elements returned in the `pRetVal` array.</span></span>  
  
 `pRetVal`  
 <span data-ttu-id="8698d-111">[out] Un tableau de pointeurs, chacun d’eux pointe vers un [ISymUnmanagedMethod](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedmethod-interface.md) objet qui représente une méthode qui contient le point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="8698d-111">[out] An array of pointers, each of which points to an [ISymUnmanagedMethod](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedmethod-interface.md) object that represents a method containing the breakpoint.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="8698d-112">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="8698d-112">Return Value</span></span>  
 <span data-ttu-id="8698d-113">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="8698d-113">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8698d-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8698d-114">Requirements</span></span>  
 <span data-ttu-id="8698d-115">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="8698d-115">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8698d-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8698d-116">See also</span></span>

- [<span data-ttu-id="8698d-117">ISymUnmanagedReader, interface</span><span class="sxs-lookup"><span data-stu-id="8698d-117">ISymUnmanagedReader Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-interface.md)
