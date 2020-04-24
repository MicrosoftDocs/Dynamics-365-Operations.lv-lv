---
title: Izstrādes un veidošanas pakalpojumu līgumu pārskats
description: Izmantojot pakalpojumu līgumus, varat definēt resursus, ko izmantot tipiskā pakalpojumu vizītē, un veidu, kā šie resursi tiek iekļauti klienta rēķinos.
author: ShylaThompson
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 41081525fb9ff7bfa3adb87ba038d899f58e436a
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216164"
---
# <a name="develop-and-establish-service-agreements-overview"></a><span data-ttu-id="6d4eb-103">Izstrādes un veidošanas pakalpojumu līgumu pārskats</span><span class="sxs-lookup"><span data-stu-id="6d4eb-103">Develop and establish service agreements overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6d4eb-104">Izmantojot pakalpojumu līgumus, varat definēt resursus, ko izmantot tipiskā pakalpojumu vizītē, un veidu, kā šie resursi tiek iekļauti klienta rēķinos.</span><span class="sxs-lookup"><span data-stu-id="6d4eb-104">Service agreements let you define the resources that are used in a typical service visit and how those resources are invoiced to the customer.</span></span>

<span data-ttu-id="6d4eb-105">Katrs pakalpojumu līgums ir piesaistīts projektam, tādējādi darbības tiek iegrāmatotas un par tām izrakstīti rēķini.</span><span class="sxs-lookup"><span data-stu-id="6d4eb-105">Every service agreement is attached to a project through which transactions are posted and invoiced.</span></span> <span data-ttu-id="6d4eb-106">Tomēr varat pakalpojuma pasūtījumu rēķinos iekļaut arī tieši caur projektu, vispirms nesavienojot pakalpojuma pasūtījumu ar pakalpojumu līgumu.</span><span class="sxs-lookup"><span data-stu-id="6d4eb-106">However, you can also invoice service order transactions directly through the project without first having to connect the service order to a service agreement.</span></span> <span data-ttu-id="6d4eb-107">Varat izlemt tā rīkoties, ja pakalpojuma pasūtījums ir tikai vienreizēja pakalpojumu vizīte un nepieciešamība apstrādāt šīs pakalpojumu darbības ātri atsver nepieciešamību uzturēt detalizētu pakalpojumu līguma informāciju par attiecīgo klientu laika periodā.</span><span class="sxs-lookup"><span data-stu-id="6d4eb-107">You might decide to do this if the service order is for a one-time-only service visit and the need for processing the service transactions quickly outweighs the need for maintaining detailed service-agreement information about the customer over a period of time.</span></span>

## <a name="service-agreement"></a><span data-ttu-id="6d4eb-108">Pakalpojumu līgums</span><span class="sxs-lookup"><span data-stu-id="6d4eb-108">Service agreement</span></span>

<span data-ttu-id="6d4eb-109">Katrā pakalpojumu līgumā jānorāda projekts, pakalpojumu līguma ID un pakalpojumu līgumu grupa.</span><span class="sxs-lookup"><span data-stu-id="6d4eb-109">In each service agreement, you must specify a project, a service-agreement ID, and a service-agreement group.</span></span> <span data-ttu-id="6d4eb-110">Pakalpojumu līgumu grupu var izmantot, lai šķirotu un sakārtotu pakalpojumu līgumus.</span><span class="sxs-lookup"><span data-stu-id="6d4eb-110">The service-agreement group can be used to sort and organize service agreements.</span></span>

<span data-ttu-id="6d4eb-111">Pakalpojumu līguma galvene satur iestatījumus, kas attiecas uz visām pievienotajām līguma rindām:</span><span class="sxs-lookup"><span data-stu-id="6d4eb-111">A service agreement header contains settings that apply to all attached agreement lines:</span></span>

