---
title: Uzkrātās projekta izmaksas pirkšanas pavadzīmēs
description: Šajā tēmā ir aprakstīts, kā var izsekot uzkrātajām projekta izmaksām pirkšanas pavadzīmēs programmā Microsoft Dynamics 365 Finance.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostControlCommittedCost
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 266984
ms.assetid: 61e7d2a3-5aab-4113-bccc-213f932885d2
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 9200b0e4bc3862abdb3ecacb6539f7ba0d619b2f
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189618"
---
# <a name="project-cost-accrual-on-purchase-receipts"></a><span data-ttu-id="a0ce9-103">Uzkrātās projekta izmaksas pirkšanas pavadzīmēs</span><span class="sxs-lookup"><span data-stu-id="a0ce9-103">Project cost accrual on purchase receipts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a0ce9-104">Šajā tēmā ir aprakstīts, kā var izsekot uzkrātajām projekta izmaksām pirkšanas pavadzīmēs programmā Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="a0ce9-104">This topic describes how accrued project costs from purchase receipts can be tracked in Microsoft Dynamics 365 Finance.</span></span> 

<span data-ttu-id="a0ce9-105">Bieži vien projekta rēķini tiek saņemti vēlāk par preču un pakalpojumu piegādi, un tas var būtiski ietekmēt projekta izpildes pamatrādītājus (KPI).</span><span class="sxs-lookup"><span data-stu-id="a0ce9-105">Invoices for a project often arrive later than the goods and services are delivered, which might have a significant impact on project key performance indicators (KPIs).</span></span> <span data-ttu-id="a0ce9-106">Ir svarīgi, lai jūs varētu izsekot šīs transakcijas gan finanšu, gan projekta pārskatos.</span><span class="sxs-lookup"><span data-stu-id="a0ce9-106">It important to be able to track these transactions in both financial and project reports.</span></span>

<span data-ttu-id="a0ce9-107">Tas ir atainots tālāk sniegtajā scenārija piemērā.</span><span class="sxs-lookup"><span data-stu-id="a0ce9-107">The following example scenario illustrates this.</span></span> 

<span data-ttu-id="a0ce9-108">Uzņēmums Contoso Consulting ir sācis jaunu mākoņa izvietošanas projektu.</span><span class="sxs-lookup"><span data-stu-id="a0ce9-108">Contoso Consulting has started a new cloud deployment project.</span></span> <span data-ttu-id="a0ce9-109">Ir izveidots pirkšanas pasūtījums, lai nopirktu datoru šī projekta vajadzībām.</span><span class="sxs-lookup"><span data-stu-id="a0ce9-109">A purchase order is created to buy a computer for the project.</span></span> <span data-ttu-id="a0ce9-110">Datora izmaksas ir $ 1500 un uzstādīšanas pakalpojumu izmaksas ir $ 150.</span><span class="sxs-lookup"><span data-stu-id="a0ce9-110">The computer will cost $1500 and installation services will cost $150.</span></span> <span data-ttu-id="a0ce9-111">Kreditors ir piegādājis un uzstādījis datoru, taču uzņēmums Contoso Consulting vēl nav saņēmis rēķinu.</span><span class="sxs-lookup"><span data-stu-id="a0ce9-111">The vendor has delivered and installed the computer, but the invoice has not yet reached Contoso Consulting.</span></span> <span data-ttu-id="a0ce9-112">Projekta vadītājs vēlas redzēt uzkrātās projekta izmaksas $ 1650, pirms tiek piegādāts rēķins.</span><span class="sxs-lookup"><span data-stu-id="a0ce9-112">The project manager would like to see project cost accrual of $1650 before the invoice gets delivered.</span></span> <span data-ttu-id="a0ce9-113">Šīs izmaksas ir arī jāietver uzņēmuma mēneša beigu finanšu pārskatos.</span><span class="sxs-lookup"><span data-stu-id="a0ce9-113">This cost should also be reflected in the company's month end financial statements.</span></span> 

