---
title: Pārdošanas pasūtījuma rēķinu izveidošana
description: Šajā uzdevuma ceļvedī ir aprakstīta pārdošanas pasūtījuma rēķina izrakstīšana, tostarp rēķinu sapludināšana un pakešapstrāde.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesEditLines,  SysQueryForm, SysRecurrence
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2a41524c773284812aa6eebddcd832c78bd29166
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178887"
---
# <a name="create-sales-order-invoices"></a><span data-ttu-id="c60e4-103">Pārdošanas pasūtījuma rēķinu izveidošana</span><span class="sxs-lookup"><span data-stu-id="c60e4-103">Create sales order invoices</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c60e4-104">Šajā uzdevuma ceļvedī ir aprakstīta pārdošanas pasūtījuma rēķina izrakstīšana, tostarp rēķinu sapludināšana un pakešapstrāde.</span><span class="sxs-lookup"><span data-stu-id="c60e4-104">This task guide describes invoicing a sales order, including merging invoices and batch processing.</span></span> <span data-ttu-id="c60e4-105">Procedūrā tiek izmantoti demonstrācijas uzņēmuma “USMF” dati.</span><span class="sxs-lookup"><span data-stu-id="c60e4-105">This procedure uses the USMF demo company.</span></span>


## <a name="create-an-invoice-from-a-sales-order"></a><span data-ttu-id="c60e4-106">Izveidot rēķinu no pārdošanas pasūtījuma</span><span class="sxs-lookup"><span data-stu-id="c60e4-106">Create an invoice from a sales order</span></span>
1. <span data-ttu-id="c60e4-107">Dodieties uz **Navigācijas rūts > Moduļi > Debitoru parādi > Pasūtījumi > Nosūtītie pārdošanas pasūtījumi, kas vēl nav iekļauti rēķinā**.</span><span class="sxs-lookup"><span data-stu-id="c60e4-107">Go to **Navigation pane > Modules > Accounts receivable > Orders > Shipped but not invoiced sales orders**.</span></span>
2. <span data-ttu-id="c60e4-108">Sarakstā atlasiet kādu pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="c60e4-108">Select a sales order in the list.</span></span> 
3. <span data-ttu-id="c60e4-109">**Darbību rūtī** noklikšķiniet uz **Rēķins > Ģenerēt > Rēķins**.</span><span class="sxs-lookup"><span data-stu-id="c60e4-109">On the **Action Pane**, click **Invoice > Generate > Invoice**.</span></span> <span data-ttu-id="c60e4-110">Ievērojiet, ka ar šo pārdošanas pasūtījumu ir saistītas vairākas pavadzīmes.</span><span class="sxs-lookup"><span data-stu-id="c60e4-110">Note that this sales order has multiple packing slips associated with it.</span></span> <span data-ttu-id="c60e4-111">Pavadzīmes numura vietā tajā tiek rādīts tikai vārds <multiple>.</span><span class="sxs-lookup"><span data-stu-id="c60e4-111">It will only show the word <multiple> instead of the packing slip number.</span></span>  
4. <span data-ttu-id="c60e4-112">Izvērsiet sadaļu **Parametri**.</span><span class="sxs-lookup"><span data-stu-id="c60e4-112">Expand the **Parameters** section.</span></span>
    - <span data-ttu-id="c60e4-113">Lai grāmatotu rēķinu, grāmatošana ir jāiestata uz Jā.</span><span class="sxs-lookup"><span data-stu-id="c60e4-113">Posting must be set to Yes to post the invoice.</span></span> <span data-ttu-id="c60e4-114">Varat arī grāmatošanu izslēgt un rēķinu tikai drukāt.</span><span class="sxs-lookup"><span data-stu-id="c60e4-114">You can also turn off posting and just print the invoice.</span></span> <span data-ttu-id="c60e4-115">Taču to pašu rezultātu varat panākt, rēķina vietā izveidojot pro forma rēķinu.</span><span class="sxs-lookup"><span data-stu-id="c60e4-115">However, you can accomplish the same result by creating a proforma invoice instead of an invoice.</span></span>  
    - <span data-ttu-id="c60e4-116">Šī opcija tiek izmantota pakešuzdevumiem.</span><span class="sxs-lookup"><span data-stu-id="c60e4-116">This option is used for batch jobs.</span></span> <span data-ttu-id="c60e4-117">Vaicājums tiek izpildīts, kad tiek veikts pakešuzdevums.</span><span class="sxs-lookup"><span data-stu-id="c60e4-117">The query is run when the batch job is run.</span></span>