-  <span data-ttu-id="6d4eb-112">Vai pakalpojumu līgums ir aizturēts.</span><span class="sxs-lookup"><span data-stu-id="6d4eb-112">Whether the service agreement is suspended.</span></span> <span data-ttu-id="6d4eb-113">Ja pakalpojumu līgums ir aizturēts, no šī pakalpojumu līguma nevar ģenerēt pakalpojuma pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="6d4eb-113">If the service agreement is suspended, you cannot generate service orders from the service agreement.</span></span>
-  <span data-ttu-id="6d4eb-114">Pakalpojumu līguma ilgums.</span><span class="sxs-lookup"><span data-stu-id="6d4eb-114">The duration of the service agreement.</span></span>
-  <span data-ttu-id="6d4eb-115">Veids, kādā pakalpojuma pasūtījuma rindas jākombinē pakalpojuma pasūtījumos.</span><span class="sxs-lookup"><span data-stu-id="6d4eb-115">How service-order lines are to be combined into service orders.</span></span>
-  <span data-ttu-id="6d4eb-116">Vai pakalpojumu līgums ir veidne.</span><span class="sxs-lookup"><span data-stu-id="6d4eb-116">Whether the service agreement is a template.</span></span>

<span data-ttu-id="6d4eb-117">Pakalpojumu līguma galvenē iestatāt arī visus pakalpojumu objektus un pakalpojumu uzdevumus, ko var izmantot ar šo pakalpojumu līgumu, ievadot konkrētos pakalpojumu uzdevumus vai pakalpojumu objektus, kas tiks pievienoti dažādām līguma rindām.</span><span class="sxs-lookup"><span data-stu-id="6d4eb-117">In the service-agreement header, you also set up all the service objects and service tasks that can be used with the service agreement by entering the specific service tasks or service objects that are to be attached to the various lines of the agreement.</span></span>

<span data-ttu-id="6d4eb-118">No pakalpojumu līguma galvenes varat arī pašreizējā pakalpojumu līgumā kopēt pakalpojumu līguma rindas vai pakalpojuma veidnes rindas.</span><span class="sxs-lookup"><span data-stu-id="6d4eb-118">From the service-agreement header, you can also copy service-agreement lines or service-template lines into the current service agreement.</span></span>

<span data-ttu-id="6d4eb-119">Jūs varat aizturēt pakalpojumu līgumus un apturēt individuālas pakalpojumu līguma rindas.</span><span class="sxs-lookup"><span data-stu-id="6d4eb-119">You can suspend service agreements and stop individual service agreement lines.</span></span>

<span data-ttu-id="6d4eb-120">Ja atzīmējat izvēles rūtiņu **Aizturēts** pakalpojumu līguma rindā, jūs nevarat:</span><span class="sxs-lookup"><span data-stu-id="6d4eb-120">If you select the **Suspended** check box on a service agreement, you cannot:</span></span>

-    <span data-ttu-id="6d4eb-121">manuāli vai automātiski izveidot pakalpojuma pasūtījumus no pakalpojumu līguma rindas.</span><span class="sxs-lookup"><span data-stu-id="6d4eb-121">Create service orders automatically or manually from the service agreement.</span></span>

<span data-ttu-id="6d4eb-122">Ja atzīmējat izvēles rūtiņu **Apturēts** pakalpojumu līguma rindā, jūs nevarat:</span><span class="sxs-lookup"><span data-stu-id="6d4eb-122">If you select the **Stopped** check box on a service agreement line, you cannot:</span></span>

-    <span data-ttu-id="6d4eb-123">manuāli vai automātiski izveidot pakalpojuma pasūtījumus no pakalpojumu līguma;</span><span class="sxs-lookup"><span data-stu-id="6d4eb-123">Create service orders automatically or manually from the service agreement line.</span></span>
-    <span data-ttu-id="6d4eb-124">Kopējiet pakalpojumu līguma rindu citā pakalpojumu līgumā vai pakalpojuma pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="6d4eb-124">Copy the service agreement line into another service agreement or service order.</span></span>


