---
title: ServiceCredentials
ms.date: 03/30/2017
ms.assetid: 9c780793-4785-46f7-add9-ac1ebeadb614
ms.openlocfilehash: d9563bd3bfe067ad83bfa03e7c6375a9db933f14
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61956977"
---
# <a name="servicecredentials"></a><span data-ttu-id="3efbe-102">ServiceCredentials</span><span class="sxs-lookup"><span data-stu-id="3efbe-102">ServiceCredentials</span></span>
<span data-ttu-id="3efbe-103">ServiceCredentials</span><span class="sxs-lookup"><span data-stu-id="3efbe-103">ServiceCredentials</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3efbe-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3efbe-104">Syntax</span></span>  
  
```csharp
class ServiceCredentials : Behavior  
{  
  string ClientCertificate;  
  string IssuedTokenAuthentication;  
  string Peer;  
  string SecureConversationAuthentication;  
  string ServiceCertificate;  
  string UserNameAuthentication;  
  string WindowsAuthentication;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="3efbe-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="3efbe-105">Methods</span></span>  
 <span data-ttu-id="3efbe-106">La classe ServiceCredentials ne définit aucune méthode.</span><span class="sxs-lookup"><span data-stu-id="3efbe-106">The ServiceCredentials class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="3efbe-107">Properties</span><span class="sxs-lookup"><span data-stu-id="3efbe-107">Properties</span></span>  
 <span data-ttu-id="3efbe-108">La classe ServiceCredentials a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="3efbe-108">The ServiceCredentials class has the following properties:</span></span>  
  
### <a name="clientcertificate"></a><span data-ttu-id="3efbe-109">ClientCertificate</span><span class="sxs-lookup"><span data-stu-id="3efbe-109">ClientCertificate</span></span>  
 <span data-ttu-id="3efbe-110">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="3efbe-110">Data type: string</span></span>  
  
 <span data-ttu-id="3efbe-111">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="3efbe-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3efbe-112">Paramètres d'authentification et d'approvisionnement des certificats clients pour ce service.</span><span class="sxs-lookup"><span data-stu-id="3efbe-112">The client certificate authentication and provisioning settings for this service.</span></span>  
  
### <a name="issuedtokenauthentication"></a><span data-ttu-id="3efbe-113">IssuedTokenAuthentication</span><span class="sxs-lookup"><span data-stu-id="3efbe-113">IssuedTokenAuthentication</span></span>  
 <span data-ttu-id="3efbe-114">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="3efbe-114">Data type: string</span></span>  
  
 <span data-ttu-id="3efbe-115">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="3efbe-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3efbe-116">Paramètres actuels d'authentification de jeton émis pour ce service.</span><span class="sxs-lookup"><span data-stu-id="3efbe-116">The current issued token authentication settings for this service.</span></span>  
  
### <a name="peer"></a><span data-ttu-id="3efbe-117">Peer</span><span class="sxs-lookup"><span data-stu-id="3efbe-117">Peer</span></span>  
 <span data-ttu-id="3efbe-118">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="3efbe-118">Data type: string</span></span>  
  
 <span data-ttu-id="3efbe-119">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="3efbe-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3efbe-120">Authentification des informations d'identification actuelles et fourniture des paramètres à utiliser par les points de terminaison de transport d'homologue.</span><span class="sxs-lookup"><span data-stu-id="3efbe-120">The current credential authentication and provisioning settings to be used by peer transport endpoints.</span></span>  
  
### <a name="secureconversationauthentication"></a><span data-ttu-id="3efbe-121">SecureConversationAuthentication</span><span class="sxs-lookup"><span data-stu-id="3efbe-121">SecureConversationAuthentication</span></span>  
 <span data-ttu-id="3efbe-122">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="3efbe-122">Data type: string</span></span>  
  
 <span data-ttu-id="3efbe-123">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="3efbe-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3efbe-124">Spécifie les paramètres actuels de conversation sécurisée.</span><span class="sxs-lookup"><span data-stu-id="3efbe-124">Specifies the current secure conversation settings.</span></span>  
  
### <a name="servicecertificate"></a><span data-ttu-id="3efbe-125">ServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="3efbe-125">ServiceCertificate</span></span>  
 <span data-ttu-id="3efbe-126">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="3efbe-126">Data type: string</span></span>  
  
 <span data-ttu-id="3efbe-127">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="3efbe-127">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3efbe-128">Certificat associé à ce service.</span><span class="sxs-lookup"><span data-stu-id="3efbe-128">The certificate associated with this service.</span></span>  
  
### <a name="usernameauthentication"></a><span data-ttu-id="3efbe-129">UserNameAuthentication</span><span class="sxs-lookup"><span data-stu-id="3efbe-129">UserNameAuthentication</span></span>  
 <span data-ttu-id="3efbe-130">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="3efbe-130">Data type: string</span></span>  
  
 <span data-ttu-id="3efbe-131">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="3efbe-131">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3efbe-132">Paramètres de nom d'utilisateur/mot de passe pour ce service.</span><span class="sxs-lookup"><span data-stu-id="3efbe-132">The username/password settings for this service.</span></span>  
  
### <a name="windowsauthentication"></a><span data-ttu-id="3efbe-133">WindowsAuthentication</span><span class="sxs-lookup"><span data-stu-id="3efbe-133">WindowsAuthentication</span></span>  
 <span data-ttu-id="3efbe-134">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="3efbe-134">Data type: string</span></span>  
  
 <span data-ttu-id="3efbe-135">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="3efbe-135">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3efbe-136">Paramètres d'authentification Windows pour ce service.</span><span class="sxs-lookup"><span data-stu-id="3efbe-136">The Windows authentication settings for this service.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3efbe-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3efbe-137">Requirements</span></span>  
  
|<span data-ttu-id="3efbe-138">MOF</span><span class="sxs-lookup"><span data-stu-id="3efbe-138">MOF</span></span>|<span data-ttu-id="3efbe-139">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="3efbe-139">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="3efbe-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3efbe-140">Namespace</span></span>|<span data-ttu-id="3efbe-141">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="3efbe-141">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="3efbe-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3efbe-142">See also</span></span>

- <xref:System.ServiceModel.Description.ServiceCredentials>
