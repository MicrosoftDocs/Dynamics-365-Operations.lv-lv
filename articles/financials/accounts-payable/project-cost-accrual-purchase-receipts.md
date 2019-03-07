---
title: Uzkrātās projekta izmaksas pirkšanas pavadzīmēs
description: Šajā tēmā ir aprakstīts, kā var izsekot uzkrātajām projekta izmaksām pirkšanas pavadzīmēs programmā Microsoft Dynamics 365 for Finance and Operations.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostControlCommittedCost
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 266984
ms.assetid: 61e7d2a3-5aab-4113-bccc-213f932885d2
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: bc822652abbba68f094fe5b8a65f796165a92c4c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "340434"
---
# <a name="project-cost-accrual-on-purchase-receipts"></a><span data-ttu-id="a944c-103">Uzkrātās projekta izmaksas pirkšanas pavadzīmēs</span><span class="sxs-lookup"><span data-stu-id="a944c-103">Project cost accrual on purchase receipts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a944c-104">Šajā tēmā ir aprakstīts, kā var izsekot uzkrātajām projekta izmaksām pirkšanas pavadzīmēs programmā Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a944c-104">This topic describes how accrued project costs from purchase receipts can be tracked in Microsoft Dynamics 365 for Finance and Operations.</span></span> 

<span data-ttu-id="a944c-105">Bieži vien projekta rēķini tiek saņemti vēlāk par preču un pakalpojumu piegādi, un tas var būtiski ietekmēt projekta izpildes pamatrādītājus (KPI).</span><span class="sxs-lookup"><span data-stu-id="a944c-105">Invoices for a project often arrive later than the goods and services are delivered, which might have a significant impact on project key performance indicators (KPIs).</span></span> <span data-ttu-id="a944c-106">Ir svarīgi, lai jūs varētu izsekot šīs transakcijas gan finanšu, gan projekta pārskatos.</span><span class="sxs-lookup"><span data-stu-id="a944c-106">It important to be able to track these transactions in both financial and project reports.</span></span>

<span data-ttu-id="a944c-107">Tas ir atainots tālāk sniegtajā scenārija piemērā.</span><span class="sxs-lookup"><span data-stu-id="a944c-107">The following example scenario illustrates this.</span></span> 

<span data-ttu-id="a944c-108">Uzņēmums Contoso Consulting ir sācis jaunu mākoņa izvietošanas projektu.</span><span class="sxs-lookup"><span data-stu-id="a944c-108">Contoso Consulting has started a new cloud deployment project.</span></span> <span data-ttu-id="a944c-109">Ir izveidots pirkšanas pasūtījums, lai nopirktu datoru šī projekta vajadzībām.</span><span class="sxs-lookup"><span data-stu-id="a944c-109">A purchase order is created to buy a computer for the project.</span></span> <span data-ttu-id="a944c-110">Datora izmaksas ir $ 1500 un uzstādīšanas pakalpojumu izmaksas ir $ 150.</span><span class="sxs-lookup"><span data-stu-id="a944c-110">The computer will cost $1500 and installation services will cost $150.</span></span> <span data-ttu-id="a944c-111">Kreditors ir piegādājis un uzstādījis datoru, taču uzņēmums Contoso Consulting vēl nav saņēmis rēķinu.</span><span class="sxs-lookup"><span data-stu-id="a944c-111">The vendor has delivered and installed the computer, but the invoice has not yet reached Contoso Consulting.</span></span> <span data-ttu-id="a944c-112">Projekta vadītājs vēlas redzēt uzkrātās projekta izmaksas $ 1650, pirms tiek piegādāts rēķins.</span><span class="sxs-lookup"><span data-stu-id="a944c-112">The project manager would like to see project cost accrual of $1650 before the invoice gets delivered.</span></span> <span data-ttu-id="a944c-113">Šīs izmaksas ir arī jāietver uzņēmuma mēneša beigu finanšu pārskatos.</span><span class="sxs-lookup"><span data-stu-id="a944c-113">This cost should also be reflected in the company's month end financial statements.</span></span> 

