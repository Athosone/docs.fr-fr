---
title: Interfaces du magasin de symboles de diagnostics
ms.date: 03/30/2017
helpviewer_keywords:
- unmanaged interfaces [.NET Framework], debugging
- diagnostics symbol store interfaces [.NET Framework]
- interfaces [.NET Framework], diagnostics symbol store
- unmanaged interfaces [.NET Framework], diagnostics symbol store
- debugging interfaces [.NET Framework]
- interfaces [.NET Framework debugging]
ms.assetid: f96987d5-e6a5-478b-ac5e-302e16545cce
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 6fca7359888b8b73b2e1cf709ab708d71abf0db6
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61787892"
---
# <a name="diagnostics-symbol-store-interfaces"></a>Interfaces du magasin de symboles de diagnostics
Cette rubrique décrit les interfaces non managées qui permettent un compilateur de générer des informations de symbole pour une utilisation par un débogueur.  
  
## <a name="in-this-section"></a>Dans cette section  
 [IBindingDisplay, interface](../../../../docs/framework/unmanaged-api/diagnostics/ibindingdisplay-interface.md)  
 Fournit des méthodes qui affichent des informations de liaison actuelles sur l’application en cours d’exécution.  
  
 [IDebugAutoAttach, interface](../../../../docs/framework/unmanaged-api/diagnostics/idebugautoattach-interface.md)  
 Définit l’interface pour l’attachement automatique du débogueur appelé par serveur.  
  
 [INotifyConnection2, interface](../../../../docs/framework/unmanaged-api/diagnostics/inotifyconnection2-interface.md)  
 Déclare des méthodes pour inscrire et désinscrire une source de notification de connexion.  
  
 [INotifySink2, interface](../../../../docs/framework/unmanaged-api/diagnostics/inotifysink2-interface.md)  
 Déclare des méthodes pour la notification du récepteur.  
  
 [INotifySource2, interface](../../../../docs/framework/unmanaged-api/diagnostics/inotifysource2-interface.md)  
 Déclare une méthode pour définir des filtres de notification.  
  
 [ISymENCUnmanagedMethod, interface](../../../../docs/framework/unmanaged-api/diagnostics/isymencunmanagedmethod-interface.md)  
 Fournit des informations pour la fonctionnalité Modifier & Continuer.  
  
 [ISymUnmanagedAsyncMethod, interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethod-interface.md)  
 Cette interface est le complément de lecture de [isymunmanagedasyncmethodpropertieswriter, Interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-interface.md).  
  
 [ISymUnmanagedAsyncMethodPropertiesWriter, interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-interface.md)  
 Permet la définition d’informations sur la méthode async facultatif par le symbole de méthode. Doit utiliser avec une méthode ouverte (autrement dit, entre les appels à la [OpenMethod, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-openmethod-method.md)et [CloseMethod, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-closemethod-method.md)).  
  
 [ISymUnmanagedBinder, interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder-interface.md)  
 Représente un classeur de symboles du code non managé.  
  
 [ISymUnmanagedBinder2, interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder2-interface.md)  
 Représente un classeur de symboles du code non managé et étend le `ISymUnmanagedBinder` interface.  
  
 [ISymUnmanagedBinder3, interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder3-interface.md)  
 Représente un classeur de symboles du code non managé et étend le `ISymUnmanagedBinder` interface.  
  
 [ISymUnmanagedConstant, interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedconstant-interface.md)  
 Fournit l’accès aux constantes non managées.  
  
 [ISymUnmanagedDispose, interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddispose-interface.md)  
 Libère les ressources non managées.  
  
 [ISymUnmanagedDocument, interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocument-interface.md)  
 Représente un document référencé par un magasin de symboles.  
  
 [ISymUnmanagedDocumentWriter, interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocumentwriter-interface.md)  
 Fournit des méthodes d'écriture dans un document référencé par un magasin de symboles.  
  
 [ISymUnmanagedENCUpdate, interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedencupdate-interface.md)  
 Fournit des méthodes pour la fonctionnalité Modifier & Continuer.  
  
 [ISymUnmanagedMethod, interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedmethod-interface.md)  
 Représente une méthode dans le magasin de symboles.  
  
 [ISymUnmanagedNamespace, interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagednamespace-interface.md)  
 Représente un espace de noms.  
  
 [ISymUnmanagedReader, interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-interface.md)  
 Représente un lecteur de symboles qui fournit l’accès aux documents, des méthodes et des variables dans un magasin de symboles.  
  
 [ISymUnmanagedReader2, interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader2-interface.md)  
 Obtient une méthode de lecteur de symboles étant donnée un jeton de méthode et un numéro de version de modifier et copier.  
  
 [ISymUnmanagedReaderSymbolSearchInfo, interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreadersymbolsearchinfo-interface.md)  
 Fournit des méthodes permettant d’obtenir des informations de recherche de symboles.  
  
 [ISymUnmanagedScope, interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-interface.md)  
 Représente une portée lexicale dans une méthode.  
  
 [ISymUnmanagedScope2, interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope2-interface.md)  
 Représente une portée lexicale dans une méthode et étend le `ISymUnmanagedScope` interface avec des méthodes qui obtiennent des informations sur les constantes définies dans l’étendue...  
  
 [ISymUnmanagedSourceServerModule, interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedsourceservermodule-interface.md)  
 Fournit des données du serveur source pour un module.  
  
 [ISymUnmanagedSymbolSearchInfo, interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedsymbolsearchinfo-interface.md)  
 Fournit des méthodes permettant d’obtenir des informations sur le chemin de recherche.  
  
 [ISymUnmanagedVariable, interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedvariable-interface.md)  
 Représente une variable, comme un paramètre, une variable locale ou un champ.  
  
 [ISymUnmanagedWriter, interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-interface.md)  
 Représente un writer de symbole et fournit des méthodes pour définir des documents, les points de séquence, les portées lexicales et variables.  
  
 [ISymUnmanagedWriter2, interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter2-interface.md)  
 Représente un writer de symbole et fournit des méthodes pour définir des documents, les points de séquence, les portées lexicales et variables. Étend la `ISymUnmanagedWriter` interface.  
  
 [ISymUnmanagedWriter3, interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter3-interface.md)  
 Représente un writer de symbole et fournit des méthodes pour définir des documents, les points de séquence, les portées lexicales et variables. Étend la `ISymUnmanagedWriter` interface.  
  
 [ISymUnmanagedWriter4, interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter4-interface.md)  
 Isymunmanagedwriter4, interface.  
  
 [ISymUnmanagedWriter5, interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter5-interface.md)  
 Isymunmanagedwriter5, interface.  
  
## <a name="related-sections"></a>Rubriques connexes  
 [Énumérations du magasin de symboles de diagnostics](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-enumerations.md)  
  
 [Structures du magasin de symboles de diagnostics](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-structures.md)  
  
 [Débogage](../../../../docs/framework/unmanaged-api/debugging/index.md)
