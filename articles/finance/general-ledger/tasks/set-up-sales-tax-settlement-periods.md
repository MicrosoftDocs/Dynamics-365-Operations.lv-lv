---
title: PVN apmaksas periodu iestatīšana
description: Šajā tēmā paskaidrots, kā iestatīt PVN apmaksas periodus programmā Dynamics 365 Finance.
author: twheeloc
manager: AnnBe
ms.date: 08/05/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxPeriod
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e5068c121e921c1586dc6ae003c0021bf41d2254
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445595"
---
# <a name="set-up-sales-tax-settlement-periods"></a><span data-ttu-id="b128d-103">PVN apmaksas periodu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="b128d-103">Set up sales tax settlement periods</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b128d-104">Šajā tēmā paskaidrots, kā iestatīt PVN apmaksas periodus.</span><span class="sxs-lookup"><span data-stu-id="b128d-104">This topic explains how to set up sales tax settlement periods.</span></span> <span data-ttu-id="b128d-105">PVN nomaksas periodi satur informāciju par periodu intervāliem, par kuriem jāsniedz atskaites un par kuriem tie jānomaksā.</span><span class="sxs-lookup"><span data-stu-id="b128d-105">Sales tax settlement periods contain information about the period intervals for which sales tax needs to be reported and paid.</span></span> <span data-ttu-id="b128d-106">Nomaksas procesu iespējams palaist maksājumu periodam, noteiktam datumu intervālam.</span><span class="sxs-lookup"><span data-stu-id="b128d-106">A settlement process can be run for a settlement period for a specific date interval.</span></span> <span data-ttu-id="b128d-107">Tiks segti visi nodokļu kodi, kas saistīti ar apmaksas periodu.</span><span class="sxs-lookup"><span data-stu-id="b128d-107">All tax codes associated with the settlement period will be settled.</span></span> <span data-ttu-id="b128d-108">Atkarībā no saistītās PVN iestādes iestatījumiem, nodokļu parāds tiek grāmatots vai nu kreditoram vai Virsgrāmatas kontā.</span><span class="sxs-lookup"><span data-stu-id="b128d-108">Depending on the set up of the related Sales tax authority, the tax liability is posted either to a vendor or a General ledger account.</span></span>

<span data-ttu-id="b128d-109">Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF.</span><span class="sxs-lookup"><span data-stu-id="b128d-109">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="b128d-110">Navigācijas rūtī atveriet **Moduļi > Nodokļi > Netiešie nodokļi > PVN > PVN apmaksas periodi**.</span><span class="sxs-lookup"><span data-stu-id="b128d-110">In the navigation pane, go to **Modules > Tax > Indirect taxes > Sales tax > Sales tax settlement periods**.</span></span>
2. <span data-ttu-id="b128d-111">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="b128d-111">Select **New**.</span></span>
3. <span data-ttu-id="b128d-112">Ierakstiet vērtību laukā **Apmaksas periods**.</span><span class="sxs-lookup"><span data-stu-id="b128d-112">In the **Settlement period** field, type a value.</span></span>
4. <span data-ttu-id="b128d-113">Laukā **Apraksts** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="b128d-113">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="b128d-114">Laukā **Iestāde** atlasiet PVN iestādi, kas saņem apmaksas perioda pārskatus un maksājumus.</span><span class="sxs-lookup"><span data-stu-id="b128d-114">In the **Authority** field, select the sales tax authority that receives the reports and the payments that are created for the settlement period.</span></span>
6. <span data-ttu-id="b128d-115">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="b128d-115">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="b128d-116">Lauka **Maksājuma nosacījumi** nolaižamajā izvēlnē atlasiet vēlamo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="b128d-116">In the **Terms of payment** field, select the desired record in the drop-down menu.</span></span> <span data-ttu-id="b128d-117">Saistītā nodokļu iestāde var tikt iestatīta kā kreditors un PVN apmaksai tiek izveidots atvērts kreditora rēķins.</span><span class="sxs-lookup"><span data-stu-id="b128d-117">The related Sales tax authority can be set up as a vendor and the Sales tax settlement will create an open vendor invoice.</span></span> <span data-ttu-id="b128d-118">Apmaksas nosacījumi norāda atvērta kreditora rēķina apmaksas datumu.</span><span class="sxs-lookup"><span data-stu-id="b128d-118">The Terms of payment defines the Due date for the open vendor invoice.</span></span>  
8. <span data-ttu-id="b128d-119">Atlasiet apmaksas perioda intervālu veidu.</span><span class="sxs-lookup"><span data-stu-id="b128d-119">Select a type for the settlement period intervals.</span></span>
9. <span data-ttu-id="b128d-120">Ievadiet perioda intervāla vienību skaitu periodā.</span><span class="sxs-lookup"><span data-stu-id="b128d-120">Enter the number of Period interval units per period.</span></span> <span data-ttu-id="b128d-121">Piemēram, ceturksnī ir 3 mēneši.</span><span class="sxs-lookup"><span data-stu-id="b128d-121">For example, a quarter has 3 months.</span></span>
10. <span data-ttu-id="b128d-122">Atlasiet vai notīriet izvēles rūtiņu **Izmantot pakešveida apstrādi PVN apmaksai**.</span><span class="sxs-lookup"><span data-stu-id="b128d-122">Select or clear the **Use batch processing for sales tax settlement** check box.</span></span> <span data-ttu-id="b128d-123">Apmaksas process apmaksas periodam var tikt apstrādāts fonā kā pakešuzdevums.</span><span class="sxs-lookup"><span data-stu-id="b128d-123">The settlement process for the settlement period can be processed as batch job in the background.</span></span> <span data-ttu-id="b128d-124">Tas ir ieteicams gadījumos, kad vienā laika periodā ir liels skaits nodokļu transakciju.</span><span class="sxs-lookup"><span data-stu-id="b128d-124">This is recommended for a large number of tax transactions within a period interval.</span></span>  
    > [!NOTE]
    > <span data-ttu-id="b128d-125">Pašlaik tas netiek atbalstīts Spānijā, Japānā un Nīderlandē.</span><span class="sxs-lookup"><span data-stu-id="b128d-125">Currently this is not supported in Spain, Japan, and the Netherlands.</span></span>
