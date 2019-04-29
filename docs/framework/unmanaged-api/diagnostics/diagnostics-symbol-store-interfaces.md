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
# <a name="diagnostics-symbol-store-interfaces"></a><span data-ttu-id="121ba-102">Interfaces du magasin de symboles de diagnostics</span><span class="sxs-lookup"><span data-stu-id="121ba-102">Diagnostics Symbol Store Interfaces</span></span>
<span data-ttu-id="121ba-103">Cette rubrique décrit les interfaces non managées qui permettent un compilateur de générer des informations de symbole pour une utilisation par un débogueur.</span><span class="sxs-lookup"><span data-stu-id="121ba-103">This topic describes the unmanaged interfaces that enable a compiler to generate symbol information for use by a debugger.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="121ba-104">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="121ba-104">In This Section</span></span>  
 [<span data-ttu-id="121ba-105">IBindingDisplay, interface</span><span class="sxs-lookup"><span data-stu-id="121ba-105">IBindingDisplay Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/ibindingdisplay-interface.md)  
 <span data-ttu-id="121ba-106">Fournit des méthodes qui affichent des informations de liaison actuelles sur l’application en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="121ba-106">Provides methods that display current binding information about the running application.</span></span>  
  
 [<span data-ttu-id="121ba-107">IDebugAutoAttach, interface</span><span class="sxs-lookup"><span data-stu-id="121ba-107">IDebugAutoAttach Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/idebugautoattach-interface.md)  
 <span data-ttu-id="121ba-108">Définit l’interface pour l’attachement automatique du débogueur appelé par serveur.</span><span class="sxs-lookup"><span data-stu-id="121ba-108">Defines the interface for a server-invoked debugger auto attach.</span></span>  
  
 [<span data-ttu-id="121ba-109">INotifyConnection2, interface</span><span class="sxs-lookup"><span data-stu-id="121ba-109">INotifyConnection2 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/inotifyconnection2-interface.md)  
 <span data-ttu-id="121ba-110">Déclare des méthodes pour inscrire et désinscrire une source de notification de connexion.</span><span class="sxs-lookup"><span data-stu-id="121ba-110">Declares methods for registering and unregistering a connection notification source.</span></span>  
  
 [<span data-ttu-id="121ba-111">INotifySink2, interface</span><span class="sxs-lookup"><span data-stu-id="121ba-111">INotifySink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/inotifysink2-interface.md)  
 <span data-ttu-id="121ba-112">Déclare des méthodes pour la notification du récepteur.</span><span class="sxs-lookup"><span data-stu-id="121ba-112">Declares methods for sink notification.</span></span>  
  
 [<span data-ttu-id="121ba-113">INotifySource2, interface</span><span class="sxs-lookup"><span data-stu-id="121ba-113">INotifySource2 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/inotifysource2-interface.md)  
 <span data-ttu-id="121ba-114">Déclare une méthode pour définir des filtres de notification.</span><span class="sxs-lookup"><span data-stu-id="121ba-114">Declares a method for setting notification filters.</span></span>  
  
 [<span data-ttu-id="121ba-115">ISymENCUnmanagedMethod, interface</span><span class="sxs-lookup"><span data-stu-id="121ba-115">ISymENCUnmanagedMethod Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymencunmanagedmethod-interface.md)  
 <span data-ttu-id="121ba-116">Fournit des informations pour la fonctionnalité Modifier & Continuer.</span><span class="sxs-lookup"><span data-stu-id="121ba-116">Provides information for the Edit and Continue feature.</span></span>  
  
 [<span data-ttu-id="121ba-117">ISymUnmanagedAsyncMethod, interface</span><span class="sxs-lookup"><span data-stu-id="121ba-117">ISymUnmanagedAsyncMethod Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethod-interface.md)  
 <span data-ttu-id="121ba-118">Cette interface est le complément de lecture de [isymunmanagedasyncmethodpropertieswriter, Interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-interface.md).</span><span class="sxs-lookup"><span data-stu-id="121ba-118">This interface is the reading complement to [ISymUnmanagedAsyncMethodPropertiesWriter Interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-interface.md).</span></span>  
  
 [<span data-ttu-id="121ba-119">ISymUnmanagedAsyncMethodPropertiesWriter, interface</span><span class="sxs-lookup"><span data-stu-id="121ba-119">ISymUnmanagedAsyncMethodPropertiesWriter Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-interface.md)  
 <span data-ttu-id="121ba-120">Permet la définition d’informations sur la méthode async facultatif par le symbole de méthode.</span><span class="sxs-lookup"><span data-stu-id="121ba-120">Allows definition of optional async method information per method symbol.</span></span> <span data-ttu-id="121ba-121">Doit utiliser avec une méthode ouverte (autrement dit, entre les appels à la [OpenMethod, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-openmethod-method.md)et [CloseMethod, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-closemethod-method.md)).</span><span class="sxs-lookup"><span data-stu-id="121ba-121">Must use with an opened method (that is, between calls to the [OpenMethod Method](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-openmethod-method.md)and the [CloseMethod Method](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-closemethod-method.md)).</span></span>  
  
 [<span data-ttu-id="121ba-122">ISymUnmanagedBinder, interface</span><span class="sxs-lookup"><span data-stu-id="121ba-122">ISymUnmanagedBinder Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder-interface.md)  
 <span data-ttu-id="121ba-123">Représente un classeur de symboles du code non managé.</span><span class="sxs-lookup"><span data-stu-id="121ba-123">Represents a symbol binder for unmanaged code.</span></span>  
  
 [<span data-ttu-id="121ba-124">ISymUnmanagedBinder2, interface</span><span class="sxs-lookup"><span data-stu-id="121ba-124">ISymUnmanagedBinder2 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder2-interface.md)  
 <span data-ttu-id="121ba-125">Représente un classeur de symboles du code non managé et étend le `ISymUnmanagedBinder` interface.</span><span class="sxs-lookup"><span data-stu-id="121ba-125">Represents a symbol binder for unmanaged code, and extends the `ISymUnmanagedBinder` interface.</span></span>  
  
 [<span data-ttu-id="121ba-126">ISymUnmanagedBinder3, interface</span><span class="sxs-lookup"><span data-stu-id="121ba-126">ISymUnmanagedBinder3 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder3-interface.md)  
 <span data-ttu-id="121ba-127">Représente un classeur de symboles du code non managé et étend le `ISymUnmanagedBinder` interface.</span><span class="sxs-lookup"><span data-stu-id="121ba-127">Represents a symbol binder for unmanaged code, and extends the `ISymUnmanagedBinder` interface.</span></span>  
  
 [<span data-ttu-id="121ba-128">ISymUnmanagedConstant, interface</span><span class="sxs-lookup"><span data-stu-id="121ba-128">ISymUnmanagedConstant Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedconstant-interface.md)  
 <span data-ttu-id="121ba-129">Fournit l’accès aux constantes non managées.</span><span class="sxs-lookup"><span data-stu-id="121ba-129">Provides access to unmanaged constants.</span></span>  
  
 [<span data-ttu-id="121ba-130">ISymUnmanagedDispose, interface</span><span class="sxs-lookup"><span data-stu-id="121ba-130">ISymUnmanagedDispose Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddispose-interface.md)  
 <span data-ttu-id="121ba-131">Libère les ressources non managées.</span><span class="sxs-lookup"><span data-stu-id="121ba-131">Disposes of unmanaged resources.</span></span>  
  
 [<span data-ttu-id="121ba-132">ISymUnmanagedDocument, interface</span><span class="sxs-lookup"><span data-stu-id="121ba-132">ISymUnmanagedDocument Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocument-interface.md)  
 <span data-ttu-id="121ba-133">Représente un document référencé par un magasin de symboles.</span><span class="sxs-lookup"><span data-stu-id="121ba-133">Represents a document referenced by a symbol store.</span></span>  
  
 [<span data-ttu-id="121ba-134">ISymUnmanagedDocumentWriter, interface</span><span class="sxs-lookup"><span data-stu-id="121ba-134">ISymUnmanagedDocumentWriter Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocumentwriter-interface.md)  
 <span data-ttu-id="121ba-135">Fournit des méthodes d'écriture dans un document référencé par un magasin de symboles.</span><span class="sxs-lookup"><span data-stu-id="121ba-135">Provides methods for writing to a document referenced by a symbol store.</span></span>  
  
 [<span data-ttu-id="121ba-136">ISymUnmanagedENCUpdate, interface</span><span class="sxs-lookup"><span data-stu-id="121ba-136">ISymUnmanagedENCUpdate Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedencupdate-interface.md)  
 <span data-ttu-id="121ba-137">Fournit des méthodes pour la fonctionnalité Modifier & Continuer.</span><span class="sxs-lookup"><span data-stu-id="121ba-137">Provides methods for the Edit and Continue feature.</span></span>  
  
 [<span data-ttu-id="121ba-138">ISymUnmanagedMethod, interface</span><span class="sxs-lookup"><span data-stu-id="121ba-138">ISymUnmanagedMethod Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedmethod-interface.md)  
 <span data-ttu-id="121ba-139">Représente une méthode dans le magasin de symboles.</span><span class="sxs-lookup"><span data-stu-id="121ba-139">Represents a method within the symbol store.</span></span>  
  
 [<span data-ttu-id="121ba-140">ISymUnmanagedNamespace, interface</span><span class="sxs-lookup"><span data-stu-id="121ba-140">ISymUnmanagedNamespace Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagednamespace-interface.md)  
 <span data-ttu-id="121ba-141">Représente un espace de noms.</span><span class="sxs-lookup"><span data-stu-id="121ba-141">Represents a namespace.</span></span>  
  
 [<span data-ttu-id="121ba-142">ISymUnmanagedReader, interface</span><span class="sxs-lookup"><span data-stu-id="121ba-142">ISymUnmanagedReader Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-interface.md)  
 <span data-ttu-id="121ba-143">Représente un lecteur de symboles qui fournit l’accès aux documents, des méthodes et des variables dans un magasin de symboles.</span><span class="sxs-lookup"><span data-stu-id="121ba-143">Represents a symbol reader that provides access to documents, methods, and variables within a symbol store.</span></span>  
  
 [<span data-ttu-id="121ba-144">ISymUnmanagedReader2, interface</span><span class="sxs-lookup"><span data-stu-id="121ba-144">ISymUnmanagedReader2 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader2-interface.md)  
 <span data-ttu-id="121ba-145">Obtient une méthode de lecteur de symboles étant donnée un jeton de méthode et un numéro de version de modifier et copier.</span><span class="sxs-lookup"><span data-stu-id="121ba-145">Gets a symbol reader method given a method token and an edit-and-copy version number.</span></span>  
  
 [<span data-ttu-id="121ba-146">ISymUnmanagedReaderSymbolSearchInfo, interface</span><span class="sxs-lookup"><span data-stu-id="121ba-146">ISymUnmanagedReaderSymbolSearchInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreadersymbolsearchinfo-interface.md)  
 <span data-ttu-id="121ba-147">Fournit des méthodes permettant d’obtenir des informations de recherche de symboles.</span><span class="sxs-lookup"><span data-stu-id="121ba-147">Provides methods that get symbol search information.</span></span>  
  
 [<span data-ttu-id="121ba-148">ISymUnmanagedScope, interface</span><span class="sxs-lookup"><span data-stu-id="121ba-148">ISymUnmanagedScope Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-interface.md)  
 <span data-ttu-id="121ba-149">Représente une portée lexicale dans une méthode.</span><span class="sxs-lookup"><span data-stu-id="121ba-149">Represents a lexical scope within a method.</span></span>  
  
 [<span data-ttu-id="121ba-150">ISymUnmanagedScope2, interface</span><span class="sxs-lookup"><span data-stu-id="121ba-150">ISymUnmanagedScope2 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope2-interface.md)  
 <span data-ttu-id="121ba-151">Représente une portée lexicale dans une méthode et étend le `ISymUnmanagedScope` interface avec des méthodes qui obtiennent des informations sur les constantes définies dans l’étendue...</span><span class="sxs-lookup"><span data-stu-id="121ba-151">Represents a lexical scope within a method, and extends the `ISymUnmanagedScope` interface with methods that get information about constants defined within the scope..</span></span>  
  
 [<span data-ttu-id="121ba-152">ISymUnmanagedSourceServerModule, interface</span><span class="sxs-lookup"><span data-stu-id="121ba-152">ISymUnmanagedSourceServerModule Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedsourceservermodule-interface.md)  
 <span data-ttu-id="121ba-153">Fournit des données du serveur source pour un module.</span><span class="sxs-lookup"><span data-stu-id="121ba-153">Provides source server data for a module.</span></span>  
  
 [<span data-ttu-id="121ba-154">ISymUnmanagedSymbolSearchInfo, interface</span><span class="sxs-lookup"><span data-stu-id="121ba-154">ISymUnmanagedSymbolSearchInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedsymbolsearchinfo-interface.md)  
 <span data-ttu-id="121ba-155">Fournit des méthodes permettant d’obtenir des informations sur le chemin de recherche.</span><span class="sxs-lookup"><span data-stu-id="121ba-155">Provides methods that get information about the search path.</span></span>  
  
 [<span data-ttu-id="121ba-156">ISymUnmanagedVariable, interface</span><span class="sxs-lookup"><span data-stu-id="121ba-156">ISymUnmanagedVariable Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedvariable-interface.md)  
 <span data-ttu-id="121ba-157">Représente une variable, comme un paramètre, une variable locale ou un champ.</span><span class="sxs-lookup"><span data-stu-id="121ba-157">Represents a variable, such as a parameter, a local variable, or a field.</span></span>  
  
 [<span data-ttu-id="121ba-158">ISymUnmanagedWriter, interface</span><span class="sxs-lookup"><span data-stu-id="121ba-158">ISymUnmanagedWriter Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-interface.md)  
 <span data-ttu-id="121ba-159">Représente un writer de symbole et fournit des méthodes pour définir des documents, les points de séquence, les portées lexicales et variables.</span><span class="sxs-lookup"><span data-stu-id="121ba-159">Represents a symbol writer, and provides methods to define documents, sequence points, lexical scopes, and variables.</span></span>  
  
 [<span data-ttu-id="121ba-160">ISymUnmanagedWriter2, interface</span><span class="sxs-lookup"><span data-stu-id="121ba-160">ISymUnmanagedWriter2 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter2-interface.md)  
 <span data-ttu-id="121ba-161">Représente un writer de symbole et fournit des méthodes pour définir des documents, les points de séquence, les portées lexicales et variables.</span><span class="sxs-lookup"><span data-stu-id="121ba-161">Represents a symbol writer, and provides methods to define documents, sequence points, lexical scopes, and variables.</span></span> <span data-ttu-id="121ba-162">Étend la `ISymUnmanagedWriter` interface.</span><span class="sxs-lookup"><span data-stu-id="121ba-162">Extends the `ISymUnmanagedWriter` interface.</span></span>  
  
 [<span data-ttu-id="121ba-163">ISymUnmanagedWriter3, interface</span><span class="sxs-lookup"><span data-stu-id="121ba-163">ISymUnmanagedWriter3 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter3-interface.md)  
 <span data-ttu-id="121ba-164">Représente un writer de symbole et fournit des méthodes pour définir des documents, les points de séquence, les portées lexicales et variables.</span><span class="sxs-lookup"><span data-stu-id="121ba-164">Represents a symbol writer, and provides methods to define documents, sequence points, lexical scopes, and variables.</span></span> <span data-ttu-id="121ba-165">Étend la `ISymUnmanagedWriter` interface.</span><span class="sxs-lookup"><span data-stu-id="121ba-165">Extends the `ISymUnmanagedWriter` interface.</span></span>  
  
 [<span data-ttu-id="121ba-166">ISymUnmanagedWriter4, interface</span><span class="sxs-lookup"><span data-stu-id="121ba-166">ISymUnmanagedWriter4 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter4-interface.md)  
 <span data-ttu-id="121ba-167">Isymunmanagedwriter4, interface.</span><span class="sxs-lookup"><span data-stu-id="121ba-167">ISymUnmanagedWriter4 interface.</span></span>  
  
 [<span data-ttu-id="121ba-168">ISymUnmanagedWriter5, interface</span><span class="sxs-lookup"><span data-stu-id="121ba-168">ISymUnmanagedWriter5 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter5-interface.md)  
 <span data-ttu-id="121ba-169">Isymunmanagedwriter5, interface.</span><span class="sxs-lookup"><span data-stu-id="121ba-169">ISymUnmanagedWriter5 interface.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="121ba-170">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="121ba-170">Related Sections</span></span>  
 [<span data-ttu-id="121ba-171">Énumérations du magasin de symboles de diagnostics</span><span class="sxs-lookup"><span data-stu-id="121ba-171">Diagnostics Symbol Store Enumerations</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-enumerations.md)  
  
 [<span data-ttu-id="121ba-172">Structures du magasin de symboles de diagnostics</span><span class="sxs-lookup"><span data-stu-id="121ba-172">Diagnostics Symbol Store Structures</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-structures.md)  
  
 [<span data-ttu-id="121ba-173">Débogage</span><span class="sxs-lookup"><span data-stu-id="121ba-173">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
