---
title: PVN apmaksas periodu iestatīšana
description: Šajā tēmā paskaidrots, kā iestatīt PVN apmaksas periodus programmā Dynamics 365 Finance.
author: twheeloc
ms.date: 08/05/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxPeriod
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 83587df3963d215fec020150e6b707e431c1b6eb
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944781"
---
# <a name="set-up-sales-tax-settlement-periods"></a><span data-ttu-id="cd1bb-103">PVN apmaksas periodu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="cd1bb-103">Set up sales tax settlement periods</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cd1bb-104">Šajā tēmā paskaidrots, kā iestatīt PVN apmaksas periodus.</span><span class="sxs-lookup"><span data-stu-id="cd1bb-104">This topic explains how to set up sales tax settlement periods.</span></span> <span data-ttu-id="cd1bb-105">PVN nomaksas periodi satur informāciju par periodu intervāliem, par kuriem jāsniedz atskaites un par kuriem tie jānomaksā.</span><span class="sxs-lookup"><span data-stu-id="cd1bb-105">Sales tax settlement periods contain information about the period intervals for which sales tax needs to be reported and paid.</span></span> <span data-ttu-id="cd1bb-106">Nomaksas procesu iespējams palaist maksājumu periodam, noteiktam datumu intervālam.</span><span class="sxs-lookup"><span data-stu-id="cd1bb-106">A settlement process can be run for a settlement period for a specific date interval.</span></span> <span data-ttu-id="cd1bb-107">Tiks segti visi nodokļu kodi, kas saistīti ar apmaksas periodu.</span><span class="sxs-lookup"><span data-stu-id="cd1bb-107">All tax codes associated with the settlement period will be settled.</span></span> <span data-ttu-id="cd1bb-108">Atkarībā no saistītās PVN iestādes iestatījumiem, nodokļu parāds tiek grāmatots vai nu kreditoram vai Virsgrāmatas kontā.</span><span class="sxs-lookup"><span data-stu-id="cd1bb-108">Depending on the set up of the related Sales tax authority, the tax liability is posted either to a vendor or a General ledger account.</span></span>

