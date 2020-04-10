---
title: Rēķinu datu ievade kreditoru sistēmā, izmantojot rēķinu kopu
description: Šajā tēmā aprakstīts, kā lietot rēķinu reģistru, lai izveidotu rēķinus.
author: abruer
manager: AnnBe
ms.date: 07/31/2019
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
ms.openlocfilehash: cd6de42dda650d42d703e905f8d48f73b9e4afd6
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143815"
---
# <a name="key-invoice-data-into-the-ap-system-using-invoice-pool"></a><span data-ttu-id="51779-103">Rēķinu datu ievade kreditoru sistēmā, izmantojot rēķinu kopu</span><span class="sxs-lookup"><span data-stu-id="51779-103">Key invoice data into the AP system using invoice pool</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="51779-104">Šajā tēmā aprakstīts, kā lietot rēķinu reģistru, lai izveidotu rēķinus.</span><span class="sxs-lookup"><span data-stu-id="51779-104">This topic describes how to use the invoice register to create invoices.</span></span> <span data-ttu-id="51779-105">Pēc tam izmantojiet rēķinu kopu, lai saskaņotu rēķinu ar pirkšanas pasūtījumu un pabeigtu izdevumu kreditora rēķina lapā.</span><span class="sxs-lookup"><span data-stu-id="51779-105">Then use the invoice pool to match the invoice to a purchase order and finalize the expense in the vendor invoice page.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="51779-106">Pirkšanas pasūtījuma izveide</span><span class="sxs-lookup"><span data-stu-id="51779-106">Create a purchase order</span></span>
1. <span data-ttu-id="51779-107">Navigācijas rūtī pārejiet uz sadaļu **Moduļi > Kreditori > Pirkuma pasūtījumi > Pirkuma pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="51779-107">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > Purchase orders**.</span></span>
2. <span data-ttu-id="51779-108">Atlasiet **Jauns**, lai izveidotu pirkuma pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="51779-108">Select **New** to create a purchase order.</span></span>
3. <span data-ttu-id="51779-109">Laukā **Piegādātāja konts** nolaižamajā izvēlnē atlasiet piegādātāju.</span><span class="sxs-lookup"><span data-stu-id="51779-109">In the **Vendor account** field, select a vendor for the drop-down list.</span></span> <span data-ttu-id="51779-110">Piemēram, atlasiet piegādātāju **1001**.</span><span class="sxs-lookup"><span data-stu-id="51779-110">For example, select vendor **1001**.</span></span>
4. <span data-ttu-id="51779-111">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="51779-111">Select **OK**.</span></span>
5. <span data-ttu-id="51779-112">Laukā **Vienuma numurs** atlasiet pakalpojumu vienuma numuru no nolaižamās izvēlnes.</span><span class="sxs-lookup"><span data-stu-id="51779-112">In the **Item number** field, select the services item number in the drop-down list.</span></span> <span data-ttu-id="51779-113">Piemēram, atlasiet **S0001**.</span><span class="sxs-lookup"><span data-stu-id="51779-113">For example, select **S0001**.</span></span> <span data-ttu-id="51779-114">Neto summa ir 75,00.</span><span class="sxs-lookup"><span data-stu-id="51779-114">The net amount is 75.00.</span></span>  <span data-ttu-id="51779-115">Tā ir summa, kuru sagaidām rēķinā.</span><span class="sxs-lookup"><span data-stu-id="51779-115">That is the amount that we will expect on the invoice.</span></span>  
6. <span data-ttu-id="51779-116">Darbību rūtī atlasiet **Iegādāties**.</span><span class="sxs-lookup"><span data-stu-id="51779-116">On the action pane, select **Purchase**.</span></span>
7. <span data-ttu-id="51779-117">Atlasiet **Apstiprināt**.</span><span class="sxs-lookup"><span data-stu-id="51779-117">Select **Confirm**.</span></span>

## <a name="create-and-post-and-invoice"></a><span data-ttu-id="51779-118">Izveidot un grāmatot rēķinu</span><span class="sxs-lookup"><span data-stu-id="51779-118">Create and post and invoice</span></span>
1. <span data-ttu-id="51779-119">Navigācijas rūtī pārejiet uz sadaļu **Moduļi > Kreditori > Rēķini > Rēķinu reģistrs**.</span><span class="sxs-lookup"><span data-stu-id="51779-119">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice register**.</span></span>
2. <span data-ttu-id="51779-120">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="51779-120">Select **New**.</span></span>
3. <span data-ttu-id="51779-121">Lai atlasītu nosaukumu rēķinu reģistram, kuru vēlaties izmantot, atveriet uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="51779-121">Open the lookup to select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="51779-122">Atlasiet nosaukumu tam rēķinu reģistram, kuru vēlaties lietot.</span><span class="sxs-lookup"><span data-stu-id="51779-122">Select the name of the invoice register that you want to use.</span></span>
5. <span data-ttu-id="51779-123">Atlasiet **Rindas**, lai atvērtu reģistru un ievadītu izmaksu rindas. </span><span class="sxs-lookup"><span data-stu-id="51779-123">Select **Lines** to open the register and enter expense lines.</span></span>
6. <span data-ttu-id="51779-124">Uzmeklēšanas skatā atlasiet kreditoru.</span><span class="sxs-lookup"><span data-stu-id="51779-124">In the lookup, select a vendor.</span></span> <span data-ttu-id="51779-125">Piemēram, atlasiet piegādātāju **1001**.</span><span class="sxs-lookup"><span data-stu-id="51779-125">For example, select vendor **1001**.</span></span>
7. <span data-ttu-id="51779-126">Laukā **Rēķins** ievadiet rēķina numuru</span><span class="sxs-lookup"><span data-stu-id="51779-126">In the **Invoice** field, enter the invoice number.</span></span>
8. <span data-ttu-id="51779-127">Laukā **Apraksts** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="51779-127">In the **Description** field, type a value.</span></span>
9. <span data-ttu-id="51779-128">Laukā **Kredīts** ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="51779-128">In the **Credit** field, enter a number.</span></span>
10. <span data-ttu-id="51779-129">Laukā **Pirkuma pasūtījums** atveriet nolaižamo izvēlni, lai atlasītu pirkuma pasūtījumu, kuru pirms tam izveidojāt.</span><span class="sxs-lookup"><span data-stu-id="51779-129">In the **Purchase order** field, open the drop-down list to select the purchase order that you created earlier.</span></span>
11. <span data-ttu-id="51779-130">Laukā **Apstiprināja** nolaižamajā sarakstā iezīmējiet apstiprinātāju un noklikšķiniet uz **Atlasīt**, lai atlasītu šo apstiprinātāju.</span><span class="sxs-lookup"><span data-stu-id="51779-130">In the **Approved by** field, highlight an approver in the drop-down list and click **Select** to select that approver.</span></span>
12. <span data-ttu-id="51779-131">Atlasiet **Grāmatot**.</span><span class="sxs-lookup"><span data-stu-id="51779-131">Select **Post**.</span></span>

