---
title: Pārdošanas pasūtījuma rēķinu izveidošana
description: Šajā uzdevuma ceļvedī ir aprakstīta pārdošanas pasūtījuma rēķina izrakstīšana, tostarp rēķinu sapludināšana un pakešapstrāde.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: ba8e0f02f2d1eb12cecc2c434fbca1e198cddbe9
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1842957"
---
# <a name="create-sales-order-invoices"></a><span data-ttu-id="40b0d-103">Pārdošanas pasūtījuma rēķinu izveidošana</span><span class="sxs-lookup"><span data-stu-id="40b0d-103">Create sales order invoices</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="40b0d-104">Šajā uzdevuma ceļvedī ir aprakstīta pārdošanas pasūtījuma rēķina izrakstīšana, tostarp rēķinu sapludināšana un pakešapstrāde.</span><span class="sxs-lookup"><span data-stu-id="40b0d-104">This task guide describes invoicing a sales order, including merging invoices and batch processing.</span></span> <span data-ttu-id="40b0d-105">Procedūrā tiek izmantoti demonstrācijas uzņēmuma “USMF” dati.</span><span class="sxs-lookup"><span data-stu-id="40b0d-105">This procedure uses the USMF demo company.</span></span>


## <a name="create-an-invoice-from-a-sales-order"></a><span data-ttu-id="40b0d-106">Izveidot rēķinu no pārdošanas pasūtījuma</span><span class="sxs-lookup"><span data-stu-id="40b0d-106">Create an invoice from a sales order</span></span>
1. <span data-ttu-id="40b0d-107">Dodieties uz Debitoru parādi > Pasūtījumi > Nosūtītie pārdošanas pasūtījumi, kas vēl nav iekļauti rēķinā.</span><span class="sxs-lookup"><span data-stu-id="40b0d-107">Go to Accounts receivable > Orders > Shipped but not invoiced sales orders.</span></span>
2. <span data-ttu-id="40b0d-108">Sarakstā atlasiet kādu pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="40b0d-108">Select a sales order in the list.</span></span> 
3. <span data-ttu-id="40b0d-109">Darbību rūtī noklikšķiniet uz Rēķins.</span><span class="sxs-lookup"><span data-stu-id="40b0d-109">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="40b0d-110">Noklikšķiniet uz Rēķins.</span><span class="sxs-lookup"><span data-stu-id="40b0d-110">Click Invoice.</span></span>
    * <span data-ttu-id="40b0d-111">Ievērojiet, ka ar šo pārdošanas pasūtījumu ir saistītas vairākas pavadzīmes.</span><span class="sxs-lookup"><span data-stu-id="40b0d-111">Note that this sales order has multiple packing slips associated with it.</span></span> <span data-ttu-id="40b0d-112">Pavadzīmes numura vietā tajā tiek rādīts tikai vārds <multiple>.</span><span class="sxs-lookup"><span data-stu-id="40b0d-112">It will only show the word <multiple> instead of the packing slip number.</span></span>  
5. <span data-ttu-id="40b0d-113">Izvērsiet sadaļu Parametri.</span><span class="sxs-lookup"><span data-stu-id="40b0d-113">Expand the Parameters section.</span></span>
    * <span data-ttu-id="40b0d-114">Lai grāmatotu rēķinu, grāmatošana ir jāiestata uz Jā.</span><span class="sxs-lookup"><span data-stu-id="40b0d-114">Posting must be set to Yes to post the invoice.</span></span> <span data-ttu-id="40b0d-115">Varat arī grāmatošanu izslēgt un rēķinu tikai drukāt.</span><span class="sxs-lookup"><span data-stu-id="40b0d-115">You can also turn off posting and just print the invoice.</span></span> <span data-ttu-id="40b0d-116">Taču to pašu rezultātu varat panākt, rēķina vietā izveidojot pro forma rēķinu.</span><span class="sxs-lookup"><span data-stu-id="40b0d-116">However, you can accomplish the same result by creating a proforma invoice instead of an invoice.</span></span>  
    * <span data-ttu-id="40b0d-117">Šī opcija tiek izmantota pakešuzdevumiem.</span><span class="sxs-lookup"><span data-stu-id="40b0d-117">This option is used for batch jobs.</span></span> <span data-ttu-id="40b0d-118">Vaicājums tiek izpildīts, kad tiek veikts pakešuzdevums.</span><span class="sxs-lookup"><span data-stu-id="40b0d-118">The query is run when the batch job is run.</span></span>    
