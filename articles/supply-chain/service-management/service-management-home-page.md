---
title: Pakalpojumu pārvaldība
description: Izmantojiet sadaļu Pakalpojumu pārvaldība, lai izveidotu pakalpojumu līgumus un pakalpojumu abonementus, apstrādātu pakalpojumu pasūtījumus un klientu pieprasījumus, un lai pārvaldītu un analizētu pakalpojumu piegādes klientiem.
author: ShylaThompson
manager: AnnBe
ms.date: 05/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 89035687d87c674cca7fa5fd3126100c4c0ad892
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1562607"
---
# <a name="service-management"></a><span data-ttu-id="e48c1-103">Pakalpojumu pārvaldība</span><span class="sxs-lookup"><span data-stu-id="e48c1-103">Service management</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="e48c1-104">Izmantojiet sadaļu **Pakalpojumu pārvaldība**, lai izveidotu pakalpojumu līgumus un pakalpojumu abonementus, apstrādātu pakalpojumu pasūtījumus un klientu pieprasījumus, un lai pārvaldītu un analizētu pakalpojumu piegādes klientiem.</span><span class="sxs-lookup"><span data-stu-id="e48c1-104">Use **Service management** to establish service agreements and service subscriptions, handle service orders and customer inquiries, and to manage and analyze the delivery of services to customers.</span></span> <span data-ttu-id="e48c1-105">Pakalpojumu līgumus var izmantot, lai definētu resursus, ko izmantot tipiskā pakalpojumu vizītē.</span><span class="sxs-lookup"><span data-stu-id="e48c1-105">You can use service agreements to define the resources that are used in a typical service visit.</span></span> <span data-ttu-id="e48c1-106">Pakalpojumu līgumus var arī izmantot, lai skatītu, kā šie resursi tiek iekļauti klienta rēķinos.</span><span class="sxs-lookup"><span data-stu-id="e48c1-106">You can also use service agreements to view how those resources are invoiced to the customer.</span></span> <span data-ttu-id="e48c1-107">Pakalpojuma līgumā var arī ietvert pakalpojumu līmeņa vienošanos, kas nosaka standarta atbildes laikus un piedāvā rīkus faktiskā laika ierakstīšanai.</span><span class="sxs-lookup"><span data-stu-id="e48c1-107">A service agreement can also include a service level agreement that specifies standard response times, and offers tools to record the actual time.</span></span>

<span data-ttu-id="e48c1-108">Varat izveidot pakalpojumu pasūtījumus, lai pārvaldītu informāciju par plānotajām un neplānotajām servisa speciālista vizītēm klienta atrašanās vietā.</span><span class="sxs-lookup"><span data-stu-id="e48c1-108">You can create service orders to manage information about scheduled and unscheduled visits by a service technician to a customer site.</span></span> <span data-ttu-id="e48c1-109">Pakalpojumu pasūtījumi ietver šādu informāciju, piemēram:</span><span class="sxs-lookup"><span data-stu-id="e48c1-109">Service orders include information such as:</span></span>

1.  <span data-ttu-id="e48c1-110">Servisa speciālista veicamo darba stundu skaitu</span><span class="sxs-lookup"><span data-stu-id="e48c1-110">The hours of work that the service technician will perform</span></span>

2.  <span data-ttu-id="e48c1-111">Pakalpojumu vai labošanas veidu</span><span class="sxs-lookup"><span data-stu-id="e48c1-111">The type of service or repair</span></span>

3.  <span data-ttu-id="e48c1-112">Labojamo objektu, ieskaitot detaļas par problēmām un diagnozi</span><span class="sxs-lookup"><span data-stu-id="e48c1-112">The item to repair, including details about the symptoms and diagnosis</span></span>

4.  <span data-ttu-id="e48c1-113">Visus izdevumus un maksas, kas saistītas ar pakalpojumu vai labošanu</span><span class="sxs-lookup"><span data-stu-id="e48c1-113">Any expenses and fees related to the service or repair</span></span>

<span data-ttu-id="e48c1-114">Apkalpošanas pieprasījumus varat saņemt, apstrādāt un nosūtīt.</span><span class="sxs-lookup"><span data-stu-id="e48c1-114">You can receive, process, and dispatch service requests.</span></span> <span data-ttu-id="e48c1-115">Pēc pakalpojumu pasūtījuma izveidošanas varat izmantot pakalpojumu stadijas, lai pārraudzītu un precizētu nosacījumus, kas kontrolē iespējotās darbības katrā stadijā.</span><span class="sxs-lookup"><span data-stu-id="e48c1-115">After you have created a service order, you can use service stages to monitor progress and specify rules that control what actions are enabled in each stage.</span></span> <span data-ttu-id="e48c1-116">Kad pakalpojuma pasūtījums ir pabeigts, jūs varat parakstīt pasūtījumu, lai apstiprinātu, ka tas ir pabeigts, un pēc tam to iegrāmatojiet, lai uzsāktu rēķina procesu.</span><span class="sxs-lookup"><span data-stu-id="e48c1-116">When a service order is complete, you can sign off on the order to confirm that it is complete, and then post the order to start the invoice process.</span></span>