<span data-ttu-id="a0ce9-114">Uzkrātās izmaksas ir jāreģistrē gan finanšu līmenī, gan projekta līmenī pārskatu izveides nolūkā.</span><span class="sxs-lookup"><span data-stu-id="a0ce9-114">The accrued cost needs to be recorded on both the financial level and project level for reporting purposes.</span></span> <span data-ttu-id="a0ce9-115">Var izsekot krājumu un sagādes kategoriju preces ieejas plūsmas finanšu atjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="a0ce9-115">The financial update of the product receipt can be tracked for the item and procurement categories.</span></span> 

<span data-ttu-id="a0ce9-116">Krājumiem lapā **Kreditoru parādu parametri** atlasiet opciju **Grāmatot produktu ieejas plūsmas Virsgrāmatā**.</span><span class="sxs-lookup"><span data-stu-id="a0ce9-116">For items, on the **Accounts payable parameters** page, select the **Post product receipts to ledger** option.</span></span>
<span data-ttu-id="a0ce9-117">[![accruals1](./media/accruals1-1024x409.png)](./media/accruals1.png)</span><span class="sxs-lookup"><span data-stu-id="a0ce9-117">[![accruals1](./media/accruals1-1024x409.png)](./media/accruals1.png)</span></span> 

<span data-ttu-id="a0ce9-118">Sagādes kategorijām lapā **Kategorijas ierobežojuma nosacījums** atlasiet nosacījumus **Pirkšana** un pēc tam katrai sagādes kategorijai atlasiet vienumu **rāt ieejas plūsmas pirkšanas izdevumus**.</span><span class="sxs-lookup"><span data-stu-id="a0ce9-118">For procurement categories, on the **Category policy rule** page, select **Purchasing** policies, and then select **Accrue purchase expense on receipt** for each procurement category.</span></span>
<span data-ttu-id="a0ce9-119">[![accruals2](./media/accruals2-1024x569.png)](./media/accruals2.png)</span><span class="sxs-lookup"><span data-stu-id="a0ce9-119">[![accruals2](./media/accruals2-1024x569.png)](./media/accruals2.png)</span></span> 

<span data-ttu-id="a0ce9-120">Grāmatojot ar preces ieejas plūsmu saistītos dokumentus, tiek izmantoti konti **Pirkšanas izdevumi, kas nav iekļauti rēķinos** un **Pirkumu uzkrājums**, kas ir ietverti sadaļā **Grāmatošanas iestatīšana**.</span><span class="sxs-lookup"><span data-stu-id="a0ce9-120">The **Purchase expenditure un-invoiced** and **Purchase accrual** accounts in **Posting setup** will be used when vouchers that are related to the product receipt are posted.</span></span>
<span data-ttu-id="a0ce9-121">[![accruals3](./media/accruals3-1024x429.png)](./media/accruals3.png)</span><span class="sxs-lookup"><span data-stu-id="a0ce9-121">[![accruals3](./media/accruals3-1024x429.png)](./media/accruals3.png)</span></span> 

<span data-ttu-id="a0ce9-122">Izmantojot to pašu scenāriju, apskatīsim, kā preces ieejas plūsmas grāmatošana ietekmē Virsgrāmatas un preces informāciju.</span><span class="sxs-lookup"><span data-stu-id="a0ce9-122">Using this same scenario, let's see how posting a product receipt will impact General ledger and Project information.</span></span> 

<span data-ttu-id="a0ce9-123">**1. darbība.** Izveidojiet un apstipriniet jaunu projekta pirkšanas pasūtījumu, lai reģistrētu datora pirkšanu par $ 1500 un uzstādīšanas pakalpojumus par $ 150.</span><span class="sxs-lookup"><span data-stu-id="a0ce9-123">**Step 1:** Create and confirm a new purchase order for the project to record the purchase of a computer for $1500 and installation services for $150.</span></span>
<span data-ttu-id="a0ce9-124">[![accruals4](./media/accruals4-1024x497.png)](./media/accruals4.png)</span><span class="sxs-lookup"><span data-stu-id="a0ce9-124">[![accruals4](./media/accruals4-1024x497.png)](./media/accruals4.png)</span></span> 