6. <span data-ttu-id="40b0d-119">Laukā Drukāt atlasiet “Pēc”.</span><span class="sxs-lookup"><span data-stu-id="40b0d-119">In the Print field, select 'After'.</span></span>
7. <span data-ttu-id="40b0d-120">Vienumam Drukāt rēķinu atlasiet vērtību Jā.</span><span class="sxs-lookup"><span data-stu-id="40b0d-120">Select Yes for Print invoice.</span></span>
    * <span data-ttu-id="40b0d-121">Drukas pārvaldība var drukāt vairākas rēķina kopijas, kā arī nosūtīt rēķinu pa e-pastu kā PDF failu.</span><span class="sxs-lookup"><span data-stu-id="40b0d-121">Print management can print  multiple copies of the invoice and also send the invoice via email as a PDF file.</span></span>  
8. <span data-ttu-id="40b0d-122">Laukā Drukāt maksas atlasiet vērtību “Apkopot”.</span><span class="sxs-lookup"><span data-stu-id="40b0d-122">In the Print charges field, select 'Summarize'.</span></span>
9. <span data-ttu-id="40b0d-123">Laukā Pārbaudīt kredīta limitu atlasiet vienumu “Bilance”.</span><span class="sxs-lookup"><span data-stu-id="40b0d-123">In the Check credit limit field, select 'Balance'.</span></span>
10. <span data-ttu-id="40b0d-124">Noklikšķiniet uz Atcelt.</span><span class="sxs-lookup"><span data-stu-id="40b0d-124">Click Cancel.</span></span>

## <a name="combine-orders-into-a-single-invoice"></a><span data-ttu-id="40b0d-125">Kombinēt pasūtījumus vienā rēķinā</span><span class="sxs-lookup"><span data-stu-id="40b0d-125">Combine orders into a single invoice</span></span>
1. <span data-ttu-id="40b0d-126">Pārejiet uz sadaļu Debitori > Pasūtījumi > Visi pārdošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="40b0d-126">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="40b0d-127">Atrodiet debitoru, kam ir atvērti vairāki rēķini.</span><span class="sxs-lookup"><span data-stu-id="40b0d-127">Locate a customer that has multiple invoices open.</span></span>
3. <span data-ttu-id="40b0d-128">Atlasiet atvērtu pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="40b0d-128">Select an open sales order.</span></span>
4. <span data-ttu-id="40b0d-129">Atlasiet citu atvērtu pārdošanas pasūtījumu tam pašam debitoram.</span><span class="sxs-lookup"><span data-stu-id="40b0d-129">Select another open sales order for the same customer.</span></span>
5. <span data-ttu-id="40b0d-130">Darbību rūtī noklikšķiniet uz Rēķins.</span><span class="sxs-lookup"><span data-stu-id="40b0d-130">On the Action Pane, click Invoice.</span></span>
6. <span data-ttu-id="40b0d-131">Noklikšķiniet uz Rēķins.</span><span class="sxs-lookup"><span data-stu-id="40b0d-131">Click Invoice.</span></span>
7. <span data-ttu-id="40b0d-132">Izvērsiet sadaļu Parametri.</span><span class="sxs-lookup"><span data-stu-id="40b0d-132">Expand the Parameters section.</span></span>
8. <span data-ttu-id="40b0d-133">Laukā Daudzums atlasiet vērtību Visi.</span><span class="sxs-lookup"><span data-stu-id="40b0d-133">In the Quantity field, select 'All'.</span></span>
    * <span data-ttu-id="40b0d-134">Ņemiet vērā, ka pārskata sadaļā ir uzskaitīti divi rēķini.</span><span class="sxs-lookup"><span data-stu-id="40b0d-134">Note that there are two invoices listed in the overview section.</span></span> <span data-ttu-id="40b0d-135">Tagad tos abus sapludināsim vienā rēķinā.</span><span class="sxs-lookup"><span data-stu-id="40b0d-135">Now let's merge them into a single invoice.</span></span>  