<span data-ttu-id="a944c-114">Uzkrātās izmaksas ir jāreģistrē gan finanšu līmenī, gan projekta līmenī pārskatu izveides nolūkā.</span><span class="sxs-lookup"><span data-stu-id="a944c-114">The accrued cost needs to be recorded on both the financial level and project level for reporting purposes.</span></span> <span data-ttu-id="a944c-115">Programmatūrā Finance and Operations var izsekot krājumu un sagādes kategoriju preces ieejas plūsmas finanšu atjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="a944c-115">In Finance and Operations, the financial update of the product receipt can be tracked for the item and procurement categories.</span></span> 

<span data-ttu-id="a944c-116">Krājumiem lapā **Kreditoru parādu parametri** atlasiet opciju **Grāmatot produktu ieejas plūsmas Virsgrāmatā**.</span><span class="sxs-lookup"><span data-stu-id="a944c-116">For items, on the **Accounts payable parameters** page, select the **Post product receipts to ledger** option.</span></span>
<span data-ttu-id="a944c-117">[![accruals1](./media/accruals1-1024x409.png)](./media/accruals1.png)</span><span class="sxs-lookup"><span data-stu-id="a944c-117">[![accruals1](./media/accruals1-1024x409.png)](./media/accruals1.png)</span></span> 

<span data-ttu-id="a944c-118">Sagādes kategorijām lapā **Kategorijas ierobežojuma nosacījums** atlasiet nosacījumus **Pirkšana** un pēc tam katrai sagādes kategorijai atlasiet vienumu **rāt ieejas plūsmas pirkšanas izdevumus**.</span><span class="sxs-lookup"><span data-stu-id="a944c-118">For procurement categories, on the **Category policy rule** page, select **Purchasing** policies, and then select **Accrue purchase expense on receipt** for each procurement category.</span></span>
<span data-ttu-id="a944c-119">[![accruals2](./media/accruals2-1024x569.png)](./media/accruals2.png)</span><span class="sxs-lookup"><span data-stu-id="a944c-119">[![accruals2](./media/accruals2-1024x569.png)](./media/accruals2.png)</span></span> 

<span data-ttu-id="a944c-120">Grāmatojot ar preces ieejas plūsmu saistītos dokumentus, tiek izmantoti konti **Pirkšanas izdevumi, kas nav iekļauti rēķinos** un **Pirkumu uzkrājums**, kas ir ietverti sadaļā **Grāmatošanas iestatīšana**.</span><span class="sxs-lookup"><span data-stu-id="a944c-120">The **Purchase expenditure un-invoiced** and **Purchase accrual** accounts in **Posting setup** will be used when vouchers that are related to the product receipt are posted.</span></span>
<span data-ttu-id="a944c-121">[![accruals3](./media/accruals3-1024x429.png)](./media/accruals3.png)</span><span class="sxs-lookup"><span data-stu-id="a944c-121">[![accruals3](./media/accruals3-1024x429.png)](./media/accruals3.png)</span></span> 

<span data-ttu-id="a944c-122">Izmantojot to pašu scenāriju, apskatīsim, kā preces ieejas plūsmas grāmatošana ietekmē Virsgrāmatas un preces informāciju.</span><span class="sxs-lookup"><span data-stu-id="a944c-122">Using this same scenario, let's see how posting a product receipt will impact General ledger and Project information.</span></span> 

<span data-ttu-id="a944c-123">**1. darbība.** Izveidojiet un apstipriniet jaunu projekta pirkšanas pasūtījumu, lai reģistrētu datora pirkšanu par $ 1500 un uzstādīšanas pakalpojumus par $ 150.</span><span class="sxs-lookup"><span data-stu-id="a944c-123">**Step 1:** Create and confirm a new purchase order for the project to record the purchase of a computer for $1500 and installation services for $150.</span></span>
<span data-ttu-id="a944c-124">[![accruals4](./media/accruals4-1024x497.png)](./media/accruals4.png)</span><span class="sxs-lookup"><span data-stu-id="a944c-124">[![accruals4](./media/accruals4-1024x497.png)](./media/accruals4.png)</span></span> 