<span data-ttu-id="a0ce9-125">Pēc pirkšanas pasūtījuma apstiprināšanas tiek izveidotas projekta fiksēto izmaksu transakcijas.</span><span class="sxs-lookup"><span data-stu-id="a0ce9-125">When the purchase order is confirmed, transactions for the committed cost are created for the project.</span></span> 
<span data-ttu-id="a0ce9-126">[![accruals5](./media/accruals5-1024x219.png)](./media/accruals5.png)</span><span class="sxs-lookup"><span data-stu-id="a0ce9-126">[![accruals5](./media/accruals5-1024x219.png)](./media/accruals5.png)</span></span> 

> [!NOTE]
> <span data-ttu-id="a0ce9-127">Tiek iestatīta fiksēto izmaksu transakciju lauka **Darbības izcelsme** vērtība **Pirkšanas pasūtījums**.</span><span class="sxs-lookup"><span data-stu-id="a0ce9-127">The transactions for the committed cost will have the **Transaction Origin** field set to **Purchase Order**.</span></span> <span data-ttu-id="a0ce9-128">Izveidojot un apstiprinot pirkšanas pasūtījumu, netiek izveidotas projekta transakcijas.</span><span class="sxs-lookup"><span data-stu-id="a0ce9-128">Creating and confirming a purchase order does not create transactions for a project.</span></span> 

<span data-ttu-id="a0ce9-129">**2. darbība.** Tiek piegādātas preces un pakalpojumu, un tiek reģistrēta preces ieejas plūsma.</span><span class="sxs-lookup"><span data-stu-id="a0ce9-129">**Step 2:** Goods and services get delivered and a product receipt is registered.</span></span> 

<span data-ttu-id="a0ce9-130">Grāmatojot preces ieejas plūsmu, tiek ģenerēts dokuments, kas tiek grāmatots Virsgrāmatā.</span><span class="sxs-lookup"><span data-stu-id="a0ce9-130">Posting a product receipt will generate and post a voucher to the ledger.</span></span> <span data-ttu-id="a0ce9-131">Šis dokuments izraisa pirkšanas izdevumu rēķinos neiekļautu izdevumu konta debitēšanu un pirkumu uzkrājuma konta kreditēšanu.</span><span class="sxs-lookup"><span data-stu-id="a0ce9-131">The voucher will debit the purchase expenditure, un-invoiced account, and credit purchase accrual account.</span></span> 
<span data-ttu-id="a0ce9-132">[![accruals6](./media/accruals6-1024x214.png)](./media/accruals6.png)</span><span class="sxs-lookup"><span data-stu-id="a0ce9-132">[![accruals6](./media/accruals6-1024x214.png)](./media/accruals6.png)</span></span>

> [!NOTE]
> <span data-ttu-id="a0ce9-133">Grāmatojot preces ieejas plūsmu, tiek izmantoti sagādes kategoriju un preču grāmatošanas iestatījumi, nevis projektu kategoriju grāmatošanas iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="a0ce9-133">Posting a product receipt will use the posting setup for procurement categories and products, and not the posting setup for the project categories.</span></span> <span data-ttu-id="a0ce9-134">Lai pareizi atainotu pirkumu uzkrājumu finanšu ietekmi, ir jāsaskaņo šie iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="a0ce9-134">In order to correctly reflect financial impact of purchase accruals, this setup needs to be aligned.</span></span> 

<span data-ttu-id="a0ce9-135">Sagādes kategorijas var kartēt ar preču kategorijām lapā **Sagādes kategorija**.</span><span class="sxs-lookup"><span data-stu-id="a0ce9-135">It is possible to map procurement categories to project categories on the **Procurement category** page.</span></span>
<span data-ttu-id="a0ce9-136">[![accruals7](./media/accruals7-1024x390.png)](./media/accruals7.png)</span><span class="sxs-lookup"><span data-stu-id="a0ce9-136">[![accruals7](./media/accruals7-1024x390.png)](./media/accruals7.png)</span></span>