## <a name="open-an-invoice-from-the-pool-and-match-it-to-a-purchase-order-to-complete-the-invoice-process"></a><span data-ttu-id="51779-132">Lai pabeigtu rēķina izveides procesu, atveriet rēķinu no kopas un salīdziniet to ar pirkšanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="51779-132">Open an invoice from the pool and match it to a purchase order to complete the invoice process</span></span>
1. <span data-ttu-id="51779-133">Navigācijas rūtī pārejiet uz sadaļu **Moduļi > Kreditori > Rēķini > Rēķinu kopa**.</span><span class="sxs-lookup"><span data-stu-id="51779-133">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice pool**.</span></span>
2. <span data-ttu-id="51779-134">Atlasiet **Pirkuma pasūtījums**, lai izveidotu piegādātāja rēķinu no kopas rēķina.</span><span class="sxs-lookup"><span data-stu-id="51779-134">Select **Purchase order** to create a vendor invoice from the invoice in the pool.</span></span>
3. <span data-ttu-id="51779-135">Atlasiet rēķinu, kuru vēlaties pārskatīt.</span><span class="sxs-lookup"><span data-stu-id="51779-135">Select the invoice that you want to review.</span></span>
4. <span data-ttu-id="51779-136">Atlasiet **Atjaunināt salīdzinājuma statusu**, lai pabeigtu salīdzināšanu.</span><span class="sxs-lookup"><span data-stu-id="51779-136">Select **Update match status** to complete the matching.</span></span>
5. <span data-ttu-id="51779-137">Darbību rūtī atlasiet **Opcijas**.</span><span class="sxs-lookup"><span data-stu-id="51779-137">On the action pane, select **Options**.</span></span>
6. <span data-ttu-id="51779-138">Atlasiet **Mainīt skatu**.</span><span class="sxs-lookup"><span data-stu-id="51779-138">Select **Change view**.</span></span>
7. <span data-ttu-id="51779-139">Atlasiet **Režģa skats**.</span><span class="sxs-lookup"><span data-stu-id="51779-139">Select **Grid view**.</span></span>
8. <span data-ttu-id="51779-140">Atlasiet **Grāmatot**.</span><span class="sxs-lookup"><span data-stu-id="51779-140">Select **Post**.</span></span>
9. <span data-ttu-id="51779-141">Aizveriet formu.</span><span class="sxs-lookup"><span data-stu-id="51779-141">Close the form.</span></span>
10. <span data-ttu-id="51779-142">Navigācijas rūtī pārejiet uz sadaļu **Moduļi > Kreditori > Piegādātāji > Piegādātāji**.</span><span class="sxs-lookup"><span data-stu-id="51779-142">In the navigation pane, go to **Modules > Accounts payable > Vendors > Vendors**.</span></span>
11. <span data-ttu-id="51779-143">Atlasiet kreditoru, kuram tika sastādīts pirkšanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="51779-143">Select the vendor that was on the purchase order.</span></span> <span data-ttu-id="51779-144">Piemēram, atlasiet piegādātāju **1001**.</span><span class="sxs-lookup"><span data-stu-id="51779-144">For example, select vendor **1001**.</span></span>
12. <span data-ttu-id="51779-145">Darbību rūtī atlasiet **Piegādātājs**.</span><span class="sxs-lookup"><span data-stu-id="51779-145">On the action pane, select **Vendor**.</span></span>
13. <span data-ttu-id="51779-146">Atlasiet **Darbības**.</span><span class="sxs-lookup"><span data-stu-id="51779-146">Select **Transactions**.</span></span>
14. <span data-ttu-id="51779-147">Atlasiet izveidoto rēķinu.</span><span class="sxs-lookup"><span data-stu-id="51779-147">Select the invoice that you created.</span></span> <span data-ttu-id="51779-148">Rēķinu reģistra uzkrāšana tika atsaukta un iegrāmatota atbilstošajā izdevumu kontā.</span><span class="sxs-lookup"><span data-stu-id="51779-148">The invoice register accrual was reversed and posted to the appropriate expense account.</span></span>  