<span data-ttu-id="a944c-125">Pēc pirkšanas pasūtījuma apstiprināšanas tiek izveidotas projekta fiksēto izmaksu transakcijas.</span><span class="sxs-lookup"><span data-stu-id="a944c-125">When the purchase order is confirmed, transactions for the committed cost are created for the project.</span></span> 
<span data-ttu-id="a944c-126">[![accruals5](./media/accruals5-1024x219.png)](./media/accruals5.png)</span><span class="sxs-lookup"><span data-stu-id="a944c-126">[![accruals5](./media/accruals5-1024x219.png)](./media/accruals5.png)</span></span> 

> [!NOTE]
> <span data-ttu-id="a944c-127">Tiek iestatīta fiksēto izmaksu transakciju lauka **Darbības izcelsme** vērtība **Pirkšanas pasūtījums**.</span><span class="sxs-lookup"><span data-stu-id="a944c-127">The transactions for the committed cost will have the **Transaction Origin** field set to **Purchase Order**.</span></span> <span data-ttu-id="a944c-128">Izveidojot un apstiprinot pirkšanas pasūtījumu, netiek izveidotas projekta transakcijas.</span><span class="sxs-lookup"><span data-stu-id="a944c-128">Creating and confirming a purchase order does not create transactions for a project.</span></span> 

<span data-ttu-id="a944c-129">**2. darbība.** Tiek piegādātas preces un pakalpojumu, un tiek reģistrēta preces ieejas plūsma.</span><span class="sxs-lookup"><span data-stu-id="a944c-129">**Step 2:** Goods and services get delivered and a product receipt is registered.</span></span> 

<span data-ttu-id="a944c-130">Grāmatojot preces ieejas plūsmu, tiek ģenerēts dokuments, kas tiek grāmatots Virsgrāmatā.</span><span class="sxs-lookup"><span data-stu-id="a944c-130">Posting a product receipt will generate and post a voucher to the ledger.</span></span> <span data-ttu-id="a944c-131">Šis dokuments izraisa pirkšanas izdevumu rēķinos neiekļautu izdevumu konta debitēšanu un pirkumu uzkrājuma konta kreditēšanu.</span><span class="sxs-lookup"><span data-stu-id="a944c-131">The voucher will debit the purchase expenditure, un-invoiced account, and credit purchase accrual account.</span></span> 
<span data-ttu-id="a944c-132">[![accruals6](./media/accruals6-1024x214.png)](./media/accruals6.png)</span><span class="sxs-lookup"><span data-stu-id="a944c-132">[![accruals6](./media/accruals6-1024x214.png)](./media/accruals6.png)</span></span>

> [!NOTE]
> <span data-ttu-id="a944c-133">Grāmatojot preces ieejas plūsmu, tiek izmantoti sagādes kategoriju un preču grāmatošanas iestatījumi, nevis projektu kategoriju grāmatošanas iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="a944c-133">Posting a product receipt will use the posting setup for procurement categories and products, and not the posting setup for the project categories.</span></span> <span data-ttu-id="a944c-134">Lai pareizi atainotu pirkumu uzkrājumu finanšu ietekmi, ir jāsaskaņo šie iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="a944c-134">In order to correctly reflect financial impact of purchase accruals, this setup needs to be aligned.</span></span> 

<span data-ttu-id="a944c-135">Sagādes kategorijas var kartēt ar preču kategorijām lapā **Sagādes kategorija**.</span><span class="sxs-lookup"><span data-stu-id="a944c-135">It is possible to map procurement categories to project categories on the **Procurement category** page.</span></span>
<span data-ttu-id="a944c-136">[![accruals7](./media/accruals7-1024x390.png)](./media/accruals7.png)</span><span class="sxs-lookup"><span data-stu-id="a944c-136">[![accruals7](./media/accruals7-1024x390.png)](./media/accruals7.png)</span></span>