<span data-ttu-id="a0ce9-137">**3. darbība.** Izveidojiet kreditora rēķina melnrakstu.</span><span class="sxs-lookup"><span data-stu-id="a0ce9-137">**Step 3:** Create a draft vendor invoice.</span></span> 

<span data-ttu-id="a0ce9-138">Preces ieejas plūsmas grāmatošana neietekmē projekta informāciju.</span><span class="sxs-lookup"><span data-stu-id="a0ce9-138">Posting a product receipt does not impact project information.</span></span> <span data-ttu-id="a0ce9-139">Lai to atrisinātu, varat ģenerēt kreditora rēķina melnrakstu uzreiz pēc pirkšanas ieejas plūsmas grāmatošanas.</span><span class="sxs-lookup"><span data-stu-id="a0ce9-139">As a workaround, you could generate a draft vendor invoice right after posting the purchase receipt.</span></span> <span data-ttu-id="a0ce9-140">Pārejiet uz lapu **Pirkšanas pasūtījums** &gt; **cilni Rēķins** &gt; **Ģenerēt** &gt; **Rēķins**.</span><span class="sxs-lookup"><span data-stu-id="a0ce9-140">Go to the **Purchase Order** page &gt; **Invoice tab** &gt; **Generate** &gt; **Invoice**.</span></span> <span data-ttu-id="a0ce9-141">Tādējādi tiek izveidots nenokārtota rēķina dokuments, kas nodrošina projekta informācijas atjaunināšanu.</span><span class="sxs-lookup"><span data-stu-id="a0ce9-141">This creates a pending invoice document that updates project information.</span></span> 

<span data-ttu-id="a0ce9-142">Izveidojot kreditora rēķina melnrakstu, tiek ģenerētas nepabeigtas projekta transakcijas.</span><span class="sxs-lookup"><span data-stu-id="a0ce9-142">Creating a draft vendor invoice will generate pending project transactions.</span></span> 
<span data-ttu-id="a0ce9-143">[![accruals8](./media/accruals8-1024x225.png)](./media/accruals8.png)</span><span class="sxs-lookup"><span data-stu-id="a0ce9-143">[![accruals8](./media/accruals8-1024x225.png)](./media/accruals8.png)</span></span> 

<span data-ttu-id="a0ce9-144">Lapā **Fiksētās izmaksas** tiek slēgti 1. darbības ietvaros izveidotie ieraksti un tiek izveidoti jauni ieraksti, kas atbilst fiksētajām izmaksām nenokārtotajā kreditora rēķinā.</span><span class="sxs-lookup"><span data-stu-id="a0ce9-144">In the **Committed cost** page, records created in step 1 will be closed and new records will be created to reflect cost commitment coming from the pending vendor invoice.</span></span> <span data-ttu-id="a0ce9-145">Tiek iestatīta fiksēto izmaksu lauka **Darbības izcelsme** vērtība **Kreditora rēķins**.</span><span class="sxs-lookup"><span data-stu-id="a0ce9-145">The **Transaction origin** field for the committed cost will be set to **Vendor invoice**.</span></span>
<span data-ttu-id="a0ce9-146">[![accruals9](./media/accruals9-1024x200.png)](./media/accruals9.png)</span><span class="sxs-lookup"><span data-stu-id="a0ce9-146">[![accruals9](./media/accruals9-1024x200.png)](./media/accruals9.png)</span></span>

<span data-ttu-id="a0ce9-147">Kreditora rēķina stāvoklis ir Nenokārtots, līdz tiek saņemts faktiskais kreditora rēķins.</span><span class="sxs-lookup"><span data-stu-id="a0ce9-147">The vendor invoice will remain in a pending state until the actual vendor invoice arrives.</span></span>



