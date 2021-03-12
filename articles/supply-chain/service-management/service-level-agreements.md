---
title: Pakalpojuma līmeņa līgumu pārskats
description: Līgumā par pakalpojumu līmeni (Service Level Agreement — SLA) klients piekrīt minimālajam atbildes laikam, pamatojoties uz laiku, kad pakalpojumu uzņēmums reģistrē problēmu un kad šī problēma ir atrisināta.
author: ShylaThompson
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServicelevelagreement
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1f2cfa8b72e515b6237914499af626ff8262429d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974364"
---
# <a name="service-level-agreements-overview"></a><span data-ttu-id="9da63-103">Pakalpojuma līmeņa līgumu pārskats</span><span class="sxs-lookup"><span data-stu-id="9da63-103">Service level agreements overview</span></span>       

[!include [banner](../includes/banner.md)]


<span data-ttu-id="9da63-104">Līgums par pakalpojumu līmeni (Service Level Agreement — SLA) ir līgums starp pakalpojumu uzņēmumu un pakalpojumu klientu.</span><span class="sxs-lookup"><span data-stu-id="9da63-104">A service level agreement (SLA) is an agreement between a service company and a service customer.</span></span> <span data-ttu-id="9da63-105">Ar SLA klients piekrīt minimālajam atbildes laikam, pamatojoties uz laiku, kad pakalpojumu uzņēmums reģistrē problēmu un kad šī problēma ir atrisināta.</span><span class="sxs-lookup"><span data-stu-id="9da63-105">In a SLA, the customer agrees to a minimum response time based on when the service company records the issue and when the issue is resolved.</span></span>

<span data-ttu-id="9da63-106">SLA regulē klientiem piedāvātā pakalpojuma standarta līmeni, kā arī skaidri norāda pakalpojumu uzņēmumam, kad ir jāizpilda pakalpojumu darbs.</span><span class="sxs-lookup"><span data-stu-id="9da63-106">A SLA enforces a standard level of service that is offered to customers, and also makes it transparent to a service company when a service job should be completed.</span></span>

<span data-ttu-id="9da63-107">Var izveidot vairākus SLA, lai sniegtu pakalpojumu klientiem dažādus pakalpojuma līmeņus.</span><span class="sxs-lookup"><span data-stu-id="9da63-107">Any number of SLAs can be created to offer service customers different levels of service.</span></span>

## <a name="create-a-service-level-agreement"></a><span data-ttu-id="9da63-108">Līguma par pakalpojumu līmeni izveidošana</span><span class="sxs-lookup"><span data-stu-id="9da63-108">Create a service level agreement</span></span>

1.  <span data-ttu-id="9da63-109">Noklikšķiniet uz **Pakalpojumu pārvaldība** \> **Iestatīšana** \> **Pakalpojumu līgumi** \> **Līgumi par pakalpojumu līmeni**.</span><span class="sxs-lookup"><span data-stu-id="9da63-109">Click **Service management** \> **Setup** \> **Service agreements** \> **Service level agreements**.</span></span>

2.  <span data-ttu-id="9da63-110">Laukā **Līgums par pakalpojumu līmeni** ierakstiet nosaukumu līgumam par pakalpojumu līmeni.</span><span class="sxs-lookup"><span data-stu-id="9da63-110">Type a name for the service level agreement in the **Service level agreement** field.</span></span>

3.  <span data-ttu-id="9da63-111">Ierakstiet laiku, kādu vēlaties atļaut šim līgumam par pakalpojumu līmeni piesaistīto pakalpojumu izsaukumu veikšanai.</span><span class="sxs-lookup"><span data-stu-id="9da63-111">Type the time that you want to allow for completion of service calls that are attached to the service level agreement.</span></span> <span data-ttu-id="9da63-112">Pēc tam atlasiet kādu kalendāru, ja šo līgumu par pakalpojumu līmeni vēlaties balstīt uz noteiktu kalendāru.</span><span class="sxs-lookup"><span data-stu-id="9da63-112">Then select a calendar if you want to base the service level agreement on a specific calendar.</span></span>

## <a name="apply-a-service-level-agreement"></a><span data-ttu-id="9da63-113">Pakalpojumu līmeņa līguma piešķiršana</span><span class="sxs-lookup"><span data-stu-id="9da63-113">Apply a service level agreement</span></span>

<span data-ttu-id="9da63-114">SLA tiek piešķirts tieši pakalpojumu līgumam.</span><span class="sxs-lookup"><span data-stu-id="9da63-114">The SLA is applied directly to a service agreement.</span></span>

<span data-ttu-id="9da63-115">Pakalpojumu pasūtījumi, ko izveidojat manuāli un ko pievienojat kādam pakalpojumu līgumam, kuram ir SLA, tiek mērīti attiecībā pret šo SLA.</span><span class="sxs-lookup"><span data-stu-id="9da63-115">Service orders that you create manually and attach to a service agreement that has an SLA are measured against that SLA.</span></span>