> [!NOTE]
> <span data-ttu-id="6d4eb-125">Ja pakalpojumu līgums ir aizturēts, visas pievienotās rindas arī ir apturētas neatkarīgi no to individuālā statusa.</span><span class="sxs-lookup"><span data-stu-id="6d4eb-125">If a service agreement is suspended, all the attached lines are stopped, regardless of their individual status.</span></span>

## <a name="service-agreement-lines"></a><span data-ttu-id="6d4eb-126">Pakalpojumu līguma rindas</span><span class="sxs-lookup"><span data-stu-id="6d4eb-126">Service-agreement lines</span></span>

<span data-ttu-id="6d4eb-127">Katrā pakalpojumu līguma rindā ir detalizēti aprakstīts piedāvātā pakalpojumu darba saturs.</span><span class="sxs-lookup"><span data-stu-id="6d4eb-127">Each service-agreement line describes in detail the content of the proposed service work.</span></span> <span data-ttu-id="6d4eb-128">Šīs rindas satur šādus iestatījumus:</span><span class="sxs-lookup"><span data-stu-id="6d4eb-128">The lines contain the following settings:</span></span>

-  <span data-ttu-id="6d4eb-129">Darbības tips un darbības tipa apraksts.</span><span class="sxs-lookup"><span data-stu-id="6d4eb-129">The transaction type and the description of the transaction type.</span></span>
-  <span data-ttu-id="6d4eb-130">Darbinieks, kas veic šo pakalpojumu darbu.</span><span class="sxs-lookup"><span data-stu-id="6d4eb-130">The employee who performs the service work.</span></span>
-  <span data-ttu-id="6d4eb-131">Objekti, kam saskaņā ar šo pakalpojumu līgumu pakalpojums jāveic.</span><span class="sxs-lookup"><span data-stu-id="6d4eb-131">The objects on which service must be performed for the service agreement.</span></span>
-  <span data-ttu-id="6d4eb-132">Tiek reģistrēts biežums, kādā tiek veikts šis darbs, un saistītās krājuma, izmaksu un apmaksas darbības.</span><span class="sxs-lookup"><span data-stu-id="6d4eb-132">The frequency with which work is performed and associated item, expense, and fee transactions are registered.</span></span>
-  <span data-ttu-id="6d4eb-133">Laika logs, kur pakalpojuma pasūtījuma rindas var grupēt pakalpojuma pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="6d4eb-133">The time window within which service-order lines can be grouped into a service order.</span></span>
-  <span data-ttu-id="6d4eb-134">Pakalpojumu uzdevumi, kas tiek izmantoti līguma rindu kopu grupēšanai kopā darba uzdevumos un kopsavilkuma izveidei pakalpojumu tehniķiem un klientiem par to, kādi pakalpojumu uzdevumi tiek sniegti.</span><span class="sxs-lookup"><span data-stu-id="6d4eb-134">The service tasks that are used to group sets of agreement lines together into work tasks and to summarize for service technicians and customers what service task is to be provided.</span></span>
-  <span data-ttu-id="6d4eb-135">Norāda, vai rinda ir apturēta.</span><span class="sxs-lookup"><span data-stu-id="6d4eb-135">Whether a line is stopped.</span></span> <span data-ttu-id="6d4eb-136">Ja rinda ir apturēta, nevarat šai atsevišķajai rindai izveidot pakalpojuma pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="6d4eb-136">If a line is stopped, you cannot create service orders for that individual line.</span></span>
-  <span data-ttu-id="6d4eb-137">Projekta iestatījumi, tādi kā kategorija un rindas statuss.</span><span class="sxs-lookup"><span data-stu-id="6d4eb-137">Project settings, such as the category and the line property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6d4eb-138">Saistītās tēmas</span><span class="sxs-lookup"><span data-stu-id="6d4eb-138">Related topics</span></span>

[<span data-ttu-id="6d4eb-139">Pakalpojumu līgumu izveide</span><span class="sxs-lookup"><span data-stu-id="6d4eb-139">Create service agreements</span></span>](create-service-agreements.md)