5. <span data-ttu-id="c60e4-118">Laukā **Drukāt** atlasiet “Pēc”.</span><span class="sxs-lookup"><span data-stu-id="c60e4-118">In the **Print** field, select 'After'.</span></span>
6. <span data-ttu-id="c60e4-119">Vienumam **Drukāt rēķinu** atlasiet vērtību **Drukāt rēķinu**.</span><span class="sxs-lookup"><span data-stu-id="c60e4-119">Select **Yes** for **Print invoice**.</span></span> <span data-ttu-id="c60e4-120">Drukas pārvaldība var drukāt vairākas rēķina kopijas, kā arī nosūtīt rēķinu pa e-pastu kā PDF failu.</span><span class="sxs-lookup"><span data-stu-id="c60e4-120">Print management can print  multiple copies of the invoice and also send the invoice via email as a PDF file.</span></span>  
7. <span data-ttu-id="c60e4-121">Laukā **Drukāt maksas** atlasiet vērtību “Apkopot”.</span><span class="sxs-lookup"><span data-stu-id="c60e4-121">In the **Print charges** field, select 'Summarize'.</span></span>
8. <span data-ttu-id="c60e4-122">Laukā **Pārbaudīt kredīta limitu** atlasiet vienumu “Bilance”.</span><span class="sxs-lookup"><span data-stu-id="c60e4-122">In the **Check credit limit** field, select 'Balance'.</span></span>
9. <span data-ttu-id="c60e4-123">Noklikšķiniet uz **Atcelt**.</span><span class="sxs-lookup"><span data-stu-id="c60e4-123">Click **Cancel**.</span></span>

## <a name="combine-orders-into-a-single-invoice"></a><span data-ttu-id="c60e4-124">Kombinēt pasūtījumus vienā rēķinā</span><span class="sxs-lookup"><span data-stu-id="c60e4-124">Combine orders into a single invoice</span></span>
1. <span data-ttu-id="c60e4-125">Dodieties uz **Navigācijas rūts > Moduļi > Debitori > Pasūtījumi > Visi pārdošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="c60e4-125">Go to **Navigation pane > Modules > Accounts receivable > Orders > All sales orders**.</span></span>
2. <span data-ttu-id="c60e4-126">Atrodiet debitoru, kam ir atvērti vairāki rēķini.</span><span class="sxs-lookup"><span data-stu-id="c60e4-126">Locate a customer that has multiple invoices open.</span></span>
3. <span data-ttu-id="c60e4-127">Atlasiet vairākus atvērtos pārdošanas pasūtījumus no tā paša debitora.</span><span class="sxs-lookup"><span data-stu-id="c60e4-127">Select multiple open sales orders from the same customer.</span></span>
4. <span data-ttu-id="c60e4-128">**Darbību rūtī** noklikšķiniet uz **Rēķins > Ģenerēt > Rēķins**.</span><span class="sxs-lookup"><span data-stu-id="c60e4-128">On the **Action Pane**, click **Invoice > Generate > Invoice**.</span></span>
5. <span data-ttu-id="c60e4-129">Izvērsiet sadaļu **Parametri**.</span><span class="sxs-lookup"><span data-stu-id="c60e4-129">Expand the **Parameters** section.</span></span>
6. <span data-ttu-id="c60e4-130">Laukā **Daudzums** atlasiet vērtību “Visi”.</span><span class="sxs-lookup"><span data-stu-id="c60e4-130">In the **Quantity** field, select 'All'.</span></span> <span data-ttu-id="c60e4-131">Ņemiet vērā, ka pārskata sadaļā ir uzskaitīti divi rēķini.</span><span class="sxs-lookup"><span data-stu-id="c60e4-131">Note that there are two invoices listed in the overview section.</span></span> <span data-ttu-id="c60e4-132">Tagad tos abus sapludināsim vienā rēķinā.</span><span class="sxs-lookup"><span data-stu-id="c60e4-132">Now let's merge them into a single invoice.</span></span>  
7. <span data-ttu-id="c60e4-133">Laukā **Kopgrāmatojums** atlasiet vērtību “Rēķina konts”.</span><span class="sxs-lookup"><span data-stu-id="c60e4-133">In the **Summary update for** field, select 'Invoice account'.</span></span>
8. <span data-ttu-id="c60e4-134">Noklikšķiniet uz **Sakārtot**, lai pārdošanas pasūtījumus sapludinātu vienā rēķinā.</span><span class="sxs-lookup"><span data-stu-id="c60e4-134">Click **Arrange** to merge the sales orders into a single invoice.</span></span> <span data-ttu-id="c60e4-135">Abi pārdošanas pasūtījumi tagad ir sapludināti vienā rēķinā.</span><span class="sxs-lookup"><span data-stu-id="c60e4-135">The two sales orders are now merged into a single invoice.</span></span>   
9. <span data-ttu-id="c60e4-136">Noklikšķiniet uz **Atcelt**.</span><span class="sxs-lookup"><span data-stu-id="c60e4-136">Click **Cancel**.</span></span>
10. <span data-ttu-id="c60e4-137">Noklikšķiniet uz pogas **Jā**.</span><span class="sxs-lookup"><span data-stu-id="c60e4-137">Click **Yes**.</span></span>