<span data-ttu-id="9da63-116">Pakalpojumu pasūtījumi, ko izveidojat automātiski, netiek pievienoti SLA.</span><span class="sxs-lookup"><span data-stu-id="9da63-116">Service orders that you create automatically are not attached to an SLA.</span></span>

## <a name="apply-the-service-level-agreement-to-the-service-agreement"></a><span data-ttu-id="9da63-117">Līguma par pakalpojumu līmeni lietošana pakalpojumu līgumam</span><span class="sxs-lookup"><span data-stu-id="9da63-117">Apply the service level agreement to the service agreement</span></span>

1.  <span data-ttu-id="9da63-118">Noklikšķiniet uz **Pakalpojumu pārvaldība** \> **Vispārīgi** \> **Pakalpojumu līgumi** \> **Pakalpojumu līgumi**.</span><span class="sxs-lookup"><span data-stu-id="9da63-118">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span> <span data-ttu-id="9da63-119">Atlasiet pakalpojumu līgumu, kuram vēlaties lietot šo SLA, un pēc tam noklikšķiniet uz **Rediģēt** sadaļā **Darbību rūts**.</span><span class="sxs-lookup"><span data-stu-id="9da63-119">Select the service agreement that you want to apply the SLA to, and then click **Edit** on the **Action Pane**.</span></span>

2.  <span data-ttu-id="9da63-120">Laukā **Līgums par pakalpojumu līmeni** atlasiet SLA, kuru vēlaties piešķirt.</span><span class="sxs-lookup"><span data-stu-id="9da63-120">In the **Service level agreement** field, select the SLA that you want to assign.</span></span>

## <a name="apply-the-service-level-agreement-to-the-service-agreement-group"></a><span data-ttu-id="9da63-121">Līguma par pakalpojumu līmeni piešķiršana pakalpojumu līgumu grupai</span><span class="sxs-lookup"><span data-stu-id="9da63-121">Apply the service level agreement to the service agreement group</span></span>

1.  <span data-ttu-id="9da63-122">Noklikšķiniet uz **Pakalpojumu pārvaldība** \> **Iestatījumi** \> **Pakalpojumu līgumi** \> **Pakalpojumu līgumu grupas**.</span><span class="sxs-lookup"><span data-stu-id="9da63-122">Click **Service management** \> **Setup** \> **Service agreements** \> **Service agreement groups**.</span></span>

2.  <span data-ttu-id="9da63-123">Laukā **Līgums par pakalpojumu līmeni** atlasiet SLA, kuru vēlaties piešķirt.</span><span class="sxs-lookup"><span data-stu-id="9da63-123">In the **Service level agreement** field, select the SLA that you want to assign.</span></span>

## <a name="track-time-on-a-service-order-against-an-sla"></a><span data-ttu-id="9da63-124">Laika izsekošana pakalpojumu pasūtījumā pret SLA</span><span class="sxs-lookup"><span data-stu-id="9da63-124">Track time on a service order against an SLA</span></span>

<span data-ttu-id="9da63-125">Kad veidojat jaunu pakalpojumu pasūtījumu kādam pakalpojumu līgumam, kuram ir piešķirts kāds SLA, tiek uzsākts pakalpojuma piegādes laika intervāls un sistēma sāk izsekot piegādes laiku.</span><span class="sxs-lookup"><span data-stu-id="9da63-125">When you create a new service order for a service agreement that an SLA is assigned to, the time interval for the delivery of the service is initiated, and the system starts to track the delivery time.</span></span> <span data-ttu-id="9da63-126">Turklāt varat iestatīt tālāk norādītās opcijas.</span><span class="sxs-lookup"><span data-stu-id="9da63-126">Additionally, you can set the following options:</span></span>

  - <span data-ttu-id="9da63-127">Varat sākt un apturēt laika ierakstīšanu šim pakalpojumu pasūtījumam, lai reģistrētu kopējo pakalpojumu pasūtījumiem veltīto laiku.</span><span class="sxs-lookup"><span data-stu-id="9da63-127">You can start and stop time recording on the service order to register the total amount of time that is spent on service orders.</span></span>

  - <span data-ttu-id="9da63-128">Varat uzraudzīt atbilstību laika intervālam, kas ir iestatītas šajā līgumā par pakalpojumu līmeni.</span><span class="sxs-lookup"><span data-stu-id="9da63-128">You can monitor compliance with the time interval that is set in the service level agreement.</span></span>

  - <span data-ttu-id="9da63-129">Varat noteikt iemeslu kodus, kas ir jāiestata, ja tiek pārsniegts līgumā par pakalpojumu līmeni noteiktais laika periods.</span><span class="sxs-lookup"><span data-stu-id="9da63-129">You can define reason codes that must be set if the time interval of the service level agreement is exceeded.</span></span>

## <a name="see-also"></a><span data-ttu-id="9da63-130">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="9da63-130">See also</span></span>

[<span data-ttu-id="9da63-131">Atbilstības skatīšana attiecībā uz līgumiem par pakalpojumu līmeni</span><span class="sxs-lookup"><span data-stu-id="9da63-131">View compliance with service level agreements</span></span>](view-compliance-with-service-level-agreements.md)

  


