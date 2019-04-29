---
title: Enregistrements de suivi personnalisé
ms.date: 03/30/2017
ms.assetid: 24284565-c68b-40bf-b7f1-e148d151a6fc
ms.openlocfilehash: d4733b4ffc0d866cf90fd5a5e7d649de261c45fb
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61945832"
---
# <a name="custom-tracking-records"></a><span data-ttu-id="82897-102">Enregistrements de suivi personnalisé</span><span class="sxs-lookup"><span data-stu-id="82897-102">Custom Tracking Records</span></span>

<span data-ttu-id="82897-103">Cette rubrique montre comment créer des enregistrements de suivi personnalisés et les remplir avec des données à émettre avec les enregistrements.</span><span class="sxs-lookup"><span data-stu-id="82897-103">This topic demonstrates how to create custom tracking records and populate them with data to be emitted along with the records.</span></span>

## <a name="emitting-custom-tracking-records"></a><span data-ttu-id="82897-104">Émission d'enregistrements de suivi personnalisé</span><span class="sxs-lookup"><span data-stu-id="82897-104">Emitting Custom Tracking Records</span></span>

<span data-ttu-id="82897-105">Les enregistrements de suivi personnalisés peuvent être issus d'une activité de code comme indiqué dans l'exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="82897-105">Custom tracking records can be emitted from a code activity as shown in the following example.</span></span>

```csharp
protected override void Execute(CodeActivityContext context)
{
…
            CustomTrackingRecord customRecord = new CustomTrackingRecord("CustomEmailSentEvent");
            customRecord.Data.Add("SendTime", sendTime);
            context.Track(customRecord);
}
```

<span data-ttu-id="82897-106">Un <xref:System.Activities.Tracking.CustomTrackingRecord> est émis dans une activité de code en appelant la méthode <xref:System.Activities.NativeActivityContext.Track%2A> sur `ActivityContext`.</span><span class="sxs-lookup"><span data-stu-id="82897-106">A <xref:System.Activities.Tracking.CustomTrackingRecord> is emitted in a code activity by invoking the <xref:System.Activities.NativeActivityContext.Track%2A> method on the `ActivityContext`.</span></span>

## <a name="see-also"></a><span data-ttu-id="82897-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="82897-107">See also</span></span>

- [<span data-ttu-id="82897-108">Surveillance de Windows Server App Fabric</span><span class="sxs-lookup"><span data-stu-id="82897-108">Windows Server App Fabric Monitoring</span></span>](https://go.microsoft.com/fwlink/?LinkId=201273)
- [<span data-ttu-id="82897-109">Surveillance des Applications avec App Fabric</span><span class="sxs-lookup"><span data-stu-id="82897-109">Monitoring Applications with App Fabric</span></span>](https://go.microsoft.com/fwlink/?LinkId=201275)
