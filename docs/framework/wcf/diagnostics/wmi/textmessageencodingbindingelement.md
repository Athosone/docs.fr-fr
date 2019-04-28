---
title: TextMessageEncodingBindingElement
ms.date: 03/30/2017
ms.assetid: 885e2d7a-3436-4093-bc5f-0a404c62acdc
ms.openlocfilehash: 67c1083daa9acfd204d4de50d4e9178b25aafcf0
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61858388"
---
# <a name="textmessageencodingbindingelement"></a><span data-ttu-id="a3f58-102">TextMessageEncodingBindingElement</span><span class="sxs-lookup"><span data-stu-id="a3f58-102">TextMessageEncodingBindingElement</span></span>
<span data-ttu-id="a3f58-103">TextMessageEncodingBindingElement</span><span class="sxs-lookup"><span data-stu-id="a3f58-103">TextMessageEncodingBindingElement</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a3f58-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a3f58-104">Syntax</span></span>  
  
```csharp
class TextMessageEncodingBindingElement : MessageEncodingBindingElement  
{  
  string Encoding;  
  sint32 MaxReadPoolSize;  
  sint32 MaxWritePoolSize;  
  XmlDictionaryReaderQuotas ReaderQuotas;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="a3f58-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a3f58-105">Methods</span></span>  
 <span data-ttu-id="a3f58-106">La classe TextMessageEncodingBindingElement ne définit pas de méthodes.</span><span class="sxs-lookup"><span data-stu-id="a3f58-106">The TextMessageEncodingBindingElement class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="a3f58-107">Properties</span><span class="sxs-lookup"><span data-stu-id="a3f58-107">Properties</span></span>  
 <span data-ttu-id="a3f58-108">La classe TextMessageEncodingBindingElement a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="a3f58-108">The TextMessageEncodingBindingElement class has the following properties:</span></span>  
  
### <a name="encoding"></a><span data-ttu-id="a3f58-109">Encodage</span><span class="sxs-lookup"><span data-stu-id="a3f58-109">Encoding</span></span>  
 <span data-ttu-id="a3f58-110">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="a3f58-110">Data type: string</span></span>  
  
 <span data-ttu-id="a3f58-111">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="a3f58-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="a3f58-112">Encodage de jeu de caractères à utiliser pour l'émission de messages sur la liaison.</span><span class="sxs-lookup"><span data-stu-id="a3f58-112">The character set encoding to be used for emitting messages on the binding.</span></span>  
  
### <a name="maxreadpoolsize"></a><span data-ttu-id="a3f58-113">MaxReadPoolSize</span><span class="sxs-lookup"><span data-stu-id="a3f58-113">MaxReadPoolSize</span></span>  
 <span data-ttu-id="a3f58-114">Type de données : sint32</span><span class="sxs-lookup"><span data-stu-id="a3f58-114">Data type: sint32</span></span>  
  
 <span data-ttu-id="a3f58-115">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="a3f58-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="a3f58-116">Entier qui définit combien de messages peuvent être lus de manière simultanée sans allouer de nouveaux lecteurs.</span><span class="sxs-lookup"><span data-stu-id="a3f58-116">An integer that defines how many messages can be read simultaneously without allocating new readers.</span></span>  
  
### <a name="maxwritepoolsize"></a><span data-ttu-id="a3f58-117">MaxWritePoolSize</span><span class="sxs-lookup"><span data-stu-id="a3f58-117">MaxWritePoolSize</span></span>  
 <span data-ttu-id="a3f58-118">Type de données : sint32</span><span class="sxs-lookup"><span data-stu-id="a3f58-118">Data type: sint32</span></span>  
  
 <span data-ttu-id="a3f58-119">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="a3f58-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="a3f58-120">Entier qui définit combien de messages peuvent être envoyés simultanément sans allouer de nouveaux enregistreurs.</span><span class="sxs-lookup"><span data-stu-id="a3f58-120">An integer that defines how many messages can be sent simultaneously without allocating new writers.</span></span>  
  
### <a name="readerquotas"></a><span data-ttu-id="a3f58-121">ReaderQuotas</span><span class="sxs-lookup"><span data-stu-id="a3f58-121">ReaderQuotas</span></span>  
 <span data-ttu-id="a3f58-122">Type de données : XmlDictionaryReaderQuotas</span><span class="sxs-lookup"><span data-stu-id="a3f58-122">Data type: XmlDictionaryReaderQuotas</span></span>  
  
 <span data-ttu-id="a3f58-123">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="a3f58-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="a3f58-124">Quotas des lecteurs.</span><span class="sxs-lookup"><span data-stu-id="a3f58-124">The quotas of the readers.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a3f58-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a3f58-125">Requirements</span></span>  
  
|<span data-ttu-id="a3f58-126">MOF</span><span class="sxs-lookup"><span data-stu-id="a3f58-126">MOF</span></span>|<span data-ttu-id="a3f58-127">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="a3f58-127">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="a3f58-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a3f58-128">Namespace</span></span>|<span data-ttu-id="a3f58-129">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="a3f58-129">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="a3f58-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a3f58-130">See also</span></span>

- <xref:System.ServiceModel.Channels.TextMessageEncodingBindingElement>