11. <span data-ttu-id="b128d-126">Atzīmējiet izvēles rūtiņu **Novērst korespondējošu nodokļu transakciju ģenerēšanu** vai noņemiet tās atzīmi.</span><span class="sxs-lookup"><span data-stu-id="b128d-126">Select or clear the **Prevent generating offset tax transactions** check box.</span></span> <span data-ttu-id="b128d-127">Pēc noklusējuma sistēma ģenerē korespondējošās nodokļu transakcijas, kamēr notiek segšanas process, un tas var radīt veiktspējas problēmas, ja kādā periodā ir liels skaits nodokļu transakciju.</span><span class="sxs-lookup"><span data-stu-id="b128d-127">By default, the system generates offset tax transactions during the settlement process, which cause can performance issue if there are a large number of tax transactions within a period interval.</span></span> <span data-ttu-id="b128d-128">Atzīmējiet šo izvēles rūtiņu, lai novērstu korespondējošu nodokļu transakciju ģenerēšanu.</span><span class="sxs-lookup"><span data-stu-id="b128d-128">Select this check box to prevent generating offset tax transactions.</span></span>
12. <span data-ttu-id="b128d-129">Izvērsiet cilni **Perioda intervāli**.</span><span class="sxs-lookup"><span data-stu-id="b128d-129">Expand the **Period intervals** tab.</span></span>
13. <span data-ttu-id="b128d-130">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="b128d-130">Select **Add**.</span></span>
14. <span data-ttu-id="b128d-131">Jaunās rindas laukā **No datuma** ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="b128d-131">In the **From date** field in the new row, enter a date.</span></span>
15. <span data-ttu-id="b128d-132">Ievadiet datumu laukā **Līdz datumam**.</span><span class="sxs-lookup"><span data-stu-id="b128d-132">In the **To date** field, enter a date.</span></span>
16. <span data-ttu-id="b128d-133">Atlasiet **Jauns perioda intervāls**.</span><span class="sxs-lookup"><span data-stu-id="b128d-133">Select **New period interval**.</span></span> <span data-ttu-id="b128d-134">Kad pirmā perioda intervāls ir ievadīts, jaunus periodus var izveidot automātiski.</span><span class="sxs-lookup"><span data-stu-id="b128d-134">Once the first period interval has been entered, new periods can be created automatically.</span></span> <span data-ttu-id="b128d-135">Pēc nepieciešamības varat atgriezties un pievienot jaunus periodu intervālus.</span><span class="sxs-lookup"><span data-stu-id="b128d-135">You can come back and add new period intervals as required.</span></span>  
17. <span data-ttu-id="b128d-136">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="b128d-136">Close the page.</span></span>

