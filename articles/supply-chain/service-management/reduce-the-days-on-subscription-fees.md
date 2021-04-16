---
title: Abonementa apmaksas dienu samazināšana
description: Lai samazinātu esošas abonementa maksas dienu skaitu, varat izveidot jaunu darījumu, kurā tiek noņemts laika periods, kas vairs nebūs abonementa maksas intervāla daļa.
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5e8158c99d2447835f3656027fd73d7c22121536
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836090"
---
# <a name="reduce-the-days-on-subscription-fees"></a><span data-ttu-id="d9a0f-103">Abonementa apmaksas dienu samazināšana</span><span class="sxs-lookup"><span data-stu-id="d9a0f-103">Reduce the days on subscription fees</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="d9a0f-104">Lai samazinātu esošas abonementa maksas dienu skaitu, varat izveidot jaunu darījumu, kurā tiek noņemts laika periods, kas vairs nebūs abonementa maksas intervāla daļa.</span><span class="sxs-lookup"><span data-stu-id="d9a0f-104">To reduce the number of days of an existing subscription fee, you can create a new transaction in which you remove the period of time that should no longer be part of the subscription fee interval.</span></span>

## <a name="reduce-the-days-on-a-subscription-fee"></a><span data-ttu-id="d9a0f-105">Samazināt dienu skaitu abonementa maksā</span><span class="sxs-lookup"><span data-stu-id="d9a0f-105">Reduce the days on a subscription fee</span></span>

1.  <span data-ttu-id="d9a0f-106">Noklikšķiniet uz **Pakalpojumu pārvaldība** \> **Vispārīgi** \> **Pakalpojumu abonementi** \> **Visi pakalpojumu abonementi**.</span><span class="sxs-lookup"><span data-stu-id="d9a0f-106">Click **Service management** \> **Common** \> **Service subscriptions** \> **All service subscriptions**.</span></span> <span data-ttu-id="d9a0f-107">Atlasiet pakalpojuma abonementu un darbību rūtī noklikšķiniet uz **Abonēšanas maksas**.</span><span class="sxs-lookup"><span data-stu-id="d9a0f-107">Select the service subscription, and on the Action Pane, click **Subscription fees**</span></span>

2.  <span data-ttu-id="d9a0f-108">Laukā **Abonementa tips** atlasiet **Dienu skaita samazināšana**.</span><span class="sxs-lookup"><span data-stu-id="d9a0f-108">In the **Subscription type** field, select **Reduction days**.</span></span>

3.  <span data-ttu-id="d9a0f-109">Izmantojiet lauku **Sākuma datums** un lauku **Beigu datums**, lai definētu abonementa maksas datumu intervālu, ko vēlaties noņemt no abonementa maksas perioda, pēc tam noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d9a0f-109">Use the **From date** field and the **To date** fields to define the date interval of the subscription fee that you want to remove from the subscription fee period, and then click **OK**.</span></span>

<span data-ttu-id="d9a0f-110">Lai apskatītu izveidoto darbību, veidlapā **Abonements** noklikšķiniet uz **Apmaksas darbības**.</span><span class="sxs-lookup"><span data-stu-id="d9a0f-110">To view the transaction that was created, in the **Subscription** form, click **Fee transactions**.</span></span>

## <a name="example"></a><span data-ttu-id="d9a0f-111">Paraugs</span><span class="sxs-lookup"><span data-stu-id="d9a0f-111">Example</span></span>

<span data-ttu-id="d9a0f-112">Ja abonementa darbību periods ir no 1. janvāra līdz 31. janvārim un vēlaties samazināt periodu par 10 dienām, izveidojiet jaunu darbību, kurā samazināšanas periods ir no 1. līdz 10. janvārim.</span><span class="sxs-lookup"><span data-stu-id="d9a0f-112">If a subscription transaction period runs from January 1 to January 31, and you want to reduce the period by 10 days, create a new transaction in which the reduction period is January 1 to January 10.</span></span> <span data-ttu-id="d9a0f-113">(Samazināšanas periods varētu būt arī no 5. līdz 15. janvārim vai jebkurš cits desmit dienu periods).</span><span class="sxs-lookup"><span data-stu-id="d9a0f-113">(The reduction period could also be January 5 to January 15, or any other ten day period).</span></span>

<span data-ttu-id="d9a0f-114">Turklāt, ja samazinājuma periodā **Sākuma datums** ir 21. janvāris (31 mīnus 10), varat iestatīt **Beigu datumu** jebkurā datumā pēc 31. janvāra un 10 dienas tik un tā tiks atņemtas no apmaksas darbības perioda.</span><span class="sxs-lookup"><span data-stu-id="d9a0f-114">Also, if the **From date** on the reduction period is January 21 (31 minus 10), you could set the **To date** to any date after January 31, and 10 days will still be removed from the fee transaction period.</span></span>

## <a name="see-also"></a><span data-ttu-id="d9a0f-115">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="d9a0f-115">See also</span></span>

[<span data-ttu-id="d9a0f-116">Piemērs dienu skaita samazināšanai</span><span class="sxs-lookup"><span data-stu-id="d9a0f-116">Reduction days example</span></span>](reduction-days-example.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]