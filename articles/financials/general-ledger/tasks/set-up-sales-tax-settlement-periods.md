--- 
title: "Iestatīt PVN apmaksas periodus"
description: "PVN nomaksas periodi satur informāciju par periodu intervāliem, par kuriem jāsniedz atskaites un par kuriem tie jānomaksā."
author: twheeloc
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxPeriod
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 0511d2c950139f9ac101af6e555f2c4523200aa5
ms.contentlocale: lv-lv
ms.lasthandoff: 09/11/2018

---
# <a name="set-up-sales-tax-settlement-periods"></a><span data-ttu-id="c3e4c-103">Iestatīt PVN apmaksas periodus</span><span class="sxs-lookup"><span data-stu-id="c3e4c-103">Set up sales tax settlement periods</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c3e4c-104">PVN nomaksas periodi satur informāciju par periodu intervāliem, par kuriem jāsniedz atskaites un par kuriem tie jānomaksā.</span><span class="sxs-lookup"><span data-stu-id="c3e4c-104">Sales tax settlement periods contain information about the period intervals for which sales tax needs to be reported and paid.</span></span> <span data-ttu-id="c3e4c-105">Nomaksas procesu iespējams palaist maksājumu periodam, noteiktam datumu intervālam.</span><span class="sxs-lookup"><span data-stu-id="c3e4c-105">A settlement process can be run for a settlement period for a specific date interval.</span></span> <span data-ttu-id="c3e4c-106">Tiks segti visi nodokļu kodi, kas saistīti ar apmaksas periodu.</span><span class="sxs-lookup"><span data-stu-id="c3e4c-106">All tax codes associated with the settlement period will be settled.</span></span> <span data-ttu-id="c3e4c-107">Atkarībā no saistītās PVN iestādes iestatījumiem, nodokļu parāds tiek grāmatots vai nu kreditoram vai Virsgrāmatas kontā.</span><span class="sxs-lookup"><span data-stu-id="c3e4c-107">Depending on the set up of the related Sales tax authority, the tax liability is posted either to a vendor or a General ledger account.</span></span>



<span data-ttu-id="c3e4c-108">Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF.</span><span class="sxs-lookup"><span data-stu-id="c3e4c-108">This task uses the USMF demo company.</span></span>



1. <span data-ttu-id="c3e4c-109">Pārejiet uz sadaļu Nodokļi > Netiešie nodokļi > PVN > PVN apmaksas periodi.</span><span class="sxs-lookup"><span data-stu-id="c3e4c-109">Go to Tax > Indirect taxes > Sales tax > Sales tax settlement periods.</span></span>
2. <span data-ttu-id="c3e4c-110">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="c3e4c-110">Click New.</span></span>
3. <span data-ttu-id="c3e4c-111">Ierakstiet vērtību laukā Apmaksas periods.</span><span class="sxs-lookup"><span data-stu-id="c3e4c-111">In the Settlement period field, type a value.</span></span>
4. <span data-ttu-id="c3e4c-112">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="c3e4c-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="c3e4c-113">Laukā Iestāde atlasiet PVN iestādi, kas saņem apmaksas perioda pārskatus un maksājumus.</span><span class="sxs-lookup"><span data-stu-id="c3e4c-113">In the Authority field, select the sales tax authority that receives the reports and the payments that are created for the settlement period.</span></span>
6. <span data-ttu-id="c3e4c-114">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="c3e4c-114">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="c3e4c-115">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="c3e4c-115">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="c3e4c-116">Laukā Apmaksas nosacījumi noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="c3e4c-116">In the Terms of payment field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="c3e4c-117">Saistītā nodokļu iestāde var tikt iestatīta kā kreditors un PVN apmaksai tiek izveidots atvērts kreditora rēķins.</span><span class="sxs-lookup"><span data-stu-id="c3e4c-117">The related Sales tax authority can be set up as a vendor and the Sales tax settlement will create an open vendor invoice.</span></span> <span data-ttu-id="c3e4c-118">Apmaksas nosacījumi norāda atvērta kreditora rēķina apmaksas datumu.</span><span class="sxs-lookup"><span data-stu-id="c3e4c-118">The Terms of payment defines the Due date for the open vendor invoice.</span></span>  
9. <span data-ttu-id="c3e4c-119">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="c3e4c-119">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="c3e4c-120">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="c3e4c-120">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="c3e4c-121">Atlasiet apmaksas perioda intervālu veidu.</span><span class="sxs-lookup"><span data-stu-id="c3e4c-121">Select a type for the settlement period intervals.</span></span>
12. <span data-ttu-id="c3e4c-122">Ievadiet perioda intervāla vienību skaitu periodā.</span><span class="sxs-lookup"><span data-stu-id="c3e4c-122">Enter the number of Period interval units per period.</span></span> <span data-ttu-id="c3e4c-123">Piemēram, ceturksnī ir 3 mēneši.</span><span class="sxs-lookup"><span data-stu-id="c3e4c-123">For example, a quarter has 3 months.</span></span>
13. <span data-ttu-id="c3e4c-124">Atlasiet vai notīriet izvēles rūtiņu Izmantot pakešveida apstrādi PVN apmaksai.</span><span class="sxs-lookup"><span data-stu-id="c3e4c-124">Select or clear the Use batch processing for sales tax settlement check box.</span></span>
    * <span data-ttu-id="c3e4c-125">Apmaksas process apmaksas periodam var tikt apstrādāts fonā kā pakešuzdevums.</span><span class="sxs-lookup"><span data-stu-id="c3e4c-125">The settlement process for the settlement period can be processed as batch job in the background.</span></span> <span data-ttu-id="c3e4c-126">Tas ir ieteicams gadījumos, kad vienā laika periodā ir liels skaits nodokļu transakciju.</span><span class="sxs-lookup"><span data-stu-id="c3e4c-126">This is recommended for a large number of tax transactions within a period interval.</span></span>  
14. <span data-ttu-id="c3e4c-127">Izvērsiet cilni Perioda intervāli.</span><span class="sxs-lookup"><span data-stu-id="c3e4c-127">Expand the Period intervals tab.</span></span>
15. <span data-ttu-id="c3e4c-128">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="c3e4c-128">Click Add.</span></span>
16. <span data-ttu-id="c3e4c-129">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="c3e4c-129">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="c3e4c-130">Ievadiet datumu laukā No datuma.</span><span class="sxs-lookup"><span data-stu-id="c3e4c-130">In the From date field, enter a date.</span></span>
18. <span data-ttu-id="c3e4c-131">Laukā Līdz datumam ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="c3e4c-131">In the To date field, enter a date.</span></span>
19. <span data-ttu-id="c3e4c-132">Noklikšķiniet uz Jauns perioda intervāls.</span><span class="sxs-lookup"><span data-stu-id="c3e4c-132">Click New period interval.</span></span>
    * <span data-ttu-id="c3e4c-133">Kad pirmā perioda intervāls ir ievadīts, jaunus periodus var izveidot automātiski.</span><span class="sxs-lookup"><span data-stu-id="c3e4c-133">Once the first period interval has been entered, new periods can be created automatically.</span></span> <span data-ttu-id="c3e4c-134">Pēc nepieciešamības varat atgriezties un pievienot jaunus periodu intervālus.</span><span class="sxs-lookup"><span data-stu-id="c3e4c-134">You can come back and add new period intervals as required.</span></span>  
20. <span data-ttu-id="c3e4c-135">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="c3e4c-135">Close the page.</span></span>