## <a name="post-invoices-in-a-batch"></a><span data-ttu-id="c60e4-138">Veikt rēķinu pakešveida grāmatošanu</span><span class="sxs-lookup"><span data-stu-id="c60e4-138">Post invoices in a batch</span></span>
1. <span data-ttu-id="c60e4-139">Dodieties uz **Navigācijas rūts > Moduļi > Debitori > Rēķini > Partijas rēķinu izrakstīšana > Rēķins**.</span><span class="sxs-lookup"><span data-stu-id="c60e4-139">Go to **Navigation pane > Modules > Accounts receivable > Invoices > Batch invoicing > Invoice**.</span></span>
2. <span data-ttu-id="c60e4-140">Noklikšķiniet uz **Atlasīt**.</span><span class="sxs-lookup"><span data-stu-id="c60e4-140">Click **Select**.</span></span>
3. <span data-ttu-id="c60e4-141">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="c60e4-141">Click **OK**.</span></span>
4. <span data-ttu-id="c60e4-142">Noklikšķiniet uz **Partija**.</span><span class="sxs-lookup"><span data-stu-id="c60e4-142">Click **Batch**.</span></span>
5. <span data-ttu-id="c60e4-143">Vienumam **Pakešapstrāde** atlasiet **Jā**.</span><span class="sxs-lookup"><span data-stu-id="c60e4-143">Select **Yes** in **Batch processing**.</span></span>
6. <span data-ttu-id="c60e4-144">Noklikšķiniet uz **Periodiskums**.</span><span class="sxs-lookup"><span data-stu-id="c60e4-144">Click **Recurrence**.</span></span>
7. <span data-ttu-id="c60e4-145">Atlasiet vienumu **Dienas**.</span><span class="sxs-lookup"><span data-stu-id="c60e4-145">Select **Days**.</span></span>
8. <span data-ttu-id="c60e4-146">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="c60e4-146">Click **OK**.</span></span>
9. <span data-ttu-id="c60e4-147">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="c60e4-147">Click **OK**.</span></span>
10. <span data-ttu-id="c60e4-148">Noklikšķiniet uz **Atcelt**.</span><span class="sxs-lookup"><span data-stu-id="c60e4-148">Click **Cancel**.</span></span>
11. <span data-ttu-id="c60e4-149">Noklikšķiniet uz pogas **Jā**.</span><span class="sxs-lookup"><span data-stu-id="c60e4-149">Click **Yes**.</span></span>