<span data-ttu-id="cd1bb-109">Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF.</span><span class="sxs-lookup"><span data-stu-id="cd1bb-109">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="cd1bb-110">Navigācijas rūtī atveriet **Moduļi > Nodokļi > Netiešie nodokļi > PVN > PVN apmaksas periodi**.</span><span class="sxs-lookup"><span data-stu-id="cd1bb-110">In the navigation pane, go to **Modules > Tax > Indirect taxes > Sales tax > Sales tax settlement periods**.</span></span>
2. <span data-ttu-id="cd1bb-111">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="cd1bb-111">Select **New**.</span></span>
3. <span data-ttu-id="cd1bb-112">Ierakstiet vērtību laukā **Apmaksas periods**.</span><span class="sxs-lookup"><span data-stu-id="cd1bb-112">In the **Settlement period** field, type a value.</span></span>
4. <span data-ttu-id="cd1bb-113">Laukā **Apraksts** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="cd1bb-113">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="cd1bb-114">Laukā **Iestāde** atlasiet PVN iestādi, kas saņem apmaksas perioda pārskatus un maksājumus.</span><span class="sxs-lookup"><span data-stu-id="cd1bb-114">In the **Authority** field, select the sales tax authority that receives the reports and the payments that are created for the settlement period.</span></span>
6. <span data-ttu-id="cd1bb-115">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="cd1bb-115">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="cd1bb-116">Lauka **Maksājuma nosacījumi** nolaižamajā izvēlnē atlasiet vēlamo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="cd1bb-116">In the **Terms of payment** field, select the desired record in the drop-down menu.</span></span> <span data-ttu-id="cd1bb-117">Saistītā nodokļu iestāde var tikt iestatīta kā kreditors un PVN apmaksai tiek izveidots atvērts kreditora rēķins.</span><span class="sxs-lookup"><span data-stu-id="cd1bb-117">The related Sales tax authority can be set up as a vendor and the Sales tax settlement will create an open vendor invoice.</span></span> <span data-ttu-id="cd1bb-118">Apmaksas nosacījumi norāda atvērta kreditora rēķina apmaksas datumu.</span><span class="sxs-lookup"><span data-stu-id="cd1bb-118">The Terms of payment defines the Due date for the open vendor invoice.</span></span>  
8. <span data-ttu-id="cd1bb-119">Atlasiet apmaksas perioda intervālu veidu.</span><span class="sxs-lookup"><span data-stu-id="cd1bb-119">Select a type for the settlement period intervals.</span></span>
9. <span data-ttu-id="cd1bb-120">Ievadiet perioda intervāla vienību skaitu periodā.</span><span class="sxs-lookup"><span data-stu-id="cd1bb-120">Enter the number of Period interval units per period.</span></span> <span data-ttu-id="cd1bb-121">Piemēram, ceturksnī ir 3 mēneši.</span><span class="sxs-lookup"><span data-stu-id="cd1bb-121">For example, a quarter has 3 months.</span></span>
10. <span data-ttu-id="cd1bb-122">Atlasiet vai notīriet izvēles rūtiņu **Izmantot pakešveida apstrādi PVN apmaksai**.</span><span class="sxs-lookup"><span data-stu-id="cd1bb-122">Select or clear the **Use batch processing for sales tax settlement** check box.</span></span> <span data-ttu-id="cd1bb-123">Apmaksas process apmaksas periodam var tikt apstrādāts fonā kā pakešuzdevums.</span><span class="sxs-lookup"><span data-stu-id="cd1bb-123">The settlement process for the settlement period can be processed as batch job in the background.</span></span> <span data-ttu-id="cd1bb-124">Tas ir ieteicams gadījumos, kad vienā laika periodā ir liels skaits nodokļu transakciju.</span><span class="sxs-lookup"><span data-stu-id="cd1bb-124">This is recommended for a large number of tax transactions within a period interval.</span></span>
11. <span data-ttu-id="cd1bb-125">Atzīmējiet izvēles rūtiņu **Novērst korespondējošu nodokļu transakciju ģenerēšanu** vai noņemiet tās atzīmi.</span><span class="sxs-lookup"><span data-stu-id="cd1bb-125">Select or clear the **Prevent generating offset tax transactions** check box.</span></span> <span data-ttu-id="cd1bb-126">Pēc noklusējuma sistēma ģenerē korespondējošās nodokļu transakcijas, kamēr notiek segšanas process, un tas var radīt veiktspējas problēmas, ja kādā periodā ir liels skaits nodokļu transakciju.</span><span class="sxs-lookup"><span data-stu-id="cd1bb-126">By default, the system generates offset tax transactions during the settlement process, which cause can performance issue if there are a large number of tax transactions within a period interval.</span></span> <span data-ttu-id="cd1bb-127">Atzīmējiet šo izvēles rūtiņu, lai novērstu korespondējošu nodokļu transakciju ģenerēšanu.</span><span class="sxs-lookup"><span data-stu-id="cd1bb-127">Select this check box to prevent generating offset tax transactions.</span></span>
12. <span data-ttu-id="cd1bb-128">Izvērsiet cilni **Perioda intervāli**.</span><span class="sxs-lookup"><span data-stu-id="cd1bb-128">Expand the **Period intervals** tab.</span></span>
13. <span data-ttu-id="cd1bb-129">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="cd1bb-129">Select **Add**.</span></span>
14. <span data-ttu-id="cd1bb-130">Jaunās rindas laukā **No datuma** ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="cd1bb-130">In the **From date** field in the new row, enter a date.</span></span>
15. <span data-ttu-id="cd1bb-131">Ievadiet datumu laukā **Līdz datumam**.</span><span class="sxs-lookup"><span data-stu-id="cd1bb-131">In the **To date** field, enter a date.</span></span>
16. <span data-ttu-id="cd1bb-132">Atlasiet **Jauns perioda intervāls**.</span><span class="sxs-lookup"><span data-stu-id="cd1bb-132">Select **New period interval**.</span></span> <span data-ttu-id="cd1bb-133">Kad pirmā perioda intervāls ir ievadīts, jaunus periodus var izveidot automātiski.</span><span class="sxs-lookup"><span data-stu-id="cd1bb-133">Once the first period interval has been entered, new periods can be created automatically.</span></span> <span data-ttu-id="cd1bb-134">Pēc nepieciešamības varat atgriezties un pievienot jaunus periodu intervālus.</span><span class="sxs-lookup"><span data-stu-id="cd1bb-134">You can come back and add new period intervals as required.</span></span>  
17. <span data-ttu-id="cd1bb-135">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="cd1bb-135">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
