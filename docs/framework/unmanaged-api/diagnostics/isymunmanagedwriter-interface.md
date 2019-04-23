---
title: ISymUnmanagedWriter, interface
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter
helpviewer_keywords:
- ISymUnmanagedWriter interface [.NET Framework debugging]
ms.assetid: 7d6733ec-f081-4166-bc17-de09e16dc304
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 4ac95cd5b79a2e1762fa9adf29d4d7926ab4ab7a
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59150577"
---
# <a name="isymunmanagedwriter-interface"></a>ISymUnmanagedWriter, interface
Représente un writer de symbole et fournit des méthodes pour définir des documents, les points de séquence, les portées lexicales et variables.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[Abort, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-abort-method.md)|Ferme le writer de symbole sans valider les symboles dans le magasin de symboles.|  
|[Close, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-close-method.md)|Ferme le writer de symbole après avoir validé les symboles dans le magasin de symboles.|  
|[CloseMethod, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-closemethod-method.md)|Ferme la méthode actuelle. Une fois qu’une méthode est fermée, plus aucun symbole ne peut être définie qu’il contient.|  
|[CloseNamespace, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-closenamespace-method.md)|Espace de noms le plus récemment ouvert par se ferme.|  
|[CloseScope, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-closescope-method.md)|Ferme la portée lexicale actuelle.|  
|[DefineConstant, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-defineconstant-method.md)|Définit un nom pour une valeur constante.|  
|[DefineDocument, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-definedocument-method.md)|Définit un document source.|  
|[DefineField, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-definefield-method.md)|Définit une variable unique qui n’est pas dans une méthode.|  
|[DefineGlobalVariable, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-defineglobalvariable-method.md)|Définit une variable globale unique.|  
|[DefineLocalVariable, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-definelocalvariable-method.md)|Définit une variable unique dans la portée lexicale actuelle.|  
|[DefineParameter, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-defineparameter-method.md)|Définit un paramètre unique dans la méthode actuelle.|  
|[DefineSequencePoints, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-definesequencepoints-method.md)|Définit un groupe de points de séquence dans la méthode actuelle.|  
|[GetDebugInfo, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-getdebuginfo-method.md)|Retourne les informations nécessaires pour un compilateur écrire l’entrée de répertoire de débogage dans l’en-tête du fichier exécutable portable (PE).|  
|[Initialize, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-initialize-method.md)|Définit l’interface d’émetteur de métadonnées avec laquelle ce writer sera associé et définit le nom de fichier de sortie dans lequel les symboles de débogage doit être écrite.|  
|[Initialize2, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-initialize2-method.md)|Définit l’interface d’émetteur de métadonnées avec laquelle ce writer sera associé, définit le nom de fichier de sortie auquel les symboles de débogage seront écrites et définit l’emplacement du fichier programme (PDB) de la base de données final.|  
|[OpenMethod, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-openmethod-method.md)|Ouvre une méthode dans le symbole qui est émis plus d’informations.|  
|[OpenNamespace, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-opennamespace-method.md)|Ouvre un nouvel espace de noms.|  
|[OpenScope, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-openscope-method.md)|Ouvre une nouvelle portée lexicale dans la méthode actuelle.|  
|[RemapToken, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-remaptoken-method.md)|Avertit le writer de symbole qu’un jeton de métadonnées a été remappé comme les métadonnées a été émises.|  
|[SetMethodSourceRange, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-setmethodsourcerange-method.md)|Spécifie les véritables début et la fin d’une méthode dans un fichier source.|  
|[SetScopeRange, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-setscoperange-method.md)|Définit la plage d'offsets pour la portée lexicale spécifiée.|  
|[SetSymAttribute, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-setsymattribute-method.md)|Définit un attribut personnalisé en fonction de son nom.|  
|[SetUserEntryPoint, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-setuserentrypoint-method.md)|Spécifie la méthode définie par l’utilisateur qui est le point d’entrée pour ce module.|  
|[UsingNamespace, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-usingnamespace-method.md)|Spécifie que le nom d’espace de noms complet donné est utilisé dans la portée lexicale actuellement ouverte.|  
  
## <a name="requirements"></a>Configuration requise  
 **En-tête :** CorSym.idl, CorSym.h  
  
## <a name="see-also"></a>Voir aussi

- [Interfaces du magasin de symboles de diagnostics](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-interfaces.md)
- [ISymUnmanagedWriter2, interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter2-interface.md)
- [ISymUnmanagedWriter3, interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter3-interface.md)
