---
title: Rēķinu datu ievade kreditoru sistēmā, izmantojot rēķinu kopu
description: Šajā uzdevuma ceļvedī aprakstīts, kā izmantot rēķinu reģistru, lai izveidotu rēķinus.
author: abruer
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6b870613512a8f4a5c19a0a05cd72b35ea32861b
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843221"
---
# <a name="key-invoice-data-into-the-ap-system-using-invoice-pool"></a><span data-ttu-id="98612-103">Rēķinu datu ievade kreditoru sistēmā, izmantojot rēķinu kopu</span><span class="sxs-lookup"><span data-stu-id="98612-103">Key invoice data into the AP system using invoice pool</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="98612-104">Šajā uzdevuma ceļvedī aprakstīts, kā izmantot rēķinu reģistru, lai izveidotu rēķinus.</span><span class="sxs-lookup"><span data-stu-id="98612-104">This task guide will show you how to use the invoice register to create invoices.</span></span>  <span data-ttu-id="98612-105">Pēc tam izmantojiet rēķinu kopu, lai saskaņotu rēķinu ar pirkšanas pasūtījumu un pabeigtu izdevumu kreditora rēķina lapā.</span><span class="sxs-lookup"><span data-stu-id="98612-105">Then use the invoice pool to match the invoice to a purchase order and finalize the expense in the vendor invoice page.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="98612-106">Pirkšanas pasūtījuma izveide</span><span class="sxs-lookup"><span data-stu-id="98612-106">Create a purchase order</span></span>
1. <span data-ttu-id="98612-107">Dodieties uz Kreditori > Pirkšanas pasūtījumi > Pirkšanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="98612-107">Go to Accounts payable > Purchase orders > Purchase orders.</span></span>
2. <span data-ttu-id="98612-108">Lai izveidotu pirkšanas pasūtījumu, noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="98612-108">Click New to create a purchase order.</span></span>
3. <span data-ttu-id="98612-109">Laukā Kreditora konts noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="98612-109">In the Vendor account field, click the drop down button to open the lookup.</span></span>
4. <span data-ttu-id="98612-110">No saraksta atlasiet kreditoru.</span><span class="sxs-lookup"><span data-stu-id="98612-110">Select the vendor from the list.</span></span> <span data-ttu-id="98612-111">Piemēram, kreditors 1001.</span><span class="sxs-lookup"><span data-stu-id="98612-111">For example, vendor 1001.</span></span>
5. <span data-ttu-id="98612-112">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="98612-112">Click OK.</span></span>
6. <span data-ttu-id="98612-113">Laukā Krājuma kods noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="98612-113">In the Item number field, click the drop down button to open the lookup.</span></span>
7. <span data-ttu-id="98612-114">Sarakstā atrodiet pakalpojumu krājuma numuru.</span><span class="sxs-lookup"><span data-stu-id="98612-114">Find the services item number in the list.</span></span> <span data-ttu-id="98612-115">Piemēram, atlasiet S0001.</span><span class="sxs-lookup"><span data-stu-id="98612-115">For example, select S0001.</span></span>
8. <span data-ttu-id="98612-116">Noklikšķiniet uz krājuma numura un atlasiet to.</span><span class="sxs-lookup"><span data-stu-id="98612-116">Click on the item number and select it.</span></span>
    * <span data-ttu-id="98612-117">Neto summa ir 75,00.</span><span class="sxs-lookup"><span data-stu-id="98612-117">The net amount is 75.00.</span></span>  <span data-ttu-id="98612-118">Tā ir summa, kuru sagaidām rēķinā.</span><span class="sxs-lookup"><span data-stu-id="98612-118">That is the amount that we will expect on the invoice.</span></span>  
9. <span data-ttu-id="98612-119">Darbību rūtī noklikšķiniet uz Pirkšana.</span><span class="sxs-lookup"><span data-stu-id="98612-119">On the action pane, click Purchase.</span></span>
10. <span data-ttu-id="98612-120">Noklikšķiniet uz Apstiprināt.</span><span class="sxs-lookup"><span data-stu-id="98612-120">Click Confirm.</span></span>

