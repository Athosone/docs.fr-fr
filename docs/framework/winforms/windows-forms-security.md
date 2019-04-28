---
title: Sécurité des Windows Forms
ms.date: 03/30/2017
helpviewer_keywords:
- designer access security [Windows Forms]
- permissions [Windows Forms], Windows Forms
- Windows Forms, security
- security [Windows Forms]
- access control [Windows Forms], Windows Forms
- security policy [Windows Forms], Windows Forms
ms.assetid: 932d438a-5285-46d8-a958-8c93d0ad6cae
ms.openlocfilehash: f64d5ef2e9bb0e977b4c007e8c5109ac0c331a84
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61799370"
---
# <a name="windows-forms-security"></a><span data-ttu-id="45bc7-102">Sécurité des Windows Forms</span><span class="sxs-lookup"><span data-stu-id="45bc7-102">Windows Forms Security</span></span>
<span data-ttu-id="45bc7-103">Windows Forms propose un modèle de sécurité est basée sur le code (niveaux de sécurité sont définis pour le code, quel que soit l’utilisateur qui exécute le code).</span><span class="sxs-lookup"><span data-stu-id="45bc7-103">Windows Forms features a security model that is code-based (security levels are set for code, regardless of the user running the code).</span></span> <span data-ttu-id="45bc7-104">Cela s’ajoute tous les schémas de sécurité qui peuvent être déjà en place sur votre système informatique.</span><span class="sxs-lookup"><span data-stu-id="45bc7-104">This is in addition to any security schemas that may be in place already on your computer system.</span></span> <span data-ttu-id="45bc7-105">Celles-ci peuvent inclure celles figurant dans le navigateur (par exemple, la sécurité par zone disponible dans Internet Explorer) ou le système d’exploitation (par exemple, la sécurité basée sur les informations d’identification de Windows NT).</span><span class="sxs-lookup"><span data-stu-id="45bc7-105">These can include those in the browser (such as the zone-based security available in Internet Explorer) or the operating system (such as the credential-based security of Windows NT).</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="45bc7-106">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="45bc7-106">In This Section</span></span>  
 [<span data-ttu-id="45bc7-107">Vue d’ensemble de la sécurité dans les Windows Forms</span><span class="sxs-lookup"><span data-stu-id="45bc7-107">Security in Windows Forms Overview</span></span>](security-in-windows-forms-overview.md)  
 <span data-ttu-id="45bc7-108">Présente brièvement le modèle de sécurité .NET Framework et les étapes de base nécessaires pour assurer les formulaires Windows dans votre application.</span><span class="sxs-lookup"><span data-stu-id="45bc7-108">Briefly explains the .NET Framework security model and the basic steps necessary to ensure the Windows Forms in your application are secure.</span></span>  
  
 [<span data-ttu-id="45bc7-109">Accès plus sécurisé aux fichiers et aux données dans les Windows Forms</span><span class="sxs-lookup"><span data-stu-id="45bc7-109">More Secure File and Data Access in Windows Forms</span></span>](more-secure-file-and-data-access-in-windows-forms.md)  
 <span data-ttu-id="45bc7-110">Décrit comment accéder aux fichiers et des données dans un environnement de confiance partiel.</span><span class="sxs-lookup"><span data-stu-id="45bc7-110">Describes how to access files and data in a semi-trusted environment.</span></span>  
  
 [<span data-ttu-id="45bc7-111">Impression plus sécurisée dans les Windows Forms</span><span class="sxs-lookup"><span data-stu-id="45bc7-111">More Secure Printing in Windows Forms</span></span>](more-secure-printing-in-windows-forms.md)  
 <span data-ttu-id="45bc7-112">Décrit comment accéder aux fonctionnalités d’impression dans un environnement de confiance partiel.</span><span class="sxs-lookup"><span data-stu-id="45bc7-112">Describes how to access printing features in a semi-trusted environment.</span></span>  
  
 [<span data-ttu-id="45bc7-113">Considérations supplémentaires sur la sécurité des Windows Forms</span><span class="sxs-lookup"><span data-stu-id="45bc7-113">Additional Security Considerations in Windows Forms</span></span>](additional-security-considerations-in-windows-forms.md)  
 <span data-ttu-id="45bc7-114">Décrit comment manipuler des fenêtres, l’utilisation du Presse-papiers et effectuer des appels au code non managé dans un environnement de confiance partiel.</span><span class="sxs-lookup"><span data-stu-id="45bc7-114">Describes performing window manipulation, using the Clipboard, and making calls to unmanaged code in a semi-trusted environment.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="45bc7-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="45bc7-115">Related Sections</span></span>  
 <span data-ttu-id="45bc7-116">[Stratégie de sécurité par défaut](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/03kwzyfc(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="45bc7-116">[Default Security Policy](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/03kwzyfc(v=vs.100))</span></span>  
 <span data-ttu-id="45bc7-117">Répertorie les autorisations par défaut accordées dans les jeux d’autorisations confiance totale, Intranet Local et Internet.</span><span class="sxs-lookup"><span data-stu-id="45bc7-117">Lists the default permissions granted in the Full Trust, Local Intranet, and Internet permission sets.</span></span>  
  
 <span data-ttu-id="45bc7-118">[Administration de stratégie de sécurité générale](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/ed5htz45(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="45bc7-118">[General Security Policy Administration](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/ed5htz45(v=vs.100))</span></span>  
 <span data-ttu-id="45bc7-119">Fournit des informations sur l’administration de la stratégie de sécurité .NET Framework et l’élévation d’autorisations.</span><span class="sxs-lookup"><span data-stu-id="45bc7-119">Gives information about the administering the .NET Framework security policy and elevating permissions.</span></span>  
  
 [<span data-ttu-id="45bc7-120">Autorisations dangereuses et Administration de stratégie</span><span class="sxs-lookup"><span data-stu-id="45bc7-120">Dangerous Permissions and Policy Administration</span></span>](../misc/dangerous-permissions-and-policy-administration.md)  
 <span data-ttu-id="45bc7-121">Traite de certaines autorisations du.NET Framework susceptibles de permettre le contournement du système de sécurité.</span><span class="sxs-lookup"><span data-stu-id="45bc7-121">Discusses some of the.NET Framework permissions that can potentially allow the security system to be circumvented.</span></span>  
  
 [<span data-ttu-id="45bc7-122">Instructions de codage sécurisé</span><span class="sxs-lookup"><span data-stu-id="45bc7-122">Secure Coding Guidelines</span></span>](../../standard/security/secure-coding-guidelines.md)  
 <span data-ttu-id="45bc7-123">Liens vers des rubriques qui expliquent les meilleures pratiques pour l’écriture en toute sécurité de code par rapport à .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="45bc7-123">Links to topics that explain the best practices for securely writing code against the .NET Framework.</span></span>  
  
 <span data-ttu-id="45bc7-124">[Demande des autorisations](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/yd267cce(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="45bc7-124">[Requesting Permissions](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/yd267cce(v=vs.100))</span></span>  
 <span data-ttu-id="45bc7-125">Décrit l’utilisation d’attributs pour informer le runtime les autorisations que votre code doit s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="45bc7-125">Discusses the use of attributes to let the runtime know what permissions your code needs to run.</span></span>  
  
 [<span data-ttu-id="45bc7-126">Concepts fondamentaux sur la sécurité</span><span class="sxs-lookup"><span data-stu-id="45bc7-126">Key Security Concepts</span></span>](../../standard/security/key-security-concepts.md)  
 <span data-ttu-id="45bc7-127">Liens vers des rubriques qui couvrent les aspects de sécurité du code base.</span><span class="sxs-lookup"><span data-stu-id="45bc7-127">Links to topics that cover the basic aspects of code security.</span></span>  
  
 [<span data-ttu-id="45bc7-128">Notions fondamentales de la sécurité d’accès du code</span><span class="sxs-lookup"><span data-stu-id="45bc7-128">Code Access Security Basics</span></span>](../misc/code-access-security-basics.md)  
 <span data-ttu-id="45bc7-129">Explique les principes fondamentaux de l’utilisation de la stratégie de sécurité du .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="45bc7-129">Discusses the basics of working with the .NET Framework run time security policy.</span></span>  
  
 <span data-ttu-id="45bc7-130">[Détermination des cas modifier la stratégie de sécurité](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/xky659fc(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="45bc7-130">[Determining When to Modify Security Policy](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/xky659fc(v=vs.100))</span></span>  
 <span data-ttu-id="45bc7-131">Explique comment déterminer quand vos applications doivent diverger de la stratégie de sécurité par défaut.</span><span class="sxs-lookup"><span data-stu-id="45bc7-131">Explains how to determine when your applications need to diverge from the default security policy.</span></span>  
  
 <span data-ttu-id="45bc7-132">[Déploiement de la stratégie de sécurité](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/13wcxx6y(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="45bc7-132">[Deploying Security Policy](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/13wcxx6y(v=vs.100))</span></span>  
 <span data-ttu-id="45bc7-133">Décrit la méthode la mieux adaptée pour déployer les modifications de stratégie de sécurité.</span><span class="sxs-lookup"><span data-stu-id="45bc7-133">Discusses the best manner for deploying security policy changes.</span></span>