9. <span data-ttu-id="40b0d-136">Laukā Kopgrāmatojums atlasiet vērtību “Rēķina konts”.</span><span class="sxs-lookup"><span data-stu-id="40b0d-136">In the Summary update for field, select 'Invoice account'.</span></span>
10. <span data-ttu-id="40b0d-137">Noklikšķiniet uz Sakārtot, lai pārdošanas pasūtījumus sapludinātu vienā rēķinā.</span><span class="sxs-lookup"><span data-stu-id="40b0d-137">Click Arrange to merge the sales orders into a single invoice.</span></span>
    * <span data-ttu-id="40b0d-138">Abi pārdošanas pasūtījumi tagad ir sapludināti vienā rēķinā.</span><span class="sxs-lookup"><span data-stu-id="40b0d-138">The two sales orders are now merged into a single invoice.</span></span>   
11. <span data-ttu-id="40b0d-139">Noklikšķiniet uz Atcelt.</span><span class="sxs-lookup"><span data-stu-id="40b0d-139">Click Cancel.</span></span>
12. <span data-ttu-id="40b0d-140">Noklikšķiniet uz Jā.</span><span class="sxs-lookup"><span data-stu-id="40b0d-140">Click Yes.</span></span>

## <a name="post-invoices-in-a-batch"></a><span data-ttu-id="40b0d-141">Veikt rēķinu pakešveida grāmatošanu</span><span class="sxs-lookup"><span data-stu-id="40b0d-141">Post invoices in a batch</span></span>
1. <span data-ttu-id="40b0d-142">Doties uz Debitoru parādi > Rēķini > Partijas rēķinu izrakstīšana > Rēķins.</span><span class="sxs-lookup"><span data-stu-id="40b0d-142">Go to Accounts receivable > Invoices > Batch invoicing > Invoice.</span></span>
2. <span data-ttu-id="40b0d-143">Noklikšķiniet uz Atlasīt.</span><span class="sxs-lookup"><span data-stu-id="40b0d-143">Click Select.</span></span>
3. <span data-ttu-id="40b0d-144">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="40b0d-144">Click OK.</span></span>
4. <span data-ttu-id="40b0d-145">Noklikšķiniet uz Partija.</span><span class="sxs-lookup"><span data-stu-id="40b0d-145">Click Batch.</span></span>
5. <span data-ttu-id="40b0d-146">Noklikšķiniet uz Jā, lai ieslēgtu pakešapstrādi.</span><span class="sxs-lookup"><span data-stu-id="40b0d-146">Click on Yes to turn on batch processing.</span></span>
6. <span data-ttu-id="40b0d-147">Noklikšķiniet uz Periodiskums.</span><span class="sxs-lookup"><span data-stu-id="40b0d-147">Click Recurrence.</span></span>
7. <span data-ttu-id="40b0d-148">Atlasiet vienumu Dienas</span><span class="sxs-lookup"><span data-stu-id="40b0d-148">Select Days</span></span>
8. <span data-ttu-id="40b0d-149">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="40b0d-149">Click OK.</span></span>
9. <span data-ttu-id="40b0d-150">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="40b0d-150">Click OK.</span></span>
10. <span data-ttu-id="40b0d-151">Noklikšķiniet uz Atcelt.</span><span class="sxs-lookup"><span data-stu-id="40b0d-151">Click Cancel.</span></span>
11. <span data-ttu-id="40b0d-152">Noklikšķiniet uz Jā.</span><span class="sxs-lookup"><span data-stu-id="40b0d-152">Click Yes.</span></span>