<span data-ttu-id="a944c-137">**3. darbība.** Izveidojiet kreditora rēķina melnrakstu.</span><span class="sxs-lookup"><span data-stu-id="a944c-137">**Step 3:** Create a draft vendor invoice.</span></span> 

<span data-ttu-id="a944c-138">Programmatūrā Finance and Operations preces ieejas plūsmas grāmatošana neietekmē projekta informāciju.</span><span class="sxs-lookup"><span data-stu-id="a944c-138">In Finance and Operations, posting a product receipt does not impact project information.</span></span> <span data-ttu-id="a944c-139">Lai to atrisinātu, varat ģenerēt kreditora rēķina melnrakstu uzreiz pēc pirkšanas ieejas plūsmas grāmatošanas.</span><span class="sxs-lookup"><span data-stu-id="a944c-139">As a workaround, you could generate a draft vendor invoice right after posting the purchase receipt.</span></span> <span data-ttu-id="a944c-140">Pārejiet uz lapu **Pirkšanas pasūtījums** &gt; **cilni Rēķins** &gt; **Ģenerēt** &gt; **Rēķins**.</span><span class="sxs-lookup"><span data-stu-id="a944c-140">Go to the **Purchase Order** page &gt; **Invoice tab** &gt; **Generate** &gt; **Invoice**.</span></span> <span data-ttu-id="a944c-141">Tādējādi tiek izveidots nenokārtota rēķina dokuments, kas nodrošina projekta informācijas atjaunināšanu.</span><span class="sxs-lookup"><span data-stu-id="a944c-141">This creates a pending invoice document that updates project information.</span></span> 

<span data-ttu-id="a944c-142">Izveidojot kreditora rēķina melnrakstu, tiek ģenerētas nepabeigtas projekta transakcijas.</span><span class="sxs-lookup"><span data-stu-id="a944c-142">Creating a draft vendor invoice will generate pending project transactions.</span></span> 
<span data-ttu-id="a944c-143">[![accruals8](./media/accruals8-1024x225.png)](./media/accruals8.png)</span><span class="sxs-lookup"><span data-stu-id="a944c-143">[![accruals8](./media/accruals8-1024x225.png)](./media/accruals8.png)</span></span> 

<span data-ttu-id="a944c-144">Lapā **Fiksētās izmaksas** tiek slēgti 1. darbības ietvaros izveidotie ieraksti un tiek izveidoti jauni ieraksti, kas atbilst fiksētajām izmaksām nenokārtotajā kreditora rēķinā.</span><span class="sxs-lookup"><span data-stu-id="a944c-144">In the **Committed cost** page, records created in step 1 will be closed and new records will be created to reflect cost commitment coming from the pending vendor invoice.</span></span> <span data-ttu-id="a944c-145">Tiek iestatīta fiksēto izmaksu lauka **Darbības izcelsme** vērtība **Kreditora rēķins**.</span><span class="sxs-lookup"><span data-stu-id="a944c-145">The **Transaction origin** field for the committed cost will be set to **Vendor invoice**.</span></span>
<span data-ttu-id="a944c-146">[![accruals9](./media/accruals9-1024x200.png)](./media/accruals9.png)</span><span class="sxs-lookup"><span data-stu-id="a944c-146">[![accruals9](./media/accruals9-1024x200.png)](./media/accruals9.png)</span></span>

<span data-ttu-id="a944c-147">Kreditora rēķina stāvoklis ir Nenokārtots, līdz tiek saņemts faktiskais kreditora rēķins.</span><span class="sxs-lookup"><span data-stu-id="a944c-147">The vendor invoice will remain in a pending state until the actual vendor invoice arrives.</span></span>