## <a name="create-and-post-and-invoice"></a><span data-ttu-id="98612-121">Izveidot un grāmatot rēķinu</span><span class="sxs-lookup"><span data-stu-id="98612-121">Create and post and invoice</span></span>
1. <span data-ttu-id="98612-122">Pārejiet uz sadaļu Kreditori > Rēķini > Rēķinu reģistrs.</span><span class="sxs-lookup"><span data-stu-id="98612-122">Go to Accounts payable > Invoices > Invoice register.</span></span>
2. <span data-ttu-id="98612-123">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="98612-123">Click New.</span></span>
3. <span data-ttu-id="98612-124">Lai atlasītu nosaukumu rēķinu reģistram, kuru vēlaties izmantot, atveriet uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="98612-124">Open the lookup to select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="98612-125">Atlasiet nosaukumu tam rēķinu reģistram, kuru vēlaties lietot.</span><span class="sxs-lookup"><span data-stu-id="98612-125">Select the name of the invoice register that you want to use.</span></span>
5. <span data-ttu-id="98612-126">Noklikšķiniet uz Rindas, lai atvērtu reģistru un ievadītu izdevumu rindas.</span><span class="sxs-lookup"><span data-stu-id="98612-126">Click on Lines to open the register and enter expense lines.</span></span>
6. <span data-ttu-id="98612-127">Uzmeklēšanas skatā atlasiet kreditoru.</span><span class="sxs-lookup"><span data-stu-id="98612-127">In the lookup, select a vendor.</span></span> <span data-ttu-id="98612-128">Piemēram, noklikšķiniet uz kreditors 1001.</span><span class="sxs-lookup"><span data-stu-id="98612-128">For example, click on vendor 1001.</span></span>
7. <span data-ttu-id="98612-129">Laukā Rēķins ievadiet rēķina numuru.</span><span class="sxs-lookup"><span data-stu-id="98612-129">In the Invoice field, enter the invoice number.</span></span>
8. <span data-ttu-id="98612-130">Laukā Apraksts ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="98612-130">In the Description field, type a value.</span></span>
9. <span data-ttu-id="98612-131">Laukā Kredīts ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="98612-131">In the Credit field, enter a number.</span></span>
10. <span data-ttu-id="98612-132">Laukā Pirkšanas pasūtījums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="98612-132">In the Purchase order field, click the drop down button to open the lookup.</span></span>
11. <span data-ttu-id="98612-133">Atlasiet iepriekš izveidoto pirkšanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="98612-133">Select the purchase order that you created earlier.</span></span>
12. <span data-ttu-id="98612-134">Laukā Apstiprināja noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="98612-134">In the Approved by field, click the drop down button to open the lookup.</span></span>
13. <span data-ttu-id="98612-135">Iezīmējiet apstiprinātāju un noklikšķiniet uz Atlasīt, lai atlasītu šo apstiprinātāju.</span><span class="sxs-lookup"><span data-stu-id="98612-135">Highlight an approver and click Select to select that approver.</span></span>
14. <span data-ttu-id="98612-136">Noklikšķiniet uz Grāmatot.</span><span class="sxs-lookup"><span data-stu-id="98612-136">Click Post.</span></span>
15. <span data-ttu-id="98612-137">Aizveriet formu.</span><span class="sxs-lookup"><span data-stu-id="98612-137">Close the form.</span></span>
16. <span data-ttu-id="98612-138">Aizveriet formu.</span><span class="sxs-lookup"><span data-stu-id="98612-138">Close the form.</span></span>

## <a name="open-an-invoice-from-the-pool-and-match-it-to-a-purchase-order-to-complete-the-invoice-process"></a><span data-ttu-id="98612-139">Lai pabeigtu rēķina izveides procesu, atveriet rēķinu no kopas un salīdziniet to ar pirkšanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="98612-139">Open an invoice from the pool and match it to a purchase order to complete the invoice process</span></span>
1. <span data-ttu-id="98612-140">Pārejiet uz sadaļu Kreditori > Rēķini > Rēķinu kopa.</span><span class="sxs-lookup"><span data-stu-id="98612-140">Go to Accounts payable > Invoices > Invoice pool.</span></span>
2. <span data-ttu-id="98612-141">Lai no kopas rēķina izveidotu kreditora rēķinu, noklikšķiniet uz Pirkšanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="98612-141">Click Purchase order to create a vendor invoice from the invoice in the pool.</span></span>
3. <span data-ttu-id="98612-142">Atlasiet rēķinu, kuru vēlaties pārskatīt.</span><span class="sxs-lookup"><span data-stu-id="98612-142">Select the invoice that you want to review.</span></span>
4. <span data-ttu-id="98612-143">Lai pabeigtu salīdzināšanu, noklikšķiniet uz Atjaunot atbilstības statusu.</span><span class="sxs-lookup"><span data-stu-id="98612-143">Click Update match status to complete the matching.</span></span>
5. <span data-ttu-id="98612-144">Darbību rūtī noklikšķiniet uz opcijas.</span><span class="sxs-lookup"><span data-stu-id="98612-144">On the action pane, click Options.</span></span>
6. <span data-ttu-id="98612-145">Noklikšķiniet uz Mainīt skatījumu.</span><span class="sxs-lookup"><span data-stu-id="98612-145">Click Change view.</span></span>
7. <span data-ttu-id="98612-146">Noklikšķiniet uz Režģa skats.</span><span class="sxs-lookup"><span data-stu-id="98612-146">Click Grid view.</span></span>
8. <span data-ttu-id="98612-147">Noklikšķiniet uz Grāmatot.</span><span class="sxs-lookup"><span data-stu-id="98612-147">Click Post.</span></span>
9. <span data-ttu-id="98612-148">Aizveriet formu.</span><span class="sxs-lookup"><span data-stu-id="98612-148">Close the form.</span></span>
10. <span data-ttu-id="98612-149">Dodieties uz Parādi kreditoriem > Kreditori > Kreditori.</span><span class="sxs-lookup"><span data-stu-id="98612-149">Go to Accounts payable > Vendors > Vendors.</span></span>
11. <span data-ttu-id="98612-150">Atlasiet kreditoru, kuram tika sastādīts pirkšanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="98612-150">Select the vendor that was on the purchase order.</span></span> <span data-ttu-id="98612-151">Piemēram, atlasiet kreditors 1001.</span><span class="sxs-lookup"><span data-stu-id="98612-151">For example, select vendor 1001.</span></span>
12. <span data-ttu-id="98612-152">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="98612-152">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="98612-153">Darbību rūtī noklikšķiniet uz Kreditors.</span><span class="sxs-lookup"><span data-stu-id="98612-153">On the action pane, click Vendor.</span></span>
14. <span data-ttu-id="98612-154">Noklikšķiniet uz Transakcijas.</span><span class="sxs-lookup"><span data-stu-id="98612-154">Click Transactions.</span></span>
15. <span data-ttu-id="98612-155">Atlasiet izveidoto rēķinu.</span><span class="sxs-lookup"><span data-stu-id="98612-155">Select the invoice that you created.</span></span>
    * <span data-ttu-id="98612-156">Rēķinu reģistra uzkrāšana tika atsaukta un iegrāmatota atbilstošajā izdevumu kontā.</span><span class="sxs-lookup"><span data-stu-id="98612-156">The invoice register accrual was reversed and posted to the appropriate expense account.</span></span>  