<span data-ttu-id="e48c1-117">Lietojiet atskaišu rīkus, lai pārraudzītu pakalpojumu pasūtījuma summas un abonementu darbības, un izdrukājiet darbu aprakstus un darba rēķinus.</span><span class="sxs-lookup"><span data-stu-id="e48c1-117">Use the reporting tools to monitor service order margins and subscription transactions, and print work descriptions and work receipts.</span></span>

## <a name="business-processes"></a><span data-ttu-id="e48c1-118">Biznesa procesi</span><span class="sxs-lookup"><span data-stu-id="e48c1-118">Business processes</span></span>

<span data-ttu-id="e48c1-119">Tālāk esošajā diagrammā ir parādīti moduļa **Pakalpojumu pārvaldība** augsta līmeņa biznesa procesi un ir norādīts, kur apkalpošanas procesi ir integrēti citos Microsoft Dynamics 365 for Finance and Operations moduļos.</span><span class="sxs-lookup"><span data-stu-id="e48c1-119">The following diagram illustrates the high level business processes for **Service management**, and shows where service processes integrate with other modules in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="e48c1-120">[![Pakalpojumu pārvaldības biznesa procesu diagramma](./media/sm_home_page.gif)](./media/sm_home_page.gif)</span><span class="sxs-lookup"><span data-stu-id="e48c1-120">[![Service management business process diagram](./media/sm_home_page.gif)](./media/sm_home_page.gif)</span></span>

## <a name="service-management-at-a-glance"></a><span data-ttu-id="e48c1-121">Pakalpojumu pārvaldības apskats</span><span class="sxs-lookup"><span data-stu-id="e48c1-121">Service management at a glance</span></span>

|<span data-ttu-id="e48c1-122">Svarīgi uzdevumi</span><span class="sxs-lookup"><span data-stu-id="e48c1-122">Important tasks</span></span>           | <span data-ttu-id="e48c1-123">Primārās lapas</span><span class="sxs-lookup"><span data-stu-id="e48c1-123">Primary pages</span></span>                         |<span data-ttu-id="e48c1-124">Populāri pārskati</span><span class="sxs-lookup"><span data-stu-id="e48c1-124">Popular reports</span></span>              |
|--------------------------|---------------------------------------|-----------------------------|
|<span data-ttu-id="e48c1-125">Pakalpojumu līgumu izpilde</span><span class="sxs-lookup"><span data-stu-id="e48c1-125">Fulfill service agreements</span></span>|<span data-ttu-id="e48c1-126">Pakalpojumu līgumi</span><span class="sxs-lookup"><span data-stu-id="e48c1-126">Service agreements</span></span>                     |<span data-ttu-id="e48c1-127">Pakalpojumu pasūtījumu uzcenojums</span><span class="sxs-lookup"><span data-stu-id="e48c1-127">Service order margin</span></span>         |
|<span data-ttu-id="e48c1-128">Klientu pieprasījumu regulēšana</span><span class="sxs-lookup"><span data-stu-id="e48c1-128">Handle customer inquiries</span></span> |<span data-ttu-id="e48c1-129">Pakalpojumu pasūtījumi</span><span class="sxs-lookup"><span data-stu-id="e48c1-129">Service orders</span></span>                         |<span data-ttu-id="e48c1-130">Darba apraksts</span><span class="sxs-lookup"><span data-stu-id="e48c1-130">Work description</span></span>             |
|                          |<span data-ttu-id="e48c1-131">Dispečera pults</span><span class="sxs-lookup"><span data-stu-id="e48c1-131">Dispatch board</span></span>                         |<span data-ttu-id="e48c1-132">Darbība - Abonements</span><span class="sxs-lookup"><span data-stu-id="e48c1-132">Transaction - subscription</span></span>   |
|                          |                                       |<span data-ttu-id="e48c1-133">Abonementu apmaksas darījumi</span><span class="sxs-lookup"><span data-stu-id="e48c1-133">Subscription fee transactions</span></span>|


## <a name="integration-of-service-management"></a><span data-ttu-id="e48c1-134">Pakalpojumu pārvaldības integrācija</span><span class="sxs-lookup"><span data-stu-id="e48c1-134">Integration of Service management</span></span>

<span data-ttu-id="e48c1-135">Pakalpojumu pārvaldību var integrēt ar šādiem moduļiem:</span><span class="sxs-lookup"><span data-stu-id="e48c1-135">Service management can be integrated with the following modules:</span></span>

  - [<span data-ttu-id="e48c1-136">Pārdošana un mārketings</span><span class="sxs-lookup"><span data-stu-id="e48c1-136">Sales and marketing</span></span>](../sales-marketing/overview-sales-marketing.md)
  - [<span data-ttu-id="e48c1-137">Personāla vadība</span><span class="sxs-lookup"><span data-stu-id="e48c1-137">Human resources</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/index)

  

